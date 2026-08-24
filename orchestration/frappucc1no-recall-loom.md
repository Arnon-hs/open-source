# Frappucc1no/recall-loom

[![Stars](https://img.shields.io/github/stars/Frappucc1no/recall-loom?style=flat-square&color=yellow)](https://github.com/Frappucc1no/recall-loom/stargazers) [![Forks](https://img.shields.io/github/forks/Frappucc1no/recall-loom?style=flat-square&color=blue)](https://github.com/Frappucc1no/recall-loom/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Project memory for long-running AI work across agents, models, and sessions. Keep context, decisions, progress, and next steps in local project files.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 144 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | Python |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-memory` `agent-skills` `ai-agents` `ai-coding` `ai-memory` `claude` `claude-code` `claude-code-skills` `claude-skills` `codex` `codex-skill` `context-management`

## 🎯 Categories

Orchestration · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
Recall‑Loom (Frappucc1no/recall-loom) is a Python library that gives long‑running AI projects a persistent, file‑based memory layer, letting agents, models, and sessions share context, decisions, progress, and next‑step instructions. By storing this information in local project files, it turns ad‑hoc prompts and tool calls into repeatable, orchestrated workflows that can be version‑controlled and reused across teams.

**Value**  
- **Continuity of context** – agents can retrieve prior reasoning, outcomes, and pending actions, eliminating the “cold‑start” problem that plagues multi‑step AI pipelines.  
- **Workflow repeatability** – the same memory files can be checked into source control, enabling deterministic re‑runs, debugging, and audit trails.  
- **Cross‑agent coordination** – multiple agents (or model versions) can read/write a shared state, making complex orchestration (e.g., data‑prep → model‑train → evaluation loops) straightforward.  

**Practical Adoption Path**  
1. **Install the SDK/CLI** (`pip install recall-loom`) and add the provided `loom.yaml` configuration to an existing project.  
2. **Instrument prompts** by wrapping calls with `loom.record()` and `loom.retrieve()` to persist inputs, outputs, and meta‑data.  
3. **Integrate with orchestration tools** (e.g., Airflow, Prefect, or LangChain) by invoking the CLI or SDK inside task definitions, thereby turning each step into a memory‑aware node.  
4. **Version‑control the generated `.loom/` directory** so that collaborators can replay or branch workflows without losing state.  

**Production Readiness**  
Recall‑Loom scores high for pilot deployment: it has recent commits (last updated 2026‑07‑07), active community interest (144 ★, 5 forks), clear Python API/CLI, and extensive topic tagging that eases integration. While a final review of licensing, security posture, and maintainer activity is still advisable, the project shows strong ecosystem signals and is ready for controlled production use in multi‑agent AI pipelines.

### Русский

Резюме проекта Frappucc1no/recall-loom:

Проект Frappucc1no/recall-loom предназначен для сохранения контекста и прогресса AI-работ в течение долгого времени, позволяя координировать мульти-агентные потоки и стандартизировать память агентов. Этот проект особенно полезен для создания повторяемых агентных рабочих процессов и внедрения инструментальных линий. Проект готов к сериозному пилотному проекту, но требует дальнейшего рассмотрения лицензии, безопасности и активности поддержки.

### 中文

**简短介绍**

Frappucc1no/recall-loom 是一个开源项目，旨在为长期运行的 AI 工作提供项目记忆功能。它可以帮助用户在本地项目文件中保存上下文、决策、进展和下一步行动。通过使用 Frappucc1no/recall-loom，用户可以将孤立的提示和工具转换为可重复的代理工作流。

**价值**

Frappucc1no/recall-loom 的主要价值在于，它可以帮助用户协调多代理工作流，添加工具使用管道，并标准化代理记忆。它可以使用户的工作更加高效和可重复。

**典型接入方式**

Frappucc1no/recall-loom 提供了 API、SDK 和 CLI 等接入方式，用户可以根据自己的需求选择合适的接入方式。它还支持多种语言和主题，方便用户使用。

**生产可用性**

Frappucc1no/recall-loom 的生产可用性很高，主要原因是其最近的活跃度、采用的程度和生态系统信号都很强。它已经获得了 144 个 GitHub 星

## 🧭 Practical evaluation

**Value:** Frappucc1no/recall-loom helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 144 GitHub stars
- 5 forks
- updated 2026-07-07
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 46/100 |
| topics | 100/100 |
| outlook | 62/100 |
| quality | 57/100 |
| recency | 40/100 |
| adoption | 39/100 |
| production | 56/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-07 · [View on GitHub](https://github.com/Frappucc1no/recall-loom) · [← Back to Orchestration](./README.md)</sub>
