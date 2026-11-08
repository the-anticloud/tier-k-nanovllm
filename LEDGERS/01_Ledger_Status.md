# Ledger Status

**Project:** `K_NANOVLLM`  
**Tier:** TIER_4_INFERENCE_AGENTS  
**Identity:** Upstream `GeeeekExplorer/nano-vllm` @ `bb823b3e0698` (MIT)

## Chain state

| Fact | Value |
| --- | --- |
| Upstream | `GeeeekExplorer/nano-vllm` |
| Commit | `bb823b3e06983d71485a8e1f23715ebd87d98ef8` |
| Upstream licence | MIT |
| Licence class | permissive |
| Clone size | 0.44 MB |
| Ledger | 0 blocks, chain verified |
| Current TRL | NOT YET MEASURED |
| Post-optimisation TRL | NOT YET MEASURED |
| II budget cap | 1000.0 IIU |
| Verified upstream edits | 1 |

- Blocks: **0**
- Head digest: `None`
- Chain verification: **verified**

## Independent verification

The chain is verifiable without trusting this project's tooling:

```
anticloud ledger verify
anticloud ledger export > ledger.jsonl
```

Each block carries the previous block's digest, so removing or reordering an
entry invalidates every block after it. That property is the reason the
ledger can stand in for a claim of what happened.
