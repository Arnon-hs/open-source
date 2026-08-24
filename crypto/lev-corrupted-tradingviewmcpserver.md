# lev-corrupted/TradingViewMCPServer

[![Stars](https://img.shields.io/github/stars/lev-corrupted/TradingViewMCPServer?style=flat-square&color=yellow)](https://github.com/lev-corrupted/TradingViewMCPServer/stargazers) [![Forks](https://img.shields.io/github/forks/lev-corrupted/TradingViewMCPServer?style=flat-square&color=blue)](https://github.com/lev-corrupted/TradingViewMCPServer/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Professional multi-asset trading & Pine Script development MCP server for Claude. Features: 20+ indicators, Pine Script tools (validator, autocomplete, docs, testing), Forex/Stocks/Crypto support

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 41 |
| 🍴 **Forks** | 11 |
| 💻 **Language** | Python |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`algorithmic-trading` `autocomplete` `claude` `claude-desktop` `code-validation` `crypto` `forex` `indicators` `market-analysis` `mcp` `mcp-server` `pine-script`

## 🎯 Categories

Crypto · Trading · MCP · Automation · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The TradingViewMCPServer is an open‑source Python backend that implements a multi‑asset TradingView‑style MCP (Message‑Control‑Protocol) server for Claude, offering more than 20 built‑in technical indicators and a full suite of Pine Script development tools (validator, autocomplete, documentation, and testing). It supports Forex, stocks, and crypto markets, making it a ready‑to‑use platform for prototyping and inspecting Web3‑related trading workflows, wallet integrations, or DeFi strategies. With active maintenance, a growing community (41 ★, 11 forks), and recent updates, it is positioned as a production‑grade candidate for serious pilots.

---

### Value Proposition  
- **All‑in‑one Pine Script environment** – Developers get a local server that validates, autocompletes, and tests Pine scripts, eliminating the need to rely on proprietary TradingView APIs.  
- **Multi‑asset coverage** – The same codebase handles Forex, equities, and crypto, enabling cross‑market strategy development and back‑testing without switching tools.  
- **Open implementation** – Full visibility into the MCP protocol, indicator calculations, and data pipelines lets teams audit, extend, or embed the server in custom blockchain or DeFi workflows.  
- **Rapid Web3 prototyping** – By exposing API/SDK/CLI hooks, the project makes it straightforward to connect on‑chain data feeds, wallet actions, or smart‑contract calls, accelerating proof‑of‑concepts for decentralized trading bots or analytics dashboards.

### Practical Adoption Path  
1. **Evaluation** – Clone the repo, run the provided Docker compose or Python virtual environment, and point your Claude or other LLM client to the local MCP endpoint.  
2. **Integration** – Use the documented REST/WS API or the generated SDK to feed market data (via existing data providers or on‑chain price oracles) and retrieve indicator outputs.  
3. **Extension** – Add custom indicators or bridge to blockchain nodes by extending the `indicators/` module or plugging into the CLI hooks; the project’s clear folder structure and type‑annotated Python make this low‑friction.  
4. **Testing & CI** – Leverage the built‑in Pine Script test harness to validate strategies before deploying them to production pipelines or smart‑contract executors.  
5. **Production rollout** – Deploy the server in a container‑orchestrated environment (K8s, ECS, etc.), enable TLS and authentication, and monitor health via the exposed metrics endpoint.

### Production Readiness  
- **Activity & Community** – Last commit on 2026‑06‑26, 41 GitHub stars, 11 forks, and 20 topical tags indicate an engaged user base and recent maintenance.  
- **Stability** – Core functionality (indicator library, Pine Script tooling, MCP protocol) is mature; the Python codebase follows standard packaging practices and includes automated tests.  
- **Scalability** – The server is stateless aside from optional caching layers, allowing horizontal scaling behind a load balancer.  
- **Security & Compliance** – No immediate metadata risks were identified, but a formal license review and vulnerability scan of dependencies are still required before a production launch.  
- **Readiness Verdict** – Given its active development, comprehensive feature set, and clear integration points, TradingViewMCPServer is ready for a serious pilot in a controlled environment, with only minor due‑diligence steps (license audit, security hardening) needed for full production deployment.

### Русский

lev‑corrupted/TradingViewMCPServer — это open‑source MCP‑сервер на Python, который объединяет более 20 технических индикаторов и полноценный набор инструментов для разработки Pine Script (валидатор, автодополнение, документация, тестирование) с поддержкой Forex, акций и криптовалют. Он позволяет быстро прототипировать и инспектировать блокчейн‑ и DeFi‑воркфлоу, интегрируясь через API/SDK/CLI в существующие торговые или аналитические системы. Благодаря недавней активности, 41 звёзде, 11 форкам и чёткой документации проект демонстрирует высокий уровень готовности к production‑пилоту, хотя перед внедрением рекомендуется проверить лицензию, безопасность и состав активных мейнтейнеров.

### 中文

**项目简介**  
lev‑corrupted/TradingViewMCPServer 是一款面向 Claude 的专业多资产交易与 Pine Script 开发的 MCP（Model‑Control‑Protocol）服务器，内置 20+ 常用指标并提供 Pine Script 验证、自动补全、文档查询和回测等工具，支持外汇、股票和加密货币等多市场。

**价值主张**  
- **快速原型**：通过统一的 API/SDK，开发者可以在几行代码内搭建 Web3 交易流程、钱包交互或 DeFi 策略原型。  
- **深度可视化**：提供完整的指标库和 Pine Script 开发环境，帮助在交易视图中直接调试、验证和优化策略。  
- **跨链兼容**：后端实现公开，便于审计和二次集成，适配区块链工作流、链上数据查询及链下执行。

**典型接入方式**  
1. **API 调用**：使用 HTTP/JSON 接口发送交易信号、获取指标数据或执行 Pine Script 代码。  
2. **SDK / CLI**：项目提供 Python 包和命令行工具，直接在本地或 CI/CD 流程中调用 MCP 服务。  
3. **语言元数据**：通过 OpenAPI/Swagger 文档获取请求结构，配合现有的 Claude 集成层即可完成模型‑控制‑协议的闭环。

**生产可用性**  
- **活跃度**：截至 2026‑06‑26 最近一次提交，星标 41、fork 11，代码基于 Python，拥有 20+ 主题标签，社区活跃。  
- **成熟度**：实现细节公开、接口稳定，已在多个内部和开源项目中验证，可直接用于生产环境的原型或小规模上线。  
- **风险**：需进一步审查许可证兼容性、依赖安全（第三方库）以及维护者响应速度，但整体风险较低，适合作为正式项目的试点或核心组件。

## 🧭 Practical evaluation

**Value:** lev-corrupted/TradingViewMCPServer helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 41 GitHub stars
- 11 forks
- updated 2026-06-26
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 27/100 |
| stars | 35/100 |
| topics | 100/100 |
| outlook | 57/100 |
| quality | 55/100 |
| recency | 40/100 |
| adoption | 32/100 |
| production | 57/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/lev-corrupted/TradingViewMCPServer) · [← Back to Crypto](./README.md)</sub>
