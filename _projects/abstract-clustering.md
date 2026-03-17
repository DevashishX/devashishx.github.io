---
layout: post
title: AbstractClustering
description: NLP pipeline for clustering research paper abstracts with multiple embedding and clustering strategies.
main_page_display_description: A full experiment pipeline for preprocessing abstracts, generating embeddings, and clustering papers with classical and deep methods.
main_page_display_description_de: Eine komplette Experiment-Pipeline zur Vorverarbeitung von Abstracts, Erzeugung von Embeddings und Clustering mit klassischen und Deep-Learning-Methoden.
tile_image: /assets/images/projects/abstract-clustering.svg
---

[GitHub Repository](https://github.com/DevashishX/AbstractClustering){:target="_blank"}

AbstractClustering is a final-year NLP/ML project focused on grouping research paper abstracts into meaningful thematic clusters.

## What it does

- Ingests large paper metadata/abstract datasets.
- Cleans and preprocesses text for downstream vectorization.
- Builds word and sentence representations using multiple embedding choices.
- Runs clustering experiments across algorithms and tracks quality metrics.

## How it is built

- Core modules separate preprocessing, word embedding loading, sentence embedding creation, and data conversion.
- Uses p-means style sentence embedding aggregation from word vectors.
- Supports several clustering workflows (K-Means, spectral, hierarchical, DBSCAN, and deep embedded clustering notebooks).
- Includes templates/notebooks for parameter sweeps and optimal K analysis, with model metadata logging.

## Tech stack

Python, NumPy, pandas, scikit-learn, TensorFlow/Keras, NLTK/Gensim, Jupyter notebooks, SQLite.
