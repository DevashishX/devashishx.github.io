---
layout: post
title: MCP Factory
description: FastMCP orchestrator and RAG tooling for PCB assembly process automation.
main_page_display_description: Dual MCP servers provide process orchestration and retrieval over PCB documentation, with both GUI and agent-ready interfaces.
main_page_display_description_de: Zwei MCP-Server bieten Prozess-Orchestrierung und Dokumenten-Retrieval für PCB-Fertigung, mit GUI und agentenfähigen Schnittstellen.
tile_image: /assets/images/projects/mcp.png
---

[GitHub Repository](https://github.com/DevashishX/MCPFactoryAutomation){:target="_blank"}

MCPFactoryAutomation demonstrates how a manufacturing workflow can be exposed through MCP tools for both human operators and AI assistants.

## What it does

- Offers a visual orchestrator for 5-step PCB assembly sequences.
- Validates user-selected step parameters against predefined valid processes.
- Exposes orchestration actions as FastMCP tools.
- Adds a RAG server that retrieves process details from markdown process documents.

## How it is built

- `orchestrator_gui.py` implements the desktop workflow editor in CustomTkinter.
- `orchestrator_fastmcp_server.py` wraps orchestration operations as MCP tools over stdio or HTTP.
- `rag_fastmcp_server.py` builds a Chroma vector store from docs using LangChain + Ollama embeddings.
- Startup scripts run both servers for local agent integration.

## Tech stack

Python, FastMCP, CustomTkinter, LangChain, Chroma, Ollama embeddings, dotenv.
