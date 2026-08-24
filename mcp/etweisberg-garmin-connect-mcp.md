# etweisberg/garmin-connect-mcp

[![Stars](https://img.shields.io/github/stars/etweisberg/garmin-connect-mcp?style=flat-square&color=yellow)](https://github.com/etweisberg/garmin-connect-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/etweisberg/garmin-connect-mcp?style=flat-square&color=blue)](https://github.com/etweisberg/garmin-connect-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> Garmin Connect MCP

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 36 |
| 🍴 **Forks** | 11 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`garmin` `garmin-connect` `garmin-watch` `mcp` `mcp-server` `typescript`

## 🎯 Categories

MCP · Backend

## 📝 Summary

### English

**Brief Summary**  
Garmin Connect MCP is an open‑source TypeScript library that implements the Model Context Protocol (MCP) for Garmin’s data services, enabling AI assistants to invoke real‑world Garmin tools and datasets via a standard, language‑agnostic API. With a modest star count (36) and recent activity (last commit 2026‑07‑12), it offers a ready‑to‑use backend component for prototyping AI‑to‑device integrations.

**Value**  
- **Standardised bridge** – By exposing Garmin’s functionality through MCP, the project lets any MCP‑compatible AI agent (e.g., LangChain, AutoGPT) call Garmin APIs without writing custom adapters.  
- **Accelerates AI‑tool integration** – Teams can reuse the same protocol across multiple domains, reducing engineering overhead and ensuring consistent security and observability.  
- **Open‑source flexibility** – The TypeScript codebase can be extended or self‑hosted, giving full control over data handling and compliance.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Docker/CLI scripts, and point your AI agent’s MCP client to the local server.  
2. **Validate** – Use the built‑in Swagger/OpenAPI docs to test key Garmin endpoints (e.g., activity upload, device sync) and confirm data flows meet your use case.  
3. **Customize** – Extend the TypeScript handlers to add authentication, caching, or domain‑specific logic.  
4. **Deploy** – Containerise the service and roll it out to a staging environment behind your API gateway; update the AI agent’s configuration to target the production endpoint.  

**Production Readiness**  
- **Maturity**: Medium – the code is functional and recently updated, but the ecosystem is small (36 ★, 11 forks) and there is limited evidence of large‑scale deployments.  
- **Risks**: Licensing and security posture need a final review; the project has few active maintainers, so you’ll likely need to assume responsibility for patches and dependency updates.  
- **Suitability**: Ideal for internal tools, pilots, or proof‑of‑concepts where you can monitor and address issues early; for mission‑critical production workloads, plan for additional hardening (e.g., automated tests, vulnerability scanning, and a clear hand‑off to an internal maintainer).

### Русский

Резюме проекта etweisberg/garmin-connect-mcp:

Проект Garmin Connect MCP предлагает стандартный протокол для связи между искусственными интеллектуальными агентами и реальными инструментами и данными. Он позволяет подключать AI-агентов к различным инструментам и стандартизировать интеграции. Проект готов к использованию в прототипах или внутренних рабочих процессах, но требует проверки зависимостей и поддержки перед внедрением в производственный режим.

### 中文

**项目简介（2‑3 句）**  
etweisberg/garmin‑connect‑mcp 是一个基于 Model Context Protocol（MCP）的后端服务，实现了 Garmin Connect 数据的标准化访问。它提供 TypeScript SDK 与 CLI，帮助 AI 助手快速对接 Garmin 设备与云端数据。

**价值**  
- 将真实的 Garmin 设备与 AI 助手桥接，统一使用 MCP 协议，降低集成复杂度。  
- 为开发者提供即插即用的 API/SDK，快速构建原型或内部工具，支持后续向生产环境迁移。  

**典型接入方式**  
1. **SDK**：在 Node.js/TypeScript 项目中 `npm install garmin-connect-mcp`，通过提供的 `GarminClient` 初始化并调用统一的 MCP 接口。  
2. **CLI**：使用 `npx garmin-mcp <command>` 直接在终端执行数据查询或同步任务，适合脚本化工作流。  
3. **自建 MCP 服务器**：将项目作为独立的 MCP 服务部署（Docker/PM2），对外暴露 REST/gRPC 接口，供其他 AI 代理或微服务调用。  

**生产可用性**  
- **成熟度**：目前适用于原型和内部工作流，具备基本的功能完整性和文档。  
- **依赖与维护**：项目依赖较少（纯 TypeScript），但仍需关注其维护者活跃度和安全审计后再用于关键业务。  
- **准备度**：中等（Medium）。在正式生产前建议进行：  
  - 代码审计与安全扫描；  
  - 版本锁定与依赖审查；  
  - 高可用部署（如容器化、负载均衡）和监控。  

总体而言，etweisberg/garmin-connect-mcp 为 AI 与 Garmin 生态的集成提供了便捷的标准化入口，适合作为快速验证和内部工具的底层组件，经过适当的安全和运维加固后即可投入生产使用。

## 🧭 Practical evaluation

**Value:** etweisberg/garmin-connect-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 36 GitHub stars
- 11 forks
- updated 2026-07-12
- primary language: TypeScript
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 27/100 |
| stars | 33/100 |
| topics | 75/100 |
| outlook | 51/100 |
| quality | 50/100 |
| recency | 40/100 |
| adoption | 32/100 |
| production | 54/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/etweisberg/garmin-connect-mcp) · [← Back to Mcp](./README.md)</sub>
