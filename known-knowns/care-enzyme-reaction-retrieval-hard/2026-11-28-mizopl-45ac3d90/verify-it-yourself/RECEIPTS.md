# Verification Receipts

- Offline `sh verify-it-yourself/run_checks.sh`: PASS (`<1s`, `--corrupt` exited `1`).
- Full Zenodo `14004425` ground-truth replay (`verify-it-yourself/verify.py --data-root ...`): Hard `10.0/32.0/42.4/80.4%` (`k=50 L4=41.7%`), Medium `11.5/55.7/77.4/89.8%` (`k=50 L4=65.4%`), Easy `74.0/88.3/95.2/98.0%` (`k=50 L4=98.7%`); `--corrupt rc=1` on all 3 splits.
