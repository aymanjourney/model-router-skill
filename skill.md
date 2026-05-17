# Model Routing Skill

**Description:** A simple routing logic for an AI Agent to select the best open-source model for a given task, based strictly on real Artificial Analysis benchmarks.

## The Strategy

When the user provides a prompt, determine its core objective. Use the following mapping to decide which model on the user's Ollama VPS should handle the task. 

### 1. 🧠 High Intelligence & Deep Reasoning
**When to use:** Math, complex logic puzzles, and high-level reasoning tasks.
**Best Models:**
- `ollama run kimi-k2.6:cloud` (Top Intelligence Index)
- `ollama run ollama run mimo-v2.5:cloud-pro:cloud` (Strong logic & lowest hallucination rate)

### 2. 💻 Coding, Software Engineering & Terminal Use
**When to use:** Writing code, debugging, creating scripts, agentic terminal workflows.
**Best Models:**
- `ollama run deepseek-v4-flash:cloud` (Top in Terminal-Bench Hard & coding)
- `ollama run kimi-k2.6:cloud` (Top in SciCode & SWE tasks)
- `ollama run glm-5.1:cloud` (Excellent agentic coding)

### 3. 📋 Planning & Agentic Execution
**When to use:** Multi-step workflows, system architecture, executing real-world agentic work tasks.
**Best Models:**
- `ollama run ollama run mimo-v2.5:cloud-pro:cloud` (Top in GDPval-AA agenticL workflows)
- `ollama run glm-5.1:cloud` 
- `ollama run deepseek-v4-flash:cloud`

### 4. ⚡ Fast Execution & General Chat
**When to use:** Quick answers, formatting text, short queries, translations where speed is priority.
**Best Models:**
- `ollama run deepseek-v4-flash:cloud` (Fastest reasoning)
- `ollama run mimo-v2.5:cloud` 
- `ollama run gemma-4:31b:cloud` (Best small model)

### 5. 🔍 Massive Context & Synthesis
**When to use:** Extremely complex synthesis, highly ambiguous requests, reading massive documents.
**Best Model:**
- `ollama run deepseek-v4-flash:cloud` (Due to massive context window limits)
- `ollama run ollama run mimo-v2.5:cloud-pro:cloud`



**⚠️ Plan Constraint (Free Tier):**
This routing is optimized for the **Ollama Free Plan**. It prioritizes high-efficiency cloud models to maximize the available free quota while maintaining quality.


## How to execute:
1. Receive task from user.
2. Identify task category (1-5).
3. Connect to the VPS Ollama API requesting the matched model.
4. Return the result to the user.
