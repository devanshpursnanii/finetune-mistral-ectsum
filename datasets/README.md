# Datasets

This project uses the **ECTSum dataset** for executive summarization of earnings calls.

Due to licensing and redistribution restrictions, the dataset files are **not included** in this repository.

---

## How to obtain ECTSum

1. Visit the official ECTSum repository or paper page
2. Download the original train / validation / test splits
3. Place the data locally in JSON or TXT form as described in the notebooks

---

## Processed subsets

The following processed dataset(s) are generated during experimentation:
- `test500.jsonl`

These are **random subsets** created from the original data using the provided notebooks.

To reproduce them, run:
- the dataset sampling cells in `finetune_ect.ipynb`
- or the sampling steps in the evaluation notebooks

---

## Attribution

ECTSum dataset:
> *ECTSum: A New Benchmark for Executive Summarization of Earnings Calls*

All rights to the dataset belong to the original authors.
