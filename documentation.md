# Technical Documentation

## Why LoRA?
LoRA enables parameter-efficient fine-tuning by training low-rank adaptation matrices instead of full model weights.

## Model Configuration
- GPT-2 small
- LoRA rank: 8 and 4
- Target module: c_attn

## Dataset Strategy
10 curated text-only datasets were combined.
Datasets were sampled to remain within Colab storage constraints.

## Training Setup
- Epochs: 2
- Batch size: 4
- Learning rate: 5e-5
- Evaluation per epoch

## Key Finding
Reducing LoRA rank from 8 to 4 reduced trainable parameters by ~50% while improving perplexity from ~76 to 18.94.
