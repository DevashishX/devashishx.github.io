---
layout: post
title: DNSGuard
description: Local DNS filtering server to block ad and malicious domains using configurable blacklists.
main_page_display_description: Runs a localhost DNS resolver proxy with runtime-reloadable blacklist matching and optional operational log archival scripts.
main_page_display_description_de: Läuft als localhost-DNS-Resolver-Proxy mit zur Laufzeit aktualisierbarer Blacklist und optionalen Skripten für Log-Archivierung.
tile_image: /assets/images/projects/dns.png
---

[GitHub Repository](https://github.com/DevashishX/DNSGuard){:target="_blank"}

DNSGuard is a lightweight DNS filtering service designed to block known advertising and risky domains at the DNS layer.

## What it does

- Listens for DNS queries on configurable host/port (default localhost:53).
- Parses requests and checks domains against a blacklist.
- Resolves and forwards allowed queries, while blocked entries are denied by policy.
- Reloads blacklist data automatically when blacklist files are modified.

## How it is built

- UDP DNS server loop in `DNSGuard.py` handles packet parse, policy check, and response writeback.
- Domain policy lives in `blacklist.py` with n-gram style suffix matching.
- Uses filesystem watch events to refresh blacklist data without restart.
- Includes ops scripts for install, log rotation copy/remove, and optional S3 log upload testing.

## Tech stack

Python, dnslib, dnspython, pyinotify, Linux ops scripts.
