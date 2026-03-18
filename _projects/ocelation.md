---
layout: post
title: ocelation
description: Object-centric event log generation from relational schemas with graph analytics and LLM-assisted steps.
main_page_display_description: Converts relational DDL into graph structures, detects communities, and derives merge/join sequences toward OCEL-style event representations.
main_page_display_description_de: Wandelt relationale DDL in Graphstrukturen um, erkennt Communities und leitet Merge/Join-Sequenzen für OCEL-ähnliche Event-Repräsentationen ab.
tile_image: /assets/images/projects/sql.png
---

[GitHub Repository](https://github.com/DevashishX/ocelation){:target="_blank"}

ocelation experiments with generating object-centric event data from relational databases by combining graph decomposition and sequence construction.

## What it does

- Parses SQL DDL into table/relationship metadata.
- Builds directed graph views of schema dependencies.
- Runs community-detection analyses to partition schemas into meaningful subgraphs.
- Produces sequence and join-generation artifacts for creating merged event-log tables.

## How it is built

- `clustering_utils` and `cluster/analyser` modules evaluate multiple NetworkX community algorithms.
- `sequence` utilities build spanning-tree-based merge sequences over expanded communities.
- `join/merge.py` generates SQL join statements and resolves naming collisions.
- Notebooks capture exploratory runs, visualization, and prompt-driven LLM experiments.

## Tech stack

Python, NetworkX, cdlib, matplotlib, Jupyter notebooks, SQL/DDL parsing.
