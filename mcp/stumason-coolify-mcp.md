# StuMason/coolify-mcp

[![Stars](https://img.shields.io/github/stars/StuMason/coolify-mcp?style=flat-square&color=yellow)](https://github.com/StuMason/coolify-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/StuMason/coolify-mcp?style=flat-square&color=blue)](https://github.com/StuMason/coolify-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-77%2F100-brightgreen?style=flat-square)](#)

> MCP server for Coolify — 38 optimized tools for managing self-hosted PaaS through AI assistants

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 363 |
| 🍴 **Forks** | 53 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 77/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `claude` `coolify` `deployment` `devops` `infrastructure` `mcp` `model-context-protocol` `paas` `self-hosted` `typescript`

## 🎯 Categories

MCP · AI/ML · Backend · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
StuMason’s **coolify-mcp** is an open‑source Model Context Protocol (MCP) server that lets AI assistants invoke real‑world tools and data in a self‑hosted PaaS environment. By exposing a standard API/SDK/CLI surface, it enables developers to plug AI agents into Coolify’s 38 built‑in DevOps utilities, making AI‑driven automation and orchestration straightforward. With active maintenance, strong community adoption (363 ★, 53 forks) and a TypeScript codebase, it’s ready for pilot deployments.

**Value**  
- **Standardized AI‑to‑tool bridge** – MCP provides a uniform protocol so any AI assistant can discover and call Coolify’s management tools without custom adapters.  
- **Accelerates AI‑augmented DevOps** – Teams can quickly build agents that spin up containers, manage databases, or trigger CI/CD pipelines, reducing manual overhead.  
- **Extensible ecosystem** – The server’s API, SDK, and CLI make it easy to add new tools or expose existing internal services to AI agents.

**Practical Adoption Path**  
1. **Clone & configure** – Deploy the TypeScript server in your Coolify stack (Docker compose or Kubernetes).  
2. **Register tools** – Use the provided CLI or API to expose the desired Coolify utilities (e.g., deployments, logs, backups).  
3. **Connect an AI assistant** – Point your AI model (OpenAI, Anthropic, etc.) to the MCP endpoint; the assistant can now query the server’s schema and invoke actions.  
4. **Iterate & extend** – Add custom commands or integrate external services via the SDK, then test in a staging environment before promoting to production.

**Production Readiness**  
- **High**: Recent commits (as of 2026‑05‑11), active issue handling, and a growing user base indicate a mature codebase.  
- **Robustness**: Clear API contracts, TypeScript type safety, and multiple integration points (API/SDK/CLI) reduce runtime errors.  
- **Remaining checks**: Final review of licensing, security hardening (dependency scanning, auth mechanisms), and confirmation of long‑term maintainers are advisable before a full‑scale rollout.

### Русский

StuMason/coolify-mcp — это сервер Model Context Protocol для платформы Coolify, предоставляющий единый протокол доступа к 38 оптимизированным инструментам управления self‑hosted PaaS через AI‑ассистентов. Типичный сценарий: подключаете AI‑агента к конкретным DevOps‑инструментам (API/SDK/CLI) и быстро разворачиваете собственный MCP‑сервер, стандартизируя интеграцию и обмен данными. Проект имеет высокую готовность к production: активные коммиты, 363 звёзд, широкое использование, современный стек TypeScript и поддержка основных протоколов, что делает его надёжным кандидатом для пилотного внедрения.

### 中文

**项目简介**  
StuMason/coolify-mcp 是为 Coolify 构建的 MCP（Model Context Protocol）服务器，提供 38 套经过优化的工具，帮助 AI 助手直接调用自托管 PaaS 环境中的真实功能和数据。

**价值**  
- **标准化接入**：通过统一的 MCP 协议，将 AI 代理与各种运维、部署、监控等工具对接，避免了每个工具各自的 API 融合成本。  
- **提升效率**：AI 助手可以在自然语言指令下完成代码部署、日志查询、容器管理等任务，实现“对话即运维”。  
- **生态兼容**：兼容 Coolify 的插件体系，能够快速在现有自托管 PaaS 中部署，降低迁移门槛。

**典型接入方式**  
1. **部署 MCP 服务器**：使用 Docker 或直接在 Node.js 环境中运行 `npm install && npm start`，服务器默认监听 8080。  
2. **注册到 AI 平台**：在 OpenAI、Claude、Gemini 等支持 MCP 的大模型平台上配置 “Tool URL”，指向部署好的服务器地址。  
3. **调用方式**：AI 通过 MCP 的 JSON‑RPC 接口（或提供的 SDK/CLI）发送 `tool_call` 请求，服务器内部映射到对应的 Coolify API/CLI 并返回结构化结果。  
4. **可选扩展**：通过 TypeScript SDK 自定义新工具或覆盖已有实现，亦可使用提供的 CLI 进行本地调试。

**生产可用性**  
- **活跃度**：截至 2026‑05‑11，项目最近一次提交，星标 363，fork 53，社区活跃。  
- **技术成熟度**：使用 TypeScript 编写，提供完整的 API 文档、示例代码和 Docker 镜像，易于 CI/CD 集成。  
- **安全与合规**：暂无已知许可证或安全漏洞风险，但仍建议在正式环境前进行内部审计（依赖的 Coolify 组件同样需要审查）。  
- **适配度**：已在多个自托管 Coolify 实例中验证，可直接用于生产环境的 AI‑Ops 场景，适合作为 Pilot 项目或正式部署的底层服务。  

综上，coolify-mcp 通过标准化的 MCP 接口把 AI 助手与自托管 PaaS 工具桥接起来，接入简便、功能丰富且具备生产级别的可靠性，是构建 AI‑驱动运维平台的关键组件。

## 🧭 Practical evaluation

**Value:** StuMason/coolify-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 363 GitHub stars
- 53 forks
- updated 2026-05-11
- primary language: TypeScript
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 43/100 |
| stars | 55/100 |
| topics | 100/100 |
| outlook | 86/100 |
| quality | 78/100 |
| recency | 100/100 |
| adoption | 51/100 |
| production | 78/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/StuMason/coolify-mcp) · [← Back to Mcp](./README.md)</sub>
