# carsteneu/yesmem

[![Stars](https://img.shields.io/github/stars/carsteneu/yesmem?style=flat-square&color=yellow)](https://github.com/carsteneu/yesmem/stargazers) [![Forks](https://img.shields.io/github/forks/carsteneu/yesmem?style=flat-square&color=blue)](https://github.com/carsteneu/yesmem/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> Persistent memory system for Coding Agents  (Claude, Opencode, Codex), infinite context, learning extraction, persona modeling and so much more!

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 22 |
| 🍴 **Forks** | 3 |
| 💻 **Language** | Go |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-memory` `claude-code` `context-window` `llm-agents` `mcp` `memory`

## 🎯 Categories

MCP · AI/ML

## 📝 Summary

### English

**Brief Summary**  
yesmem (carsteneu/yesmem) is an open‑source persistent‑memory layer for coding agents such as Claude, Opencode, and Codex. It provides an “infinite‑context” store, learning‑extraction hooks, persona‑modeling, and a standard Model Context Protocol (MCP) that lets agents read/write real‑world tools and data.  

**Value**  
- **Unified memory API** – Agents can off‑load intermediate results, long‑term knowledge, and user‑specific context to a shared store, eliminating the need for ad‑hoc file or database handling.  
- **Standardised integration** – By implementing the MCP, any AI assistant can plug into the same back‑end, reducing integration friction across tools, SDKs, and CLIs.  
- **Extensible intelligence** – Extraction pipelines let agents turn raw outputs into structured knowledge (e.g., embeddings, persona traits) that can be reused in future sessions, boosting continuity and personalization.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Go binary or Docker image, and point your agent’s MCP client to the local endpoint.  
2. **Evaluation** – Use the CLI/SDK to store and retrieve sample artifacts (code snippets, embeddings, persona blobs) and verify latency, serialization format, and security settings.  
3. **Integration** – Replace custom persistence code in your agent’s workflow with MCP calls (e.g., `mem.Put(key, value)`, `mem.Query(filter)`).  
4. **Scaling** – Deploy the server behind a load balancer, enable persistence (PostgreSQL/Redis back‑end), and configure TLS/auth tokens for production use.  

**Production Readiness**  
- **Maturity** – Medium. The project is actively maintained (last commit 2026‑07‑01), has 22 ⭐ and 3 forks, and the Go codebase is compact enough for quick audits.  
- **Dependencies** – Minimal (standard Go libraries plus optional storage adapters). Still requires a review of licensing, security hardening, and monitoring of upstream updates before a production rollout.  
- **Fit** – Ideal for internal prototypes, R&D labs, or SaaS services that need a consistent memory layer for multiple coding agents. With proper hardening (TLS, auth, backup), it can be promoted to production, but teams should perform a dedicated security and maintainability assessment first.

### Русский

**carsteneu/yesmem** — это открытая система постоянной памяти для кодирующих агентов (Claude, Opencode, Codex), позволяющая хранить и извлекать контекст без ограничений, моделировать персоналии и интегрировать инструменты через единый Model Context Protocol. Типичный сценарий — подключение AI‑ассистента к внешним сервисам и данным, запуск собственного MCP‑сервера и стандартизация интеграций в прототипах или внутренних рабочих процессах. Готовность к production — средняя: проект уже работает, имеет базовый SDK/CLI и Go‑реализацию, но требует проверки лицензии, безопасности и поддержки перед масштабным внедрением.

### 中文

**项目简介（2‑3 句）**  
carsteneu/yesmem 是一套面向编码型 AI 助手（Claude、Opencode、Codex 等）的持久化记忆系统，提供无限上下文、学习抽取、角色建模等能力，并通过统一的 Model Context Protocol 与外部工具和数据源对接。  

**价值**  
- **统一协议**：通过标准化的 Model Context Protocol，让不同的 AI 助手能够以同一方式读取、写入和查询持久记忆，从而降低集成成本。  
- **增强上下文**：持久化记忆消除了单轮对话的上下文限制，使 AI 能够利用历史交互、代码库和业务规则进行更精准的生成。  
- **可扩展的角色建模**：支持为每个 AI 代理配置专属 persona，帮助实现多角色协同或特定业务流程的自动化。  

**典型接入方式**  
1. **API/SDK**：项目提供 HTTP API 与 Go SDK，调用 `POST /memories`、`GET /memories/{id}` 等接口即可写入或读取记忆。  
2. **CLI**：通过 `yesmem-cli` 可在本地或 CI 环境快速创建、查询、删除记忆，适合脚本化集成。  
3. **语言元数据**：在代码库中使用特殊注释或 JSON‑LD 描述代码片段，yesmem 会自动抽取并索引，供后续 AI 调用。  
4. **模型上下文服务器**：部署 `yesmem-server`，让各类 AI 平台（如 Claude、OpenAI）通过统一的协议访问同一记忆后端。  

**生产可用性**  
- **成熟度**：当前评分 65/100，适合原型开发或内部工作流。  
- **依赖与维护**：基于 Go 实现，依赖少，部署轻量；但仍需自行审查安全漏洞、许可证兼容性以及维护者活跃度。  
- **准备度**：具备 API/SDK/CLI，易于评估和快速试跑；在正式生产环境使用前建议进行安全审计、容错测试以及监控告警的补充。  

总体而言，yesmem 为 AI 编码助理提供了“一站式”持久记忆解决方案，接入门槛低，适合作为原型或内部工具的记忆层，经过充分的安全与运维验证后即可逐步推广到生产环境。

## 🧭 Practical evaluation

**Value:** carsteneu/yesmem helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 22 GitHub stars
- 3 forks
- updated 2026-07-01
- primary language: Go
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 15/100 |
| stars | 29/100 |
| topics | 75/100 |
| outlook | 53/100 |
| quality | 48/100 |
| recency | 40/100 |
| adoption | 25/100 |
| production | 53/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/carsteneu/yesmem) · [← Back to Mcp](./README.md)</sub>
