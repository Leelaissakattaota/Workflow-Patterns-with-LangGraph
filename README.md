# 🤖 Implement Workflow Patterns with LangGraph

![LangChain](https://img.shields.io/badge/Framework-LangChain-blue?style=for-the-badge&logo=langchain)
![LangGraph](https://img.shields.io/badge/Library-LangGraph-orange?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3.9+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![OpenAI](https://img.shields.io/badge/Model-GPT--4o--Mini-412991?style=for-the-badge&logo=openai)

Explore the architectural patterns that transform standalone Large Language Models into sophisticated, coordinated AI systems. This project demonstrates three essential workflow patterns: **Sequential Prompt Chaining**, **Intent-Based Routing**, and **Parallel Agent Execution**.

---

## 🛠️ Workflow Patterns Explored

### 🔗 1. Prompt Chaining (Sequential)
Decomposes complex tasks into a sequence of LLM calls where each step depends on the previous output.
* **Use Case:** Job Application Assistant.
* **Flow:** Job Description ➡️ Resume Tailoring ➡️ Cover Letter Generation.

### 🚦 2. Intent-Based Routing
Uses an LLM as a "switchboard" to classify user intent and direct the workflow to specialized handlers.
* **Use Case:** Task Classifier.
* **Flow:** User Input ➡️ Router (Classification) ➡️ Summarization **OR** Translation.

### ⚡ 3. Parallelization
Executes independent tasks simultaneously to improve speed and efficiency, then aggregates results.
* **Use Case:** Multilingual Assistant.
* **Flow:** English Input ➡️ (French + Spanish + Japanese Translations) ➡️ Aggregated Report.

---

## 🏗️ Architecture Visualization

The workflows are built using **LangGraph**'s state machine architecture:

| Pattern | Logic Type | Key Component |
| :--- | :--- | :--- |
| **Chaining** | Linear | `workflow.add_edge(node_a, node_b)` |
| **Routing** | Conditional | `workflow.add_conditional_edges()` |
| **Parallel** | Concurrent | `graph.add_edge(START, parallel_nodes)` |

---

## 🚀 Getting Started

### Prerequisites
- Python 3.9+
- OpenAI API Key

### Installation
```bash
pip install langchain-openai langgraph pygraphviz
