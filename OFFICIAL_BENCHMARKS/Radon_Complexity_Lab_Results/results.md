# Radon_Complexity_Lab_Results
**Project:** `K_NANOVLLM` | **Status:** `PASS` | **Run:** `2026-09-30T17:14:20.030944+00:00`

**Framework:** [Radon — Cyclomatic Complexity & Maintainability Index](https://radon.readthedocs.io/)

## Key Metrics

- **files_analyzed:** `10`
- **average_complexity:** `{'grade': 'A', 'score': 3.24}`
- **complexity_grade:** `A`
- **complexity_score:** `3.24`
- **mi_output:** `E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_NANOVLLM\UPSTREAM\bench.py - A (79.72)
E:\fenta\Downloads\The`

## Raw Output (first 50 lines)
```
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_NANOVLLM\UPSTREAM\bench.py
    F 8:0 main - A (5)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_NANOVLLM\UPSTREAM\example.py
    F 6:0 main - A (3)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_NANOVLLM\UPSTREAM\nanovllm\config.py
    C 7:0 Config - A (5)
    M 20:4 Config.__post_init__ - A (4)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_NANOVLLM\UPSTREAM\nanovllm\llm.py
    C 4:0 LLM - A (1)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_NANOVLLM\UPSTREAM\nanovllm\sampling_params.py
    C 5:0 SamplingParams - A (3)
    M 10:4 SamplingParams.__post_init__ - A (2)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_NANOVLLM\UPSTREAM\nanovllm\_anticloud_egress.py
    F 38:0 _is_frontier - A (4)
    F 43:0 guarded_connect - A (4)
    F 61:0 install - A (3)
    F 33:0 is_offline - A (1)
    C 29:0 EgressDenied - A (1)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_NANOVLLM\UPSTREAM\nanovllm\engine\block_manager.py
    M 58:4 BlockManager.can_allocate - B (6)
    M 75:4 BlockManager.allocate - A (5)
    C 26:0 BlockManager - A (4)
    M 43:4 BlockManager._allocate_block - A (4)
    M 110:4 BlockManager.hash_blocks - A (4)
    M 94:4 BlockManager.deallocate - A (3)
    C 8:0 Block - A (2)
    M 28:4 BlockManager.__init__ - A (2)
    M 36:4 BlockManager.compute_hash - A (2)
    M 53:4 BlockManager._deallocate_block - A (2)
    M 106:4 BlockManager.may_ap
```

---
_Anticloud Independent Benchmark — 2026-09-30T17:14:20.030944+00:00_