# Aureven-v1

Latest update and model weights for a 0.128B or 100 Million parameter LLM, built as an edge AI 
for agentic behavior research and neural network studying.

## Overview

Aureven-v1 is a fully custom-built and custom-trained Small Language Model (SLM), 
paired with a fully custom-trained tokenizer designed specifically for this model 
family. Unlike fine-tunes of existing architectures, both the model and tokenizer 
were built from scratch as part of an ongoing research effort into efficient, 
lightweight language models capable of running on edge hardware.

The model was trained for over 8 hours on 2x NVIDIA T4 GPUs, and achieves:
- **12 PPL** on the training set
- **58 PPL** on the validation set

Training data was the [TinyStories](https://huggingface.co/datasets/roneneldan/TinyStories) 
dataset, chosen for its simple narrative structure — ideal for validating whether 
a small custom architecture and tokenizer can learn coherent language patterns 
without the scale of larger foundation models.

## Purpose

Aureven-v1 serves as a **base benchmark** — a proof-of-concept to validate 
Aureven AI's custom tokenizer and architecture decisions before scaling up. It's 
the first step in a planned progression:

- **Aureven-v1** (0.128B) — current release, tokenizer/architecture validation
- **Aureven-v2** (0.5B) — planned, expanded capacity and training data
- **Aureven-v3** (1B) — planned, full-scale agentic research model

Despite its small size and the limited scope of its training data, Aureven-v1 
performed exceptionally well, demonstrating fast text generation and stable 
convergence — validating the tokenizer design ahead of larger training runs.

## Architecture

- **Parameters:** 0.128B
- **Architecture:** [fill in — e.g. decoder-only transformer, GPT-style]
- **Context length:** [fill in]
- **Tokenizer:** Custom-trained, vocab size [fill in]
- **Training hardware:** 2x NVIDIA T4 GPUs
- **Training time:** ~8 hours

## Intended Use

Designed for agentic behavior research, neural network study, and as a 
lightweight edge-deployable SLM for experimentation. Not intended for 
production use or tasks requiring broad world knowledge, given its limited 
training corpus.

## Model Weights & Tokenizer

This repo contains the code only. Model weights and tokenizer files are hosted 
on Kaggle:

🔗 **[Aureven-v1 on Kaggle](https://kaggle.com/datasets/46cd1aa1879801c3c8d31f3e206db7de31a97624149a52a13c85a2de5b36fe57)**

Download `model.pt`, `aureven_latest_checkpoint.pt`, `tokenizer.json`, and 
`tokenizer_meta.json` from the link above to run the model locally.

## License

See [LICENSE](LICENSE) for details.
