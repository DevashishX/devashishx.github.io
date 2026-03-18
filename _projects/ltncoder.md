---
layout: post
title: LTNcoder
description: Neuro-symbolic process anomaly detection using logic constraints and deep learning.
main_page_display_description: A research-oriented anomaly detection framework that combines Declare process rules with Logic Tensor Networks and neural models.
main_page_display_description_de: Ein forschungsorientiertes Framework für Anomalieerkennung, das Declare-Regeln mit Logic Tensor Networks und neuronalen Modellen kombiniert.
tile_image: /assets/images/projects/neurosymbolic.png
---

[GitHub Repository](https://github.com/DevashishX/LTNcoder){:target="_blank"}

LTNcoder explores **neuro-symbolic process anomaly detection** by combining classical process mining signals with neural anomaly detection models. The project centers around a notebook-driven workflow for data preparation, Declare rule mining, model training, and evaluation.

## What it does

- Generates and prepares process event logs (including BPIC and synthetic variants).
- Mines Declare constraints and transforms them into features usable by downstream models.
- Trains anomaly detectors across multiple datasets and compares strategies/heuristics.
- Evaluates models with reproducible notebook pipelines and database-backed experiment tracking.

## How it is built

- Uses a python package structure for datasets, filesystem conventions, evaluators, and anomaly detection modules.
- Integrates TensorFlow/Keras-based models with Logic Tensor Network concepts in custom encoder modules.
- Stores and tracks event logs/models/results with structured naming and SQLite-backed metadata.
- Provides dataset-specific training/evaluation notebooks (e.g., paper, small/large, BPIC variants) for controlled experiments.

## Tech stack

Python, TensorFlow/Keras, Logic Tensor Network tooling, SQLAlchemy, scikit-learn, Jupyter notebooks, process-mining libraries.
