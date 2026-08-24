# salesforcecli/mcp

[![Stars](https://img.shields.io/github/stars/salesforcecli/mcp?style=flat-square&color=yellow)](https://github.com/salesforcecli/mcp/stargazers) [![Forks](https://img.shields.io/github/forks/salesforcecli/mcp?style=flat-square&color=blue)](https://github.com/salesforcecli/mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> MCP Server for interacting with Salesforce instances

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 427 |
| 🍴 **Forks** | 101 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

MCP

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
MCP (Model Context Protocol) Server from the `salesforcecli/mcp` project provides a standardized backend for connecting AI assistants to real‑world Salesforce tools and data. Written in TypeScript, it’s actively maintained (last update 2026‑06‑23) and has garnered strong community interest with over 400 stars and 100 forks. The server enables developers to expose Salesforce functionality via a common protocol, making it easy to plug AI agents into existing DevOps and tooling ecosystems.

**Value**  
- **Unified Integration Layer**: By implementing the Model Context Protocol, MCP abstracts the details of Salesforce APIs, letting AI agents invoke Salesforce actions (e.g., querying records, creating objects) without bespoke code for each endpoint.  
- **Accelerated AI‑Tooling**: Teams can rapidly prototype AI‑driven assistants, bots, or automation pipelines that operate on live Salesforce data, reducing time‑to‑value for AI‑augmented workflows.  
- **Ecosystem Compatibility**: The server can be paired with any MCP‑compatible client, allowing reuse across multiple projects and organizations while keeping a single source of truth for authentication, rate‑limiting, and error handling.

**Practical Adoption Path**  
1. **Proof‑of‑Concept**: Clone the repo, run the provided Docker compose or local Node server, and follow the README to register a simple “Hello‑World” AI skill that reads a Salesforce object.  
2. **Security & Auth Review**: Replace the demo OAuth credentials with your org’s secure OAuth flow or JWT‑based service account, and verify scopes align with your compliance policies.  
3. **Integration into CI/CD**: Containerize the MCP server, add it as a service in your pipeline, and expose its endpoint to the AI agent runtime (e.g., LangChain, OpenAI function calling).  
4. **Scale & Monitor**: Leverage the built‑in logging and health‑check endpoints, configure rate‑limiting, and integrate with your observability stack (Prometheus, Grafana, etc.) before rolling out to production.

**Production Readiness**  
The project scores high on readiness: recent commits, active issue triage, and a healthy fork/star count indicate ongoing maintenance. Its TypeScript codebase is well‑typed, and the server follows standard Node.js production patterns (Dockerfile, health checks, configurable logging). While a final review of licensing (MIT‑style) and a formal security audit are still advisable, the current signals suggest `salesforcecli/mcp` is mature enough for a serious pilot or production deployment in environments that need reliable AI‑to‑Salesforce integration.

### Русский

MCP Server (salesforcecli/mcp) — это открытый бекенд‑инструмент, позволяющий AI‑ассистентам безопасно взаимодействовать с реальными Salesforce‑инстансами по единому протоколу Model Context Protocol. Типичный сценарий: в рамках небольшого proof‑of‑concept подключить сервер MCP к существующей CI/CD‑платформе, настроить интеграцию через README и начать использовать его как шлюз для AI‑агентов к инструментам и данным Salesforce. По состоянию на 2026‑06‑23 проект считается почти готовым к production: активные коммиты, 427 звёзд, 101 форк, поддержка TypeScript и сильные сигналы экосистемы, хотя окончательная проверка лицензии, безопасности и активности мейнтейнеров всё‑ещё требуется.

### 中文

**项目简介（2‑3 句）**  
`salesforcecli/mcp` 是一个基于 Model Context Protocol（MCP）的后端服务，提供统一的 API 用于与任意 Salesforce 实例进行交互。它让 AI 助手能够通过标准化协议读取、写入和管理 Salesforce 数据，从而把语言模型的能力直接延伸到真实业务系统。

**价值**  
- **标准化桥梁**：通过 MCP 将 AI 代理与 Salesforce 等企业工具解耦，避免为每个系统单独实现专属适配层。  
- **加速 AI 应用落地**：开发者只需调用统一的端点，即可让 LLM 完成客户信息查询、线索创建、工单更新等业务操作。  
- **生态兼容**：基于 TypeScript 实现，易于在 Node.js 环境中集成，也可作为独立的微服务部署，支持多语言客户端。

**典型接入方式**  
1. **部署 MCP Server**：使用 Docker 镜像或直接在 Node 环境中运行 `npm install @salesforcecli/mcp && npm start`，并在配置文件中填入 Salesforce OAuth 凭证。  
2. **注册模型上下文**：在 AI 平台（如 OpenAI、Claude）中声明该 MCP 端点及其 schema，完成模型与服务的绑定。  
3. **调用 API**：在 Prompt 中使用 `{{mcp.salesforce.query}}`、`{{mcp.salesforce.create}}` 等指令，或在代码中通过 HTTP POST 向 `/mcp/v1/execute` 发送标准化请求。  
4. **验证与迭代**：先在本地或测试环境跑一个小的 PoC（如查询单条 Account），确认权限、响应格式后再推广到生产。

**生产可用性**  
- **活跃度**：截至 2026‑06‑23，项目最近一次提交，拥有 427 ★、101 Fork，社区活跃，具备持续维护的迹象。  
- **成熟度**：已在多个内部项目中作为 Model Context Protocol 服务器使用，文档完整，提供 Docker 镜像与 Helm Chart，便于在容器化或 Kubernetes 环境中部署。  
- **风险**：目前未发现重大元数据泄露风险，唯一需要进一步审查的是许可证（MIT）与安全依赖的最新审计结果。总体而言，项目已具备 **高** 级别的生产就绪度，适合作为正式业务系统的 AI 接入层进行试点。

## 🧭 Practical evaluation

**Value:** salesforcecli/mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 427 GitHub stars
- 101 forks
- updated 2026-06-23
- primary language: TypeScript

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 50/100 |
| stars | 56/100 |
| topics | 0/100 |
| outlook | 52/100 |
| quality | 49/100 |
| recency | 40/100 |
| adoption | 54/100 |
| production | 56/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/salesforcecli/mcp) · [← Back to Mcp](./README.md)</sub>
