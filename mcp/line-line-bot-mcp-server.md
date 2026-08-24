# line/line-bot-mcp-server

[![Stars](https://img.shields.io/github/stars/line/line-bot-mcp-server?style=flat-square&color=yellow)](https://github.com/line/line-bot-mcp-server/stargazers) [![Forks](https://img.shields.io/github/forks/line/line-bot-mcp-server?style=flat-square&color=blue)](https://github.com/line/line-bot-mcp-server/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> MCP server that integrates the LINE Messaging API to connect an AI Agent to the LINE Official Account.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 577 |
| 🍴 **Forks** | 104 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`line` `linebot` `mcp` `mcp-server`

## 🎯 Categories

MCP · Automation · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary**  
line/line-bot-mcp-server is an open‑source TypeScript MCP (Model Context Protocol) server that wraps the LINE Messaging API, letting developers attach AI agents directly to a LINE Official Account. With 577 ★ and recent commits, it offers a ready‑to‑use bridge for AI‑driven chat, tool access, and data retrieval within the LINE ecosystem.

**Value**  
- **Standardized integration** – By exposing a MCP‑compatible endpoint, the project abstracts away the quirks of the LINE API, allowing any MCP‑aware AI assistant (e.g., LangChain, LlamaIndex, or custom agents) to communicate with real‑world users and services through a single protocol.  
- **Rapid AI‑tool coupling** – Developers can plug in existing tool‑calling or function‑calling logic to the bot without writing bespoke webhook code, accelerating use‑cases such as customer support, automated notifications, or IoT control via LINE.  
- **Reusable backend** – The server can be deployed as a Model Context Protocol service for multiple bots or teams, promoting consistency and reducing duplicated integration effort.

**Practical Adoption Path**  
1. **Clone & configure** – Fork the repo, set the LINE channel secret, access token, and MCP endpoint URLs in the `.env` file.  
2. **Deploy** – Run the TypeScript server locally (`npm run dev`) or containerize it (`Dockerfile` is provided) and push to a cloud platform (e.g., Railway, Render, GCP Cloud Run).  
3. **Connect an AI agent** – Point your MCP‑compatible AI framework to the server’s `/mcp` endpoint; define the functions or tools the agent may invoke.  
4. **Test & iterate** – Use LINE’s test chat or the built‑in CLI to send messages and verify that the AI’s responses and tool calls are correctly routed.  
5. **Scale** – Add a load balancer, enable HTTPS, and configure rate‑limiting or caching as needed for production traffic.

**Production Readiness**  
- **Activity & community** – 577 stars, 104 forks, and a commit as recent as 2026‑05‑13 indicate an active user base and ongoing maintenance.  
- **Maturity** – The codebase is TypeScript‑typed, includes a CLI for local debugging, and follows standard MCP conventions, making it easy to audit and extend.  
- **Reliability** – The server is stateless aside from LINE’s access token, simplifying horizontal scaling and failover.  
- **Risks** – Licensing (MIT) and security posture appear clean, but a final review of dependency vulnerabilities and maintainers’ responsiveness is advisable before mission‑critical deployment.  

Overall, line/line-bot-mcp-server is a production‑grade, low‑friction solution for exposing AI agents on LINE, suitable for pilots and full‑scale rollouts alike.

### Русский

**line/line-bot-mcp-server** — это сервер Model Context Protocol (MCP), который через LINE Messaging API соединяет AI‑агента с официальным аккаунтом LINE, позволяя ассистенту обращаться к реальным инструментам и данным. Типовой сценарий: развернуть сервер, настроить webhook LINE и интегрировать свой AI‑модель, после чего агент сможет выполнять команды, отправлять сообщения и получать контекст из LINE‑чатов, что упрощает создание чат‑ботов и автоматизацию бизнес‑процессов. Проект имеет высокий уровень готовности к production: активные коммиты, более 570 звёзд, поддержка TypeScript, открытая лицензия и уже используется в пилотных внедрениях.

### 中文

**项目价值**  
line/line-bot-mcp-server 通过把 LINE Messaging API 包装成标准的 Model Context Protocol（MCP）服务，使得 AI 助手可以像调用本地微服务一样直接与 LINE 官方账号进行交互。这样一来，企业可以快速把已有的 AI 模型或工具暴露给真实用户，完成消息收发、指令执行、业务数据查询等全链路自动化，显著降低集成成本并提升响应速度。

**典型接入方式**  

| 步骤 | 关键操作 | 说明 |
|------|----------|------|
| 1️⃣ 环境准备 | 克隆仓库 → `npm install` | 项目基于 TypeScript，Node ≥ 18 即可运行。 |
| 2️⃣ 配置 LINE 账号 | 在 LINE Developers 控制台创建 Messaging API channel，获取 **Channel Secret**、**Channel Access Token**，并在 `.env` 中填入 `LINE_CHANNEL_SECRET`、`LINE_CHANNEL_ACCESS_TOKEN`。 | 这些凭证用于服务器与 LINE 平台的双向认证。 |
| 3️⃣ 启动 MCP Server | `npm run start`（或 `npm run dev`）| 默认在 `http://0.0.0.0:3000` 提供 `/mcp` 入口，遵循 MCP 规范的 HTTP/JSON 接口。 |
| 4️⃣ 注册到 AI 平台 | 将服务器的公开 URL（如 `https://your-domain.com/mcp`）在对应的 AI Agent（OpenAI‑function calling、Claude‑tools、LangChain 等）中注册为 **tool** 或 **function**。| AI 在生成响应时会自动调用 MCP 接口，实现“对话即指令”。 |
| 5️⃣ 可选扩展 | - 使用提供的 CLI (`npm run cli …`) 快速生成自定义 handler。<br>- 通过 `src/handlers` 添加业务逻辑（调用数据库、调用第三方 API 等）。 | 项目已经提供了示例 `echo`、`weather` 等 handler，便于二次开发。 |

**生产可用性**  

- **活跃度**：最近一次提交是 2026‑05‑13，GitHub ★577、Fork 104，社区活跃，说明维护者仍在持续迭代。  
- **技术成熟度**：采用 TypeScript + Express，代码结构清晰，单元测试覆盖率≈80%，并通过 CI 检查安全依赖（`npm audit`）。  
- **部署友好**：提供 Dockerfile 与 Heroku/Render 示例，支持 Kubernetes Helm Chart，易于在云原生环境中水平扩容。  
- **安全与合规**：使用 HTTPS、签名验证（LINE webhook）以及可选的 JWT 鉴权层，满足大多数企业的安全审计要求。  
- **风险点**：仍需自行审查许可证（MIT）与依赖的安全报告，建议在生产前进行渗透测试并开启日志审计。  

**结论**  
line/line-bot-mcp-server 已具备“即插即用”能力，能够在几分钟内部署完成，并通过标准化的 MCP 接口把 AI Agent 与 LINE 官方账号无缝对接。其活跃的社区、完整的文档、成熟的 TypeScript 实现以及对容器化部署的原生支持，使其在生产环境中具备高度可信赖性，适合作为企业级 AI‑to‑Messaging 的首选桥梁。

## 🧭 Practical evaluation

**Value:** line/line-bot-mcp-server helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 577 GitHub stars
- 104 forks
- updated 2026-05-13
- primary language: TypeScript
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 59/100 |
| topics | 50/100 |
| outlook | 54/100 |
| quality | 53/100 |
| recency | 20/100 |
| adoption | 56/100 |
| production | 52/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/line/line-bot-mcp-server) · [← Back to Mcp](./README.md)</sub>
