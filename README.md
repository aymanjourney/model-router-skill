# 🧠 Model Router Skill — Intelligent Task-to-Model Routing

## Overview
An orchestrator agent skill that automatically analyzes every incoming task and routes it to the optimal open-source model running on your local machine or remote VPS. Based strictly on benchmarks from Artificial Analysis.

## Architecture

```
model-router-skill/
├── README.md                    # This file
├── skill.md                     # Core skill logic (Routing Matrix)
├── awaken_skill.md              # Skill installer/awakener for any AI Agent
├── model_registry.yaml          # Model catalog with capabilities
├── router.py                    # Python routing engine (Ollama API)
└── config.env                   # Connection settings (Ollama VPS)
```

## How It Works

```
User Request
     │
     ▼
┌──────────────┐
│ Orchestrator │  ← Analyzes task type (Reasoning, Coding, Planning, etc.)
│   (Agent)    │
└──────┬───────┘
       │ Routes to best open-source model via Ollama
       ▼
┌────────────────────────────────────────────────────────┐
│                      Model Pool                        │
│                                                        │
│  🧠 Intelligence/Reasoning → Kimi-K2.6 / MiMo-V2.5-Pro │
│  💻 Coding & Terminal      → DeepSeek-V4-Pro / Kimi    │
│  📋 Planning & Agentic     → MiMo-V2.5-Pro / GLM-5.1   │
│  ⚡ Fast Execution         → DeepSeek-V4-Flash         │
│  🔋 Small Models (<40B)    → Gemma-4-31B / QwQ-32B     │
└────────────────────────────────────────────────────────┘
```

## Quick Start
1. Edit `config.env` with your Ollama VPS address.
2. Ensure the top open-source models are pulled to your VPS.
3. Feed the `awaken_skill.md` file to your AI Agent to permanently install this routing logic.
4. From now on, your Agent will automatically delegate tasks to the best localized model without relying on external paid APIs.

## Compatibility
- **Ollama** (Local or remote VPS via standard API)
- 100% Open Source Models, no external API keys required.
