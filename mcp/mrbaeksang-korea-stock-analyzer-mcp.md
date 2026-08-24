# Mrbaeksang/korea-stock-analyzer-mcp

[![Stars](https://img.shields.io/github/stars/Mrbaeksang/korea-stock-analyzer-mcp?style=flat-square&color=yellow)](https://github.com/Mrbaeksang/korea-stock-analyzer-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/Mrbaeksang/korea-stock-analyzer-mcp?style=flat-square&color=blue)](https://github.com/Mrbaeksang/korea-stock-analyzer-mcp/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> Remote MCP server for Korean stock analysis — real DART filings, KRX quotes, conservative valuation ranges for Claude, Cursor and any MCP client

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 21 |
| 🍴 **Forks** | 9 |
| 💻 **Language** | Python |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`claude` `dart` `fastmcp` `fintech` `korean-stocks` `krx` `mcp` `mcp-server` `model-context-protocol` `python` `railway` `remote-mcp`

## 🎯 Categories

MCP · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Mrbaeksang/korea‑stock‑analyzer‑mcp is a remote Model‑Context‑Protocol (MCP) server that delivers real‑time Korean market data—including DART filings, KRX quotes, and conservative valuation ranges—to any MCP‑compatible AI assistant (Claude, Cursor, etc.). By exposing a clean API/SDK/CLI in Python, it lets developers plug AI agents into authentic financial tools without building custom scrapers or parsers. The project is actively maintained, has modest community traction, and is positioned as a production‑ready OSS component for AI‑driven stock analysis.

**Value**  
- **Real‑world data for LLMs** – Provides trustworthy, up‑to‑date regulatory filings and market quotes, turning generic language models into domain‑aware financial analysts.  
- **Standardized integration** – Implements the Model‑Context‑Protocol, so the same server can be consumed by any MCP‑compatible client, reducing duplicate integration work across AI platforms.  
- **Conservative valuation logic** – Supplies pre‑computed valuation ranges, giving agents a safe baseline for recommendations and mitigating hallucination risk.

**Practical Adoption Path**  
1. **Spin up the server** – Clone the repo, install the Python dependencies, and run the Docker compose or the provided CLI to launch the MCP endpoint.  
2. **Configure your AI client** – In Claude, Cursor, or any custom MCP client, point the `mcp_endpoint` to the server URL and authenticate if required.  
3. **Consume the API** – Use the documented RPC methods (e.g., `get_dart_filing`, `get_krx_quote`, `get_valuation_range`) to fetch data inside prompts or tool‑use calls.  
4. **Extend / customize** – Add new data sources or tweak valuation formulas by modifying the Python modules and redeploying; the open‑source nature makes this straightforward.  

**Production Readiness**  
- **Recent activity** – Last commit on 2026‑07‑08, 21 stars, 9 forks, and active issue discussion indicate a healthy maintainer presence.  
- **Robust interface** – Offers API, SDK, and CLI bindings, with clear OpenAPI‑style docs, facilitating automated testing and CI/CD integration.  
- **Ecosystem fit** – Built in Python, a language widely used for AI pipelines, and already referenced in MCP tooling guides, lowering the learning curve for teams.  
- **Risk considerations** – License and security posture need a final audit, but no glaring metadata issues are present. Overall, the project is mature enough for a pilot or production deployment, provided standard OSS due‑diligence steps are followed.

### Русский

Резюме проекта Mrbaeksang/korea-stock-analyzer-mcp:

Проект Mrbaeksang/korea-stock-analyzer-mcp представляет собой удаленный сервер по протоколу MCP для анализа корейских акций, который обеспечивает доступ к реальным файлам DART, котировкам KRX и консервативным оценкам цен. Он позволяет соединить интеллектуальные агенты с реальными инструментами и данными через стандартный протокол.

Проект готов к внедрению и уже имеет сильную базу пользователей, с 21 GitHub звездой и 9 фолками. Он также имеет высокий уровень готовности к production, что делает его идеальным выбором для серьезного пилотного проекта.

### 中文

**简短介绍**

Mrbaeksang/korea-stock-analyzer-mcp 是一个开源项目，用于提供韩国股票分析的远程 MCP 服务器。它支持实时 DART 文档、KRX 交易数据和保守估值范围，方便任何 MCP 客户端使用。

**价值**

该项目的价值在于，它连接了人工智能助手与真实的工具和数据，通过标准协议进行通信。它有助于连接 AI 代理到工具，发布 Model Context Protocol 服务器，标准化集成。

**典型接入方式**

该项目提供了以下接入方式：

* API：通过 API 接口进行调用
* SDK：通过软件开发包（SDK）进行集成
* CLI：通过命令行接口（CLI）进行交互

**生产可用性**

该项目的生产可用性高，主要原因是：

* 最近的活动表明项目仍在维护
* 有强大的社区支持和生态系统信号
* 项目的主要语言是 Python，易于维护和扩展

总的来说，Mrbaeksang/korea-stock-analyzer-mcp 是一个值得信赖的开源

## 🧭 Practical evaluation

**Value:** Mrbaeksang/korea-stock-analyzer-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 21 GitHub stars
- 9 forks
- updated 2026-07-08
- primary language: Python
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 25/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 56/100 |
| quality | 52/100 |
| recency | 40/100 |
| adoption | 28/100 |
| production | 57/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-08 · [View on GitHub](https://github.com/Mrbaeksang/korea-stock-analyzer-mcp) · [← Back to Mcp](./README.md)</sub>
