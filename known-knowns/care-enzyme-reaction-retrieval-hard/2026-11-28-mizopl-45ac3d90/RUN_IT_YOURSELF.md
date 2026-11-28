# Run It Yourself

Offline check (`<1s`, zero external downloads):

```sh
sh verify-it-yourself/run_checks.sh
```

Full Zenodo `14004425` ground-truth replay (`0.000%` drift vs official `performance_evaluation.ipynb`):

```sh
python3 verify-it-yourself/verify.py --data-root /path/to/CARE_datasets
```
