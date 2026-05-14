# keboola/mcp-server

[![Stars](https://img.shields.io/github/stars/keboola/mcp-server?style=flat-square&color=yellow)](https://github.com/keboola/mcp-server/stargazers) [![Forks](https://img.shields.io/github/forks/keboola/mcp-server?style=flat-square&color=blue)](https://github.com/keboola/mcp-server/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Model Context Protocol (MCP) Server for the Keboola Platform

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 84 |
| 🍴 **Forks** | 25 |
| 💻 **Language** | Python |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

`data-platform` `etl-pipeline` `keboola-platform` `mcp` `mcp-server` `model-context-protocol`

## 🎯 Categories

MCP · Backend · Data · Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
keboola/mcp-server is a Python‑based implementation of the Model Context Protocol (MCP) that lets AI assistants interact with real‑world tools and data on the Keboola Platform through a standardized API/SDK/CLI interface. It provides a ready‑to‑run MCP server that can be deployed as a microservice, enabling developers to ship custom MCP endpoints and unify integrations across disparate data sources. With 84 GitHub stars and recent activity (last update 2026‑05‑14), it is a solid starting point for prototyping AI‑driven workflows.

**Value**  
- **Standardised AI‑to‑tool communication** – By exposing a common protocol, the server removes the need to write bespoke adapters for each tool, accelerating the integration of LLM agents with databases, ETL pipelines, and other Keboola services.  
- **Re‑usability and composability** – Once an MCP server is running, any compliant AI assistant can discover and invoke its capabilities, making it easy to build reusable AI‑powered micro‑services across teams.  
- **Open‑source flexibility** – The Python codebase can be extended or hardened to match internal security and compliance requirements while benefiting from community contributions.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Docker compose or local Python server, and point your LLM client to the `/api` endpoint to test basic tool calls.  
2. **Customize** – Implement the required MCP handlers (e.g., data query, model execution) that map to your internal Keboola jobs or external APIs; adjust the OpenAPI spec if needed.  
3. **Integrate** – Register the server’s endpoint in your AI orchestration layer (e.g., LangChain, AutoGPT) and expose the necessary authentication tokens or API keys.  
4. **Deploy** – Containerise the service and push it to your production Kubernetes or serverless environment, adding monitoring, rate‑limiting, and TLS termination.  
5. **Govern** – Add CI/CD checks for dependency updates, run static security scans, and document the MCP contract for downstream consumers.

**Production Readiness**  
- **Maturity** – Medium. The project is actively maintained (last commit 2026‑05‑14) and has modest community traction (84 stars, 25 forks), indicating a functional core but limited large‑scale validation.  
- **Stability** – The core MCP server runs out‑of‑the‑box, but production use will require reviewing its dependency tree, adding robust authentication, and implementing logging/metrics.  
- **Risks** – No major licensing or metadata issues were found, yet a formal security audit and confirmation of an active maintainer are advisable before critical deployments.  
- **Suitability** – Ideal for internal prototypes, proof‑of‑concepts, or as a “gateway” service in a controlled environment; with proper hardening it can be promoted to production for mission‑critical AI‑tool integrations.

### Русский

**keboola/mcp-server** — это Python‑реализация сервера Model Context Protocol, позволяющая быстро подключать AI‑ассистентов к реальным инструментам и данным Keboola через единый стандартный протокол. Типичный сценарий — развертывание собственного MCP‑сервера для интеграции AI‑агентов с внутренними сервисами, создания прототипов или автоматизации рабочих процессов, а также стандартизация взаимодействия между моделями и внешними системами. Готовность к production — средняя: проект стабилен и активно обновляется (84 ★, 25 forks, последний коммит 2026‑05‑14), но перед запуском в продакшн рекомендуется проверить лицензию, безопасность и наличие постоянных мейнтейнеров.

### 中文

**项目简介**  
keboola/mcp‑server 是 Keboola 平台上的 Model Context Protocol（MCP）服务器，实现了一个统一的协议，用于把 AI 助手与真实的工具、数据源以及数据库进行交互。它提供了可直接调用的 API/SDK/CLI，帮助开发者快速搭建 AI‑to‑tool 的桥梁。

**价值**  
- **标准化**：通过 MCP 协议抽象不同后端系统，使 AI 代理能够以统一的方式调用各种工具和数据。  
- **加速集成**：无需为每个工具单独实现适配层，直接使用服务器提供的接口即可对接。  
- **灵活扩展**：支持自定义模型上下文和元数据，适配多种业务场景（如自动化 ETL、数据分析、模型部署等）。

**典型接入方式**  
1. **API 调用**：在业务代码或 AI 代理中通过 HTTP/REST 调用服务器的 `/execute`、`/context` 等端点。  
2. **Python SDK**：使用项目提供的 `keboola-mcp` 包，直接在 Python 脚本或 Jupyter Notebook 中创建 `MCPClient` 实例并发送指令。  
3. **CLI**：通过 `mcp-cli` 命令行工具在 CI/CD 流程或本地调试时快速触发模型上下文请求。  

**生产可用性**  
- **成熟度**：项目已获 84 ⭐，活跃度良好（最近一次提交 2026‑05‑14），代码基于 Python，社区有一定规模的 Fork 与 Issue 反馈。  
- **适用范围**：适合原型开发、内部工作流自动化以及中小规模的生产环境。  
- **注意事项**：在正式生产前需评估以下几点：  
  - **许可证兼容性**：确认项目许可证（MIT/Apache 等）与贵公司合规要求一致。  
  - **安全审计**：检查依赖库的安全漏洞、API 鉴权机制以及数据脱敏策略。  
  - **运维准备**：部署时建议使用容器化（Docker/K8s）或托管的 Python 环境，配合健康检查和日志收集。  

总体而言，keboola/mcp‑server 为 AI 与业务工具的集成提供了一个可靠且易上手的标准层，只要完成安全与运维的必要审查，即可在生产环境中稳定使用。

## 🧭 Practical evaluation

**Value:** keboola/mcp-server helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 84 GitHub stars
- 25 forks
- updated 2026-05-14
- primary language: Python
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 41/100 |
| topics | 75/100 |
| outlook | 74/100 |
| quality | 69/100 |
| recency | 100/100 |
| adoption | 39/100 |
| production | 75/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/keboola/mcp-server) · [← Back to Mcp](./README.md)</sub>
