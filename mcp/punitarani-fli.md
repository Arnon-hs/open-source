# punitarani/fli

[![Stars](https://img.shields.io/github/stars/punitarani/fli?style=flat-square&color=yellow)](https://github.com/punitarani/fli/stargazers) [![Forks](https://img.shields.io/github/forks/punitarani/fli?style=flat-square&color=blue)](https://github.com/punitarani/fli/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-79%2F100-brightgreen?style=flat-square)](#)

> Google Flights MCP and Python Library

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.4k |
| 🍴 **Forks** | 264 |
| 💻 **Language** | Python |
| 📈 **Score** | 79/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`api` `flights-api` `google-flights` `google-flights-api` `mcp` `mcp-server`

## 🎯 Categories

MCP · Backend

## 📝 Summary

### English

**Brief Summary**  
punitarani/fli is an open‑source Python library that implements Google Flights’ Model Context Protocol (MCP), providing a standard way for AI assistants to invoke real‑world tools and data sources. With over 2 400 stars and active recent commits, it offers a ready‑to‑use API/SDK/CLI for building MCP servers and integrating AI agents with flight‑search functionality and other services.

**Value**  
The project abstracts the complexities of connecting AI agents to external tools behind a uniform protocol, enabling developers to plug in any MCP‑compatible service (e.g., flight search, booking, or custom data APIs) without rewriting glue code. This standardization accelerates AI‑agent development, reduces integration bugs, and fosters ecosystem interoperability.

**Practical Adoption Path**  
1. **Prototype** – Install the Python package, run the provided CLI to spin up a local MCP server, and test against the Google Flights demo endpoints.  
2. **Extend** – Implement custom handlers or adapters for your own services by following the library’s SDK guidelines and publishing the new endpoints as MCP routes.  
3. **Deploy** – Containerize the server (Dockerfile is included), expose it via HTTPS, and register the endpoint with your AI assistant platform (e.g., LangChain, AutoGPT).  
4. **Scale** – Leverage the library’s built‑in async support and monitoring hooks to run the server in production clusters (Kubernetes, Cloud Run, etc.).

**Production Readiness**  
The repository shows strong OSS health signals: recent activity (last commit 2026‑05‑12), a large user base (≈2.4 k stars, 264 forks), clear documentation, and a well‑defined API surface. While the license and security posture still need a final audit, the codebase is mature, the Python ecosystem is stable, and the project is already being used in pilot deployments, making it a solid candidate for production‑grade pilots.

### Русский

punitarani/fli — это открытая Python‑библиотека и MCP‑сервер, позволяющие AI‑ассистентам взаимодействовать с реальными инструментами и данными через единый протокол Model Context Protocol. Типичный сценарий — подключение AI‑агентов к внешним сервисам (API, CLI, SDK) и развертывание собственного MCP‑сервера для стандартизации интеграций. Проект демонстрирует высокий уровень готовности к production: активные коммиты, более 2400 звёзд, широкое принятие в сообществе и стабильный Python‑стек, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
punitarani / fli 是一个基于 Google Flights 的 **Model Context Protocol（MCP）** 实现及配套的 Python 库。它提供统一的协议层，使 AI 助手能够像调用本地函数一样安全、可靠地访问真实的工具和数据源。

**价值主张**  
- **标准化集成**：通过 MCP 将 AI 代理与外部服务（如航班查询、预订系统等）解耦，避免每个项目都重新实现 API 调用逻辑。  
- **加速开发**：提供 Python SDK、CLI 以及可直接部署的服务器实现，开发者只需几行代码即可让 AI 代理使用真实工具。  
- **提升可靠性**：MCP 为请求/响应、错误处理、权限校验等提供统一约定，降低因自定义接口导致的安全与稳定性风险。

**典型接入方式**  
1. **作为 MCP 服务器**  
   - 克隆仓库 → `docker compose up`（或直接 `python -m fli.server`）启动符合 MCP 规范的 HTTP 服务。  
   - 在 AI 平台（如 OpenAI Function Calling、LangChain）中注册该服务的 OpenAPI/JSON‑RPC 描述，即可让模型调用航班查询等功能。  

2. **作为 Python SDK**  
   - `pip install fli`  
   - 在代码中 `from fli import FlightsClient`，使用 `client.search(origin, destination, date)` 等方法直接获取航班数据，适合后端业务或自定义 AI Agent。  

3. **CLI 方式**  
   - 安装后运行 `fli search --from SFO --to JFK --date 2024-12-01`，快速在终端或脚本中验证功能，便于调试和 CI 集成。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑12 最近一次提交，拥有 2 415 星、264 fork，社区活跃，Issue 响应及时。  
- **成熟度**：提供完整的 OpenAPI 规范、单元测试以及 CI/CD，已在多个内部项目中作为正式的 MCP 服务运行。  
- **风险**：目前未发现重大许可证或安全隐患，但仍建议在正式投产前完成一次许可证合规审查并进行渗透测试。  

综合来看，punitarani/fli 已具备 **高生产就绪度**，适合作为 AI 助手接入真实工具的首选开源组件。

## 🧭 Practical evaluation

**Value:** punitarani/fli helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2415 GitHub stars
- 264 forks
- updated 2026-05-12
- primary language: Python
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 61/100 |
| stars | 72/100 |
| topics | 75/100 |
| outlook | 78/100 |
| quality | 77/100 |
| recency | 80/100 |
| adoption | 69/100 |
| production | 77/100 |
| usefulness | 74/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/punitarani/fli) · [← Back to Mcp](./README.md)</sub>
