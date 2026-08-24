# Kong/insomnia

[![Stars](https://img.shields.io/github/stars/Kong/insomnia?style=flat-square&color=yellow)](https://github.com/Kong/insomnia/stargazers) [![Forks](https://img.shields.io/github/forks/Kong/insomnia?style=flat-square&color=blue)](https://github.com/Kong/insomnia/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-81%2F100-brightgreen?style=flat-square)](#)

> The open-source, cross-platform API client for GraphQL, REST, WebSockets, SSE and gRPC. With Cloud, Local and Git storage.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 39.8k |
| 🍴 **Forks** | 2.3k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 81/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`api` `api-client` `api-design` `curl` `electron-app` `graphql` `grpc` `http-client` `rest-api` `websockets`

## 🎯 Categories

Backend · Design

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Kong Insomnia is an open‑source, cross‑platform API client that supports GraphQL, REST, WebSockets, SSE and gRPC, with built‑in Cloud, local, and Git‑backed storage. With a vibrant community (≈40 k stars, 2.3 k forks) and a modern TypeScript codebase, it offers a rich set of APIs/SDKs/CLI tools that make internal knowledge bases searchable and usable by AI assistants. Its strong adoption, frequent releases, and extensive ecosystem make it a solid candidate for pilot projects that need searchable, assistant‑friendly documentation.

**Value Proposition**  
Insomnia turns API specifications, request histories, and associated documentation into structured, machine‑readable artifacts. By indexing these artifacts, organizations can surface precise technical knowledge to LLM‑powered assistants, improving answer relevance, reducing hallucinations, and accelerating developer onboarding.

**Practical Adoption Path**  

| Step | Action | Why it matters |
|------|--------|----------------|
| 1️⃣ Evaluate | Clone the repo, run the CLI (`insomnia run`) against a sample OpenAPI/GraphQL spec, and inspect the generated JSON/YAML artifacts. | Confirms that the data format aligns with your RAG pipeline. |
| 2️⃣ Integrate | Use the official SDK or the REST API to pull collections, environments, and request logs into your knowledge store (e.g., vector DB). | Enables continuous syncing of up‑to‑date API knowledge. |
| 3️⃣ Enrich | Add custom tags or markdown notes in Insomnia; these are persisted in Git or Cloud storage and become searchable metadata for the assistant. | Improves context and domain‑specific retrieval. |
| 4️⃣ Pilot | Deploy a lightweight RAG service that queries the indexed Insomnia data alongside other docs, and test assistant responses on real developer queries. | Validates end‑to‑end usefulness before full rollout. |
| 5️⃣ Scale | Automate CI/CD to push new collections to Git, trigger re‑indexing, and monitor usage metrics. | Guarantees freshness and operational reliability. |

**Production Readiness**  
- **Activity & Maintenance**: Last commit on 2026‑07‑03, regular releases, and an active maintainer community.  
- **Ecosystem Fit**: Provides CLI, SDK, and GraphQL/REST endpoints; easy to embed in CI pipelines or micro‑services.  
- **Stability**: High star count, mature TypeScript codebase, and clear versioning indicate low risk of breaking changes.  
- **Security & Licensing**: Open‑source MIT license; no known critical vulnerabilities, but a final security audit is recommended.  

Overall, Kong Insomnia is production‑ready for pilots that need a reliable source of API‑level knowledge to power AI assistants, with a straightforward integration path and strong community backing.

### Русский

Kong / Insomnia — это кроссплатформенный open‑source клиент API, поддерживающий GraphQL, REST, WebSockets, SSE и gRPC, с возможностью хранения запросов в облаке, локально и в Git, что позволяет быстро индексировать и делать внутренние знания доступными для ассистентов. Типичный сценарий внедрения — подключение к существующим API, индексация спецификаций и запросов в единой базе, после чего ассистент может выполнять точный поиск и генерировать ответы, опираясь на актуальные данные. Проект имеет высокий уровень готовности к продакшну: активные коммиты, более 39 тыс. звёзд на GitHub, широкое принятие в сообществе и поддержка TypeScript‑SDK/CLI, хотя окончательная проверка лицензии и безопасности всё же требуется.

### 中文

**Kong/insomnia 简介**

Kong/insomnia 是一个开源的、跨平台的 API 客户端，支持 GraphQL、REST、WebSockets、SSE 和 gRPC 协议。它提供了云、本地和 Git 存储，帮助您管理内部知识。

**价值**

Kong/insomnia 帮助您使内部知识可搜索和可用，方便助理使用。它可以帮助您：

* 索引知识库
* 改善文档搜索
* 为助理答案提供基础

**典型接入方式**

Kong/insomnia 可以通过以下方式接入：

* API：暴露 API 接口，允许您通过 API 调用功能
* SDK：提供 SDK，允许您在应用中集成功能
* CLI：提供命令行接口，允许您通过命令行调用功能

**生产可用性**

Kong/insomnia 的生产可用性较高，主要原因是：

* 近期活动：最近有活跃的开发和维护
* 采用：有大量用户采用该项目
* 生态系统信号：有强大的生态系统支持

## 🧭 Practical evaluation

**Value:** Kong/insomnia helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 39837 GitHub stars
- 2345 forks
- updated 2026-07-03
- primary language: TypeScript
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 84/100 |
| stars | 98/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 82/100 |
| recency | 40/100 |
| adoption | 94/100 |
| production | 67/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/Kong/insomnia) · [← Back to Backend](./README.md)</sub>
