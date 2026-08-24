# corezoid/simulator-ai-plugin

[![Stars](https://img.shields.io/github/stars/corezoid/simulator-ai-plugin?style=flat-square&color=yellow)](https://github.com/corezoid/simulator-ai-plugin/stargazers) [![Forks](https://img.shields.io/github/forks/corezoid/simulator-ai-plugin?style=flat-square&color=blue)](https://github.com/corezoid/simulator-ai-plugin/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Claude Code & Codex plugin for Simulator.Company — a Go MCP server exposing the platform REST API plus skills for actors, graphs, forms, and financial accounts.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 54 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | Go |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-plugin` `anthropic` `bpm` `business-process` `claude` `claude-code` `golang` `mcp` `model-context-protocol` `simulator-company`

## 🎯 Categories

MCP · AI/ML · Backend

## 📝 Summary

### English

**Project Summary**

The corezoid/simulator-ai-plugin is an open-source project that enables the connection of AI assistants to real tools and data through a standard protocol, specifically the Model Context Protocol (MCP). This project provides a Go-based MCP server exposing the platform REST API and skills for actors, graphs, forms, and financial accounts. By standardizing integrations, it facilitates the connection of AI agents to tools and enables the shipping of MCP servers.

**Value Proposition**

The value proposition of this project lies in its ability to standardize integrations between AI assistants and real tools and data. This allows developers to easily connect AI agents to tools and enables the creation of more seamless and efficient workflows.

**Practical Adoption Path**

To adopt this project, developers can follow these steps:

1. Evaluate the project's documentation and codebase to understand its implementation and usage.
2. Expose the API/SDK/CLI implementation signals to integrate the project with existing tools and systems.
3. Standardize integrations using the Model Context Protocol (MCP) to connect AI agents to tools.

**Production Readiness**

The project has a high level of production readiness due to recent activity, adoption, and ecosystem signals. It has a strong primary language (Go) and 10 topics, indicating

### Русский

Резюме проекта:

Corezoid/simulator-ai-plugin - это открытое исходное кодное решение, которое позволяет соединять интеллектуальные ассистенты с реальными инструментами и данными через стандартный протокол. Этот проект предназначен для подключения агентов AI к инструментам и.standardизации интеграций, обеспечивая простоту внедрения и высокий уровень готовности к производству.

### 中文

**项目简介**  
corezoid/simulator-ai-plugin 是为 **Simulator.Company** 提供的 Claude Code & Codex 插件，基于 Go 实现的 MCP（Model Context Protocol）服务器。它在统一的 REST API 之上，额外暴露了演员、图谱、表单和财务账户等业务技能，使 AI 助手能够直接调用真实的业务工具和数据。

**价值主张**  
- **标准化桥接**：通过 MCP/REST 接口把 AI 助手与企业内部系统、数据库、业务服务等“真实工具”对接，避免为每个 AI 场景单独开发专属集成。  
- **快速落地**：内置的演员、图谱、表单、财务等业务能力即插即用，帮助企业在几行代码或一次配置后即可让 AI 完成业务流程、查询报表、执行交易等任务。  
- **生态兼容**：遵循 Model Context Protocol，天然兼容 Claude Code、Codex 以及其他支持 MCP 的 AI 平台，便于在多模型、多供应商环境中统一管理。

**典型接入方式**  
1. **部署 MCP 服务器**：使用 Docker 或直接在 Go 环境中运行 `simulator-ai-plugin`，对外提供 HTTP/HTTPS 接口。  
2. **注册插件**：在 Claude/Code 或其他 MCP 客户端中添加插件的 OpenAPI/Swagger 描述或直接使用插件提供的 SDK。  
3. **调用业务技能**：AI 助手通过标准的 `invoke`、`query`、`execute` 等 MCP 方法调用演员、图谱、表单或财务账户等功能；也可以通过 CLI/SDK 进行本地调试。  
4. **安全与鉴权**：插件支持基于 OAuth2、API‑Key 或自定义 JWT 的鉴权方案，可与企业 SSO、IAM 系统集成。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑30，GitHub 统计 54 ⭐、4 🍴，拥有 10+ 主题标签，表明社区关注度和文档覆盖较好。  
- **成熟度**：代码基于 Go，具备静态类型检查和编译期错误捕获，运行时性能稳定；MCP 协议已在多个内部项目中验证。  
- **可评估性**：提供完整的 OpenAPI 描述、Go SDK 与 CLI，便于快速在测试环境进行功能验证。  
- **风险**：目前未发现重大许可证或安全漏洞，但仍建议在正式上线前完成一次依赖审计、渗透测试以及维护者确认的 SLA 约定。

综合来看，corezoid/simulator-ai-plugin 已具备 **高** 的生产就绪度，适合作为 **AI‑to‑Tool** 集成的底层平台，在企业内部或面向客户的 AI 产品中快速部署使用。

## 🧭 Practical evaluation

**Value:** corezoid/simulator-ai-plugin helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 54 GitHub stars
- 4 forks
- updated 2026-06-30
- primary language: Go
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 37/100 |
| topics | 100/100 |
| outlook | 57/100 |
| quality | 54/100 |
| recency | 40/100 |
| adoption | 32/100 |
| production | 59/100 |
| usefulness | 74/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/corezoid/simulator-ai-plugin) · [← Back to Mcp](./README.md)</sub>
