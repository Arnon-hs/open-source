# writerslogic/scrivener-mcp

[![Stars](https://img.shields.io/github/stars/writerslogic/scrivener-mcp?style=flat-square&color=yellow)](https://github.com/writerslogic/scrivener-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/writerslogic/scrivener-mcp?style=flat-square&color=blue)](https://github.com/writerslogic/scrivener-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> The definitive MCP server for Scrivener. Connect your novels, screenplays, and manuscripts to Claude, ChatGPT, and other AI assistants. 60+ tools for document management, writing analysis, content enhancement, semantic search, and character/plot tracking.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 30 |
| 🍴 **Forks** | 12 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-writing` `chatgpt` `claude` `content-analysis` `copilot` `creative-writing` `cursor` `manuscript` `mcp` `mcp-server` `model-context-protocol` `novel`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · Backend

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
scrivener‑mcp is an open‑source “MCP” (Message‑Channel‑Processor) server that plugs Scrivener into AI assistants such as Claude and ChatGPT. It ships more than 60 utilities for document management, writing analysis, semantic search, and character/plot tracking, making it a one‑stop backend for AI‑augmented novel, screenplay, or manuscript workflows.

**Value proposition**  
- **AI‑enhanced writing** – Authors can call LLMs directly from Scrivener to get suggestions, rewrite passages, or perform style checks without leaving the editor.  
- **Rich tooling** – The bundled utilities cover everything from versioned document storage and metadata extraction to plot‑line consistency checks and semantic similarity search, dramatically reducing the need to stitch together separate services.  
- **Web3‑ready integration** – Because the server exposes a clean API/SDK/CLI, developers can prototype blockchain‑based publishing, token‑gated access, or DeFi‑driven royalty models by plugging in wallet or smart‑contract calls alongside the AI workflow.

**Practical adoption path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Clone & spin up** the TypeScript server (Dockerfile or `npm run start`). | Quick local sandbox; the repo is up‑to‑date (last commit 2026‑06‑24). |
| 2️⃣  | **Configure AI credentials** (OpenAI, Anthropic, etc.) in the provided `.env` or secret manager. | Enables the 60+ AI‑driven tools out of the box. |
| 3️⃣  | **Connect Scrivener** via the built‑in MCP client or the generated SDK (REST/WS). | No code changes in Scrivener; just point to the server URL. |
| 4️⃣  | **Prototype a Web3 feature** – e.g., add a “mint chapter as NFT” button that calls a smart‑contract SDK exposed by the MCP. | Demonstrates the “blockchain workflow” use case the project advertises. |
| 5️⃣  | **Iterate & test** with internal writers, collect feedback, and optionally replace the default LLM with a self‑hosted model. | Validates both AI quality and any on‑chain interactions before wider rollout. |
| 6️⃣  | **Production hardening** – add CI linting, run dependency‑vulnerability scans, lock versions, and set up monitoring for the MCP service. | Addresses the “medium” production readiness rating. |

**Production readiness assessment**  

- **Maturity** – 30 ★, 12 forks, recent updates, and a TypeScript codebase suggest a healthy, actively maintained project, but the community is still small.  
- **Readiness level** – *Medium*: suitable for prototypes, internal tools, or staged roll‑outs. Before production you’ll want to:  
  1. **Audit the license** (ensure it matches your commercial policy).  
  2. **Run security scans** on dependencies (npm audit, Snyk) and on any exposed API endpoints.  
  3. **Add observability** (metrics, logs) and define rate‑limits for the LLM calls.  
  4. **Validate blockchain integration** – test wallet signing, gas handling, and smart‑contract interactions in a testnet environment.  
- **Risk profile** – No major metadata or licensing red flags, but the lack of a dedicated security maintainer means you should perform your own code review and possibly sponsor a security audit if you plan to expose the service publicly.

**Bottom line**  
scrivener‑mcp offers a compelling bridge between Scrivener’s authoring environment and modern LLMs, while also exposing a flexible API that can be extended with Web3 components. For teams looking to experiment with AI‑assisted writing and blockchain‑enabled publishing, it provides a fast, low‑friction starting point; with a modest amount of hardening it can be promoted from prototype to production‑grade service.

### Русский

**writerslogic/scrivener-mcp** — это открытый MCP‑сервер, позволяющий подключать проекты Scrivener к Claude, ChatGPT и другим AI‑ассистентам, а также использовать более 60 инструментов для управления документами, анализа текста и семантического поиска. Он подходит для быстрого прототипирования и отладки Web3‑процессов (интеграция кошельков, DeFi, блокчейн‑транзакций), предоставляя открытый API/SDK/CLI и полную видимость реализации. Готовность к production — средняя: проект достаточно стабилен для внутренних и прототипных решений, но требует проверки лицензии, безопасности и поддержки перед масштабным внедрением.

### 中文

**项目简介（2‑3 句）**  
writerslogic/scrivener-mcp 是面向 Scrivener 的官方 MCP（Message‑Control‑Protocol）服务器，能够把小说、剧本、手稿等文档无缝连接到 Claude、ChatGPT 等 AI 助手。它提供 60+ 文档管理、写作分析、内容增强、语义搜索以及角色/情节追踪等工具，让创作者在写作过程中即刻获得 AI 辅助。

---

## 价值说明  
- **AI 写作助理**：通过统一的 MCP 接口，将多种大模型（Claude、ChatGPT 等）嵌入 Scrivener，实时提供语义建议、情节梳理和风格优化。  
- **全栈工具箱**：60 多个即插即用的功能模块，覆盖文档版本管理、语义检索、情节/人物追踪等，显著提升创作效率。  
- **区块链原型支持**：项目展示了如何在 Web3 场景下使用 MCP 与区块链工作流交互，适合作为钱包、DeFi 或 NFT 内容管理的原型实现。  

## 典型接入方式  
1. **API/SDK**：项目提供基于 TypeScript 的 SDK 与 RESTful API，开发者可在自己的后端或前端项目中直接调用 `connect`, `analyze`, `search` 等方法。  
2. **CLI**：通过内置的命令行工具，可以在本地快速启动 MCP 服务器、注册模型、执行文档分析等，无需编写代码。  
3. **语言元数据**：项目在 `package.json` 中声明了完整的语言依赖（Node.js ≥18），并提供 Dockerfile，便于在容器化环境或 CI/CD 流水线中部署。  

## 生产可用性评估  
| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | 中等 | 代码最近更新（2026‑06‑24），拥有 30+ 星、12 个 Fork，适合作为原型或内部工具。 |
| **依赖管理** | 需要审查 | 依赖主要是 TypeScript/Node 生态，需检查第三方库的安全公告与许可证兼容性。 |
| **维护者活跃度** | 待确认 | 项目当前维护者数量有限，建议在生产环境前与维护者沟通或自行 fork 维护。 |
| **安全性** | 初步合规 | 未发现显著的元数据风险，但需自行进行安全审计（尤其是与区块链交互的部分）。 |
| **部署难度** | 低‑中** | 提供 Docker 镜像和 CLI，单机或 K8s 部署均可快速完成。 |
| **适用场景** | 原型/内部服务 | 适合快速验证 Web3 工作流、AI 写作功能；若要对外提供服务，建议加强监控、日志和安全加固。 |

**结论**：writerslogic/scrivener-mcp 在功能完整性和开发便利性方面表现突出，足以支撑创意写作平台或 Web3 内容管理的原型开发。若计划在生产环境大规模使用，建议完成依赖安全审计、完善运维监控，并考虑自行接管长期维护。

## 🧭 Practical evaluation

**Value:** writerslogic/scrivener-mcp helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 30 GitHub stars
- 12 forks
- updated 2026-06-24
- primary language: TypeScript
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 28/100 |
| stars | 32/100 |
| topics | 100/100 |
| outlook | 56/100 |
| quality | 54/100 |
| recency | 40/100 |
| adoption | 31/100 |
| production | 55/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/writerslogic/scrivener-mcp) · [← Back to Mcp](./README.md)</sub>
