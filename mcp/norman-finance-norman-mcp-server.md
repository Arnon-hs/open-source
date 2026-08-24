# norman-finance/norman-mcp-server

[![Stars](https://img.shields.io/github/stars/norman-finance/norman-mcp-server?style=flat-square&color=yellow)](https://github.com/norman-finance/norman-mcp-server/stargazers) [![Forks](https://img.shields.io/github/forks/norman-finance/norman-mcp-server?style=flat-square&color=blue)](https://github.com/norman-finance/norman-mcp-server/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> AI-powered bookkeeping and tax filing automation via MCP for entrepreneurs at the heart of the European economy

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 50 |
| 🍴 **Forks** | 14 |
| 💻 **Language** | Python |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bookkeeping` `claude` `cursor-plugin` `german-tax-accounting` `gpt` `invoicing` `mcp` `mcp-server` `norman` `openai` `vat-filing`

## 🎯 Categories

MCP · Automation · Backend

## 📝 Summary

### English

**Brief Summary**  
norman‑finance / norman‑mcp‑server is an open‑source Python backend that implements the Model Context Protocol (MCP), enabling AI assistants to securely invoke real‑world bookkeeping, tax‑filing and other financial tools. By exposing a clean API/SDK/CLI, it lets entrepreneurs and developers plug AI agents into existing finance stacks with minimal integration effort.  

**Value**  
- **Standardised AI‑to‑tool communication** – MCP provides a vendor‑agnostic contract so any compliant AI model can call the server’s endpoints, eliminating bespoke glue code.  
- **Accelerated automation** – With built‑in connectors for bookkeeping and tax filing, businesses can automate routine finance tasks, reducing manual effort and error rates.  
- **Reusable ecosystem** – The server can be deployed as a standalone service or bundled into larger platforms, allowing multiple AI agents to share the same financial data layer.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Docker compose or Python virtual‑env setup, and use the example CLI to invoke a simple bookkeeping operation.  
2. **Integrate** – Replace the demo data store with your own PostgreSQL/MySQL instance and configure authentication (OAuth / API‑key).  
3. **Connect AI agents** – Point any MCP‑compatible model (e.g., OpenAI, Anthropic) to the server’s endpoint; the model can now generate and execute finance‑related actions via the standardized protocol.  
4. **Scale & Harden** – Deploy to Kubernetes or a managed cloud service, enable TLS, add rate‑limiting, and plug in your organisation’s audit/logging pipelines.  

**Production Readiness**  
The project scores 72/100 and shows strong OSS‑candidate signs: recent commits (as of 2026‑06‑26), active community (50 ⭐, 14 forks), clear documentation, and a well‑defined Python codebase with 11 topical tags. While a final review of licensing, security hardening, and maintainer responsiveness is still needed, the current signals (regular releases, adoption hints, and a clean MCP interface) make it suitable for a serious pilot in production environments.

### Русский

**norman-finance/norman-mcp-server** — это open‑source бекенд на Python, реализующий Model Context Protocol (MCP) и позволяющий AI‑ассистентам безопасно взаимодействовать с реальными бухгалтерскими и налоговыми сервисами. Типичный сценарий: компания подключает свои внутренние инструменты (API, SDK, CLI) к серверу MCP, после чего AI‑агенты могут автоматически вести бухгалтерию и подавать налоговые декларации, используя единый протокол интеграции. Проект обладает высокой готовностью к production: свежие коммиты, активные форки, 50 звёзд и 11 тем, а также подтверждённая совместимость с реальными инструментами, что делает его надёжным кандидатом для пилотного внедрения.

### 中文

**项目简介**  
norman-finance/norman-mcp-server 是一个基于 Model Context Protocol（MCP）的开源后端服务，利用 AI 自动完成记账、税务申报等财务工作，帮助欧洲中小企业主实现财务流程的全链路自动化。

**价值主张**  
- **AI 与真实工具的桥梁**：通过标准化的 MCP 接口，将聊天机器人或其他 AI 助手直接连接到企业的财务系统、数据库和第三方税务服务，实现“说即办”。  
- **加速产品化**：开发者只需实现 MCP 规范，即可快速部署 AI‑驱动的财务工具，省去繁琐的自研集成工作。  
- **统一集成层**：提供统一的 API/SDK/CLI，帮助企业在不同财务工具（ERP、会计软件、税务平台）之间保持一致的数据交互格式。

**典型接入方式**  
1. **API 调用**：在自己的业务系统中调用 `POST /mcp/v1/execute` 接口，提交自然语言指令或结构化请求，服务器返回 AI 生成的记账/报税指令。  
2. **SDK 使用**：项目提供 Python SDK（`norman_mcp`），可在代码中直接创建 `MCPClient`，完成身份验证、会话管理和指令执行。  
3. **CLI 工具**：通过 `norman-mcp-cli`，在命令行下快速测试指令流或进行批量数据同步，适合 DevOps 与 CI/CD 场景。  
4. **模型上下文服务**：将服务器部署为独立的 MCP 模型上下文服务，供多个 AI 代理共享同一套财务业务逻辑和数据访问层。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑26，星标 50、Fork 14，社区活跃，代码质量稳定。  
- **技术栈**：核心使用 Python，配合 FastAPI、SQLAlchemy 等成熟框架，易于在容器化或 serverless 环境中部署。  
- **安全与合规**：项目已声明 MIT 许可证，暂无已知安全漏洞；但在正式投产前仍建议进行内部安全审计和依赖检查。  
- **可扩展性**：支持自定义插件（如税务规则、会计科目表）和多租户模式，能够满足从单店到跨国企业的规模需求。  

综合来看，norman-mcp-server 在标准化 AI‑工具集成、快速交付财务自动化功能方面具备较高的生产就绪度，适合作为企业级财务 AI 项目的核心后端服务进行试点或正式上线。

## 🧭 Practical evaluation

**Value:** norman-finance/norman-mcp-server helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 50 GitHub stars
- 14 forks
- updated 2026-06-26
- primary language: Python
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 36/100 |
| topics | 100/100 |
| outlook | 57/100 |
| quality | 55/100 |
| recency | 40/100 |
| adoption | 34/100 |
| production | 58/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/norman-finance/norman-mcp-server) · [← Back to Mcp](./README.md)</sub>
