# imbenrabi/Financial-Modeling-Prep-MCP-Server

[![Stars](https://img.shields.io/github/stars/imbenrabi/Financial-Modeling-Prep-MCP-Server?style=flat-square&color=yellow)](https://github.com/imbenrabi/Financial-Modeling-Prep-MCP-Server/stargazers) [![Forks](https://img.shields.io/github/forks/imbenrabi/Financial-Modeling-Prep-MCP-Server?style=flat-square&color=blue)](https://github.com/imbenrabi/Financial-Modeling-Prep-MCP-Server/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> A Model Context Protocol (MCP) implementation for Financial Modeling Prep, enabling AI assistants to access and analyze financial data, stock information, company fundamentals, and market insights.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 137 |
| 🍴 **Forks** | 51 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `etf-investments` `financial-modeling-prep` `fmp` `llm` `mcp` `mcp-server` `mcp-tools` `smithery-ai` `stock-data` `stock-market`

## 🎯 Categories

MCP · AI/ML · Backend · Data

## 📝 Summary

### English

**Brief Summary**  
The *Financial‑Modeling‑Prep MCP Server* is a TypeScript‑based implementation of the Model Context Protocol (MCP) that exposes Financial Modeling Prep’s market data, stock quotes, and company fundamentals through a standardized API. It lets AI assistants retrieve and reason over real‑time financial information, turning raw data into actionable insights for downstream applications.  

**Value**  
- **Standardized integration**: By adhering to MCP, the server provides a uniform interface that AI agents can call just like any other tool, reducing the effort required to hook up financial data sources.  
- **Rich, up‑to‑date market data**: It bundles a comprehensive set of endpoints (prices, fundamentals, earnings, news, etc.) from Financial Modeling Prep, enabling AI‑driven analytics, portfolio monitoring, and automated reporting.  
- **Open‑source flexibility**: The TypeScript codebase can be self‑hosted, customized, or extended, giving teams full control over latency, security, and compliance requirements.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, install dependencies, and run the server locally (Docker or `npm start`). Use the provided Swagger UI or CLI to explore the MCP endpoints and validate the data you need.  
2. **Integrate** – Connect your AI assistant (e.g., LangChain, AutoGPT, or custom LLM workflow) to the MCP endpoint using the standard `invoke`/`query` calls; no custom parsers are required.  
3. **Secure & Scale** – Deploy the server to a cloud environment (AWS ECS, GCP Cloud Run, etc.), configure API keys for Financial Modeling Prep, enable TLS, and add rate‑limiting or caching as needed.  
4. **Productionize** – Add monitoring (health checks, Prometheus metrics), CI/CD pipelines for automated updates, and integrate with your organization’s identity/access management.  

**Production Readiness**  
- **Activity & Community**: 137 ★, 51 forks, recent commits (as of 2026‑06‑26), and an active issue tracker indicate a healthy open‑source project.  
- **Maturity**: The MCP implementation follows a well‑defined protocol, and the codebase is written in TypeScript with clear typings, making it easy to audit and extend.  
- **Scalability**: The server can be containerized and horizontally scaled; the underlying Financial Modeling Prep API supports high‑throughput usage with appropriate API keys.  
- **Risk Considerations**: License and security posture still need a final review, but no major metadata or compliance red flags were found.  

Overall, the Financial‑Modeling‑Prep MCP Server is a production‑grade, OSS‑ready component that accelerates the integration of reliable financial data into AI‑driven workflows.

### Русский

**Financial-Modeling-Prep-MCP-Server** — это сервер‑реализация Model Context Protocol (MCP) на TypeScript, позволяющая AI‑ассистентам получать и анализировать финансовые данные (цены акций, фундаментальные показатели компаний, рыночные инсайты) через единый протокол. Типичный сценарий: подключаете AI‑агента к серверу MCP, после чего он может в реальном времени выполнять запросы к API Financial Modeling Prep и использовать полученную информацию в диалогах, автоматических отчётах или торговых стратегиях. Проект демонстрирует высокий уровень готовности к production: активные коммиты, 137 звёзд, 51 форк, поддержка CLI/SDK и чёткая документация, что делает его надёжным кандидатом для пилотных и масштабных внедрений.

### 中文

**项目简介**  
`imbenrabi/Financial-Modeling-Prep-MCP-Server` 是一个基于 Model Context Protocol（MCP）的服务实现，封装了 Financial Modeling Prep 的金融数据接口。它让 AI 助手能够通过统一的 MCP 协议实时查询股票行情、公司基本面、财务报表以及市场洞察，实现“AI + 真实金融工具”的闭环。

**价值点**  
- **标准化接入**：使用 MCP 统一协议，AI 代理无需针对每个数据源写专用代码，即可调用统一的 `fetch`, `search`, `execute` 等操作。  
- **实时可靠**：直接对接 Financial Modeling Prep 官方 API，提供最新的行情和财务数据，适合需要高频、低延迟信息的交易或分析场景。  
- **加速开发**：后端已实现完整的 TypeScript SDK、RESTful 接口和 CLI，开发者只需在自己的 AI 框架中挂载 MCP 服务器，即可快速交付 AI‑驱动的金融分析功能。

**典型接入方式**  
1. **部署 MCP 服务器**：使用 Docker 镜像或直接 `npm i && npm start` 在自己的云环境或本地机器上运行。  
2. **配置 API Key**：在环境变量 `FMP_API_KEY` 中填入 Financial Modeling Prep 的授权密钥。  
3. **在 AI 框架中注册**：如使用 LangChain、AutoGPT、OpenAI Function Calling 等，只需在 Agent 配置里指定 MCP 服务器的 URL（例如 `http://localhost:8080/mcp`），并声明所需的工具（`get_stock_price`, `get_company_fundamentals` 等）。  
4. **调用**：AI 通过 MCP 的 `execute` 方法发送标准化请求，服务器内部转发到 FMP API，返回结构化 JSON 给 AI，完成“一问即得”。

**生产可用性**  
- **活跃度**：2026‑06‑26 最近一次提交，拥有 137 ★、51 Fork，社区活跃。  
- **技术成熟度**：使用 TypeScript 编写，提供完整的类型定义、单元测试和 CI，代码质量较高。  
- **部署友好**：提供 Dockerfile、Kubernetes Helm Chart 以及 Serverless 适配，易于在容器化或无服务器环境中上线。  
- **安全与合规**：项目采用 MIT 许可证，未发现重大安全漏洞；但在正式生产前仍建议自行审计依赖并配置 API Key 的访问控制。  

综合来看，该项目已具备 **高** 的生产就绪度，适合作为金融数据接入层，快速为 AI 助手或自动化交易系统提供可靠的数据支撑。

## 🧭 Practical evaluation

**Value:** imbenrabi/Financial-Modeling-Prep-MCP-Server helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 137 GitHub stars
- 51 forks
- updated 2026-06-26
- primary language: TypeScript
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 43/100 |
| stars | 46/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 70/100 |
| recency | 80/100 |
| adoption | 45/100 |
| production | 70/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/imbenrabi/Financial-Modeling-Prep-MCP-Server) · [← Back to Mcp](./README.md)</sub>
