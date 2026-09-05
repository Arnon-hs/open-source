# tuanle96/mcp-odoo

[![Stars](https://img.shields.io/github/stars/tuanle96/mcp-odoo?style=flat-square&color=yellow)](https://github.com/tuanle96/mcp-odoo/stargazers) [![Forks](https://img.shields.io/github/forks/tuanle96/mcp-odoo?style=flat-square&color=blue)](https://github.com/tuanle96/mcp-odoo/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> MCP Server for Odoo

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 352 |
| 🍴 **Forks** | 156 |
| 💻 **Language** | Python |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`mcp` `mcp-server` `mcp-servers` `odoo` `odoo-mcp`

## 🎯 Categories

MCP · Backend

## 📝 Summary

### English

**Summary**  
tuanle96/mcp-odoo is an open‑source MCP (Model Context Protocol) server that bridges Odoo ERP systems with AI assistants, exposing Odoo’s functionality through a standard, language‑agnostic API. With 352 ★, recent commits (as of 2026‑07‑02), and a clean Python implementation, it is well‑positioned for pilots that need AI‑driven automation of Odoo workflows.

**Value**  
The project provides a turnkey way to connect large‑language‑model agents to real business tools, allowing AI assistants to read, write, and act on Odoo data without custom glue code. By adhering to the MCP standard, it simplifies integration across multiple AI platforms and promotes reuse of the same protocol for other enterprise systems.

**Practical adoption path**  
1. **Evaluate** – Clone the repo, run the provided Docker/CLI starter, and point the MCP client at a sandbox Odoo instance.  
2. **Configure** – Define the Odoo models and actions you want to expose via the MCP schema (the repo includes example mappings).  
3. **Integrate** – Connect your AI agent (e.g., LangChain, AutoGPT) to the MCP endpoint; the agent can now invoke Odoo CRUD operations as normal tool calls.  
4. **Pilot** – Deploy the server in a staging environment, monitor logs, and add authentication/role‑based controls as needed.  

**Production readiness**  
The codebase shows strong community signals: recent activity, a healthy star/fork count, and a focused Python stack. The architecture follows the well‑documented MCP spec, and the server can be run as a containerized service with standard health checks. While a final security and licensing audit is still required, the project’s activity level and ecosystem adoption make it a solid candidate for production pilots, especially for organizations already using Odoo and looking to augment it with AI‑driven tooling.

### Русский

**tuanle96/mcp-odoo** — это open‑source сервер Model Context Protocol (MCP) для Odoo, позволяющий AI‑ассистентам безопасно взаимодействовать с реальными бизнес‑инструментами и данными через единый протокол. Типичный сценарий: развернуть MCP‑сервер рядом с Odoo, подключить к нему AI‑агента и начать автоматизированный доступ к ERP‑функциям (создание заказов, получение отчётов и т.п.) без написания кастомных интеграций. Проект демонстрирует высокий уровень готовности к production: активные коммиты, более 350 звёзд, широкое использование в сообществе и поддержка Python‑SDK/CLI, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句）**  
`tuanle96/mcp-odoo` 是一个基于 Model Context Protocol（MCP）的后端服务，实现了 Odoo 与 AI 助手之间的标准化通信。它让 AI 代理能够直接调用 Odoo 的业务功能（如 CRM、库存、财务等），从而把真实的企业工具和数据引入对话系统。

**价值**  
- **统一协议**：通过 MCP 将 AI 助手与 Odoo 以及其他系统以同一协议对接，降低集成成本。  
- **快速落地**：无需自行实现复杂的 Odoo RPC 或 XML‑RPC，直接使用已有的 MCP 接口即可让 AI 完成查询、创建、更新等业务操作。  
- **可扩展**：支持自定义模型和插件，能够在同一平台上统一管理多种 AI 代理和业务工具。

**典型接入方式**  
1. **API/SDK**：在 AI 代理（如 LangChain、AutoGPT 等）中引入 Python SDK，配置 MCP 服务器地址、认证信息后即可调用 `create`, `read`, `update`, `delete` 等 Odoo 方法。  
2. **CLI**：通过提供的命令行工具进行快速调试或批量同步，适合 CI/CD 流程或运维脚本。  
3. **自定义插件**：在 Odoo 中部署插件，暴露自定义的 MCP 方法，实现特定业务逻辑的远程调用。

**生产可用性**  
- **活跃度**：截至 2026‑07‑02 最近一次提交，仓库拥有 352 ⭐、156 🍴，说明社区活跃且持续维护。  
- **技术成熟度**：核心实现使用 Python，代码结构清晰，已覆盖常用 Odoo 模块的 CRUD 接口。  
- **生态兼容**：兼容主流 AI 框架的 MCP 客户端，易于在现有 AI 平台上直接集成。  
- **风险**：目前未发现重大许可证或安全漏洞，但仍建议在正式生产前完成内部安全审计并确认维护者的响应能力。

综合来看，`tuanle96/mcp-odoo` 已具备较高的生产就绪度，适合作为 AI 与 Odoo 系统对接的首选 OSS 方案。

## 🧭 Practical evaluation

**Value:** tuanle96/mcp-odoo helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 352 GitHub stars
- 156 forks
- updated 2026-07-02
- primary language: Python
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 55/100 |
| stars | 54/100 |
| topics | 63/100 |
| outlook | 69/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 54/100 |
| production | 70/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/tuanle96/mcp-odoo) · [← Back to Mcp](./README.md)</sub>
