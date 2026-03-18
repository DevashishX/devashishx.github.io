---
layout: post
title: PythonHostIDS
description: Host-based intrusion detection with filesystem monitoring and email alerts.
main_page_display_description: Watches files/folders for suspicious access or modification events and sends structured alert reports by email.
main_page_display_description_de: Ueberwacht Dateien/Ordner auf verdaechtige Zugriffe oder Aenderungen und versendet strukturierte Alarmberichte per E-Mail.
tile_image: /assets/images/projects/IDS.PNG
---

[GitHub Repository](https://github.com/DevashishX/PythonHostIDS){:target="_blank"}

PythonHostIDS is a lightweight host-based IDS that focuses on **file activity visibility** and quick incident notification.

## What it does

- Monitors a target directory using Linux inotify events.
- Collects access/modification event metadata in real time.
- Generates CSV reports from captured events.
- Sends alert emails with report attachments via SendGrid.

## How it is built

- Uses a custom `pyinotify` event processor that pushes event records to a queue.
- Main loop drains events, builds pandas DataFrames, and persists timestamped reports.
- `sendmail.py` encapsulates SendGrid API handling and attachment delivery.
- CLI arguments configure watch path, report output path, sender, and recipient list.

## Tech stack

Python, pyinotify, pandas, SendGrid API.
