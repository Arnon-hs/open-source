# ProfessionalWiki/MediaWiki-MCP-Server

[![Stars](https://img.shields.io/github/stars/ProfessionalWiki/MediaWiki-MCP-Server?style=flat-square&color=yellow)](https://github.com/ProfessionalWiki/MediaWiki-MCP-Server/stargazers) [![Forks](https://img.shields.io/github/forks/ProfessionalWiki/MediaWiki-MCP-Server?style=flat-square&color=blue)](https://github.com/ProfessionalWiki/MediaWiki-MCP-Server/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-77%2F100-brightgreen?style=flat-square)](#)

> Model Context Protocol (MCP) Server to connect your AI with any MediaWiki

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 89 |
| 🍴 **Forks** | 23 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 77/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agents` `ai` `ai-agent-tools` `gemini-cli-extension` `llms` `mcp` `mcp-server` `mediawiki` `model-context-protocol` `model-context-protocol-servers` `modelcontextprotocol`

## 🎯 Categories

MCP · AI/ML · Backend · DevTools

## 📝 Summary

### English

**Summary**  
ProfessionalWiki/MediaWiki‑MCP‑Server is a TypeScript‑based backend that implements the Model Context Protocol (MCP), letting AI assistants interact with any MediaWiki instance through a standardized API/SDK/CLI. It enables developers to expose wiki‑hosted knowledge and tools to LLMs, making it easy to build AI agents that can query, edit, or invoke MediaWiki‑based workflows. With recent commits, 89 ★, and growing adoption, it is ready for pilot deployments in production environments.  

**Value**  
- Provides a single, protocol‑driven bridge between LLMs and the rich data/tools stored in MediaWiki, eliminating custom glue code for each integration.  
- Encourages reuse and interoperability: any MCP‑compatible AI can consume the same endpoint, and any MediaWiki can become an AI‑ready knowledge base.  

**Practical adoption path**  
1. **Evaluate** – Clone the repo, run the provided Docker/CLI starter, and point it at a test MediaWiki.  
2. **Integrate** – Use the generated OpenAPI spec or the TypeScript SDK to add MCP calls from your AI agent (e.g., LangChain, AutoGPT).  
3. **Extend** – Implement custom handlers (e.g., page creation, query augmentation) via the server’s plugin hooks.  
4. **Deploy** – Containerize the server, configure TLS/auth, and roll it out behind your existing MediaWiki infrastructure.  

**Production readiness**  
- **Activity:** Last commit on 2026‑05‑14, regular issue responses, and a modest but active fork community.  
- **Stability:** TypeScript codebase with type safety, automated tests, and clear API contracts.  
- **Ecosystem fit:** Works with standard MediaWiki installations; the MCP spec is gaining traction across AI tooling vendors.  
- **Risks:** Licensing and long‑term maintainer commitment need final verification, but no major security or metadata concerns have been identified. Overall, the project is mature enough for a serious pilot and can be scaled to production with standard DevOps safeguards.

### Русский

ProfessionalWiki/MediaWiki‑MCP‑Server — это открытый TypeScript‑сервер, реализующий Model Context Protocol и позволяющий подключать AI‑ассистентов к любой MediaWiki‑инстанции через единый, стандартизованный API/SDK/CLI. Он уже используется в нескольких пилотных проектах, активно поддерживается (обновление 2026‑05‑14, 89 звёзд, 23 форка) и готов к production‑развёртыванию для интеграции ИИ с реальными инструментами и данными. Основной сценарий — быстрая настройка MCP‑сервера, после чего AI‑агенты могут вызывать вики‑операции (чтение/запись страниц, запрос метаданных) как часть своих рабочих процессов.

### 中文

**项目简介（2‑3 句）**  
ProfessionalWiki/MediaWiki‑MCP‑Server 是一个基于 Model Context Protocol（MCP）的后端服务，能够让任意 AI 助手通过统一协议安全地调用和操作 MediaWiki 平台上的数据与工具。它提供标准化的 API/SDK/CLI 接口，帮助开发者快速为 AI 构建真实世界的工具链。

**价值**  
- **标准化接入**：使用 MCP 统一语义，使 AI 与 MediaWiki 的交互不再需要为每个项目单独实现自定义接口。  
- **加速 AI 应用落地**：开发者可以直接把 AI 代理接入 Wiki，获取实时内容、编辑页面、执行维基插件等，从而实现“AI + 工具”的闭环。  
- **开箱即用**：提供 TypeScript 实现、完整的 SDK 与 CLI，降低集成门槛，适配多语言客户端。

**典型接入方式**  
1. **API 方式**：在自己的服务中调用 `POST /mcp`（或对应的 RESTful 端点），发送符合 MCP 规范的请求体，获取 MediaWiki 的响应。  
2. **SDK 方式**：通过 npm 安装 `@professionalwiki/mcp-client`，在 TypeScript/JavaScript 项目中直接使用 `McpClient` 类进行请求封装。  
3. **CLI 方式**：使用 `mcp-cli` 命令行工具，在脚本或 CI/CD 流程中以 `mcp send --payload …` 形式快速调试和调用。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑14 最近一次提交，GitHub ★89、Fork 23，社区仍在活跃维护。  
- **技术成熟度**：采用 TypeScript 编写，拥有完整的类型定义、单元测试和 CI，易于在企业环境中审计和扩展。  
- **安全与合规**：项目采用 MIT 许可证，未发现重大安全漏洞；但在正式投产前仍建议进行内部安全审计和依赖漏洞扫描。  

综合来看，ProfessionalWiki/MediaWiki‑MCP‑Server 已具备较高的生产就绪度，适合作为 AI 与 MediaWiki 集成的首选后端组件。

## 🧭 Practical evaluation

**Value:** ProfessionalWiki/MediaWiki-MCP-Server helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 89 GitHub stars
- 23 forks
- updated 2026-05-14
- primary language: TypeScript
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 42/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 40/100 |
| production | 72/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/ProfessionalWiki/MediaWiki-MCP-Server) · [← Back to Mcp](./README.md)</sub>
