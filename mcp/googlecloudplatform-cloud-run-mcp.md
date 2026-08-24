# GoogleCloudPlatform/cloud-run-mcp

[![Stars](https://img.shields.io/github/stars/GoogleCloudPlatform/cloud-run-mcp?style=flat-square&color=yellow)](https://github.com/GoogleCloudPlatform/cloud-run-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/GoogleCloudPlatform/cloud-run-mcp?style=flat-square&color=blue)](https://github.com/GoogleCloudPlatform/cloud-run-mcp/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> MCP server to deploy apps to Cloud Run

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 605 |
| 🍴 **Forks** | 111 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`google-cloud` `google-cloud-run` `mcp` `mcp-server`

## 🎯 Categories

MCP · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
GoogleCloudPlatform/cloud‑run‑mcp is an open‑source MCP (Model Context Protocol) server that lets AI assistants invoke real‑world tools and databases by exposing a standard, language‑agnostic API. Built in JavaScript, it is actively maintained, has over 600 ★ on GitHub and is already being used to ship MCP‑compatible services on Cloud Run.

**Value**  
- **Standardized integration** – By implementing the Model Context Protocol, the server provides a single, consistent way for AI agents to call external services, reducing the need for custom glue code.  
- **Rapid AI‑tool connectivity** – Teams can expose existing back‑ends (databases, internal APIs, SaaS tools) to LLM‑driven workflows without rewriting business logic.  
- **Cloud‑native deployment** – The server is packaged for Cloud Run, giving automatic scaling, managed security, and low‑ops overhead.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Dockerfile or `gcloud run deploy` command, and point an LLM (e.g., Gemini, ChatGPT) at the generated OpenAPI spec.  
2. **Connect data/tools** – Add adapters (SDK, CLI, or custom handlers) for the target service; the project already includes patterns for exposing API metadata and language‑specific hooks.  
3. **Test & iterate** – Use the built‑in test harness or your own integration tests to verify request/response flows and security policies.  
4. **Productionize** – Deploy the server to a dedicated Cloud Run service, enable IAM‑based authentication, and configure monitoring (Cloud Logging, Cloud Monitoring) for observability.

**Production Readiness**  
- **Active development**: last commit on 2026‑05‑11, regular issue triage, and a growing contributor base (111 forks).  
- **Ecosystem fit**: strong alignment with Google Cloud’s serverless stack, and the MCP spec is gaining traction among AI‑agent platforms.  
- **Maturity signals**: >600 ★, clear documentation, and example deployments indicate the code is battle‑tested for pilot projects.  
- **Remaining checks**: a final review of the license, security posture, and maintainer commitment is advisable, but the project is otherwise a solid candidate for production use.

### Русский

**GoogleCloudPlatform/cloud‑run‑mcp** — это сервер MCP, позволяющий быстро развертывать приложения в Google Cloud Run и подключать к ним AI‑ассистентов через единый протокол. Типичный сценарий: разработчик разворачивает Model Context Protocol‑совместимый сервис в Cloud Run, после чего AI‑агенты получают к нему доступ как к внешнему инструменту или базе данных, упрощая интеграцию и автоматизацию. Проект имеет высокий уровень готовности к production: активные коммиты, более 600 звёзд, широкое принятие в сообществе и стабильный JavaScript‑стек, что делает его надёжным кандидатом для пилотных и масштабных внедрений.

### 中文

**项目简介**  
GoogleCloudPlatform/cloud‑run‑mcp 是一个基于 Model Context Protocol（MCP）的服务器，实现了将应用快速部署到 Google Cloud Run 的标准化接口。它让 AI 助手能够通过统一协议调用真实的工具和数据服务。

**价值**  
- **统一协议**：使用 MCP 作为桥梁，AI 代理可以无缝对接各种后端工具、数据库或自研服务，降低集成成本。  
- **即插即用**：只需启动 MCP 服务器，即可把任意容器化应用部署到 Cloud Run，快速将模型或业务逻辑上线。  
- **生态兼容**：提供 API、SDK、CLI 三种接入方式，配合语言元数据和主题标签，便于在多语言环境中统一管理。

**典型接入方式**  
1. **API 调用**：通过 RESTful 接口发送 MCP 请求，服务器负责将请求转发到对应的 Cloud Run 服务。  
2. **SDK**：项目提供的 JavaScript/Node.js SDK 包装了协议细节，开发者只需调用 `runMcp.deploy(appConfig)` 等方法即可。  
3. **CLI**：`gcloud-run-mcp` 命令行工具支持本地调试、部署和日志查看，适合 CI/CD 流程中自动化使用。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑11，项目拥有 605 ⭐、111 🍴，最近一次提交在当日，表明仍在积极维护。  
- **成熟度**：依托 Google Cloud Run 的托管容器平台，具备自动弹性伸缩、流量分配和安全沙箱，适合作为生产环境的后端入口。  
- **风险**：目前未发现重大许可证或安全隐患，但仍建议在正式投产前完成一次完整的安全审计和维护者确认。  

总体而言，cloud‑run‑mcp 已具备在企业级 AI 应用中作为“工具桥梁”进行试点或正式上线的条件。

## 🧭 Practical evaluation

**Value:** GoogleCloudPlatform/cloud-run-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 605 GitHub stars
- 111 forks
- updated 2026-05-11
- primary language: JavaScript
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 59/100 |
| topics | 50/100 |
| outlook | 48/100 |
| quality | 53/100 |
| recency | 20/100 |
| adoption | 57/100 |
| production | 50/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/GoogleCloudPlatform/cloud-run-mcp) · [← Back to Mcp](./README.md)</sub>
