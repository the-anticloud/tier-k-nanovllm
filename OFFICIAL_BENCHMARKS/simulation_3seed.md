# 3-Seed Simulation — K_NANOVLLM

**Seeds:** `60638` · `91975` · `26174`

**Seed method:** `sha256("K_NANOVLLM")[:8]` as hex→int, offsets +0 / +31337 / +65536

> These seeds are deterministic and documented. Any researcher can reproduce this simulation exactly by running `write_three_seed_simulation.py` with project name `K_NANOVLLM`.

## Confidence Intervals (mean ± σ across 3 seeds)

| Metric | Mean | σ | 95% CI |
|--------|------|---|--------|
| trl_score | 7.0523 | 0.1101 | ±0.2158 |
| throughput_tokens_per_sec | 287.8667 | 33.3804 | ±65.4256 |
| p50_latency_ms | 48.72 | 2.6384 | ±5.1713 |
| p99_latency_ms | 115.0367 | 12.6514 | ±24.7967 |
| ttft_ms | 29.9533 | 4.5298 | ±8.8784 |
| mmlu_proxy | 0.728 | 0.0304 | ±0.0596 |
| hellaswag_proxy | 0.7801 | 0.0302 | ±0.0592 |
| truthfulqa_proxy | 0.6102 | 0.0204 | ±0.04 |
| arc_proxy | 0.681 | 0.0183 | ±0.0359 |
| complexity_cyclomatic | 4.2633 | 0.2941 | ±0.5764 |
| maintainability_index | 75.9533 | 4.3653 | ±8.556 |
| security_issues_high | 0.3333 | 0.4714 | ±0.9239 |
| dependency_freshness_pct | 79.5667 | 2.2306 | ±4.372 |
| test_coverage_pct | 65.1 | 10.3965 | ±20.3771 |
| doc_coverage_pct | 66.6333 | 8.2099 | ±16.0914 |
| memory_mb | 50.0 | 0.0 | ±0.0 |
| gpu_util_pct | 66.1667 | 5.4908 | ±10.762 |
| openssf_score | 6.6467 | 0.6373 | ±1.2491 |
| eu_ai_act_compliance_pct | 86.2667 | 0.7134 | ±1.3983 |
| slsa_level | 1.3333 | 0.4714 | ±0.9239 |

## Per-Seed Raw Results

| Metric | Seed 60638 | Seed 91975 | Seed 26174 |
|--------|------------|------------|------------|
| trl_score | 6.959 | 6.991 | 7.207 |
| throughput_tokens_per_sec | 241.0 | 306.4 | 316.2 |
| p50_latency_ms | 45.01 | 50.23 | 50.92 |
| p99_latency_ms | 122.34 | 125.53 | 97.24 |
| ttft_ms | 32.58 | 23.58 | 33.7 |
| mmlu_proxy | 0.7495 | 0.7495 | 0.685 |
| hellaswag_proxy | 0.8166 | 0.7809 | 0.7427 |
| truthfulqa_proxy | 0.637 | 0.6061 | 0.5875 |
| arc_proxy | 0.7064 | 0.6726 | 0.6641 |
| complexity_cyclomatic | 4.51 | 4.43 | 3.85 |
| maintainability_index | 79.01 | 69.78 | 79.07 |
| security_issues_high | 0 | 1 | 0 |
| dependency_freshness_pct | 77.3 | 82.6 | 78.8 |
| test_coverage_pct | 72.7 | 72.2 | 50.4 |
| doc_coverage_pct | 76.5 | 56.4 | 67.0 |
| memory_mb | 50 | 50 | 50 |
| gpu_util_pct | 65.5 | 59.8 | 73.2 |
| openssf_score | 7.41 | 6.68 | 5.85 |
| eu_ai_act_compliance_pct | 85.3 | 86.5 | 87.0 |
| slsa_level | 1 | 1 | 2 |

---
_Anticloud 3-Seed Simulation — 2026-09-30T16:01:40.704491+00:00_
_Citation: Lois-Kleinner. (2026). The Anticloud. DOI: pending._