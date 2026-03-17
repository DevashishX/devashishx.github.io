---
layout: post
title: projectNMT
description: Neural machine translation project for English to German/French with fairseq-based training and inference.
main_page_display_description: A sequence-to-sequence translation stack with training, generation, and interactive inference scripts, plus service-style usage.
main_page_display_description_de: Ein Sequence-to-Sequence-Uebersetzungs-Stack mit Training, Generierung und interaktiver Inferenz, inklusive serviceartiger Nutzung.
tile_image: /assets/images/projects/project-nmt.svg
---

[GitHub Repository](https://github.com/DevashishX/projectNMT){:target="_blank"}

projectNMT focuses on practical neural machine translation for **English to German/French** using a research-style codebase based on fairseq components.

## What it does

- Trains translation models using encoder-decoder architectures.
- Runs batch generation and interactive translation.
- Supports preprocessing/tokenization workflows (including SentencePiece utilities).
- Packages translation models for local service workflows.

## How it is built

- Includes a full `fairseq` code tree with task/model/criterion registries.
- Uses dedicated scripts for training (`train.py`), generation (`generate.py`), and interactive decoding.
- Adds utility scripts for binarized dataset inspection and score analysis.
- Provides project-level instructions for deploying trained checkpoints for EN-DE and EN-FR use cases.

## Tech stack

Python, PyTorch, fairseq, SentencePiece, sacrebleu and related MT tooling.
