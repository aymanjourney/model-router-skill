# Model Routing Skill

**Description:** A simple routing logic for an AI Agent to select the best open-source model for a given task, based strictly on real Artificial Analysis benchmarks.

## The Strategy

When the user provides a prompt, determine its core objective. Use the following mapping to decide which model on the user's Ollama VPS should handle the task. 

### 1. 🧠 High Intelligence & Deep Reasoning
**When to use:** Math, complex logic puzzles, and high-level reasoning tasks.
**Best Models:**
- `kimi-k2.6` (Top Intelligence Index)
- `mimo-v2.5-pro` (Strong logic & lowest hallucination rate)

### 2. 💻 Coding, Software Engineering & Terminal Use
**When to use:** Writing code, debugging, creating scripts, agentic terminal workflows.
**Best Models:**
- `deepseek-v4-pro` (Top in Terminal-Bench Hard & coding)
- `kimi-k2.6` (Top in SciCode & SWE tasks)
- `glm-5.1` (Excellent agentic coding)

### 3. 📋 Planning & Agentic Execution
**When to use:** Multi-step workflows, system architecture, executing real-world agentic work tasks.
**Best Models:**
- `mimo-v2.5-pro` (Top in GDPval-AA agentic workflows)
- `glm-5.1` 
- `deepseek-v4-pro`

### 4. ⚡ Fast Execution & General Chat
**When to use:** Quick answers, formatting text, short queries, translations where speed is priority.
**Best Models:**
- `deepseek-v4-flash` (Fastest reasoning)
- `mimo-v2.5` 
- `gemma-4:31b` (Best small model)

### 5. 🔍 Massive Context & Synthesis
**When to use:** Extremely complex synthesis, highly ambiguous requests, reading massive documents.
**Best Model:**
- `deepseek-v4-pro` (Due to massive context window limits)
- `mimo-v2.5-pro`

## How to execute:
1. Receive task from user.
2. Identify task category (1-5).
3. Connect to the VPS Ollama API requesting the matched model.
4. Return the result to the user.
