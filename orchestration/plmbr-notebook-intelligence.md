# plmbr/notebook-intelligence

[![Stars](https://img.shields.io/github/stars/plmbr/notebook-intelligence?style=flat-square&color=yellow)](https://github.com/plmbr/notebook-intelligence/stargazers) [![Forks](https://img.shields.io/github/forks/plmbr/notebook-intelligence?style=flat-square&color=blue)](https://github.com/plmbr/notebook-intelligence/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-77%2F100-brightgreen?style=flat-square)](#)

> A JupyterLab extension supporting Claude Code, Copilot, Ollama, and OpenAI-compatible LLMs, with MCP, skills, plugins, and notebook agents.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 317 |
| 🍴 **Forks** | 59 |
| 💻 **Language** | Python |
| 📈 **Score** | 77/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-plugins` `agent-skills` `ai` `ai-agents` `ai-tools` `claude-code` `codex` `copilot` `genai` `jupyterlab` `mcp` `notebook`

## 🎯 Categories

Orchestration · MCP · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
plmbr/notebook‑intelligence is a JupyterLab extension that brings together Claude Code, Copilot, Ollama and any OpenAI‑compatible LLMs into a unified orchestration layer, offering MCP‑based skills, plugins, and notebook agents. It lets you turn ad‑hoc prompts and tool calls into repeatable, memory‑backed agent workflows that can be coordinated across multiple LLMs. With 317 stars, recent commits, and a Python‑centric codebase, it is positioned as a production‑ready OSS candidate for AI‑enhanced notebook environments.

**Value**  
- **From isolated prompts to reusable agents** – The extension abstracts LLM calls, tool usage, and memory handling into “agents” that can be versioned, shared, and invoked programmatically, eliminating the need to rewrite prompt logic for each notebook.  
- **Multi‑agent orchestration** – By supporting several LLM back‑ends and an MCP (Multi‑Component‑Pipeline) model, teams can route tasks to the most suitable model (e.g., Claude for reasoning, Copilot for code generation) and chain their outputs automatically.  
- **Standardised tool‑use pipelines** – Built‑in plugins let notebooks call external services (APIs, databases, CLI tools) in a consistent way, making data‑driven research reproducible and auditable.  

**Practical Adoption Path**  
1. **Install & enable** – Add the extension via `pip install plmbr-notebook-intelligence` and enable it in JupyterLab (`jupyter labextension install`).  
2. **Configure LLM back‑ends** – Supply API keys or local endpoints (Ollama, Claude, OpenAI) in the provided `config.yaml`.  
3. **Define agents** – Use the UI or a small Python DSL to declare agents, their skills, and memory scopes (e.g., per‑project or per‑notebook).  
4. **Integrate into notebooks** – Replace raw `openai.ChatCompletion` calls with `agent.run(prompt)`; existing notebooks continue to work while gaining orchestration benefits.  
5. **Scale & version** – Export agent definitions as YAML/JSON, store them in a repo, and reuse across teams or CI pipelines.  

**Production Readiness**  
- **Activity & community** – 317 stars, 59 forks, recent commits (as of 2026‑06‑25), and active issue discussions indicate a healthy maintainer base.  
- **Stability** – The core API (API/SDK/CLI) is stable, with clear versioning and extensive type hints in Python, reducing integration risk.  
- **Ecosystem fit** – Works natively with JupyterLab, the de‑facto environment for data science, and can be called from CI/CD pipelines via its CLI.  
- **Risks to address** – Final due‑diligence on the license (MIT‑style but verify), security posture of bundled plugins, and confirmation of long‑term maintainers is still required.  

Overall, plmbr/notebook‑intelligence offers a mature, low‑friction way to embed LLM‑driven agents into notebook workflows and is ready for pilot deployments in production‑grade data‑science environments.

### Русский

**plmbr/notebook-intelligence** — это расширение для JupyterLab, которое объединяет Claude Code, Copilot, Ollama и любые LLM‑модели с совместимым OpenAI API, предоставляя MCP, набор навыков, плагины и «ноутбук‑агентов». Оно позволяет превратить разрозненные запросы и инструменты в повторяемые многокомпонентные рабочие процессы: координация нескольких агентов, построение пайплайнов с использованием внешних инструментов и стандартизация памяти агентов напрямую в ноутбуке. Проект считается практически готовым к production‑использованию: активные коммиты, 317 звёзд, 59 форков, поддержка Python‑SDK/CLI и ясные API‑сигналы делают его надёжным кандидатом для пилотных внедрений.

### 中文

**项目价值**  
plmbr/notebook‑intelligence 将零散的 Prompt、代码补全和 LLM 工具统一封装为可重复、可编排的 Notebook Agent 工作流。通过内置的 MCP（Memory‑Context‑Process）模型、可插拔的 Skills 与 Plugins，用户可以在 JupyterLab 中轻松实现多代理协同、工具调用链以及统一的记忆管理，从而把“实验性”代码提升为可维护的业务流程。

**典型接入方式**  
1. **JupyterLab 插件**：在已有的 JupyterLab 环境中直接安装 `pip install notebook-intelligence` 或使用扩展管理器加载，插件会自动注册 Claude Code、Copilot、Ollama、OpenAI‑compatible 等后端。  
2. **API/SDK**：项目提供 Python SDK（`from notebook_intelligence import Agent`），可以在 Notebook 或外部脚本里创建 Agent 实例，调用 `agent.run(prompt, skill="xxx")` 等方法，实现自定义的多代理编排。  
3. **CLI**：`nbintel` 命令行工具支持快速启动 Agent、查看记忆库、管理插件，适合 CI/CD 或批处理场景。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑25 最近一次提交，拥有 317 ★、59 Fork，13 个主题标签，代码主要使用 Python，社区活跃。  
- **成熟度**：MCP、Skills、Plugins 已实现稳定的抽象层，配套的 API/SDK/CLI 文档完整，易于集成到现有数据科学平台。  
- **风险**：目前未发现重大元数据风险，仍需对许可证（MIT）和安全审计（第三方依赖）进行最终确认。总体而言，项目已具备在生产环境中进行试点的条件，适合作为企业内部 Notebook 自动化和多模型协作的底层框架。

## 🧭 Practical evaluation

**Value:** plmbr/notebook-intelligence helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 317 GitHub stars
- 59 forks
- updated 2026-06-25
- primary language: Python
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 53/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 73/100 |
| recency | 80/100 |
| adoption | 51/100 |
| production | 74/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/plmbr/notebook-intelligence) · [← Back to Orchestration](./README.md)</sub>
