# LoRA Fine-Tuning of GPT-2

## Overview
This project demonstrates parameter-efficient fine-tuning of GPT-2 using LoRA (PEFT) across a curated mixture of 10 text-only datasets. The goal was to evaluate efficiency–performance trade-offs using different LoRA ranks.

---

## 🔎 Full Execution Notebook

⚠️ Note: Outputs were removed from the GitHub notebook to ensure compatibility with GitHub rendering.

To view the **complete executed notebook with outputs, training logs, and results**, please visit:

👉 **Colab Link:**  
https://colab.research.google.com/drive/1Ql2CWIoQslneqnkDMHU4JWgXYgXsxSAB?usp=sharing

---

## Model Details
- Base model: GPT-2 (124M parameters)
- Fine-tuning method: LoRA (PEFT)
- Target module: `c_attn`
- LoRA ranks tested:
  - r = 8
  - r = 4

---

## Datasets Used
The model was trained on a curated mixture of the following text-only datasets:

- WikiText-2
- WikiText-103
- TinyStories
- AG News
- XSum
- CNN/DailyMail
- SQuAD (context field)
- Yelp Review Full
- IMDB
- Menlo Instruction Text Only

All datasets were sampled to remain within T4 GPU memory constraints.

---

## Results

| Configuration | LoRA Rank | Perplexity |
|--------------|-----------|------------|
| Run 1        | r = 8     | ~76        |
| Run 2        | r = 4     | **18.94**  |

Reducing LoRA rank by 50% reduced trainable parameters and improved validation perplexity, indicating better generalization.

---

## Hardware
- NVIDIA T4 GPU (Google Colab)

---

## Experiment Tracking
All experiments were tracked using **Weights & Biases (W&B)**.

---

## Installation

```bash
pip install -r requirements.txt
