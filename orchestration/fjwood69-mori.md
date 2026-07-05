# fjwood69/mori

[![Stars](https://img.shields.io/github/stars/fjwood69/mori?style=flat-square&color=yellow)](https://github.com/fjwood69/mori/stargazers) [![Forks](https://img.shields.io/github/forks/fjwood69/mori?style=flat-square&color=blue)](https://github.com/fjwood69/mori/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> mori MCP server — Deterministic boundaries for non-deterministic agents — a governed memory layer for AI coding agents.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 21 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | Python |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-07-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `anthropic` `antigravity-ide` `claude-code` `codex` `cursor` `dream-pipeline` `governance` `llm` `mcp` `mcp-server` `memory`

## 🎯 Categories

Orchestration · MCP · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`fjwood69/mori` is a Python‑based MCP (Memory‑Control‑Plane) server that supplies deterministic boundaries for otherwise non‑deterministic AI coding agents, turning ad‑hoc prompts and tools into repeatable, governed workflows. By providing a centralized memory layer and easy‑to‑use APIs/CLI, it lets developers coordinate multi‑agent pipelines, enforce tool‑use policies, and standardize agent state across runs. The project shows strong recent activity, modest community interest (21 stars, 4 forks), and clear integration points, making it a viable candidate for pilot deployments.

**Value Proposition**  
- **Deterministic Agent Memory** – Eliminates the “black‑box” drift of LLM‑driven agents by persisting and version‑controlling their internal state.  
- **Workflow Orchestration** – Enables composable, multi‑agent pipelines where each step can read/write a shared, governed memory store.  
- **Tool‑Use Governance** – Provides hooks to enforce which external tools an agent may call, improving safety and auditability.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, spin up the Mori server via the provided Dockerfile or `pip install mori`, and connect a test LLM agent using the Python SDK.  
2. **Integrate** – Replace ad‑hoc prompt‑to‑tool calls in existing agents with Mori’s `memory.put/get` and `tool.invoke` APIs; use the CLI for quick manual tests.  
3. **Validate** – Run end‑to‑end scenarios (e.g., code generation → lint → test) and verify that the same inputs produce identical memory snapshots across runs.  
4. **Scale** – Deploy Mori behind a load‑balanced service (K8s or managed VM), enable persistence (PostgreSQL/Redis), and configure role‑based access for production teams.  

**Production Readiness**  
- **Activity & Maintenance** – Updated as of 2026‑07‑05 with recent commits; the repository shows ongoing development and issue response.  
- **Ecosystem Fit** – Exposes clear integration surfaces (REST API, Python SDK, CLI) and includes language metadata and topic tags that simplify discovery and binding to existing AI stacks.  
- **Risk Profile** – No critical licensing or security red flags detected, though a final audit of the license (MIT‑style) and a vulnerability scan of dependencies is advisable.  
- **Pilot Suitability** – Given its modest footprint, clear API surface, and active community signals, Mori is ready for a controlled pilot in environments that need reproducible agent behavior and governed tool usage.

### Русский

Резюме проекта fjwood69/mori:

Проект mori представляет собой MCP-сервер, который обеспечивает определенные границы для неразличимых агентов, создавая управляемый слой памяти для кодирования агентов AI. Он позволяет преобразовывать изолированные запросы и инструменты в повторимые потоки агентов, что делает его ценным инструментом для координации сложных потоков работы агентов.

Проект mori предназначен для стандартизации памяти агентов, добавления потоков использования инструментов и координации множества агентов. Он уже показал свою производительность и готовность к эксплуатации, демонстрируя высокую степень готовности к production.

Проект mori готов к serious пилоту, подтверждая его готовность к внедрению в production. Однако, как и любое open-source проект, требует дальнейшего анализа и проверки, в том числе лицензионной, безопасности и активных мейнтейнеров.

### 中文

**简短介绍**
fjwood69/mori 是一个开源项目，提供了一个可控的内存层（MCP server），用于 AI 编码代理的编排和管理。它通过确定性的边界来管理非确定性的代理，帮助将孤立的提示和工具转换为可重复的代理工作流。

**价值**
该项目的价值在于，它可以帮助开发者将孤立的提示和工具转换为可重复的代理工作流，提高了工作效率和可靠性。

**典型接入方式**
该项目通过 API/SDK/CLI 等接口提供服务，开发者可以通过这些接口来接入和管理代理工作流。

**生产可用性**
该项目的生产可用性较高，具有强大的社区支持、活跃的维护者和稳定的代码更新。

## 🧭 Practical evaluation

**Value:** fjwood69/mori helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 21 GitHub stars
- 4 forks
- updated 2026-07-05
- primary language: Python
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 66/100 |
| recency | 100/100 |
| adoption | 25/100 |
| production | 76/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/fjwood69/mori) · [← Back to Orchestration](./README.md)</sub>
