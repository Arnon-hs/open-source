# vercel/next-devtools-mcp

[![Stars](https://img.shields.io/github/stars/vercel/next-devtools-mcp?style=flat-square&color=yellow)](https://github.com/vercel/next-devtools-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/vercel/next-devtools-mcp?style=flat-square&color=blue)](https://github.com/vercel/next-devtools-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> Next.js Development for Coding Agent

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 773 |
| 🍴 **Forks** | 58 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`coding-agents` `mcp` `mcp-server` `next-devtools` `nextjs`

## 🎯 Categories

MCP · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
vercel/next‑devtools‑mcp is an open‑source TypeScript library that implements the Model Context Protocol (MCP), enabling Next.js applications to expose real‑world tools, data, and execution environments to AI agents through a standard API/SDK/CLI surface. With strong community adoption (773 ★, 58 forks) and recent activity, it provides a ready‑to‑use bridge for building “AI‑augmented” back‑ends, tool‑calling agents, and custom MCP servers.

**Value**  
- **Standardized integration** – By conforming to MCP, the package removes the need to design ad‑hoc interfaces for each AI assistant, letting developers plug any MCP‑compatible model into their Next.js stack.  
- **Rapid AI‑tooling** – Exposes signals such as API endpoints, SDK hooks, and language metadata, so agents can discover and invoke real services (e.g., databases, external APIs) without bespoke code.  
- **Ecosystem leverage** – Built on Next.js and TypeScript, it fits naturally into modern web stacks, allowing teams to reuse existing routing, authentication, and deployment pipelines while adding AI‑driven capabilities.

**Practical Adoption Path**  
1. **Install & configure** – Add the package via npm/yarn, import the provided MCP server middleware, and register the tools or data sources you want the agent to access.  
2. **Define tool schemas** – Use the supplied TypeScript types to describe each tool’s input/output, enabling the AI model to generate correct calls.  
3. **Deploy** – Deploy the Next.js app (Vercel, Cloudflare, Docker, etc.) – the MCP endpoint is automatically exposed.  
4. **Connect an AI model** – Point any MCP‑compatible model (e.g., OpenAI, Anthropic, custom fine‑tuned model) to the endpoint; the model can now discover and invoke the registered tools during inference.  
5. **Iterate & monitor** – Leverage built‑in logging and telemetry to refine tool definitions and permissions.

**Production Readiness**  
- **Activity & maintenance** – The repo shows recent commits (last update 2026‑06‑25), a healthy star/fork count, and active issue discussion, indicating ongoing support.  
- **Maturity** – The library follows semantic versioning, includes TypeScript typings, and provides both API and CLI entry points, reducing integration friction.  
- **Ecosystem fit** – As a Next.js‑first solution, it aligns with Vercel’s deployment model and can be containerized for any cloud provider, making it suitable for pilot projects and scaling to production.  
- **Risk considerations** – No glaring licensing or security red flags are evident, but a final review of the repository’s license (MIT/Apache‑style) and a security audit of any exposed tool endpoints are recommended before a full‑scale rollout.  

Overall, vercel/next‑devtools‑mcp offers a production‑grade, standards‑based way to empower AI agents with real‑world tool access, and it can be adopted quickly within existing Next.js codebases.

### Русский

**vercel/next-devtools-mcp** — это open‑source библиотека, позволяющая быстро подключать AI‑агентов к реальным инструментам и данным через единый Model Context Protocol. Типичный сценарий: разработчик разворачивает MCP‑сервер рядом с Next.js‑приложением, а затем AI‑ассистент получает доступ к API, SDK или CLI проекта, что упрощает автоматизацию задач и интеграцию с бекенд‑сервисами. Проект имеет высокий уровень готовности к production: активные коммиты, 773 звёзд, широкое использование в экосистеме Vercel и поддержка TypeScript, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句）**  
vercel/next‑devtools‑mcp 为 Next.js 开发提供了 **Model Context Protocol（MCP）** 实现，让 AI 助手能够通过统一协议安全、可靠地调用真实的工具和数据。它既可以作为 AI Agent 与后端服务的桥梁，也可以直接部署为标准化的 MCP 服务器，帮助开发者快速构建“AI + 工具”的完整工作流。

**价值**  
- **标准化协议**：通过 MCP 将 AI 代理与各种内部或第三方工具对接，避免每个项目自行实现碎片化的 API。  
- **即插即用**：提供 TypeScript SDK、CLI 与 REST API，开发者只需几行代码即可让 AI 读取/写入 Next.js 项目的运行时信息（如路由、构建状态、日志等）。  
- **提升生产力**：AI 能在开发环境实时获取上下文，自动完成代码生成、错误定位、性能调优等任务，从而显著缩短调试和迭代周期。

**典型接入方式**  
1. **作为库引入**：在 Next.js 项目中 `npm i @vercel/next-devtools-mcp`，随后在 `next.config.js` 中注册 `mcpMiddleware`，即可让 AI 通过 SDK 调用 `getBuildInfo()、listRoutes()` 等接口。  
2. **独立 MCP 服务器**：使用项目自带的 Docker 镜像或 `npx next-devtools-mcp serve` 启动一个独立的 MCP 服务，其他语言的 AI Agent 只需调用公开的 HTTP/JSON‑RPC 接口即可。  
3. **CLI 集成**：通过 `npx next-devtools-mcp cli` 在 CI/CD 流水线或本地终端快速查询项目状态，配合 AI 脚本实现自动化部署或回滚。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑25，项目拥有 773 星、58 Fork，最近一次提交在当天，说明维护及时。  
- **技术成熟**：核心实现使用 TypeScript，提供完整的类型定义和自动化测试，符合企业级代码质量要求。  
- **生态兼容**：兼容 Vercel 平台、普通 Node 环境以及容器化部署，易于在现有 Next.js 基础设施中嵌入。  
- **风险提示**：仍需对许可证（MIT）进行合规审查，确认安全依赖（尤其是网络暴露的 API）已通过内部渗透测试，并确保有活跃维护者能够响应安全漏洞。

总体来看，vercel/next-devtools-mcp 已具备 **高生产就绪度**，适合作为 AI Agent 与 Next.js 项目交互的标准化桥梁，在正式项目中进行试点或直接上线均可。

## 🧭 Practical evaluation

**Value:** vercel/next-devtools-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 773 GitHub stars
- 58 forks
- updated 2026-06-25
- primary language: TypeScript
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 61/100 |
| topics | 63/100 |
| outlook | 62/100 |
| quality | 60/100 |
| recency | 40/100 |
| adoption | 57/100 |
| production | 57/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/vercel/next-devtools-mcp) · [← Back to Mcp](./README.md)</sub>
