# Qoyyuum/mcp-metatrader5-server

[![Stars](https://img.shields.io/github/stars/Qoyyuum/mcp-metatrader5-server?style=flat-square&color=yellow)](https://github.com/Qoyyuum/mcp-metatrader5-server/stargazers) [![Forks](https://img.shields.io/github/forks/Qoyyuum/mcp-metatrader5-server?style=flat-square&color=blue)](https://github.com/Qoyyuum/mcp-metatrader5-server/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> A Model Context Protocol (MCP) server for interacting with the MetaTrader 5 trading platform. This server provides AI assistants with tools and resources to access market data, perform trading operations, and analyze trading history.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 170 |
| 🍴 **Forks** | 63 |
| 💻 **Language** | Python |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`mcp-server` `metatrader-5`

## 🎯 Categories

Trading · MCP · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Qoyyuum’s **mcp‑metatrader5‑server** is a Python‑based Model Context Protocol (MCP) server that bridges AI assistants with the MetaTrader 5 platform, exposing market data, trade execution, and historical analysis as programmable tools. It enables researchers and developers to prototype, back‑test, and automate trading workflows directly from AI‑driven agents, turning trading ideas into runnable code with minimal friction.  

**Value Proposition**  
- **Unified AI interface:** By wrapping MT5’s API behind the MCP standard, the server lets LLMs and other AI assistants query live quotes, place orders, and retrieve trade logs without writing low‑level MT5 code.  
- **Accelerated research & automation:** Traders can quickly spin up back‑testing rigs, explore strategy variations, and monitor live positions from a single, scriptable endpoint, shortening the iteration cycle from days to minutes.  
- **Open‑source flexibility:** With 170 ★ and an active Python codebase, the project can be customized (e.g., adding custom risk checks or proprietary data feeds) while keeping costs low.

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC):** Fork the repo, run the provided Docker/virtual‑env setup, and verify connectivity to a sandbox MT5 account using the README examples.  
2. **Integration Layer:** Wrap the MCP calls in your internal service mesh (e.g., expose via gRPC or HTTP) and create thin adapters for your existing strategy libraries.  
3. **Pilot Automation:** Deploy the server on a staging environment, connect an LLM‑powered assistant (or a simple script) to execute a limited set of trades under strict risk limits.  
4. **Scale & Harden:** Add logging, authentication (OAuth/JWT), and monitoring; integrate with your CI/CD pipeline for automated testing of strategy code before it reaches production.

**Production Readiness Assessment**  
- **Maturity:** Medium. The code is recent (last updated 2026‑06‑29) and functional for prototypes, but it lacks enterprise‑grade features such as built‑in rate limiting, comprehensive audit trails, and formal SLA documentation.  
- **Dependencies & Maintenance:** Python‑centric with modest external libs; a review of version pinning and vulnerability scanning is advisable. The maintainer activity appears modest, so consider forking and taking ownership of critical bug fixes.  
- **Risk Considerations:** No immediate licensing or metadata red flags, but perform a security audit (especially around order‑execution endpoints) and verify that the chosen MT5 broker permits automated API trading.  

**Bottom Line**  
The MCP‑MetaTrader5 server is a solid foundation for building AI‑enhanced trading tools and is ready for internal pilots or research environments. With a focused PoC, proper security hardening, and integration into your CI/CD and monitoring stack, it can be elevated to a production‑grade component for automated market workflows.

### Русский

Qoyyuum/mcp-metatrader5-server — это Python‑сервер протокола Model Context Protocol (MCP), позволяющий AI‑ассистентам получать рыночные данные, выполнять торговые операции и анализировать историю сделок в MetaTrader 5. Он подходит для быстрого прототипирования и автоматизации исследовательских или бэктестовых сценариев (например, построения и мониторинга торговых стратегий), однако перед выводом в продакшн рекомендуется провести небольшое POC, проверить README, убедиться в актуальности зависимостей и оценить безопасность/лицензию. Готовность к production — средняя: проект стабилен для внутренних и экспериментальных workflows, но требует дополнительной проверки и возможных доработок перед масштабным использованием.

### 中文

**项目简介**  
Qoyyuum/mcp‑metatrader5‑server 是一个基于 Model Context Protocol（MCP）的后端服务，帮助 AI 助手直接对接 MetaTrader 5（MT5）平台，提供行情获取、下单交易、历史回测等功能，方便研发和自动化交易工作流。

**价值**  
- **快速获取真实行情**：AI 可以实时读取 MT5 的报价、深度和历史数据，用于模型训练或实时决策。  
- **一键执行交易**：通过统一的 MCP 接口下单、修改、撤单，降低手动脚本的复杂度。  
- **完整回测支撑**：服务器能够调取历史交易记录，帮助研究人员快速评估策略表现。  

**典型接入方式**  
1. **阅读 README**，确认 Python 环境（>=3.9）和 MT5 客户端已安装并配置好 API 访问权限。  
2. **克隆仓库**并在虚拟环境中 `pip install -r requirements.txt`。  
3. **启动 MCP Server**（`python -m mcp_mt5_server`），默认在本地 8000 端口提供 REST/gRPC 接口。  
4. **在 AI 助手或业务系统中**，使用 MCP SDK（或直接调用 HTTP API）注册 `mt5` 资源，发送如 `get_market_data(symbol, timeframe)`、`place_order(...)` 等指令即可。  
5. **先做小规模 POC**：例如只读取单一品种的行情或执行一次模拟下单，验证权限、延迟和异常处理后再扩展到完整工作流。

**生产可用性**  
- **成熟度**：GitHub ★170、Fork 63，最近一次提交在 2026‑06‑29，代码活跃度尚可。  
- **适用场景**：原型开发、内部研究、策略回测以及小规模自动化交易。  
- **风险与准备**：  
  - 需要自行审查许可证（MIT/Apache 等）以及依赖库的安全性。  
  - 生产环境应加入监控、日志和容错（如进程守护、API 超时重试）。  
  - 建议在隔离的测试账户或模拟环境中完成完整的功能验证后，再迁移到实盘账户。  

综上，mcp‑metatrader5‑server 对于想把 AI 与 MT5 交易闭环的团队是一个 **中等成熟度、快速上手** 的解决方案，适合作为原型或内部自动化工具使用，进入生产前需完成安全审计和运维加固。

## 🧭 Practical evaluation

**Value:** Qoyyuum/mcp-metatrader5-server helps research and automate market workflows.

**Best use cases**

- research trading systems
- backtest strategies
- monitor market workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 170 GitHub stars
- 63 forks
- updated 2026-06-29
- primary language: Python
- 2 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 48/100 |
| topics | 25/100 |
| outlook | 67/100 |
| quality | 60/100 |
| recency | 80/100 |
| adoption | 47/100 |
| production | 67/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/Qoyyuum/mcp-metatrader5-server) · [← Back to Trading](./README.md)</sub>
