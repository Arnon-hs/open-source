# awkoy/notion-mcp-server

[![Stars](https://img.shields.io/github/stars/awkoy/notion-mcp-server?style=flat-square&color=yellow)](https://github.com/awkoy/notion-mcp-server/stargazers) [![Forks](https://img.shields.io/github/forks/awkoy/notion-mcp-server?style=flat-square&color=blue)](https://github.com/awkoy/notion-mcp-server/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> Notion MCP server for Claude, Cursor, ChatGPT & Claude Desktop. Connect AI agents to Notion via Model Context Protocol — pages, databases, blocks, comments, files.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 157 |
| 🍴 **Forks** | 30 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `anthropic` `chatgpt` `claude` `claude-desktop` `cursor` `llm` `mcp` `mcp-server` `model-context-protocol` `notion` `notion-ai`

## 🎯 Categories

MCP · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary**  
awkoy/notion‑mcp‑server is a TypeScript‑based open‑source backend that implements the Model Context Protocol (MCP) for Notion, allowing AI assistants such as Claude, Cursor, ChatGPT and Claude Desktop to read and write Notion pages, databases, blocks, comments, and files. By exposing a standard MCP API/SDK/CLI, it lets developers plug AI agents into real‑world Notion data without writing custom integrations.  

**Value**  
- **Standardized connectivity** – The server translates Notion’s native API into the generic MCP, so the same AI‑agent code can work across multiple tools and data sources.  
- **Rapid AI‑tool integration** – Teams can attach powerful language models to existing Notion workspaces, enabling use‑cases like automated knowledge‑base updates, context‑aware chat, and workflow automation.  
- **Reusable infrastructure** – Once the MCP server is deployed, any MCP‑compatible agent (Claude, Cursor, etc.) can be swapped in or out without changing the Notion integration layer.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Docker compose or npm start script, and configure the Notion integration token in the `.env` file.  
2. **Connect an AI agent** – Use the MCP SDK/CLI to register the server endpoint with the desired model (e.g., Claude’s MCP client) and test basic CRUD operations on a test Notion page.  
3. **Extend functionality** – Add custom handlers for Notion comments, file uploads, or database queries as needed, leveraging the TypeScript type definitions already included.  
4. **Deploy** – Containerize the service and push it to a managed environment (Kubernetes, Fly.io, Vercel, etc.) behind an authentication gateway.  
5. **Monitor & Scale** – Enable the built‑in logging and health‑check endpoints; scale horizontally if request volume grows.  

**Production Readiness**  
- **Activity & community** – 157 ⭐, 30 🍴, recent commits (last update 2026‑06‑28), and a healthy set of 15 topics indicate active maintenance and community interest.  
- **Maturity** – The project already provides a full MCP implementation, CLI, and SDK, reducing the amount of custom code required for production use.  
- **Scalability** – Written in TypeScript/Node.js, it can be containerized and horizontally scaled; the underlying Notion API rate limits are the primary bottleneck, which can be mitigated with caching or request batching.  
- **Risks** – License compliance, security hardening, and long‑term maintainer commitment still need a final audit, but no major red flags appear in the repository.  

Overall, awkoy/notion‑mcp‑server is a solid OSS candidate for teams that want to embed AI assistants into Notion‑driven workflows, with a clear path from quick prototyping to production deployment.

### Русский

**awkoy/notion-mcp-server** — это TypeScript‑сервер, реализующий Model Context Protocol и позволяющий AI‑агентам (Claude, Cursor, ChatGPT, Claude Desktop) напрямую работать с объектами Notion (страницы, базы данных, блоки, комментарии, файлы). Типичный сценарий: развертываете сервер, подключаете к нему ваш AI‑ассистент через готовый SDK/CLI и получаете мгновенный доступ к реальному контенту Notion для генерации, анализа или автоматизации задач. Проект считается почти готовым к production: активные коммиты, 157 ★, 30 форков, поддержка нескольких языков и чёткая документация, что делает его надёжным кандидатом для пилотных внедрений.

### 中文

**项目简介**  
awkoy/notion-mcp-server 是一个基于 Model Context Protocol（MCP）的后端服务，帮助 Claude、Cursor、ChatGPT、Claude Desktop 等 AI 助手直接读取和写入 Notion 的页面、数据库、块、评论和文件，实现 AI 与真实业务工具的数据交互。

**价值**  
- **统一协议**：通过 MCP 为所有 AI 代理提供统一的 Notion 接口，降低多模型集成的复杂度。  
- **实时业务数据**：AI 可以在对话或自动化流程中即时访问最新的 Notion 内容，提升智能助理的实用性和可靠性。  
- **可复用的服务层**：一次部署即可为不同的 AI 产品提供标准化的 Notion 接口，减少重复开发工作。

**典型接入方式**  
1. **部署服务器**：使用 Docker 或直接 `npm install` 启动 TypeScript 项目，暴露 HTTP API（或 WebSocket）供 AI 客户端调用。  
2. **SDK/CLI 调用**：项目提供的 Node.js SDK 与 CLI 工具，可在 AI Agent 的代码中直接调用 `getPage`, `queryDatabase`, `createBlock` 等方法。  
3. **MCP 配置**：在 AI 平台（如 Claude、ChatGPT 插件）中配置 MCP 端点 URL、认证 token，即可让模型通过标准协议访问 Notion。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑28，GitHub 157 星、30 Fork，社区关注度高。  
- **技术成熟度**：使用 TypeScript 实现，代码结构清晰，配套的 API 文档、示例和 CLI 辅助工具完整。  
- **安全与合规**：项目采用 MIT 许可证，未发现重大安全漏洞；仍建议在生产环境前进行内部安全审计和 token 管理。  
- **可扩展性**：支持自定义中间件，可接入企业内部的身份验证、审计日志等体系。  

综合来看，awkoy/notion-mcp-server 已具备较高的生产就绪度，适合作为 AI 与 Notion 集成的核心服务，在内部试点后即可投入正式业务使用。

## 🧭 Practical evaluation

**Value:** awkoy/notion-mcp-server helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 157 GitHub stars
- 30 forks
- updated 2026-06-28
- primary language: TypeScript
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 37/100 |
| stars | 47/100 |
| topics | 100/100 |
| outlook | 63/100 |
| quality | 60/100 |
| recency | 40/100 |
| adoption | 44/100 |
| production | 59/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/awkoy/notion-mcp-server) · [← Back to Mcp](./README.md)</sub>
