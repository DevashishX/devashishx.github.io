---
layout: post
title: FIXConnect
description: Early UI scaffolding for trade order modify/cancel workflows in a FIX integration context.
main_page_display_description: Prototype desktop forms for order lifecycle actions, generated with PAGE/Tkinter and prepared for backend request wiring.
main_page_display_description_de: Prototypische Desktop-Formulare fuer Order-Lifecycle-Aktionen, mit PAGE/Tkinter erzeugt und fuer Backend-Request-Wiring vorbereitet.
tile_image: /assets/images/projects/fix.png
---

[GitHub Repository](https://github.com/DevashishX/FIXConnect){:target="_blank"}

FIXConnect captures an early-stage UI prototype for handling order management actions commonly found in trading connectivity workflows.

## What it does

- Provides dedicated desktop windows for cancel and modify actions.
- Exposes fields for key order attributes and time-in-force related parameters.
- Includes tooltip-assisted controls and generated support modules for window lifecycle handling.
- Defines placeholders for request payload/endpoint handling.

## How it is built

- GUI forms are generated via PAGE (Tkinter/Tcl tooling), with Python wrappers and Tcl source files.
- Window start/stop and widget bootstrapping are separated into support modules.
- Request integration scaffolding exists in `requestlib.py` and `requestformat.py` for later API wiring.
- Current repository state focuses on frontend interaction flow rather than completed trade transport logic.

## Tech stack

Python Tkinter, Tcl/Tk (PAGE-generated forms).
