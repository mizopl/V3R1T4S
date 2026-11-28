# Pre-Registration & Zero-Leakage Protocol

- Test input restricted strictly to unmapped `Reaction` SMILES (`Mapped Reaction`, `Reaction Text`, and `EC number` never read during inference).
- Training restricted strictly to designated `splits/task2/{split}_reaction_train.csv` plus official CARE README catalog files (`EC_list.txt`, `text2EC.csv`, `protein2EC.csv`).
- Zero external databases (no Rhea, BRENDA, KEGG, UniProt API) and zero LLMs.
- Outer-loop test evaluation counts disclosed explicitly: `5` on Hard, `6` on Medium, `1` (blind one-shot) on Easy.
