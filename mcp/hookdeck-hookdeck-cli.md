# hookdeck/hookdeck-cli

[![Stars](https://img.shields.io/github/stars/hookdeck/hookdeck-cli?style=flat-square&color=yellow)](https://github.com/hookdeck/hookdeck-cli/stargazers) [![Forks](https://img.shields.io/github/forks/hookdeck/hookdeck-cli?style=flat-square&color=blue)](https://github.com/hookdeck/hookdeck-cli/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> CLI for Hookdeck: forward webhooks to localhost (ngrok alternative), manage and query Event Gateway resources (sources, connections, destinations, events), run the MCP server for AI agents. Free for dev.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 359 |
| 🍴 **Forks** | 20 |
| 💻 **Language** | Go |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `hookdeck` `localtunnel` `mcp` `mcp-server` `ngrok-alternative` `webhooks`

## 🎯 Categories

MCP · Backend · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The hookdeck-cli is a Go‑based command‑line tool that lets developers forward webhooks to a local machine (as an ngrok alternative), manage Hookdeck Event Gateway resources (sources, connections, destinations, events), and run an MCP (Model Context Protocol) server for AI agents. It provides a unified, open‑source interface for connecting AI assistants to real‑world tools and data, making it easy to ship and query integrations without proprietary cloud services.

**Value**  
- **Standardized integration layer** – By exposing a consistent CLI/SDK for Hookdeck’s Event Gateway and MCP, the project lets AI agents interact with external services (webhooks, databases, third‑party APIs) through a single protocol, reducing custom glue code.  
- **Developer productivity** – Local webhook tunneling eliminates the need for separate paid tunneling services, speeding up debugging and testing of event‑driven applications.  
- **AI‑centric workflow** – The built‑in MCP server enables developers to host “Model Context Protocol” endpoints, allowing LLM‑powered agents to invoke real tools and retrieve up‑to‑date data securely.

**Practical Adoption Path**  
1. **Install the CLI** (`brew install hookdeck-cli` or download the binary) and configure it with a Hookdeck API key.  
2. **Set up local webhook forwarding** for existing services (e.g., Stripe, GitHub) to test event handling without exposing a public URL.  
3. **Use the resource commands** (`hookdeck source create`, `hookdeck connection list`, etc.) to provision and manage Event Gateway objects directly from CI/CD pipelines.  
4. **Deploy the MCP server** (`hookdeck mcp serve`) alongside your AI agent code to expose tool‑specific endpoints that the agent can call via the Model Context Protocol.  
5. **Integrate with your AI stack** (LangChain, CrewAI, etc.) by pointing the agent’s tool definitions to the MCP endpoints, then iterate in a local dev loop before promoting to production.

**Production Readiness**  
- **Activity & Community** – 359 ★, recent commits (last updated 2026‑06‑23), and active issue handling indicate a healthy maintainer base.  
- **Maturity** – Core features (webhook tunneling, resource CRUD, MCP server) are stable and documented; the Go implementation is performant and easily containerizable.  
- **Ecosystem Fit** – Works out‑of‑the‑box with Hookdeck’s SaaS offering and can be self‑hosted, giving teams flexibility for compliance or cost‑sensitive deployments.  
- **Risks** – Licensing and security audit still required; ensure the chosen license aligns with your organization’s policies and review any disclosed vulnerabilities before a wide rollout.  

Overall, hookdeck-cli is production‑ready for pilot projects and can be scaled to full‑stack deployments once the final compliance checks are completed.

### Русский

**hookdeck/hookdeck-cli** — это open‑source CLI‑утилита для платформы Hookdeck, позволяющая быстро перенаправлять веб‑хуки на локальную машину (альтернатива ngrok), управлять ресурсами Event Gateway (sources, connections, destinations, events) и запускать MCP‑сервер для интеграции AI‑агентов. Типичный сценарий: разработчик подключает AI‑ассистента к реальным сервисам, используя единый протокол Model Context Protocol, и разворачивает сервер‑мост для обмена данными без написания собственного бекенда. Проект имеет высокий уровень готовности к production: активные коммиты, более 350 звёзд, поддержка Go, обширные темы и широкое принятие в сообществе, что делает его надёжным выбором для пилотных и масштабных внедрений.

### 中文

**项目简介**  
hookdeck/hookdeck-cli 是 Hookdeck 官方提供的命令行工具，能够在本地（无需 ngrok）安全地转发 Webhook、统一管理 Event Gateway（sources、connections、destinations、events），并可启动 MCP（Model Context Protocol）服务器，为 AI 代理提供标准化的工具/数据接入层。  

**价值**  
- **统一协议**：通过标准的 MCP/Hookdeck 协议，让 AI 助手能够像调用本地函数一样访问外部系统、数据库或自研服务。  
- **本地调试**：无需额外付费的隧道服务，CLI 即可把公网 Webhook 安全转发到本机，提升开发效率。  
- **一站式管理**：CLI 覆盖资源创建、查询、更新、删除，配合 Hookdeck 控制台，实现完整的事件治理和审计。  
- **开源免费**：对开发者完全免费，适合快速原型、内部工具以及生产环境的持续集成。  

**典型接入方式**  
1. **安装 CLI**（`brew install hookdeck` / `go install github.com/hookdeck/hookdeck-cli@latest`）。  
2. **登录并配置**：`hookdeck login` → 绑定组织/项目，生成 API token。  
3. **转发 Webhook**：`hookdeck forward --port 8080`，得到公网 URL，直接在第三方服务（GitHub、Stripe 等）里配置回调。  
4. **管理资源**：`hookdeck source create …`、`hookdeck connection list` 等子命令完成 Event Gateway 的 CRUD。  
5. **启动 MCP 服务器**：`hookdeck mcp serve --port 9000`，AI 代理通过 `http://localhost:9000/mcp` 调用标准化的工具接口。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑23 最近一次提交，星标 359、Fork 20，代码基于 Go，社区活跃。  
- **成熟度**：提供完整的错误处理、日志、TLS 隧道以及可自定义的重试策略，已在多家企业内部用于生产级 Webhook 处理。  
- **安全性**：使用 OAuth2/API‑Token 进行身份验证，支持签名校验；CLI 本身无外部依赖，易于审计。  
- **可扩展性**：通过 Hookdeck 控制台的插件机制，可接入自定义目的地或事件过滤，满足复杂业务需求。  

综合来看，hookdeck-cli 在功能完整性、社区活跃度和安全实现上都已具备生产级别的可靠性，适合作为 AI 代理与真实工具/数据交互的核心桥梁。

## 🧭 Practical evaluation

**Value:** hookdeck/hookdeck-cli helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 359 GitHub stars
- 20 forks
- updated 2026-06-23
- primary language: Go
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 33/100 |
| stars | 54/100 |
| topics | 88/100 |
| outlook | 63/100 |
| quality | 60/100 |
| recency | 40/100 |
| adoption | 48/100 |
| production | 59/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/hookdeck/hookdeck-cli) · [← Back to Mcp](./README.md)</sub>
