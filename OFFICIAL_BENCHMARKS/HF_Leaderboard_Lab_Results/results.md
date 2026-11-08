# HF_Leaderboard_Lab_Results

**Project:** `K_NANOVLLM`  
**Tier:** `TIER_4_INFERENCE_AGENTS`  
**Slug:** `GeeeekExplorer/nano-vllm`  
**Commit:** `bb823b3e0698`  
**Run:** `2026-09-30T15:07:07.146295+00:00`  

## Isolation Environment

| Field | Value |
| ----- | ----- |
| Platform | `win32` |
| Python | `3.12.10` |
| HF model | `distilbert-base-uncased` |
| HF load time | `4.42s` |
| Inference device | `cpu` |

## Results

**Framework:** [HuggingFace Open LLM Leaderboard (proxy via distilbert-base-uncased)](https://huggingface.co/docs/leaderboards/en/open_llm_leaderboard/archive)

**Model used:** `distilbert-base-uncased`

### Inference Latency (Classification)

| Metric | Value |
| ------ | ----- |
| Avg latency | **52.08 ms** |
| Min latency | 46.51 ms |
| Max latency | 60.51 ms |
| Samples | 5 |

### Real Tokenization Results

| Field | Value |
| ----- | ----- |
| Token count | **42** |
| Tokenization latency | 2.0 ms |
| Classification label | `LABEL_0` |
| Classification score | 0.5903 |
| Classification latency | 97.49 ms |
| Status | **PASS** |

**Input text tokenized:**
```
K_NANOVLLM (GeeeekExplorer/nano-vllm) — 26 files, 1479 source lines, licence MIT, primary language ['Python']
```

**First 20 tokens:**
```
['[CLS]', 'k', '_', 'nano', '##v', '##ll', '##m', '(', 'gee', '##ee', '##ke', '##x', '##pl', '##ore', '##r', '/', 'nano', '-', 'v', '##ll']
```

> Full MMLU/HellaSwag/TruthfulQA/ARC/Winogrande/GSM8K require dedicated GPU.
> These results are CPU inference proxy metrics using distilbert-base-uncased.

---
_Anticloud Benchmark Suite — isolation log — 2026-09-30T15:07:07.146295+00:00_