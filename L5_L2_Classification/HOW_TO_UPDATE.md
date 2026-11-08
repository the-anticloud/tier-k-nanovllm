# How to Update — K_NANOVLLM
**Platform:** Anticloud | **IP:** USPTO pending 2026, Anticloud FZ LLE, 0-1.gg

## Module: K_NANOVLLM
Domain: Nano-vLLM: lightweight vLLM-compatible inference engine for Kaggle T4 16GB deployment


## Update Procedure
1. Backup current state
2. Test in api-oss-labs sandbox
3. `pip install --upgrade anticloud-k_nanovllm`
4. `python -m k_nanovllm.tests.smoke`
5. `aioss verify --chain ./k_nanovllm.aioss`
6. Monitor 30 min via api-oss-monitor

## Rollback
```bash
pip install anticloud-k_nanovllm==<previous>
python -m api_oss_backup restore --archive ./backups/<latest>
```

## Weight Updates
PAX 27B weight updates are signed by Anticloud FZ LLE:
```bash
anticloud tool verify-weights --model ./pax-27b-q4-new.gguf --sig ./pax-27b-q4-new.sig
```
