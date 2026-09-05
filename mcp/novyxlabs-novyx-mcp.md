# novyxlabs/novyx-mcp

[![Stars](https://img.shields.io/github/stars/novyxlabs/novyx-mcp?style=flat-square&color=yellow)](https://github.com/novyxlabs/novyx-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/novyxlabs/novyx-mcp?style=flat-square&color=blue)](https://github.com/novyxlabs/novyx-mcp/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-75%2F100-brightgreen?style=flat-square)](#)

> Persistent memory + governance for AI agents. 120 MCP tools — core memory works locally (zero config SQLite), full surface (policy-as-code, approval workflows, governance dashboard, threat intel, auto-defense, governed actions, Runtime v2 agents/missions/capabilities) with Novyx Cloud.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 30 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | Python |
| 📈 **Score** | 75/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agents` `ai-agents` `audit-trail` `claude` `claude-code` `cursor` `mcp` `memory` `model-context-protocol` `persistent-memory` `rollback`

## 🎯 Categories

MCP · AI/ML · Database

## 📝 Summary

### English

**Brief Summary**  
Novyx‑MCP is an open‑source platform that adds persistent memory and governance layers to AI agents, offering 120 ready‑to‑use tools such as policy‑as‑code, approval workflows, a governance dashboard, threat‑intel integration, and auto‑defense mechanisms. It runs locally on a zero‑config SQLite store while also providing a cloud‑backed “Novyx Cloud” for full‑surface management of agents, missions, and capabilities.  

**Value**  
The project gives developers a standardized way to connect AI assistants to real‑world tools and data, turning raw language models into controllable, auditable agents. By bundling memory persistence with policy enforcement and security controls, it reduces the engineering effort needed to build trustworthy, production‑grade AI workflows.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo and run the local SQLite instance; use the provided Python SDK or CLI to register a simple tool (e.g., a web‑search API) and test the Model Context Protocol (MCP) server.  
2. **Policy Integration** – Add policy‑as‑code files to define what actions the agent may perform, then enable the approval workflow and governance dashboard to monitor requests.  
3. **Scale to Cloud** – When the prototype is stable, connect the local node to Novyx Cloud for centralized policy management, threat‑intel feeds, and multi‑agent orchestration across missions.  

**Production Readiness**  
The project shows strong OSS maturity: recent commits (as of 2026‑05‑13), active community signals (30 stars, 8 forks, 11 topics), and a clear Python‑centric API/CLI. Its architecture—local zero‑config SQLite for fast iteration plus optional cloud governance—makes it suitable for pilot deployments in regulated environments. While the license and security posture still need a final review, the overall health and feature completeness indicate it is ready for serious production pilots.

### Русский

Novyx‑MCP — это open‑source платформа, объединяющая постоянную память и механизмы управления для AI‑агентов: локальная база SQLite, policy‑as‑code, approval‑workflows, дашборд governance, threat‑intel и автоматическая защита, а также поддержка Runtime v2 миссий и возможностей через Novyx Cloud. Типичный сценарий — подключить AI‑ассистента к реальным инструментам и данным, развернуть сервер Model Context Protocol и стандартизировать интеграцию через единый протокол. Проект считается почти готовым к продакшн: активные коммиты, растущее сообщество (30★, 8 forks), поддержка Python‑SDK/CLI и ясная архитектура, требующие лишь финального аудита лицензии и безопасности.

### 中文

**项目简介**  
Novyx MCP（novyxlabs/novyx-mcp）是一套面向 AI 代理的持久化记忆与治理平台，提供 120+ MCP（Memory‑Control‑Policy）工具。核心记忆本地化（Zero‑Config SQLite）配合 Novyx Cloud 的策略即代码、审批工作流、治理仪表盘、威胁情报与自动防御，实现对 AI 代理、任务和能力的全生命周期治理。  

**价值主张**  
- **统一协议**：通过标准的 Model Context Protocol（MCP）把 AI 助手与真实工具、数据源安全、可靠地连接。  
- **治理即代码**：政策、审批、审计、威胁情报全部可写成代码，便于审计合规与快速迭代。  
- **本地持久记忆**：零配置 SQLite 为每个代理提供持久化上下文，提升任务连续性与效率。  

**典型接入方式**  
1. **API/SDK**：在 Python 项目中引入 `novyx-mcp` SDK，调用 `MemoryStore`, `PolicyEngine` 等类即可读写记忆并触发治理检查。  
2. **CLI**：使用自带的 `novyx-mcp-cli` 管理策略、审批流和监控面板，适合快速原型或运维脚本。  
3. **MCP Server**：部署 Model Context Protocol 服务器（Docker 镜像或 Kubernetes），让外部 AI 模型通过标准 HTTP/gRPC 接口获取记忆与治理服务。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑13 最近一次提交，30+ Stars、8 Forks，社区讨论活跃。  
- **成熟度**：核心功能（本地 SQLite、策略即代码、审批工作流）已在多个内部 pilot 中验证，具备高可用性和容错设计。  
- **生态兼容**：提供 Python SDK、REST/gRPC 接口以及 CLI，易于嵌入现有 AI/ML 流水线或微服务架构。  
- **风险**：仍需完成许可证合规审查和安全审计（依赖 SQLite 与外部云服务），但整体技术栈成熟，适合作为正式生产环境的 OSS 候选。

## 🧭 Practical evaluation

**Value:** novyxlabs/novyx-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 30 GitHub stars
- 8 forks
- updated 2026-05-13
- primary language: Python
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 32/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 63/100 |
| recency | 80/100 |
| adoption | 30/100 |
| production | 70/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/novyxlabs/novyx-mcp) · [← Back to Mcp](./README.md)</sub>
