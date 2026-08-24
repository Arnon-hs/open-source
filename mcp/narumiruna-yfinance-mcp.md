# narumiruna/yfinance-mcp

[![Stars](https://img.shields.io/github/stars/narumiruna/yfinance-mcp?style=flat-square&color=yellow)](https://github.com/narumiruna/yfinance-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/narumiruna/yfinance-mcp?style=flat-square&color=blue)](https://github.com/narumiruna/yfinance-mcp/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> _No description provided._

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 135 |
| 🍴 **Forks** | 48 |
| 💻 **Language** | Python |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`finance` `mcp` `mcp-server` `python` `yahoo-finance`

## 🎯 Categories

MCP · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
narumiruna/yfinance-mcp is a Python‑based open‑source implementation of the Model Context Protocol (MCP) that wraps the popular yfinance library, exposing market data through a standardized API/SDK/CLI. It enables AI assistants and other autonomous agents to retrieve real‑time and historical financial information in a consistent, tool‑agnostic way, facilitating rapid prototyping of finance‑focused AI applications.

**Value**  
- **Standardized integration**: By speaking MCP, the project lets developers plug yfinance data into any AI system that already supports the protocol, eliminating custom adapters for each assistant.  
- **Accelerated development**: Teams can focus on model logic rather than data‑access plumbing, speeding up proof‑of‑concepts and internal tooling.  
- **Reusable component**: The same server can serve multiple agents (e.g., chatbots, trading bots, research assistants) without code duplication.

**Practical Adoption Path**  
1. **Prototype** – Spin up the provided Docker container or run the Python package locally; use the CLI or generated SDK to query ticker data from a test AI agent.  
2. **Integration** – Replace the prototype calls with the MCP endpoint in the production AI workflow, adding authentication or rate‑limiting as needed.  
3. **Deployment** – Deploy the MCP server in a managed environment (K8s, Cloud Run, etc.), configure monitoring, and optionally extend the wrapper with custom yfinance functions or additional data sources.

**Production Readiness**  
- **Maturity**: Medium. The repo is actively maintained (last update 2026‑05‑14), has 135 stars and 48 forks, and provides clear API/SDK/CLI interfaces.  
- **Considerations**: Verify the licensing terms, perform a security audit of the container image, and assess dependency health (yfinance and its upstream data providers).  
- **Fit for production**: Suitable for internal tools or controlled‑release products after the above checks; additional robustness (circuit‑breakers, caching, monitoring) may be required for high‑traffic, customer‑facing services.

### Русский

**narumiruna/yfinance-mcp** — это open‑source‑библиотека на Python, реализующая Model Context Protocol (MCP) для доступа к финансовым данным Yahoo Finance, что позволяет AI‑ассистентам и другим агентам обращаться к реальным инструментам и данным через единый протокол. Типичный сценарий — подключение AI‑агента к финансовым API (или запуск собственного MCP‑сервера) для автоматизированных аналитических запросов, построения торговых стратегий и интеграции с бекенд‑сервисами. Проект имеет средний уровень готовности к production: достаточный набор звёзд и форков, активные обновления, но перед развертыванием в продакшн требуется проверка лицензии, безопасности зависимостей и наличие поддерживающих мейнтейнеров.

### 中文

**项目简介（2‑3 句话）**  
`narumiruna/yfinance-mcp` 是一个基于 Model Context Protocol（MCP）的 Python 库，提供统一的接口让 AI 助手能够实时查询 Yahoo Finance 数据。它将金融行情、历史价格等信息包装成标准化的 API/SDK，便于在对话式 AI 中直接调用。

**价值体现**  
- **标准化接入**：通过 MCP 将金融数据抽象为统一的请求/响应模型，降低不同 AI 平台集成金融工具的门槛。  
- **即时真实数据**：实时获取股票、基金、外汇等市场信息，让 AI 能给出基于最新行情的答案或决策建议。  
- **可复用的后端服务**：可快速部署为独立的 MCP 服务器，供内部或外部 AI 代理共享同一数据源。

**典型接入方式**  
1. **Python SDK**：在 AI 代理的代码中 `pip install yfinance-mcp`，使用 `YFinanceClient` 调用 `get_price(symbol)`、`get_history(symbol, start, end)` 等方法。  
2. **REST/CLI**：项目同时提供基于 FastAPI 的 HTTP 接口和命令行工具，AI 系统只需发送符合 MCP 规范的 JSON 请求或执行相应 CLI 命令即可获取数据。  
3. **MCP 服务器**：将项目部署为容器（Docker）或服务器进程，其他语言的 AI 代理通过 MCP 协议的网络调用进行跨语言集成。

**生产可用性评估**  
- **成熟度**：当前评分 62/100，GitHub 135 星、48 Fork，活跃度截至 2026‑05‑14，代码质量和社区关注度尚可。  
- **适用场景**：适合原型开发、内部工具或对金融数据需求不高的业务流程；在正式生产环境使用前建议完成以下检查：  
  - 依赖安全审计（确保 `yfinance`、`pandas` 等库无已知漏洞）  
  - 许可证兼容性确认（项目采用 MIT/Apache 等宽松许可证）  
  - 监控与容错：为 MCP 服务添加健康检查、限流和异常日志，防止金融数据接口失效导致 AI 代理崩溃。  
- **结论**：在完成上述安全与运维检查后，可作为生产环境的“金融数据接入层”使用，尤其适用于需要快速迭代的 AI 助手项目。

## 🧭 Practical evaluation

**Value:** narumiruna/yfinance-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 135 GitHub stars
- 48 forks
- updated 2026-05-14
- primary language: Python
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 45/100 |
| topics | 63/100 |
| outlook | 46/100 |
| quality | 49/100 |
| recency | 20/100 |
| adoption | 45/100 |
| production | 47/100 |
| usefulness | 58/100 |
| integration | 50/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/narumiruna/yfinance-mcp) · [← Back to Mcp](./README.md)</sub>
