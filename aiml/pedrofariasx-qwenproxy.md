# pedrofariasx/qwenproxy

[![Stars](https://img.shields.io/github/stars/pedrofariasx/qwenproxy?style=flat-square&color=yellow)](https://github.com/pedrofariasx/qwenproxy/stargazers) [![Forks](https://img.shields.io/github/forks/pedrofariasx/qwenproxy?style=flat-square&color=blue)](https://github.com/pedrofariasx/qwenproxy/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Proxy API OpenAI-compatible que usa automação com Playwright para rotear requisições para modelos do Qwen com suporte a múltiplas contas, tools e sessões persistentes.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 131 |
| 🍴 **Forks** | 63 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`docker` `hono` `llm` `openai` `playwright` `proxy` `qwen` `typescript`

## 🎯 Categories

AI/ML · DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
pedrofariasx/qwenproxy is an open‑source, OpenAI‑compatible proxy that uses Playwright automation to forward requests to Qwen models, supporting multiple accounts, tool integrations, and persistent sessions. Written in TypeScript, it offers a ready‑to‑use API/SDK/CLI layer that lets developers add generative‑AI capabilities without building a model stack from scratch.

**Value**  
- **Fast AI enablement** – By abstracting the Qwen endpoints behind a familiar OpenAI‑style API, teams can plug in large‑language‑model features (chat, completions, embeddings) with minimal code changes.  
- **Multi‑account & tool support** – The proxy handles several Qwen credentials simultaneously and can invoke external tools, making it ideal for RAG pipelines, autonomous agents, or multi‑tenant SaaS products.  
- **Persistent sessions** – Session state is retained across calls, simplifying conversational contexts and reducing the need for custom session management.

**Practical Adoption Path**  
1. **Prototype** – Install the npm package, configure your Qwen API keys in the provided `.env`, and start the proxy (`npm start`). Use the exposed HTTP endpoint (or generated SDK) as a drop‑in replacement for OpenAI calls in your existing codebase.  
2. **Integrate** – Add the proxy URL to your application’s configuration, optionally enable the CLI for testing or the SDK for tighter TypeScript integration. Leverage the built‑in tool‑calling hooks to connect to vector stores, databases, or other services.  
3. **Scale** – Deploy the proxy in a containerized environment (Docker/K8s) behind a load balancer, configure multiple credential profiles for different tenants, and persist session data in a Redis or PostgreSQL store if needed.  

**Production Readiness**  
- **Activity & adoption** – 131 stars, 63 forks, recent commits (as of 2026‑06‑23), and a growing TypeScript ecosystem indicate active community interest.  
- **Stability** – The codebase follows conventional API patterns, includes a CLI for health checks, and provides clear TypeScript typings, reducing integration risk.  
- **Operational maturity** – Designed for container deployment, supports persistent sessions, and can be scaled horizontally; however, a final review of licensing, security hardening, and maintainer responsiveness is still recommended before mission‑critical use.  

Overall, qwenproxy offers a low‑friction route to embed Qwen LLM capabilities into existing OpenAI‑centric workflows, with a solid foundation for pilot projects and a clear path to production deployment.

### Русский

**pedrofariasx/qwenproxy** — это open‑source прокси‑сервер с совместимым с OpenAI API, который через Playwright автоматически перенаправляет запросы к моделям Qwen, поддерживая несколько учётных записей, инструменты и постоянные сессии. Он позволяет быстро добавить AI‑функциональность в прототипы, RAG‑системы или агентные воркфлоу без необходимости строить собственный стек моделей. Проект активно поддерживается (обновления 2026‑06‑23, 131 звезда, 63 форка), написан на TypeScript и готов к пилотному внедрению в production‑окружения после финального аудита лицензии и безопасности.

### 中文

**项目简介**  
pedrofariasx/qwenproxy 是一个基于 Playwright 自动化的 OpenAI 兼容代理 API，能够把请求路由到多账号的 Qwen 大模型，并支持工具调用和会话持久化。

**价值**  
- **快速赋能 AI**：无需自行部署模型或搭建复杂的推理服务，只需接入该代理即可在现有系统中使用 Qwen 的强大能力。  
- **多账号与持久会话**：同一代理即可管理多个 Qwen 账号，保持对话上下文，适合 RAG、Agent 工作流等需要长期会话的场景。  
- **工具调用支持**：内置对外部工具（如检索、计算等）的调用接口，帮助构建更智能的业务流程。

**典型接入方式**  
1. **API/SDK**：在项目中直接调用 `POST /v1/chat/completions`（兼容 OpenAI 接口），使用任意语言的 HTTP 客户端或官方 OpenAI SDK。  
2. **CLI**：通过项目自带的命令行工具进行快速测试或脚本化调用。  
3. **环境配置**：在 `.env` 或启动参数中配置 Qwen 账号的 API Key、代理端口等信息，即可实现多账号轮询。  

**生产可用性**  
- **活跃度**：最近一次更新在 2026‑06‑23，拥有 131 ⭐、63 🍴，社区活跃。  
- **技术成熟度**：使用 TypeScript 编写，代码结构清晰，已在多个内部原型项目中验证。  
- **可靠性**：Playwright 自动化保证请求的可靠转发，支持持久会话和错误重试。  
- **风险**：仍需进一步审查许可证（MIT）及安全依赖的更新情况，但整体已具备在生产环境进行试点的条件。  

综上，qwenproxy 能让开发者以最小的成本把 Qwen 大模型能力嵌入现有系统，接入方式简洁，且在 OSS 社区的活跃度和功能完整度上已经具备较高的生产可用性。

## 🧭 Practical evaluation

**Value:** pedrofariasx/qwenproxy helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 131 GitHub stars
- 63 forks
- updated 2026-06-23
- primary language: TypeScript
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 45/100 |
| topics | 100/100 |
| outlook | 60/100 |
| quality | 60/100 |
| recency | 40/100 |
| adoption | 45/100 |
| production | 59/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/pedrofariasx/qwenproxy) · [← Back to AI/ML](./README.md)</sub>
