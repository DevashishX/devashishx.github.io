---
layout: post
title: GenKI-Karten
description: AI-assisted enhancement pipeline for Anki vocabulary decks.
main_page_display_description: Enriches flashcards with generated usage examples, with a mock mode for safe testing and automated deck validation.
main_page_display_description_de: Reichert Flashcards mit generierten Anwendungsbeispielen an, mit Mock-Modus fuer sicheres Testen und automatischer Deck-Validierung.
tile_image: /assets/images/projects/flashcards.png
---

[GitHub Repository](https://github.com/DevashishX/GenKI-Karten){:target="_blank"}

GenKI-Karten is an Anki workflow helper that augments vocabulary cards with generated explanations and usage examples.

## What it does

- Loads tab-separated Anki deck exports.
- Generates additional explanatory content per card entry.
- Supports mock generation for deterministic tests.
- Writes updated deck files ready for re-import.

## How it is built

- Uses an abstraction layer (`Explanation`) with concrete implementations for mock and LLM-backed generation.
- Defines structured example output models with Pydantic.
- Includes test utilities to reset fixture decks and validate read/write behavior.
- Uses environment-based API key configuration for provider access.

## Tech stack

Python, pandas-style deck processing workflow, Pydantic, dotenv, Google GenAI client.
