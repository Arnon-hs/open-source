# russellbrenner/jurisd

[![Stars](https://img.shields.io/github/stars/russellbrenner/jurisd?style=flat-square&color=yellow)](https://github.com/russellbrenner/jurisd/stargazers) [![Forks](https://img.shields.io/github/forks/russellbrenner/jurisd?style=flat-square&color=blue)](https://github.com/russellbrenner/jurisd/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> jurisd (formerly auslaw-mcp) is a local-first MCP server and CLI giving any AI agent grounded Australian and New Zealand legal research: AustLII and jade.io retrieval with resilient fallback, deterministic provision lookup, offline citation graph, fast AGLC4 linting, plus optional semantic search and graph recall over your own local corpora.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 24 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic-ai` `agentic-coding` `aglc4` `austlii` `australia` `case-law` `citation-management` `claude` `claude-code` `codex` `command-line-tool` `gemini`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
Jurisd (formerly auslaw‑mcp) is a TypeScript‑based, local‑first MCP server and CLI that gives AI agents authoritative access to Australian and New Zealand legal sources. It bundles AustLII and jade.io retrieval, deterministic provision lookup, an offline citation graph, fast AGLC4 linting, and optional semantic‑search/graph‑recall over user‑supplied corpora, all behind a standard Model Context Protocol (MCP) interface.

**Value**  
- **Grounded legal knowledge** – AI assistants can query up‑to‑date statutes, case law, and regulations rather than hallucinating, which is essential for compliance‑heavy domains.  
- **Standardised integration** – By exposing a clean MCP/CLI/SDK surface, Jurisd lets developers plug any MCP‑compatible model (e.g., Claude, GPT‑4o) into a reliable legal‑research back‑end with minimal custom code.  
- **Offline resilience** – All core data (citation graph, AGLC4 rules) lives locally, so the service continues to work even when external sites are down or rate‑limited.  
- **Extensible RAG** – The optional semantic‑search layer lets teams augment the built‑in legal corpus with proprietary documents, creating a unified “legal‑plus‑internal” knowledge base.

**Practical Adoption Path**  
1. **Spin up the server** – Clone the repo, run `npm install && npm start` (or use the provided Docker image) to launch a local MCP endpoint.  
2. **Configure data sources** – Add AustLII/jade.io API keys (if needed) and point the server at any additional document collections you want to index for semantic search.  
3. **Connect your model** – In your AI‑agent code, use the MCP SDK or simple HTTP calls to send `search`, `lookup`, or `lint` requests to the Jurisd endpoint.  
4. **Iterate & test** – Verify responses against known legal citations; adjust fallback settings or indexing parameters.  
5. **Deploy** – Package the server as a container or a managed VM; because it’s local‑first, scaling is just a matter of adding more instances behind a load balancer.

**Production Readiness**  
- **Activity & community** – 24 ★, 8 forks, recent commits (as of 2026‑06‑28) and a clear TypeScript codebase indicate an active project.  
- **Maturity** – Core legal‑research features (AustLII, jade.io, citation graph, AGLC4 linting) are stable; the optional semantic layer is modular and can be disabled if not needed.  
- **Integration simplicity** – Exposes a well‑documented MCP API, CLI, and SDK, making it straightforward to evaluate and embed in existing pipelines.  
- **Risk considerations** – No major metadata or licensing red flags yet, but a final security audit and confirmation of maintainer commitment are advisable before a large‑scale rollout.

Overall, Jurisd is a high‑readiness OSS component for any organization that wants to ground AI assistants in authoritative Australian/New Zealand law while retaining the flexibility to add private corpora.

### Русский

jurisd — это локальный MCP‑сервер и CLI, написанные на TypeScript, которые дают AI‑агентам мгновенный доступ к официальным источникам правовой информации Австралии и Новой Зеландии (AustLII, jade.io), а также к офлайн‑графу цитирований, детерминированному поиску нормативных актов и быстрому линтингу по AGLC4; при желании можно подключить семантический поиск и воспоминание по собственным корпусам. Типичный сценарий — интеграция AI‑ассистента в корпоративные или исследовательские системы через единый протокол (Model Context Protocol), позволяя быстро развернуть сервер‑провайдер правовых данных и подключать к нему любые инструменты через API/SDK/CLI. Проект находится на высокой стадии готовности к production: активные коммиты, 24 звёзд, 8 форков, свежий релиз (28 июня 2026 г.), хорошая экосистема и поддержка, требующая лишь финального аудита лицензии и безопасности.

### 中文

**项目简介**  
jurisd（前身 auslaw‑mcp）是一个本地优先的 MCP 服务器与 CLI，专为 AI 代理提供澳大利亚和新西兰法律检索能力。它集成了 AustLII 与 jade.io 的可靠抓取、确定性法规查找、离线引文图、快速 AGLC4 规范检查，并可选地对本地语料库进行语义搜索和图谱召回。

**价值主张**  
- **真实法律数据接入**：让任何语言模型直接查询官方法律文献，避免“幻觉”。  
- **统一协议层**：通过标准化的 Model Context Protocol（MCP）把法律检索、引用校验、语义搜索等功能包装成可即插即用的服务。  
- **本地化与离线安全**：所有检索与图谱均可在本地运行，满足合规和数据隐私要求。  

**典型接入方式**  
1. **作为 MCP 服务器**：在本地或容器中启动 `jurisd serve`，对外暴露 HTTP/MCP 接口。  
2. **CLI 调用**：在脚本或 CI 中使用 `jurisd query …`、`jurisd lint …` 等子命令，获取检索结果或引用校验报告。  
3. **SDK/库**：项目提供 TypeScript SDK，直接在 Node.js 应用中调用 `JurisdClient`，实现实时查询、语义检索或图谱回溯。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑28，星标 24、fork 8，代码基于 TypeScript，拥有 19 个相关话题，社区活跃。  
- **成熟度**：核心功能（AustLII/Jade 抓取、AGLC4 lint、离线引文图）已实现并通过自动化测试，具备容错的回退机制。  
- **安全与合规**：项目采用 MIT 许可证，暂无已知安全漏洞；但在正式投产前仍建议自行审计依赖并确认维护者的响应速度。  

综合以上，jurisd 已具备在内部 AI 助手或法律科技平台中进行试点的条件，适合需要本地化、合规且可扩展的法律检索与引用校验能力的生产环境。

## 🧭 Practical evaluation

**Value:** russellbrenner/jurisd helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 24 GitHub stars
- 8 forks
- updated 2026-06-28
- primary language: TypeScript
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 30/100 |
| topics | 100/100 |
| outlook | 61/100 |
| quality | 53/100 |
| recency | 40/100 |
| adoption | 28/100 |
| production | 57/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/russellbrenner/jurisd) · [← Back to Mcp](./README.md)</sub>
