# LeslieLeung/glean

[![Stars](https://img.shields.io/github/stars/LeslieLeung/glean?style=flat-square&color=yellow)](https://github.com/LeslieLeung/glean/stargazers) [![Forks](https://img.shields.io/github/forks/LeslieLeung/glean?style=flat-square&color=blue)](https://github.com/LeslieLeung/glean/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> A self-hosted RSS reader and personal knowledge management tool.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 837 |
| 🍴 **Forks** | 64 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`mcp` `mcp-server` `rss` `rss-reader`

## 🎯 Categories

MCP · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
LeslieLeung/glean is a self‑hosted RSS reader that doubles as a personal knowledge‑management platform, built in TypeScript and designed to expose a standard Model Context Protocol (MCP) API. It enables AI assistants to fetch, index, and act on real‑world web feeds and user notes through a clean, language‑agnostic interface. With over 800 stars, recent commits, and an active community, it’s ready for pilot deployments in production environments.

**Value**  
- **Bridges AI and real data** – By offering a standardized MCP endpoint, glean lets LLM‑driven agents retrieve up‑to‑date RSS content and personal knowledge bases without custom scraping or ad‑hoc integrations.  
- **Reusable integration layer** – The same API can serve as a Model Context Protocol server for multiple AI services, reducing duplicate connector code across projects.  
- **Self‑hosted control** – Organizations keep data on‑premises, satisfying privacy and compliance requirements while still benefiting from AI‑augmented workflows.

**Practical Adoption Path**  
1. **Deploy** – Spin up the Docker image or run the TypeScript service on a VM; configure RSS sources and knowledge‑base imports via the provided CLI or web UI.  
2. **Connect** – Point your AI assistant (e.g., LangChain, OpenAI function calls, or custom LLM wrapper) to the MCP endpoint using the generated OpenAPI spec.  
3. **Extend** – If needed, add custom plugins or SDK calls (Node.js/JS) to push additional data sources into glean’s store.  
4. **Iterate** – Use the built‑in query interface to test retrieval, then integrate the calls into production AI pipelines.

**Production Readiness**  
- **Activity & Adoption** – Last commit on 2026‑06‑28, 837 stars, 64 forks, and multiple topics indicate a healthy, actively maintained project.  
- **Robustness** – Exposes a well‑defined API/CLI, written in TypeScript with type safety, and includes Docker support for reproducible deployments.  
- **Risk Considerations** – No major metadata or licensing red flags yet; a final security audit and verification of maintainer responsiveness are recommended before full‑scale rollout.  

Overall, glean offers a mature, open‑source bridge between AI agents and live RSS/knowledge data, making it a solid candidate for production pilots that need a controllable, standards‑based integration layer.

### Русский

**LeslieLeung/glean** — это самохостинговый RSS‑ридер и инструмент для персонального управления знаниями, который реализует стандартный протокол Model Context Protocol, позволяя AI‑ассистентам напрямую обращаться к реальным сервисам и данным. Типичный сценарий: развернуть сервер Glean, подключить к нему AI‑агента (или несколько агентов) и через единый API/CLI предоставлять ленту новостей, заметки и другие пользовательские ресурсы для контекстуального взаимодействия. По готовности к production проект считается высоким: активная разработка, 837 звёзд, регулярные обновления (последний — 2026‑06‑28), зрелый TypeScript‑стек и поддержка API/SDK делают его готовым к пилотному внедрению, хотя окончательная проверка лицензии и безопасности всё же требуется.

### 中文

**LeslieLeung/glean 简介**

LeslieLeung/glean 是一个开源项目，提供了一个自主托管的 RSS 阅读器和个人知识管理工具。它通过标准协议连接 AI 助手和实用工具，帮助实现更好的整合和标准化。

**价值**

LeslieLeung/glean 的价值在于，它帮助连接 AI 助手和真实的工具和数据，从而实现更好的整合和标准化。它可以用于连接 AI 代理到工具、部署 Model Context Protocol 服务器以及标准化整合。

**典型接入方式**

LeslieLeung/glean 可以通过以下方式接入：

1. API/SDK：通过 API 或 SDK 接入 LesileLeung/glean 的功能。
2. CLI：使用命令行界面接入 LesileLeung/glean 的功能。
3. 集成工具：通过标准协议连接 LesileLeung/glean 到其他工具和服务。

**生产可用性**

LeslieLeung/glean 的生产可用性较高，具有以下优点：

1. 近期活跃：项目最近有活跃的维护和更新。
2. 广泛

## 🧭 Practical evaluation

**Value:** LeslieLeung/glean helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 837 GitHub stars
- 64 forks
- updated 2026-06-28
- primary language: TypeScript
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 62/100 |
| topics | 50/100 |
| outlook | 61/100 |
| quality | 58/100 |
| recency | 40/100 |
| adoption | 57/100 |
| production | 56/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/LeslieLeung/glean) · [← Back to Mcp](./README.md)</sub>
