# Developer Cookbook — K_NANOVLLM
**Stack:** Python 3.11, PyTorch 2.10+, CUDA 12.x, custom CUDA kernels, AIOSS_FORMAT
**Domain:** Nano-vLLM: lightweight vLLM-compatible inference engine for Kaggle T4 16GB deployment

## Start inference server
```python
from k_nanovllm import NanoVLLM

engine = NanoVLLM(
    model_path="./pax-27b-q4.gguf",
    max_batch_size=4,
    max_seq_len=4096,
    aioss_chain="./nanovllm.aioss"
)

# Single inference
result = engine.generate("Analyze this biosignal data:", max_tokens=256)
print(result.text, f"({result.tokens_per_sec:.1f} tok/s)")
print(f"Chain: {result.chain_hash}")
```

## Continuous batching
```python
requests = [
    {"prompt": "Summarize K_BRAINFLOW deploy guide", "max_tokens": 128},
    {"prompt": "List TIER_8 RF projects", "max_tokens": 64},
    {"prompt": "Explain AIOSS chain format", "max_tokens": 256},
]
results = engine.batch_generate(requests)
for r in results:
    print(f"{r.text[:60]}... ({r.tokens_per_sec:.1f} tok/s)")
```

## Benchmark T4 throughput
```python
bench = engine.benchmark(n_tokens=100, n_trials=10)
print(f"Throughput: {bench.tokens_per_sec:.1f} tok/s")
print(f"VRAM used: {bench.vram_mb:.0f}MB / 15872MB")
```

## OpenAI-compatible API server
```bash
python -m k_nanovllm.server --model ./pax-27b-q4.gguf --port 8000
# curl http://localhost:8000/v1/completions -d '{"model":"pax-27b","prompt":"Hello"}'
```

## AIOSS Chain Append
```python
import hashlib, time

def aioss_append(chain_path, payload: bytes, module_id: str):
    entry_hash = hashlib.sha3_256(payload).digest()
    ts = int(time.time_ns()).to_bytes(8, 'big')
    with open(chain_path, 'rb') as f:
        f.seek(-32, 2); prev_hash = f.read(32)
    new_hash = hashlib.sha3_256(prev_hash + entry_hash + ts).digest()
    with open(chain_path, 'ab') as f:
        f.write(ts + entry_hash + new_hash)
    return new_hash.hex()
```
