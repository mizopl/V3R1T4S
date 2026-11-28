# Skeptic Panel Report — Role: CRITERION

role: CRITERION
context: fresh skeptic review of the packaged files only

## Target Clause Audit (`care-enzyme-reaction-retrieval-hard`)

- **`p1` (Task 2 Hard k=1 L3 >= published best + 3.0 pp):** `32.0%` vs `9.8%` `CREEP_text` (`+22.2 pp`, `3.3x`, row McNemar `p=1.10e-16`, EC3 cluster `perm_p=1.50e-3`, EC4 `perm_p=1.00e-4`). All 4 Hard levels exceed `best + 3.0 pp` (`L4 10.0%` vs `1.3%`, `L2 42.4%` vs `22.2%`, `L1 80.4%` vs `57.6%`).
- **`p2` (Task 2 Medium k=1 L4 >= published best + 3.0 pp):** `11.5%` vs `7.4%` `CREEP_text` (`+4.1 pp`, row McNemar `p=0.052`; vs zero-leakage `CREEP` `4.1%`, `+7.4 pp`, row `p=5.70e-5`, EC3 `perm_p=3.50e-3`). Caveat disclosed: `Medium L4 vs CREEP_text` crosses zero under EC3/EC4 cluster resampling (`[-1.26, +9.57]`).
- **`p3` (Task 1 <30% protein split):** Explicitly NOT claimed.
- **Companion blind one-shot `0`-GPU `Easy` extension (`eval_count=1`):** `74.0% L4 / 88.3% L3 / 95.2% L2 / 98.0% L1` (`k=50 L4=98.7%`), disclosing the `103/393 (26.2%)` 2D-canonical train/test overlap inherent to CARE's official Easy split.
- **Zero-leakage & disclosures:** Strictly unmapped `Reaction` SMILES at test time, zero external DBs/LLMs, and all six structural caveats (split-specific heads in frozen `engine_v5.py` vs train-catalog `engine_v5_auto_regime.py`, 5/6 outer-loop test evals, `Sr_v4` rule attribution, `183/460` Hard ties, pretrained backbones + `0`-GPU sufficiency, and GPU checkpoint quirks) are disclosed upfront.

pass: true
