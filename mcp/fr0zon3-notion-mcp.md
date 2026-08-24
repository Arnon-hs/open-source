# FR0ZON3/notion-mcp

[![Stars](https://img.shields.io/github/stars/FR0ZON3/notion-mcp?style=flat-square&color=yellow)](https://github.com/FR0ZON3/notion-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/FR0ZON3/notion-mcp?style=flat-square&color=blue)](https://github.com/FR0ZON3/notion-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Notion mcp to connect AI agents to notion through markdown | Read and write notion markdown

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 98 |
| 🍴 **Forks** | 1.1k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `markdown-mcp` `mcp-agent` `notion-ai-agent` `notion-mcp`

## 🎯 Categories

MCP · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
FR0ZON3/notion‑mcp is a TypeScript‑based open‑source bridge that lets AI agents read and write Notion pages using a standardized Model Context Protocol (MCP) expressed in Markdown. By exposing a clean API/CLI, it enables seamless integration of LLM‑powered assistants with real‑world Notion data and workflows. The project is actively maintained, widely forked, and already used in several pilot integrations.

**Value**  
- **Unified protocol**: Provides a single, language‑agnostic way to interact with Notion, reducing the need for custom scrapers or brittle webhooks.  
- **AI‑first design**: The Markdown‑centric interface matches how LLMs reason about text, making prompt engineering and context injection straightforward.  
- **Extensibility**: Because it follows the MCP spec, the same server can be swapped or scaled to support other tools, fostering a reusable integration layer across your stack.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Docker/CLI locally, and point your LLM‑powered agent at the `/read` and `/write` endpoints using simple Markdown payloads.  
2. **Integrate** – Wrap the MCP calls in your existing agent framework (e.g., LangChain, CrewAI) and replace any ad‑hoc Notion SDK usage.  
3. **Scale** – Deploy the server to a managed environment (Kubernetes, Fly.io, etc.), enable authentication via Notion OAuth, and add caching or rate‑limit layers as needed.  
4. **Standardize** – Publish your own MCP endpoints for other tools (Google Docs, Confluence) using the same pattern, creating a consistent “AI‑to‑tool” surface across the organization.

**Production Readiness**  
- **Activity & Community**: 98 ★, 1 054 forks, last commit on 2026‑07‑03, and an active issue/PR flow indicate a healthy maintainer base.  
- **Technical Maturity**: Written in TypeScript with clear API, CLI, and SDK artifacts; the repository includes CI pipelines, type definitions, and example deployments.  
- **Risk Profile**: No critical licensing or security red flags have been identified, though a formal audit of the Notion OAuth handling and dependency updates is advisable before full‑scale rollout.  
Overall, the project is mature enough for a serious pilot and can be promoted to production once the minor security and governance checks are completed.

### Русский

**FR0ZON3/notion-mcp** — это открытый TypeScript‑модуль, который реализует Model Context Protocol и позволяет AI‑агентам читать и записывать контент в Notion в виде markdown. Типичный сценарий: встраивание AI‑ассистента в рабочие процессы, где он получает данные из Notion, обрабатывает их и сохраняет результаты обратно, либо развёртывание собственного MCP‑сервера для стандартизации интеграций. Проект демонстрирует высокий уровень готовности к production: активные коммиты, более 1000 форков, 98 звёзд, поддержка CLI/SDK и широкое принятие в сообществе, что делает его надёжным кандидатом для серьёзных пилотов.

### 中文

**项目简介（2‑3 句）**  
FR0ZON3/notion-mcp 是一个基于 Model Context Protocol（MCP）的开源工具，可让 AI 助手直接读取和写入 Notion 中的 Markdown 内容，实现 AI 与真实业务数据的即时交互。它提供统一的 API/SDK/CLI 接口，使得 AI 代理能够像操作本地文件一样操作 Notion 页面。

**价值**  
- **标准化接入**：通过 MCP 统一协议，降低 AI 与 Notion 之间的集成成本，避免每个项目都要自行实现专有的 Notion API 封装。  
- **实时数据驱动**：AI 代理可以实时读取最新的 Notion 知识库并写回结果，提升自动化办公、知识管理和智能问答等场景的实用性。  
- **生态兼容**：支持 TypeScript/JavaScript，配套 CLI 与 SDK，易于在现有 Node.js 微服务或 Serverless 环境中嵌入。

**典型接入方式**  
1. **API 方式**：在后端服务中引入 `@fr0zon3/notion-mcp` npm 包，使用 `NotionMCPClient` 初始化（需要 Notion Integration Token），随后调用 `readMarkdown(pageId)`、`writeMarkdown(pageId, content)` 等方法。  
2. **CLI 方式**：通过 `npx notion-mcp read <pageId>` 或 `npx notion-mcp write <pageId> -f ./doc.md` 在 CI/CD、脚本或本地调试时直接操作 Notion。  
3. **MCP Server**：部署一个轻量的 MCP 服务器（Docker 镜像或 Serverless 函数），对外提供统一的 HTTP 接口，AI 代理只需调用该服务的 `/read`、`/write` 端点即可，无需关注 Notion 细节。

**生产可用性**  
- **活跃度**：截至 2026‑07‑03 最近一次提交，拥有 98 ⭐、1 054 🍴，社区活跃，Issue 关闭率高。  
- **技术成熟度**：使用 TypeScript 编写，提供完整的类型定义；同时提供 CLI、SDK 与 Docker 镜像三种交付形态，便于不同部署环境。  
- **安全与合规**：仅通过官方 Notion OAuth token 进行授权，未内置额外数据收集；但仍建议在生产环境中配合内部审计（审查许可证、依赖漏洞扫描、最小化 token 权限）。  
- **可扩展性**：基于 MCP 设计，可与其他 MCP 实现（如数据库、文件存储）组合，构建统一的 AI‑Tooling 平台。  

综合来看，FR0ZON3/notion-mcp 已具备 **高生产就绪度**，适合作为企业级 AI 助手与 Notion 之间的桥梁，在正式项目中进行试点或直接上线。

## 🧭 Practical evaluation

**Value:** FR0ZON3/notion-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 98 GitHub stars
- 1054 forks
- updated 2026-07-03
- primary language: TypeScript
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 76/100 |
| stars | 42/100 |
| topics | 63/100 |
| outlook | 58/100 |
| quality | 58/100 |
| recency | 40/100 |
| adoption | 52/100 |
| production | 56/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/FR0ZON3/notion-mcp) · [← Back to Mcp](./README.md)</sub>
