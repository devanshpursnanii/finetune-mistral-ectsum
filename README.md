# ECTSum Fine-Tuning with QLoRA (Mistral-7B)

This repository contains experiments on fine-tuning a large language model for **executive summarization of earnings call transcripts** using the ECTSum dataset.

The project covers:
- Dataset preprocessing and sampling
- QLoRA fine-tuning with Unsloth
- Evaluation against a base model
- Metric-based comparison and analysis

---

## Dataset

This project uses the **ECTSum dataset** introduced in the paper:

> *ECTSum: A New Benchmark for Executive Summarization of Earnings Calls*

The dataset consists of earnings call transcripts paired with executive-style summaries.

**Important notes:**
- The full ECTSum dataset is **not redistributed** in this repository.
- Only small sampled / processed subsets are included for experimentation.
- All rights to the dataset belong to the original authors.
  
---

## Repository Structure

notebooks/ # Jupyter notebooks for training, testing, and comparison
scripts/ # Helper scripts for sampling and evaluation
datasets/ # Small processed datasets or download instructions
predictions/ # Model prediction outputs (if included)
results/ # Metric summaries and comparisons

---


---

## Experiments

The following experiments are included:

- Base model evaluation (Mistral-7B, 4-bit)
- Fine-tuned model with QLoRA
- Comparison using ROUGE, BLEU, and BERTScore

---

## Notes

This project is intended for:
- learning and experimentation
- benchmarking fine-tuning workflows
- portfolio demonstration

It is **not** an official reproduction of the ECTSum paper.

---

## Reproducibility (Quick)

1. Clone the repository
2. Install dependencies from `requirements.txt`
3. Download the ECTSum dataset 
4. Run `notebooks/finetune_ect.ipynb` to fine-tune
5. Run `notebooks/base_test.ipynb` and `notebooks/ft2_test.ipynb` for evaluation
6. Use `notebooks/final_comparison.ipynb` to compare results

