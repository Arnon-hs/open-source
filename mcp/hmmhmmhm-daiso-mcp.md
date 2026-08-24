# hmmhmmhm/daiso-mcp

[![Stars](https://img.shields.io/github/stars/hmmhmmhm/daiso-mcp?style=flat-square&color=yellow)](https://github.com/hmmhmmhm/daiso-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/hmmhmmhm/daiso-mcp?style=flat-square&color=blue)](https://github.com/hmmhmmhm/daiso-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> 한국 로컬 리테일과 영화관 조회를 MCP, CLI, Codex Skill로 연결합니다.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 305 |
| 🍴 **Forks** | 21 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cgv` `clawhub` `cli` `codex-skill` `daiso` `gs25` `inventory` `korea` `korean-retail` `mcp` `mcp-server` `model-context-protocol`

## 🎯 Categories

MCP · Backend · DevTools

## 📝 Summary

### English

**Brief Summary**  
hmmhmmhm/daiso‑mcp is a TypeScript‑based open‑source framework that implements the Model Context Protocol (MCP) and provides CLI, SDK, and Codex‑Skill bindings for querying Korean local‑retail inventories and movie‑theater schedules. By exposing a standard MCP interface, it lets AI assistants call real‑world services as if they were native functions, enabling seamless tool integration and data retrieval.

**Value**  
- **Standardised AI‑tool bridge** – The project implements MCP, a protocol designed to let large language models invoke external services safely and predictably, removing the need for custom adapters for each new data source.  
- **Multi‑modal access** – With a REST‑style API, a CLI, and a Codex Skill, developers can integrate the service into backend pipelines, command‑line workflows, or directly into AI‑driven agents.  
- **Domain‑specific data** – It aggregates Korean retail product listings and cinema showtimes, offering a ready‑made knowledge source for localized conversational agents, recommendation bots, and inventory‑aware assistants.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run `npm install && npm run dev` to spin up the local MCP server. Use the provided CLI (`daiso-mcp`) to query a product or movie schedule and verify responses.  
2. **Integrate with an AI agent** – Register the server’s OpenAPI spec (or generated MCP schema) in your LLM orchestration platform (e.g., LangChain, CrewAI, or OpenAI Functions). The agent can now call `getRetailItem` or `getShowtimes` as native functions.  
3. **Extend** – Add new data sources (e.g., additional retailers or ticketing APIs) by implementing the MCP `Tool` interface; the existing SDK and CLI will automatically expose the new endpoints.  
4. **Deploy** – Containerise the server (Dockerfile is included) and push to a cloud provider or on‑prem Kubernetes cluster. Update DNS and authentication (API keys or OAuth) as required for production use.

**Production Readiness**  
- **Activity & Community** – 305 ★, 21 forks, recent commits (last updated 2026‑06‑23) and a healthy set of 14 topics indicate an active maintainer base.  
- **Maturity** – The project already ships a fully‑functional API, CLI, and Codex Skill, covering the core MCP use‑cases; the codebase is TypeScript with type‑safe contracts, reducing runtime errors.  
- **Scalability** – The server is stateless and can be horizontally scaled behind a load balancer; Docker support simplifies deployment in CI/CD pipelines.  
- **Risks** – Licensing and security audits are still pending, and long‑term maintainer commitment should be confirmed before mission‑critical roll‑outs. Once those checks are cleared, the repo is suitable for a serious pilot or production integration.

### Русский

**hmmhmmhm/daiso-mcp** — это open‑source‑решение на TypeScript, которое реализует Model Context Protocol (MCP) и предоставляет CLI, SDK и Codex‑skill для доступа к данным корейских локальных ритейлеров и кинотеатров. С его помощью AI‑ассистенты могут в реальном времени вызывать внешние инструменты и получать актуальную информацию, что упрощает построение интеграций и ускоряет выпуск MCP‑серверов. Проект активно поддерживается (обновления 2026‑06‑23, 305 звёзд, 21 форк), имеет хорошую документированность и готов к использованию в продакшн‑средах после финальной проверки лицензии и безопасности.

### 中文

**项目简介**  
hmmhmmhm/daiso‑mcp 是一个基于 **Model Context Protocol (MCP)** 的开源后端服务，提供统一的 API/CLI/SDK 接口，将韩国本地零售店和电影院的实时查询数据暴露给 AI 助手或其他自动化工具。  

**价值主张**  
- **标准化桥接**：通过 MCP 将 AI 代理（如 ChatGPT、Codex Skill 等）与真实业务系统对接，避免每个工具都要实现独立的适配层。  
- **即插即用**：只需调用统一的 API 或使用提供的 CLI/SDK，即可让 AI 读取、搜索或预订本地商店、电影场次等信息。  
- **加速产品落地**：帮助企业快速搭建“AI‑to‑Tool”场景，如智能客服、推荐系统或内部运营机器人。  

**典型接入方式**  
1. **API 调用**：向 MCP 服务器发送 JSON‑RPC 请求（如查询某地区的便利店库存或电影排片），服务器返回结构化响应。  
2. **CLI**：在 CI/CD、脚本或本地调试时使用 `daiso-mcp` 命令行工具，直接查询或管理数据。  
3. **SDK**（TypeScript/Node.js）：在自定义 AI Skill 或后端服务中引入 `@daiso/mcp` 包，调用 `client.query()` 等方法完成业务交互。  

**生产可用性**  
- **活跃度**：2026‑06‑23 最近一次提交，拥有 305 ★、21 Fork，14 个相关主题，社区活跃。  
- **技术成熟度**：采用 TypeScript 编写，提供完整的类型定义和 OpenAPI 文档，易于集成和调试。  
- **安全与合规**：暂无重大许可证或安全风险，但建议在正式部署前进行依赖审计和内部安全评估。  
- **适配性**：实现了标准的 MCP 协议，兼容多种 AI 平台（OpenAI、Claude、Codex 等），可在本地或云端部署，具备横向扩展能力。  

综合来看，hmmhmmhm/daiso-mcp 已具备较高的生产就绪度，适合作为企业在 AI 与本地业务系统之间的桥梁进行试点或正式上线。

## 🧭 Practical evaluation

**Value:** hmmhmmhm/daiso-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 305 GitHub stars
- 21 forks
- updated 2026-06-23
- primary language: TypeScript
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 53/100 |
| topics | 100/100 |
| outlook | 61/100 |
| quality | 61/100 |
| recency | 40/100 |
| adoption | 47/100 |
| production | 60/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/hmmhmmhm/daiso-mcp) · [← Back to Mcp](./README.md)</sub>
