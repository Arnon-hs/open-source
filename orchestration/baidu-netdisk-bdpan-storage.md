# baidu-netdisk/bdpan-storage

[![Stars](https://img.shields.io/github/stars/baidu-netdisk/bdpan-storage?style=flat-square&color=yellow)](https://github.com/baidu-netdisk/bdpan-storage/stargazers) [![Forks](https://img.shields.io/github/forks/baidu-netdisk/bdpan-storage?style=flat-square&color=blue)](https://github.com/baidu-netdisk/bdpan-storage/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-77%2F100-brightgreen?style=flat-square)](#)

> Agent Skill for Baidu Netdisk (百度网盘) — upload, download, transfer,    share, search files via natural language. Works with Claude Code,   Cursor, Codex, Gemini CLI, OpenClaw.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 152 |
| 🍴 **Forks** | 11 |
| 💻 **Language** | Shell |
| 📈 **Score** | 77/100 |
| 🗓️ **Last push** | 2026-07-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-skills` `agentic-ai` `ai-agents` `baidu` `baidu-netdisk` `claude-code` `claude-code-plugin` `claude-code-skills` `clawhub` `cloud-storage` `codex-skills` `developer-tools`

## 🎯 Categories

Orchestration · Knowledge/RAG · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
baidu-netdisk/bdpan‑storage is an open‑source agent‑skill that lets LLMs interact with Baidu Netdisk through natural‑language commands—uploading, downloading, transferring, sharing and searching files. It exposes a simple Shell‑based CLI/SDK that can be wired into Claude Code, Cursor, Codex, Gemini CLI, OpenClaw and other AI‑assistant frameworks, turning ad‑hoc prompts into repeatable, orchestrated workflows.

**Value**  
- **Unified tool‑use**: Provides a single, language‑agnostic interface for all Baidu Netdisk operations, eliminating the need to write custom API wrappers for each LLM.  
- **Workflow repeatability**: By encapsulating file‑management actions as agent “skills,” developers can compose multi‑step, memory‑aware pipelines (e.g., fetch a file, process it with another model, then share the result).  
- **Ecosystem compatibility**: Designed to plug into popular AI‑assistant platforms, it accelerates the creation of end‑to‑end solutions that combine retrieval‑augmented generation, code execution, and cloud storage.

**Practical Adoption Path**  
1. **Clone & install** – Pull the repository and install the Shell CLI (`./install.sh`), which sets up the required Baidu Netdisk token handling.  
2. **Configure credentials** – Store the access token in a secure secret manager (e.g., Vault, GitHub Secrets) and point the CLI via environment variables.  
3. **Integrate with an LLM framework** – Register the skill in Claude Code, Cursor, or Gemini by referencing the provided OpenAPI‑like spec or by invoking the CLI from a custom tool definition.  
4. **Compose pipelines** – Use the skill in orchestration tools (e.g., LangChain, CrewAI) to chain file‑management steps with other agents (search, summarization, code generation).  
5. **Test & monitor** – Run the built‑in test suite, enable logging, and set up alerts for quota or permission errors.

**Production Readiness**  
- **Activity & community**: 152 stars, recent commits (as of 2026‑07‑13), and active issue responses indicate a healthy maintainer presence.  
- **Stability**: The core functionality is encapsulated in a thin Shell wrapper around Baidu’s official SDK, reducing surface‑area for bugs.  
- **Security**: No known metadata leaks; however, a final review of the license (MIT‑compatible) and token handling practices is advisable before a wide rollout.  
- **Scalability**: Works with standard CLI invocations, so it can be containerized or run as a sidecar service to handle high‑throughput workloads.  

Overall, bdpan‑storage is mature enough for a pilot in production environments, especially where Baidu Netdisk is a required storage backend and the goal is to embed file operations into LLM‑driven automation.

### Русский

**baidu-netdisk/bdpan-storage** — это open‑source‑агент, позволяющий управлять файлами в Baidu Netdisk (загрузка, скачивание, передача, шаринг, поиск) через естественный язык и интегрировать его в цепочки инструментов (Claude, Cursor, Codex, Gemini CLI, OpenClaw). Типичный сценарий: построение повторяемых многоканальных воркфлоу, где агент автоматически координирует действия нескольких ИИ‑моделей и сохраняет контекст/память между запросами. Проект находится на высоком уровне готовности к production: активные коммиты, 152 звёзд, поддержка Shell‑CLI, широкие сигналы экосистемы и отсутствие серьёзных метаданных‑рисков, что делает его надёжным кандидатом для пилотных внедрений.

### 中文

**项目简介**

baidu-netdisk/bdpan-storage 是一个开源项目，旨在为百度网盘提供Agent技能，支持文件上传、下载、转移、共享、搜索等功能。它可以与 Claude Code、Cursor、Codex、Gemini CLI、OpenClaw 等工具集成，帮助用户创建可重复的Agent工作流程。

**价值**

baidu-netdisk/bdpan-storage 的价值在于它可以帮助用户将孤立的提示和工具连接起来，形成可重复的Agent工作流程。它可以协调多Agent工作流程、添加工具使用管道、标准化Agent内存。

**典型接入方式**

baidu-netdisk/bdpan-storage 支持多种接入方式，包括：

* 使用API/SDK/CLI等接口
* 使用语言元数据
* 使用专注的主题

**生产可用性**

项目的生产可用性较高，理由包括：

* 近期活动：最近更新于2026-07-13
* 采用：152 GitHub星标，11个分支
* 生态系统信号：强大的生态系统信号
* 高度评估

## 🧭 Practical evaluation

**Value:** baidu-netdisk/bdpan-storage helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 152 GitHub stars
- 11 forks
- updated 2026-07-13
- primary language: Shell
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 27/100 |
| stars | 46/100 |
| topics | 100/100 |
| outlook | 85/100 |
| quality | 73/100 |
| recency | 100/100 |
| adoption | 41/100 |
| production | 76/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/baidu-netdisk/bdpan-storage) · [← Back to Orchestration](./README.md)</sub>
