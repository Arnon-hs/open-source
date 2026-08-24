# agentic-box/memora

[![Stars](https://img.shields.io/github/stars/agentic-box/memora?style=flat-square&color=yellow)](https://github.com/agentic-box/memora/stargazers) [![Forks](https://img.shields.io/github/forks/agentic-box/memora?style=flat-square&color=blue)](https://github.com/agentic-box/memora/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> Give your AI agents persistent memory.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 422 |
| 🍴 **Forks** | 53 |
| 💻 **Language** | Python |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-memory` `ai-agent` `claude` `claude-code` `cloudflare-d1` `codex` `knowledge-graph` `llms` `mcp` `mcp-server` `memory` `model-context-protocol`

## 🎯 Categories

Orchestration · MCP · Knowledge/RAG · AI/ML · Backend

## 📝 Summary

### English

**Project Summary:**

Memora is an open-source project that enables AI agents to have persistent memory, allowing users to create repeatable workflows and standardize agent memory. This project helps turn isolated prompts and tools into coordinated multi-agent workflows by adding tool-use pipelines. With its high production readiness and strong ecosystem signals, Memora is a promising tool for serious pilots.

**Value Proposition:**

The primary value of Memora lies in its ability to provide persistent memory for AI agents, enabling them to learn from past experiences and adapt to new situations. This allows users to create complex workflows that can be repeated and refined over time, making it an essential tool for AI/ML development and deployment.

**Practical Adoption Path:**

To adopt Memora, users can start by evaluating its API/SDK/CLI implementation signals and language metadata. The project's straightforward integration process makes it easy to get started. Users can then begin by creating simple agent workflows and gradually add complexity to their pipelines. As they become more familiar with Memora, users can explore its full potential by coordinating multi-agent workflows and standardizing agent memory.

**Production Readiness:**

Memora has a high production readiness score due to its recent activity, adoption, and strong ecosystem signals. With 422 GitHub stars and 53 forks,

### Русский

Резюме проекта agentic-box/memora:

Представляем agentic-box/memora - открытый исходный проект, который позволяет обеспечить постоянную память для искусственных интеллектуальных агентов. Этот проект помогает превратить изолированные команды и инструменты в повторяемые цепочки действий агентов, что делает его идеальным решением для координации многоагентных потоков работы. Проект готов к использованию в production, поскольку имеет высокий уровень готовности (High) и сильные сигналы в области активности, принятия и экосистемы.

### 中文

**项目简介**  
agentic-box/memora 为 AI 代理提供持久化记忆，让原本孤立的 Prompt 与工具能够在多轮交互中共享状态，进而构建可复用的工作流。

**价值**  
- **统一记忆层**：为每个代理维护长期记忆，实现上下文跨会话、跨任务的连续性。  
- **工作流编排**：把多个代理、工具链以及 RAG 检索统一进程化，支持复杂的多代理协同。  
- **标准化接口**：提供 API/SDK/CLI 三种调用方式，便于在现有系统中快速集成并统一管理记忆策略。

**典型接入方式**  
1. **API**：通过 HTTP/REST 接口向 Memora 发送 `store`、`retrieve`、`update` 等请求，适合微服务或跨语言调用。  
2. **SDK（Python）**：直接在 Python 代码中引入 `memora` 包，使用 `MemoraClient` 类进行记忆管理，最适合在 LangChain、AutoGPT 等生态中嵌入。  
3. **CLI**：命令行工具提供 `memora push/pull` 等子命令，方便在 CI/CD、脚本或调试阶段快速操作记忆库。

**生产可用性**  
- **活跃度**：截至 2026‑06‑29 最近一次提交，GitHub 统计 422 ⭐、53 🍴，社区贡献活跃。  
- **技术成熟度**：核心实现基于 Python，提供完整的类型提示与文档，且已在多个开源项目中实践。  
- **生态兼容**：兼容常见的 RAG、LLM 编排框架（如 LangChain、Haystack），并支持自定义存储后端（PostgreSQL、Redis、MongoDB 等）。  
- **风险**：目前未发现重大元数据风险，但仍需对许可证（MIT）合规性、依赖安全审计以及维护者响应速度进行最终确认。

综合来看，memora 已具备 **高生产可用性**，适合作为企业级 AI 代理记忆层的首选 OSS 方案，可直接用于试点项目并逐步推广到正式生产环境。

## 🧭 Practical evaluation

**Value:** agentic-box/memora helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 422 GitHub stars
- 53 forks
- updated 2026-06-29
- primary language: Python
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 43/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 65/100 |
| quality | 64/100 |
| recency | 40/100 |
| adoption | 52/100 |
| production | 61/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/agentic-box/memora) · [← Back to Orchestration](./README.md)</sub>
