# Deploy Guide — K_NANOVLLM
**Tier:** TIER_4_INFERENCE_AGENTS | **Stack:** Python 3.11, PyTorch 2.10+, CUDA 12.x, custom CUDA kernels, AIOSS_FORMAT
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, PyTorch 2.10+, CUDA 12.x, T4 GPU (15.6GB VRAM). PAX 27B Q4 weights (~8GB VRAM).

## Environment
T4 GPU required (15.6GB VRAM). CUDA 12.x. 16GB system RAM. PAX 27B Q4: ~8GB VRAM.

## AIOSS Integration
```bash
aioss init --module K_NANOVLLM --output ./k_nanovllm.aioss
aioss append --chain ./k_nanovllm.aioss --payload ./output.bin --module K_NANOVLLM
aioss verify --chain ./k_nanovllm.aioss
```

## Air-Gap Setup
```bash
pip download -r requirements.txt -d ./wheels/
pip install --no-index --find-links ./wheels/ -r requirements.txt
```

## PAX 27B Harness Wiring
```python
from anticloud_pax import PAXHarness
harness = PAXHarness(
    model_path="./pax-27b-q4.gguf",
    module="K_NANOVLLM",
    aioss_chain="./K_NANOVLLM.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./K_NANOVLLM.aioss --verbose
python -m K_NANOVLLM.tests.smoke
```
