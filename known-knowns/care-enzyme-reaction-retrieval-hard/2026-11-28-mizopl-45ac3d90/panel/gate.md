# Honesty Gate Verdict (`care-enzyme-reaction-retrieval-hard` — Partial Wins `p1`, `p2`)

- `target_id`: `care-enzyme-reaction-retrieval-hard`
- `status`: `CONFIRMED_PARTIAL`
- `confirmed_scope`: Partial wins `p1` (CARE Task 2 Hard `n=460`, `k=1 L3=32.0%` vs `9.8%` `+22.2 pp`, plus `L4=10.0%`, `L2=42.4%`, `L1=80.4%`, `k=50 L4=41.7%`, EC3/EC4 cluster `perm_p <= 1.80e-3`) and `p2` (CARE Task 2 Medium `n=393`, `k=1 L4=11.5%` vs `7.4%` `CREEP_text` `+4.1 pp` and `4.1%` rxn-only `CREEP` `+7.4 pp`, `L3=55.7%`, `L2=77.4%`, `L1=89.8%`, `k=50 L4=65.4%`), plus a separate blind one-shot `0`-GPU `Easy` extension (`74.0% L4`, `k=50=98.7%`). Task 1 (`p3`) and Medium `L3/L1` vs multimodal `CREEP (w/ Text)` are not claimed.

## Panel Summary

| Role | Context | Verdict | Key Findings |
|---|---|---|---|
| `REPRODUCE` | fresh skeptic review of the packaged files only | `pass: true` | Verified `object/v5_hard_top50.csv.gz` (`37.7 KB`), `object/v5_medium_top50.csv.gz` (`31.2 KB`), and `object/v5_auto_easy_top50.csv.gz` (`39.3 KB`), `SHA256SUMS`, zero-leakage provenance manifests, `0.000%` baseline drift against Zenodo `14004425`, and `--corrupt` exit code `1`. |
| `NOVELTY` | fresh skeptic review of the packaged files only | `pass: true` | Audited 53 OpenAlex citing works and 2024-2026 preprints (`BioCG`, `VenusRXN-RE`, `PoinnCARE`, `FuncSeek`, `ERAM`, `GERO`, `EnzymeCAGE`, `VenusRX-Bench`, `RIVER`); confirmed Task 2 Hard and Medium Table 4 baselines stand unbeaten. |
| `CRITERION` | fresh skeptic review of the packaged files only | `pass: true` | Verified `p1` and `p2` bars, zero external DBs/LLMs, EC3/EC4 cluster CIs (flagging where Medium `L1 vs CREEP` and `L4 vs CREEP_text` cross zero), `183/460` Hard tie-break stability, and explicit disclosure of split-specific heads vs `engine_v5_auto_regime.py` and CARE Easy `26.2%` 2D-canonical overlap. |
