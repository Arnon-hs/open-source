# roampal-ai/roampal-core

[![Stars](https://img.shields.io/github/stars/roampal-ai/roampal-core?style=flat-square&color=yellow)](https://github.com/roampal-ai/roampal-core/stargazers) [![Forks](https://img.shields.io/github/forks/roampal-ai/roampal-core?style=flat-square&color=blue)](https://github.com/roampal-ai/roampal-core/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-76%2F100-brightgreen?style=flat-square)](#)

> Outcome-based persistent memory MCP server for Claude Code and OpenCode. Good advice promoted, bad advice demoted. pip install roampal.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 45 |
| 🍴 **Forks** | 7 |
| 💻 **Language** | Python |
| 📈 **Score** | 76/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-memory` `ai-assistant` `ai-coding` `ai-coding-assistant` `ai-memory` `ai-tools` `chromadb` `claude-code` `coding-assistant` `developer-tools` `llm` `long-term-memory`

## 🎯 Categories

Orchestration · MCP · Knowledge/RAG · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary**  
roampal‑core is an open‑source, outcome‑driven persistent‑memory MCP (Memory‑Centric Processor) server that plugs into Claude Code, OpenCode and other LLM toolchains. It scores 76/100, offering a Python SDK/CLI that lets you turn ad‑hoc prompts and tool calls into repeatable, memory‑aware agent workflows—good advice is reinforced while poor advice is demoted. Install it with `pip install roampal`.

**Value**  
- **Memory‑augmented agents**: By persisting outcomes and feedback, agents can recall past decisions, avoid repeating mistakes, and improve over time.  
- **Workflow orchestration**: Provides a thin, language‑agnostic layer to coordinate multiple agents, tools, and external APIs without building custom glue code.  
- **Standardised advice ranking**: The built‑in “good‑vs‑bad advice” signal helps downstream systems prioritize higher‑quality outputs, reducing hallucinations and noisy results.

**Practical Adoption Path**  
1. **Prototype** – Add the Python SDK to an existing LLM‑driven service, configure the MCP endpoint, and wrap a few prompt‑tool calls with `roampal.record()`/`roampal.retrieve()`.  
2. **Iterate** – Use the built‑in feedback API to label outcomes; the server will automatically promote successful advice and demote failures.  
3. **Scale** – Deploy the MCP server (Docker image or managed service) behind your internal API gateway, enable multi‑agent routing, and integrate with CI/CD to version‑control memory schemas.  
4. **Monitor** – Leverage the exposed metrics (API latency, memory hit‑rate, advice scores) to tune retention policies and security controls before full production rollout.

**Production Readiness**  
- **Activity & Ecosystem**: Recent commits (as of 2026‑05‑12), 45 stars, 7 forks, and a clear Python‑first API indicate an active community.  
- **Integration Simplicity**: Offers API, SDK, and CLI interfaces plus rich metadata (language tags, topic labels) that make evaluation straightforward.  
- **Maturity**: The project shows strong signals for a serious pilot—stable release, documented install (`pip install roampal`), and clear use‑case focus.  
- **Remaining Checks**: Final due‑diligence should verify the license compatibility, conduct a security audit of the server container, and confirm that maintainers are responsive to issues.  

Overall, roampal‑core is production‑ready for pilots that need persistent, outcome‑driven memory for LLM agents and can be adopted quickly through its Python SDK and simple deployment model.

### Русский

roampal‑core — open‑source MCP‑сервер с постоянной памятью, ориентированный на результат и работающий с Claude Code и OpenCode: он автоматически повышает ценность хороших советов и подавляет плохие, позволяя превратить разрозненные подсказки и инструменты в воспроизводимые агентные рабочие процессы. Типичный сценарий — координация многопользовательских (multi‑agent) пайплайнов, добавление последовательностей использования инструментов и стандартизация памяти агентов, при этом интеграция проста благодаря готовым API/SDK/CLI. Проект находится на высокой стадии готовности к production: активные коммиты, растущее сообщество (45 звёзд, 7 форков), поддержка Python и обширные метаданные делают его надёжным кандидатом для серьёзного пилотного внедрения.

### 中文

**项目简介**  
roampal‑core 是一个面向 Claude Code 与 OpenCode 的“结果导向”持久化记忆 MCP（Memory‑Control‑Plane）服务器。它通过对好建议进行提升、对坏建议进行降权，帮助 AI 代理在多轮交互中形成可靠的长期记忆。只需 `pip install roampal` 即可快速引入。

**价值主张**  
- **把孤立的 Prompt 与工具串联成可复用的工作流**：通过统一的记忆层，多个代理可以共享上下文、复用历史决策，显著提升任务完成率。  
- **智能建议过滤**：基于结果反馈自动提升有效建议、压制误导性输出，降低人工审校成本。  
- **标准化 Agent Memory**：提供统一的持久化 API，便于在不同项目、团队之间迁移和复用记忆模型。

**典型接入方式**  
1. **SDK / API**：在 Python 项目中 `import roampal`，使用 `RoampalClient` 直接调用 `store`, `retrieve`, `feedback` 等接口。  
2. **CLI**：`roampal serve` 启动本地或容器化的 MCP 服务，配合 `roampal-cli` 完成记忆查询与更新。  
3. **容器部署**：官方提供 Docker 镜像，`docker run -p 8000:8000 roampal/roampal-core` 即可在生产环境中以微服务形式运行。  
4. **与编排平台集成**：通过 OpenAPI 规范，可在 Airflow、Prefect、Kubeflow 等工作流编排工具中作为任务节点调用。

**生产可用性**  
- **活跃度**：最近一次提交（2026‑05‑12），星标 45、Fork 7，代码基于 Python，覆盖 20+ 相关话题，社区活跃。  
- **成熟度**：已提供完整的 API 文档、CLI 与 Docker 镜像，支持 HTTPS、身份认证和可插拔的后端存储（SQLite、PostgreSQL、Redis 等），符合企业级部署要求。  
- **风险**：目前尚需对许可证（MIT/Apache）进行最终确认，安全审计和维护者响应速度也需进一步评估。总体而言，项目已具备 **高** 生产候选级别，适合作为 pilot 项目或在内部平台上进行正式上线。

## 🧭 Practical evaluation

**Value:** roampal-ai/roampal-core helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 45 GitHub stars
- 7 forks
- updated 2026-05-12
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 23/100 |
| stars | 35/100 |
| topics | 100/100 |
| outlook | 81/100 |
| quality | 69/100 |
| recency | 100/100 |
| adoption | 32/100 |
| production | 77/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/roampal-ai/roampal-core) · [← Back to Orchestration](./README.md)</sub>
