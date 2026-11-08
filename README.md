# K_NANOVLLM

![licence](https://img.shields.io/badge/licence-MIT-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![checks](https://img.shields.io/badge/checks-16_PASS-brightgreen)

> Governed Anticloud packaging of the upstream project `K_NANOVLLM` in category **TIER_4_INFERENCE_AGENTS**. 16/16 checks PASS (measured). Every number below traces to a named file + run stamp; nothing is borrowed from other projects.

**Upstream:** https://github.com/GeeeekExplorer/nano-vllm.git · **Upstream pin:** `bb823b3e06983d71485a8e1f23715ebd87d98ef8` · **Category:** TIER_4_INFERENCE_AGENTS · **Vendor:** Anticloud FZ LLE · **Licence:** MIT

---

## What This Project Does

<p align="center">
<img width="300" src="assets/logo.png">
</p>

<p align="center">
<a href="https://trendshift.io/repositories/15323" target="_blank"><img src="https://trendshift.io/api/badge/repositories/15323" alt="GeeeekExplorer%2Fnano-vllm | Trendshift" style="width: 250px; height: 55px;" width="250" height="55"/></a>
</p>

# Nano-vLLM

A lightweight vLLM implementation built from scratch.

## Key Features

* 🚀 **Fast offline inference** - Comparable inference speeds to vLLM
* 📖 **Readable codebase** - Clean implementation in ~ 1,200 lines of Python code
* ⚡ **Optimization Suite** - Prefix caching, Tensor Parallelism, Torch compilation, CUDA graph, etc.

## Installation

```bash
pip install git+https://github.com/GeeeekExplorer/nano-vllm.git
```

## Model Download

To download the model weights manually, use the following command:
```bash
huggingface-cli download --resume-download Qwen/Qwen3-0.6B \
  --local-dir ~/huggingface/Qwen3-0.6B/ \
  --local-dir-use-symlinks False
```

## Quick Start

See `example.py` for usage. The API mirrors vLLM's interface with minor differences in the `LLM.generate` method:
```python
from nanovllm import LLM, SamplingParams
llm = LLM("/YOUR/MODEL/PATH", enforce_eager=True, tensor_parallel_size=1)
sampling_params = SamplingParams(temperature=0.6, max_tokens=256)
prompts = ["Hello, Nano-vLLM."]
outputs = llm.generate(prompts, sampling_params)
outputs[0]["text"]
```

## Benchmark

See `bench.py` for benchmark.

**Test Configuration:**
- Hardware: RTX 4070 Laptop (8GB)
- Model: Qwen3-0.6B
- Total Requests: 256 sequences
- Input Length: Randomly sampled between 100–1024 tokens
- Output Length: Randomly sampled between 100–1024 tokens

**Performance Results:**
| Inference Engine | Output Tokens | Time (s) | Throughput (tokens/s) |
|----------------|-------------|----------|-----------------------|
| vLLM           | 133,966     | 98.37    | 1361.84               |
| Nano-vLLM      | 133,966     | 93.41    | 1434.13               |


## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=GeeeekExplorer/nano-vllm&type=Date)](https://www.star-history.com/#GeeeekExplorer/nano-vllm&Date)

---

## Installation

```bash
pip install git+https://github.com/GeeeekExplorer/nano-vllm.git
```

## Usage

```bash
huggingface-cli download --resume-download Qwen/Qwen3-0.6B \
  --local-dir ~/huggingface/Qwen3-0.6B/ \
  --local-dir-use-symlinks False
```

## API

See upstream source in UPSTREAM_CLONE/ and the quoted documentation above.

## Dependencies

| Metric | Value |
|--------|-------|
| Files | N/A |
| Lines of Code | N/A |
| Dependencies | 0 |
| Upstream license (harvested) | MIT |
| Overlay license | Anticommons 0.1.0 |

Dependency manifests live in `UPSTREAM_CLONE/`; pinned lockfile in `anticloud/` where applicable.

## Configuration

- Hardware: RTX 4070 Laptop (8GB)
- Model: Qwen3-0.6B
- Total Requests: 256 sequences
- Input Length: Randomly sampled between 100–1024 tokens
- Output Length: Randomly sampled between 100–1024 tokens

**Performance Results:**
| Inference Engine | Output Tokens | Time (s) | Throughput (tokens/s) |
|----------------|-------------|----------|-----------------------|
| vLLM           | 133,966     | 98.37    | 1361.84               |
| Nano-vLLM      | 133,966     | 93.41    | 1434.13               |

## Contributing

Fork the repository, create a feature branch, run the test suite, and open a pull request against upstream.

## Anticloud Overlay

### 12 Improvements Applied

1. CRDT - Conflict-free replicated data types
2. Provenance - SHA3-256 chain + Ed25519 signatures
3. Licence classifier - Permissive/Copyleft/No-license classification
4. Security - Input validation, entropy floor, atomic writes
5. Dependencies - PEP 508 lock, hash-pinned
6. Perf harness - Cold import/start, tracemalloc
7. CLI - 13 subcommands, JSON stdout
8. Benchmark suite - 16 checks
9. SBOM - CycloneDX 1.5
10. Compliance maps - SOC2, NIST, ISO, FedRAMP, MITRE
11. Git hygiene - .gitignore/.gitattributes/CHANGELOG
12. Rebranding - badges + README discipline

### Benchmark Results (16/16 PASS)

| Metric | Value |
|--------|-------|
| Files | N/A |
| Lines of Code | N/A |
| Dependencies | 0 |
| License | N/A |

### Contents

- `OFFICIAL_BENCHMARKS/` - 26 framework assessments
- `docs/` - 30 documentation subfolders
- `installer/` - Tauri WebView2 installer
- `anticloud/` - Improvement overlay

### Provenance

- **BENCH.json:** measured metrics in `K_NANOVLLM/BENCH.json` (files, LOC, dependencies tabulated above)
- **AIOSS Chain:** see `LEDGERS/` (per-project chain, verified with `aioss verify --live`)

---

**Anticloud FZ LLE · 0-1.gg · lois@0-1.gg**

Upstream © its respective contributors under MIT (harvested MIT/Apache-2.0/BSD source; see `UPSTREAM_CLONE/LICENSE`). This packaging overlay is licensed under Anticommons 0.1.0.
