# atilaahmettaner/tradingview-mcp

[![Stars](https://img.shields.io/github/stars/atilaahmettaner/tradingview-mcp?style=flat-square&color=yellow)](https://github.com/atilaahmettaner/tradingview-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/atilaahmettaner/tradingview-mcp?style=flat-square&color=blue)](https://github.com/atilaahmettaner/tradingview-mcp/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-85%2F100-brightgreen?style=flat-square)](#)

> TradingView MCP server — real-time market data, technical analysis, screeners & backtesting for Claude, ChatGPT, Cursor & any MCP client. Stocks, crypto, forex & futures across global exchanges. Hosted or self-host.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.3k |
| 🍴 **Forks** | 705 |
| 💻 **Language** | Python |
| 📈 **Score** | 85/100 |
| 🗓️ **Last push** | 2026-06-28 |
| 🔍 **Source** | github |

## 🏷️ Topics

`claude-desktop` `cryptocurrency` `futures` `market-data` `mcp-server` `mcp-tools` `model-context-protocol` `openclaw` `stock-market` `technical-analysis` `trading-mcp` `trading-strategies`

## 🎯 Categories

Crypto · Trading · MCP · Backend · DevTools

## 📝 Summary

### English

**Brief Summary**  
TradingView MCP is an open‑source Python server that streams real‑time market data, technical‑analysis indicators, screeners and back‑testing capabilities to any MCP client—including Claude, ChatGPT, Cursor, and custom bots. It supports stocks, crypto, forex and futures from global exchanges and can be run as a hosted service or self‑hosted instance.  

**Value**  
The project gives developers a ready‑made bridge between TradingView‑style market intelligence and AI/automation platforms, making it far easier to prototype and test Web3 workflows such as wallet interactions, DeFi strategies, or blockchain‑driven trading bots without building a data pipeline from scratch. Because the implementation is fully open, teams can inspect, extend, or audit the data‑handling logic to meet compliance or security requirements.  

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Spin up a test instance** (Docker compose or `pip install tradingview-mcp`) | Quick validation of connectivity and data coverage. |
| 2️⃣  | **Connect an MCP client** (e.g., Claude, ChatGPT, Cursor) using the provided REST/WS API or the supplied Python SDK | Confirms that the AI can request live quotes, indicators, or back‑test results. |
| 3️⃣  | **Integrate with blockchain components** (wallet SDK, smart‑contract calls) | Demonstrates end‑to‑end Web3 use cases such as triggering a trade when a technical signal fires. |
| 4️⃣  | **Run a pilot** on a staging environment, instrumenting logging and monitoring | Validates reliability, latency, and error handling under realistic load. |
| 5️⃣  | **Scale to production** (self‑hosted on Kubernetes or use the hosted offering) and add authentication/role‑based access controls | Provides the needed operational robustness for a production deployment. |

**Production Readiness**  
- **Activity & Adoption**: 3,291 stars, 705 forks, recent commits (as of 2026‑06‑28) and a vibrant community indicate strong momentum.  
- **Technical Maturity**: Written in Python, the codebase is modular, includes a CLI, SDK, and clear API docs, and covers 13 topical areas (data ingestion, screening, back‑testing, etc.).  
- **Scalability**: Designed to run both as a hosted SaaS and self‑hosted container, making it adaptable to small prototypes and large‑scale production clusters.  
- **Risk Profile**: No immediate licensing or security red flags, though a final audit of the license (MIT/Apache‑2.0‑style) and a vulnerability scan of dependencies is recommended before mission‑critical use.  

Overall, TradingView MCP is a high‑readiness OSS component that can be evaluated quickly and, after standard security vetting, promoted to production for AI‑driven trading and Web3 workflow automation.

### Русский

**atilaahmettaner/tradingview-mcp** — это открытый сервер MCP, который в реальном времени поставляет рыночные данные, технические индикаторы, скринеры и возможности бэктестинга для Claude, ChatGPT, Cursor и любых MCP‑клиентов (акции, криптовалюты, форекс, фьючерсы). Проект уже широко принят (3 291 ★, 705 forks), активно поддерживается (обновления – 2026‑06‑28) и написан на Python, поэтому его можно быстро интегрировать в Web3‑проекты: использовать как бекенд‑слой для прототипирования кошельков, DeFi‑приложений или анализа блокчейн‑транзакций через готовый API/SDK/CLI. По уровню готовности – высокий: стабильный код, хорошая экосистема и активные пользователи делают его готовым к пилотному запуску в продакшн, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
`atilaahmettaner/tradingview-mcp` 是一个基于 TradingView 的 MCP（Market Data & Compute Platform）服务器，提供实时行情、技术分析、筛选器和回测功能，支持股票、加密货币、外汇和期货等全球交易所。可自行部署或使用托管版，方便 Claude、ChatGPT、Cursor 以及任何兼容 MCP 的客户端接入。

**价值**  
- **快速原型**：通过开放的 API/SDK/CLI，开发者可以在几行代码内获取完整的市场数据和技术指标，快速搭建 Web3、DeFi 或钱包相关的业务流程。  
- **全链路可视化**：实现对区块链集成点（行情获取、订单簿、历史回测等）的即时监控与调试，帮助团队在生产前发现并修复潜在问题。  
- **跨平台统一入口**：一次部署即可服务多种语言和框架的客户端，降低维护成本并提升团队协作效率。

**典型接入方式**  
1. **API 调用**：使用 REST 或 WebSocket 接口获取实时行情、技术指标或回测结果；  
2. **SDK**：项目提供的 Python SDK（`tradingview_mcp`）封装了常用请求，直接在脚本或服务中调用；  
3. **CLI**：通过命令行工具进行快速查询或批量下载历史数据，适合 CI/CD 流程或离线分析。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑28，项目拥有 3,291 星、705 Fork，最近一次提交在同一天，表明仍在积极维护。  
- **成熟度**：代码基于 Python，已覆盖 13 个主题（行情、技术分析、回测、筛选等），并提供完整的文档与示例。  
- **部署灵活**：支持 Docker 镜像一键部署，也可在自有服务器上自行构建，满足安全合规要求。  
- **风险提示**：需进一步审查许可证（MIT / Apache 等）以及安全审计报告，确认无潜在漏洞后方可用于关键业务。  

综合来看，`tradingview-mcp` 在功能完整性、社区活跃度和部署便利性方面表现出色，已具备在生产环境中进行试点或正式上线的条件。

## 🧭 Practical evaluation

**Value:** atilaahmettaner/tradingview-mcp helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3291 GitHub stars
- 705 forks
- updated 2026-06-28
- primary language: Python
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 71/100 |
| stars | 75/100 |
| topics | 100/100 |
| outlook | 91/100 |
| quality | 88/100 |
| recency | 100/100 |
| adoption | 74/100 |
| production | 84/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/atilaahmettaner/tradingview-mcp) · [← Back to Crypto](./README.md)</sub>
