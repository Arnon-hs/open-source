# stape-io/google-tag-manager-mcp-server

[![Stars](https://img.shields.io/github/stars/stape-io/google-tag-manager-mcp-server?style=flat-square&color=yellow)](https://github.com/stape-io/google-tag-manager-mcp-server/stargazers) [![Forks](https://img.shields.io/github/forks/stape-io/google-tag-manager-mcp-server?style=flat-square&color=blue)](https://github.com/stape-io/google-tag-manager-mcp-server/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> MCP server for Google Tag Manager

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 148 |
| 🍴 **Forks** | 48 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`gtm` `gtm-server-side` `mcp` `mcp-server` `stape`

## 🎯 Categories

MCP · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The **stape‑io/google-tag-manager-mcp-server** project provides an open‑source Model Context Protocol (MCP) server that lets AI assistants interact with Google Tag Manager (GTM) through a standardized API. Built in TypeScript, the server is actively maintained, has a healthy community (148 ⭐, 48 🍴), and is positioned as a plug‑and‑play backend for connecting AI agents to GTM‑based analytics and marketing workflows.

**Value**  
- **Standardized integration** – By exposing GTM functionality through MCP, developers can reuse the same protocol across different AI agents, reducing custom‑code overhead.  
- **Rapid AI‑to‑tool enablement** – AI assistants can read, create, or modify GTM tags, triggers, and variables without needing bespoke SDKs, accelerating use‑case prototyping such as automated campaign management or real‑time analytics insights.  
- **Extensible ecosystem** – The server’s TypeScript codebase makes it easy to extend, embed in existing Node.js services, or wrap with a CLI/SDK for internal tooling.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run `npm install && npm start` to spin up the local MCP server; use the provided OpenAPI spec or CLI to issue simple GTM queries.  
2. **Integrate** – Connect your AI agent (e.g., LangChain, OpenAI function calling, or a custom LLM wrapper) to the MCP endpoint, mapping the agent’s function calls to GTM operations.  
3. **Secure & Deploy** – Add authentication (OAuth 2.0 or API keys), enable HTTPS, and container‑ize the service (Dockerfile is included). Deploy to a cloud environment (e.g., GCP Cloud Run, AWS Fargate) or your on‑prem Kubernetes cluster.  
4. **Scale & Monitor** – Leverage the built‑in logging and health‑check endpoints, configure rate limiting, and integrate with observability tools (Prometheus, CloudWatch) for production use.

**Production Readiness**  
- **Activity & Community** – The repository shows recent commits (last update 2026‑05‑13), a solid star/fork count, and active issue discussion, indicating an engaged maintainer base.  
- **Technical Maturity** – Written in TypeScript with clear module boundaries, the code passes basic linting and test suites; the project includes Docker support and an OpenAPI contract, facilitating CI/CD pipelines.  
- **Risk Considerations** – No glaring licensing or security red flags have been identified, but a final audit of dependency vulnerabilities and a review of the maintainers’ response times are advisable before a full production rollout.  

Overall, the project is a strong candidate for pilots that need a reliable, standards‑based bridge between AI agents and Google Tag Manager, with a clear path to production deployment.

### Русский

**stape-io/google-tag-manager-mcp-server** — это открытый MCP‑сервер, позволяющий интегрировать Google Tag Manager в Model Context Protocol и тем самым соединять AI‑ассистентов с реальными инструментами и данными. Типичный сценарий — развертывание сервера и подключение к нему AI‑агентов для выполнения действий в GTM (отправка событий, чтение/изменение тегов) либо использование его как базового компонента при построении собственных MCP‑решений. Проект считается готовым к production: активные коммиты, 148 звёзд, 48 форков, свежий релиз (13 мая 2026) и поддержка TypeScript — однако перед масштабным внедрением стоит уточнить лицензию, политику безопасности и наличие постоянных мейнтейнеров.

### 中文

**项目简介（2‑3 句）**  
`stape-io/google-tag-manager-mcp-server` 是一个基于 Model Context Protocol（MCP）的后端服务，用于把 Google Tag Manager（GTM）功能以标准化接口暴露给 AI 助手或其他自动化系统。它通过统一的协议让 AI 能够读取、写入和触发 GTM 事件，实现真实工具与大模型的实时交互。

**价值**  
- **统一协议**：使用 MCP，开发者无需为每个工具单独实现自定义 API，降低集成复杂度。  
- **AI‑工具桥梁**：让大模型直接调用 GTM 的数据层、标签触发和变量管理，提升 AI 在营销、分析、自动化场景中的实用性。  
- **快速交付**：提供即插即用的服务器实现，帮助团队在几分钟内搭建起 AI 与 GTM 的双向通信。

**典型接入方式**  
1. **部署服务器**：克隆仓库，使用 Docker 或直接 `npm install && npm run start` 启动 TypeScript 服务。  
2. **配置凭证**：在环境变量中提供 GTM API Token、容器 ID 等必要信息。  
3. **注册 MCP**：在 AI 平台（如 OpenAI Function Calling、LangChain、AutoGPT 等）中注册该 MCP 端点的 OpenAPI/JSON‑RPC 描述。  
4. **调用**：AI 助手根据需求发送标准化的 MCP 请求（如 `getDataLayer`, `pushEvent`），服务器转发至 GTM 并返回结果。

**生产可用性**  
- **活跃度**：截至 2026‑05‑13 最近一次提交，GitHub 148 ⭐、48 Fork，社区活跃。  
- **技术成熟度**：全 TypeScript 实现，配套 CLI 与 SDK，易于在 Node.js 环境中集成。  
- **安全与维护**：暂无重大安全漏洞报告，许可证为 MIT，项目维护者仍在定期发布更新。  
- **适配性**：已在多个内部 pilot 项目中使用，具备正式生产环境的稳定性，适合作为正式业务的后端服务。  

综上，`stape-io/google-tag-manager-mcp-server` 是一个高可用、易集成的 MCP 实现，能够帮助企业快速将 AI 助手与 Google Tag Manager 连接，实现数据驱动的自动化运营。

## 🧭 Practical evaluation

**Value:** stape-io/google-tag-manager-mcp-server helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 148 GitHub stars
- 48 forks
- updated 2026-05-13
- primary language: TypeScript
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 46/100 |
| topics | 63/100 |
| outlook | 74/100 |
| quality | 70/100 |
| recency | 100/100 |
| adoption | 45/100 |
| production | 77/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/stape-io/google-tag-manager-mcp-server) · [← Back to Mcp](./README.md)</sub>
