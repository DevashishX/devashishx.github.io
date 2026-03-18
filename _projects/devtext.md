---
layout: post
title: devtext
description: Terminal text editor in C using ncurses and a custom linked-list buffer model.
main_page_display_description: A from-scratch TUI editor with file operations, navigation, search/replace, and clipboard-style editing behavior.
main_page_display_description_de: Ein von Grund auf gebauter TUI-Editor mit Dateiverarbeitung, Navigation, Suchen/Ersetzen und Zwischenablage-aehnlichen Funktionen.
tile_image: /assets/images/projects/terminal.jpg
---

[GitHub Repository](https://github.com/DevashishX/devtext){:target="_blank"}

devtext is a systems-style project that implements a text editor in C for the terminal, with explicit memory management and custom buffer logic.

## What it does

- Opens existing files or starts new buffers from CLI.
- Supports cursor navigation, page movement, and home/end controls.
- Handles editing actions like insert/delete/backspace/enter.
- Provides search, search-replace, cut/copy/paste, save, and save+quit shortcuts.

## How it is built

- Uses ncurses for screen rendering, keyboard input, colors, and status/help overlays.
- Represents the document as a doubly-linked list of line buffers (`buffer.c` / `buffer.h`).
- Implements explicit line insert/delete and buffer split/merge logic.
- Keeps rendering and data structure concerns separated (`gui_ncs.*` vs `buffer.*`).

## Tech stack

C, ncurses, Makefile-based build flow.
