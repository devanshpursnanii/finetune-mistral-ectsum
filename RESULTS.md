# Results and Evaluation

This document summarizes the evaluation results for executive summarization on the ECTSum dataset.

---

## Models Evaluated

- **Base model**: Mistral-7B (4-bit, no fine-tuning)
- **Fine-tuned model**: Mistral-7B with QLoRA adapters trained on ECTSum

Evaluation was performed on a fixed random subset (`test500.jsonl`) sampled from the test split.

---

## Automatic Metrics

| Metric        | Base Model | Fine-tuned Model |
|--------------|-----------:|-----------------:|
| ROUGE-1      | ~0.03      | ~0.03            |
| ROUGE-2      | ~0.01      | ~0.01            |
| ROUGE-L      | ~0.02      | ~0.02            |
| BLEU         | ~0.005     | ~0.005           |
| BERTScore F1 | ~0.80      | ~0.80            |

(Exact values may vary slightly depending on the sampled subset.)

---

## Interpretation

- ROUGE and BLEU scores are low for both models due to the **highly abstractive nature** of executive summaries.
- The base model already captures general financial semantics, leading to relatively high BERTScore values.
- Fine-tuning with lightweight LoRA adapters resulted in **minimal changes in surface-level metrics**, suggesting that:
  - the fine-tuning primarily affects style and structure
  - or that the adapter capacity / training duration was conservative

---

## Notes on Evaluation

- Automatic metrics alone are insufficient for fully judging summary quality in this task.
- Qualitative inspection of generated summaries is recommended to assess improvements in:
  - executive tone
  - conciseness
  - structural clarity

---

## Limitations

- Evaluation was performed on a small sampled subset for efficiency.
- All datasets and training parameters were scaled down due to GPU limitations (T4 GPU free tier on Google Colab)
- No human evaluation was conducted.
- Metrics should be interpreted as **relative signals**, not absolute measures of quality.
