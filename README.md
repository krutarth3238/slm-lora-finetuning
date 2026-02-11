# LoRA Fine-Tuning of GPT-2

## Overview
This project demonstrates LoRA-based fine-tuning of GPT-2 on multiple text-only datasets using PEFT.

## Model
- Base model: GPT-2 (124M parameters)
- LoRA ranks tested: r=8 and r=4

## Results

| Rank | Perplexity |
|------|------------|
| r=8  | ~76 |
| r=4  | 18.94 |

Lower rank achieved better generalization.

## Hardware
- NVIDIA T4 (Google Colab)

## Experiment Tracking
- Weights & Biases used

## How to Run
Install dependencies:
