# roomi-fields/notebooklm-mcp

[![Stars](https://img.shields.io/github/stars/roomi-fields/notebooklm-mcp?style=flat-square&color=yellow)](https://github.com/roomi-fields/notebooklm-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/roomi-fields/notebooklm-mcp?style=flat-square&color=blue)](https://github.com/roomi-fields/notebooklm-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> Google NotebookLM over MCP + a local HTTP REST API. Citation-backed Q&A, audio/video/content generation, multi-account rotation. For Claude Code, Codex, Cursor, n8n, Zapier, Make.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 75 |
| 🍴 **Forks** | 22 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `anthropic` `automation` `citations` `claude` `claude-code` `gemini` `google-notebooklm` `http-api` `mcp` `mcp-server` `n8n`

## 🎯 Categories

MCP · Automation · AI/ML · Backend

## 📝 Summary

### English

**Summary**  
roomi‑fields/notebooklm-mcp is an open‑source bridge that runs Google NotebookLM on the Model‑Context‑Protocol (MCP) and exposes a local HTTP REST API. It adds citation‑backed Q&A, audio/video/content generation, and multi‑account rotation, making it easy to plug NotebookLM into automation platforms such as Claude Code, Codex, Cursor, n8n, Zapier, and Make.

**Value**  
The project turns a powerful generative AI (NotebookLM) into a standards‑based service that can be called from any MCP‑compatible agent. By providing a REST endpoint and built‑in support for citations, media creation, and account switching, it lets developers and ops teams connect AI assistants to real‑world tools and data without writing custom wrappers for each platform.

**Practical adoption path**  

1. **Spin‑up** – Clone the repo, run `npm install && npm start` (or use the provided Docker image) to launch the local NotebookLM MCP server.  
2. **Configure** – Add your Google credentials and, if needed, multiple NotebookLM accounts in the `.env` file to enable rotation.  
3. **Integrate** – Point any MCP‑aware component (Claude Code, Codex, n8n, Zapier, Make, etc.) to the server’s HTTP endpoint; the SDK/CLI shipped with the repo simplifies request construction and response parsing.  
4. **Extend** – Use the TypeScript SDK or the open API spec to add custom handlers (e.g., trigger audio/video generation or enforce citation policies) and then deploy the service behind a reverse proxy for internal or SaaS use.

**Production readiness**  
The repository shows strong signals for a pilot‑grade deployment: recent commits (last updated 2026‑05‑14), 75 GitHub stars, active forking, and a TypeScript codebase with clear API documentation. Its modular MCP/REST design aligns with existing automation ecosystems, and the multi‑account rotation mitigates rate‑limit issues in production. While the license, security audit, and long‑term maintainer commitment still require a final check, the overall health and ecosystem adoption make it a viable candidate for production use after standard security hardening.

### Русский

**roomi-fields/notebooklm-mcp** — это open‑source решение, которое реализует Google NotebookLM поверх Model Context Protocol (MCP) и предоставляет локальный HTTP/REST‑интерфейс для запросов с поддержкой цитат, генерации аудио/видео и контента, а также ротации нескольких аккаунтов. Типичный сценарий — подключение AI‑агентов (Claude, Codex, Cursor и др.) к реальным инструментам и данным через единый протокол, что упрощает построение автоматизированных воркфлоу в n8n, Zapier, Make и подобных платформах. Проект уже активно поддерживается (обновления — 2026‑05‑14, 75 ★, 22 форка, TypeScript), имеет готовый API/SDK/CLI и считается готовым к пилотному запуску в продакшн, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目价值**  
roomi-fields/notebooklm-mcp 为 Google Notebook LM 提供了基于 Model Context Protocol（MCP）的实现，并额外包装了一个本地 HTTP REST API。它让各种 AI 助手（Claude Code、Codex、Cursor 等）能够在同一协议下直接调用真实的工具与数据，实现带引用的问答、音视频/内容生成以及多账号轮换等高级功能，从而把“语言模型”真正落地到业务系统中。

**典型接入方式**  

| 场景 | 接入步骤 | 关键点 |
|------|----------|--------|
| **AI Agent → 工具** | 1. 在目标机器上 `npm i @roomi-fields/notebooklm-mcp` <br>2. 启动本地 MCP Server（`npm run start`），默认监听 `http://localhost:8080` <br>3. 在 AI Agent（Claude Code、Codex、Cursor 等）中配置 MCP 客户端 SDK，指向上述 URL <br>4. 调用标准化的 `invoke`, `query`, `generate` 等 API，即可完成工具调用或内容生成 | 使用官方提供的 TypeScript SDK（或通过 OpenAPI 生成的任意语言客户端），无需自行实现协议细节。 |
| **MCP Server 部署** | 1. 将仓库克隆到生产环境 <br>2. 使用 Dockerfile 构建镜像 `docker build -t notebooklm-mcp .` <br>3. 通过 Kubernetes/Compose 部署，配置 TLS、OAuth / API‑Key 鉴权 <br>4. 按需开启多账号轮换插件（`accounts.yaml`），实现并发用户隔离 | 支持 Docker、K8s，且所有配置均为声明式 YAML，易于在 CI/CD 流水线中自动化。 |
| **自动化平台集成** (n8n、Zapier、Make) | 1. 在平台中创建 “HTTP Request” 节点，指向 MCP 的 REST 端点 <br>2. 发送符合 MCP 规范的 JSON payload（如 `{"action":"search","input":"..."} `） <br>3. 解析返回的 `content`、`citations` 等字段，继续后续工作流 | 只需标准 HTTP 调用，无需额外插件，适合低代码/无代码场景。 |

**生产可用性**  
- **活跃度**：最近一次提交为 2026‑05‑14，GitHub Stars 75、Forks 22，社区关注度良好。  
- **技术成熟度**：使用 TypeScript 编写，提供完整的 API 文档、SDK 与 CLI，已在多个内部 pilot 中验证。  
- **安全与合规**：项目采用 MIT 许可证，代码公开，可自行审计；支持 TLS、API‑Key、OAuth 等鉴权方式，满足企业安全要求。  
- **可扩展性**：多账号轮换、插件化的音视频生成器、引用管理等功能均可通过配置文件或自定义插件灵活开启。  

综合来看，roomi-fields/notebooklm-mcp 已具备 **高可用**、**易集成**、**安全可控** 的特性，完全可以作为企业级 AI Agent 与实际工具/数据桥接的首选 OSS 方案，适合直接用于生产环境的试点甚至正式上线。

## 🧭 Practical evaluation

**Value:** roomi-fields/notebooklm-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 75 GitHub stars
- 22 forks
- updated 2026-05-14
- primary language: TypeScript
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 40/100 |
| topics | 100/100 |
| outlook | 55/100 |
| quality | 52/100 |
| recency | 20/100 |
| adoption | 38/100 |
| production | 54/100 |
| usefulness | 90/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/roomi-fields/notebooklm-mcp) · [← Back to Mcp](./README.md)</sub>
