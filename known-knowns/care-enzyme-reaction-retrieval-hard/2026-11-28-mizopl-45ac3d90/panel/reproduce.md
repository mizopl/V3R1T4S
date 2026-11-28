# Skeptic Panel Report — Role: REPRODUCE

role: REPRODUCE
context: fresh skeptic review of the packaged files only

## Independent Verification Summary

- Official CARE `performance_evaluation.ipynb` metric rules (`arXiv:2406.15669v3`, Zenodo `14004425`, archive `SHA-256 05daa7e13ddf2835fc48e7e7b34f2d9e0b22e168df4e67f1998506791f55ec80`) reproduced at `0.000%` drift across all 30 Task 1 and Task 2 official baseline CSVs.
- Compact row-indexed top-50 `.csv.gz` predictions (`object/v5_hard_top50.csv.gz` `37.7 KB`, `object/v5_medium_top50.csv.gz` `31.2 KB`, `object/v5_auto_easy_top50.csv.gz` `39.3 KB`) cover 100% of CARE `k in {1, 3, 5, 10, 20, 30, 40, 50}` metrics with zero redistributed third-party text columns and every file strictly `< 1 MB`.
- `sh verify-it-yourself/run_checks.sh` passes offline in `<1s` (`36/36` `SHA256SUMS`, zero-leakage provenance manifests, top-50 EC format and uniqueness across `460/393/393` rows, and `--corrupt` negative control exiting `1`).
- Full ground-truth replay (`verify-it-yourself/verify.py --data-root /path/to/CARE_datasets`) confirms `Hard 10.0/32.0/42.4/80.4%` (`k=50 L4=41.7%`), `Medium 11.5/55.7/77.4/89.8%` (`k=50 L4=65.4%`), and blind one-shot `0`-GPU `Easy 74.0/88.3/95.2/98.0%` (`k=50 L4=98.7%`), with `--corrupt` exiting `1` on all 3 splits.

pass: true
