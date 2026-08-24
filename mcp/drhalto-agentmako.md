# drhalto/agentmako

[![Stars](https://img.shields.io/github/stars/drhalto/agentmako?style=flat-square&color=yellow)](https://github.com/drhalto/agentmako/stargazers) [![Forks](https://img.shields.io/github/forks/drhalto/agentmako?style=flat-square&color=blue)](https://github.com/drhalto/agentmako/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Local-first MCP server that gives coding agents structured context packets, code/schema facts, and diagnostics - backed by a local SQLite store.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 43 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-coding` `claude-code` `claude-code-plugin` `code-intelligence` `codex` `cursor` `developer-tools` `llm-tools` `local-first` `mcp` `mcp-server` `model-context-protocol`

## 🎯 Categories

MCP · AI/ML · Backend · DevTools · Database

## 📝 Summary

### English

**Brief Summary**  
AgentMako (drhalto/agentmako) is a local‑first MCP (Message‑Centric Protocol) server that supplies coding agents with structured context packets, code‑ and schema‑facts, and diagnostics, persisting everything in a lightweight SQLite store. By turning ad‑hoc prompts and tool calls into repeatable, memory‑aware workflows, it lets developers orchestrate multi‑agent pipelines, add tool‑use stages, and standardize agent state across projects.  

**Value**  
- **Structured context & memory** – Agents receive deterministic packets (facts, schemas, diagnostics) instead of raw prompts, which improves reliability and reduces hallucination.  
- **Repeatable workflows** – The server records interactions in SQLite, enabling replay, debugging, and incremental improvement of agent pipelines.  
- **Local‑first & privacy‑first** – All data stays on‑premises, making it suitable for regulated environments or developers who cannot ship code or data to the cloud.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the TypeScript server locally, and connect an existing LLM‑client via the provided SDK/CLI to send a simple “hello‑world” context packet.  
2. **Integrate** – Replace ad‑hoc prompt construction in your toolchain with AgentMako’s `createPacket` API; map your domain schemas to the server’s fact store.  
3. **Orchestrate** – Define multi‑agent pipelines (e.g., code‑generator → tester → reviewer) using the server’s orchestration endpoints or the CLI, persisting each step’s diagnostics.  
4. **Scale** – Deploy the SQLite‑backed server behind a lightweight reverse proxy for internal CI/CD runners; optionally swap SQLite for a more robust embedded DB if needed.  

**Production Readiness**  
- **Activity & community** – 43 ★, 5 forks, last commit 2026‑06‑27, active issue discussions, and a clear TypeScript codebase indicate healthy maintenance.  
- **Integration friendliness** – Exposes API, SDK, and CLI; language metadata and focused topics make it easy to embed in existing Node/TS stacks.  
- **Risk profile** – No glaring licensing or security red flags, but a final audit of the MIT‑style license, dependency vulnerabilities, and maintainer responsiveness is advisable before a full‑scale rollout.  

Overall, AgentMako is a mature OSS candidate that can be piloted quickly in a dev environment and, after a brief security/license review, promoted to production for any workflow that needs deterministic, local‑first agent orchestration.

### Русский

Резюме проекта drhalto/agentmako:

Проект drhalto/agentmako представляет собой локальный сервер MCP, предоставляющий структурированные пакеты контекста, факты кода и диагностические данные – все это хранится в локальной базе данных SQLite. Он помогает превратить изолированные команды и инструменты в повторяемые агентные потоки. 

Проект подходит для сценария координации многозадачных агентных потоков, добавления трубопроводов использования инструментов и стандартизации агентной памяти. 

Проект готов к production на высоком уровне, что подтверждается активностью, принятием и экосистемными сигналами, но требует дальнейшего обзора подозрений по лицензии, безопасности и активных поддерживающих разработчиков.

### 中文

**项目简介**

drhalto/agentmako 是一个本地化的 MCP 服务器，提供了结构化的上下文包、代码/模式事实和诊断信息，使用本地 SQLite 存储。它可以帮助将孤立的提示和工具转换为可重复的代理工作流程。

**价值**

drhalto/agentmako 的价值在于它可以帮助协调多代理工作流程、添加工具使用管道以及标准化代理记忆。

**典型接入方式**

drhalto/agentmako 可以通过 API、SDK 或 CLI 方式接入。它暴露了实现信号，如 API/SDK/CLI、语言元数据或关注的主题。

**生产可用性**

drhalto/agentmako 的生产可用性较高，主要原因是最近的活动、采用和生态系统信号强大。它适合用于严肃的试验或生产环境。

## 🧭 Practical evaluation

**Value:** drhalto/agentmako helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 43 GitHub stars
- 5 forks
- updated 2026-06-27
- primary language: TypeScript
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 35/100 |
| topics | 100/100 |
| outlook | 60/100 |
| quality | 54/100 |
| recency | 40/100 |
| adoption | 31/100 |
| production | 57/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/drhalto/agentmako) · [← Back to Mcp](./README.md)</sub>
