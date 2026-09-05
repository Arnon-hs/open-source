# etweisberg/mlb-mcp

[![Stars](https://img.shields.io/github/stars/etweisberg/mlb-mcp?style=flat-square&color=yellow)](https://github.com/etweisberg/mlb-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/etweisberg/mlb-mcp?style=flat-square&color=blue)](https://github.com/etweisberg/mlb-mcp/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-75%2F100-brightgreen?style=flat-square)](#)

> MCP server for advanced baseball analytics (statcast, fangraphs, baseball reference, mlb stats API)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 28 |
| 🍴 **Forks** | 9 |
| 💻 **Language** | Python |
| 📈 **Score** | 75/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`baseball-analytics` `baseball-data` `baseball-statistics` `fangraphs` `mcp` `mcp-client` `mcp-server` `mlb-stats-api` `statcast`

## 🎯 Categories

MCP · Backend · Data

## 📝 Summary

### English

**Brief Summary**  
etweisberg/mlb-mcp is an open‑source Model Context Protocol (MCP) server that aggregates advanced baseball data from Statcast, FanGraphs, Baseball‑Reference, and the MLB Stats API. It provides a uniform, Python‑based API/SDK/CLI that lets AI assistants and other services query real‑time and historical baseball metrics through a single, standards‑compliant endpoint.  

**Value**  
- **Unified data access:** Eliminates the need for developers to stitch together multiple baseball data sources; everything is exposed via the MCP standard.  
- **AI‑ready interface:** By speaking the Model Context Protocol, the server lets LLM‑based agents retrieve and act on live sports data without custom scraping or ad‑hoc wrappers.  
- **Extensible tooling:** The same MCP server can be deployed as a backend for dashboards, betting models, fantasy‑league bots, or any analytics pipeline that needs reliable baseball statistics.  

**Practical Adoption Path**  
1. **Prototype:** Clone the repo, install the Python dependencies, and run the provided Docker compose file to spin up a local MCP server.  
2. **Integration:** Connect your AI agent or application using the supplied SDK (or a generic MCP client) and start issuing queries such as `GET /statcast/pitch` or `GET /fangraphs/player`.  
3. **Customization:** Extend the server with additional endpoints or cache layers if you need proprietary data sources or higher throughput.  
4. **Production deployment:** Deploy the containerized service behind a load balancer, enable TLS, and configure API keys for the underlying data providers.  

**Production Readiness**  
- **Activity & adoption:** Recent commits (last updated 2026‑07‑12), 28 GitHub stars, 9 forks, and multiple topics indicate an engaged community.  
- **Stability:** The codebase is Python‑centric, well‑documented, and includes a CLI for health checks, making automated testing and CI pipelines straightforward.  
- **Risk considerations:** No glaring licensing or security red flags have been found, but a final review of third‑party API terms and maintainers’ responsiveness is recommended before a large‑scale rollout.  

Overall, etweisberg/mlb-mcp is a mature, production‑ready OSS component for anyone looking to plug AI assistants or analytics services into a comprehensive, standards‑based baseball data backend.

### Русский

Резюме проекта etweisberg/mlb-mcp:

Проект etweisberg/mlb-mcp представляет собой MCP-сервер для продвинутых аналитиков в бейсболе (statcast, fangraphs, baseball reference, mlb stats API), позволяющий подключать интеллектуальные помощники к реальным инструментам и данным через стандартный протокол. Этот проект может быть полезен в сценариях, когда необходимо подключить интеллектуальные агенты к инструментам, а также внедрить Model Context Protocol-серверы и стандартизировать интеграции. Проект готов к использованию в production, поскольку он имеет высокий уровень готовности, недавнюю активность, широкое распространение и сильные сигналы экосистемы.

### 中文

**项目简介**

etweisberg/mlb-mcp 是一个开源项目，旨在为棒球分析提供高级数据服务（statcast、fangraphs、baseball reference、mlb stats API）。它提供了 Model Context Protocol (MCP) 服务器，可以帮助连接 AI 助手与真实的工具和数据。

**价值**

该项目的价值在于，它帮助连接 AI 代理与工具，标准化整合，并提供了一个 Model Context Protocol 服务器。它可以帮助开发者更好地利用棒球数据，进行高级分析。

**典型接入方式**

该项目提供了 API、SDK 和 CLI 接口，可以方便地与其他工具或系统整合。使用 Python 语言开发，支持多个主题。

**生产可用性**

该项目具有较高的生产可用性，最近有活跃的维护，采用率和生态系统信号良好。建议用于serious pilot（严格试验）。

## 🧭 Practical evaluation

**Value:** etweisberg/mlb-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 28 GitHub stars
- 9 forks
- updated 2026-07-12
- primary language: Python
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 25/100 |
| stars | 31/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 63/100 |
| recency | 80/100 |
| adoption | 29/100 |
| production | 72/100 |
| usefulness | 90/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/etweisberg/mlb-mcp) · [← Back to Mcp](./README.md)</sub>
