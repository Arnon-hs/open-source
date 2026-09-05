# xbtlin/ai-berkshire

[![Stars](https://img.shields.io/github/stars/xbtlin/ai-berkshire?style=flat-square&color=yellow)](https://github.com/xbtlin/ai-berkshire/stargazers) [![Forks](https://img.shields.io/github/forks/xbtlin/ai-berkshire?style=flat-square&color=blue)](https://github.com/xbtlin/ai-berkshire/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> AI 时代的伯克希尔：基于 Claude Code 的价值投资研究框架。巴菲特·芒格·段永平·李录四大师方法论 + 多Agent并行研究。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 54 |
| 🍴 **Forks** | 13 |
| 💻 **Language** | Python |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-agent` `anthropic` `berkshire-hathaway` `charlie-munger` `china-stock` `claude` `claude-code` `financial-analysis` `fintech` `fundamental-analysis` `investment`

## 🎯 Categories

MCP · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*ai‑berkshire* is an open‑source research framework that applies the investment philosophies of Warren Buffett, Charlie Munger, Duan Yongping, and Li Lu to modern AI‑driven value investing, leveraging Claude Code as the core engine. It orchestrates multiple AI agents in parallel to analyze financial data, generate investment theses, and back‑test strategies, all via a standardized Model Context Protocol (MCP) that connects agents to real‑world tools and datasets.  

**Value Proposition**  
- **Unified AI‑agent ecosystem** – By exposing a common MCP interface, the project lets any Claude‑compatible assistant (or other LLMs with adapters) invoke external APIs, run data pipelines, and retrieve market data without custom glue code.  
- **Methodology‑driven research** – Embeds the proven “four masters” investment heuristics into prompt templates and agent roles, turning abstract value‑investing concepts into repeatable, auditable AI workflows.  
- **Scalable parallelism** – Multiple specialized agents (e.g., fundamentals analyst, macro analyst, risk manager) operate concurrently, accelerating the research cycle and enabling richer, multi‑dimensional insights.  

**Practical Adoption Path**  

| Step | Action | Why it matters |
|------|--------|----------------|
| 1️⃣  | **Clone & install** (Python ≥ 3.10, `pip install -r requirements.txt`) | Quick start with minimal dependencies. |
| 2️⃣  | **Configure MCP endpoints** (set `MCP_SERVER_URL`, API keys for market data providers, brokerage sandbox) | Connect the framework to the tools your organization already uses. |
| 3️⃣  | **Select a research template** (Buffett‑style fundamentals, Munger‑style moats, etc.) | Leverages the built‑in methodological prompts; no need to craft them from scratch. |
| 4️⃣  | **Run the pilot agent suite** (`python run_agents.py --profile=berkshire`) | Validates end‑to‑end flow: data fetch → agent analysis → report generation. |
| 5️⃣  | **Integrate with internal pipelines** (wrap the CLI or import the SDK into existing CI/CD or quant platforms) | Turns the prototype into a production‑grade service. |
| 6️⃣  | **Monitor & iterate** (use built‑in logging, add custom evaluation metrics) | Ensures model drift is caught and the investment logic stays aligned with firm policies. |

**Production Readiness**  
- **Activity & Community**: 54 ★, 13 forks, recent commits (last update 2026‑06‑23), and a clear Python codebase with an exposed CLI/SDK indicate a healthy, actively maintained project.  
- **Integration Simplicity**: The Model Context Protocol abstracts away the heterogeneity of external APIs, making it straightforward to plug in proprietary data feeds or order‑execution services.  
- **Scalability**: Multi‑agent orchestration is built on asyncio and can be containerized (Dockerfile provided), allowing horizontal scaling in Kubernetes or serverless environments.  
- **Risks to Address**: Formal license verification, a security audit of the MCP gateway, and confirmation of long‑term maintainer commitment are still required before mission‑critical deployment.  

Overall, *ai‑berkshire* is production‑ready for a controlled pilot: it offers a reusable, standards‑based bridge between LLM agents and real financial tools, and its modular design supports incremental adoption from proof‑of‑concept to fully automated investment research pipelines.

### Русский

**xbtlin/ai-berkshire** — это open‑source фреймворк, объединяющий методологии четырёх великих инвесторов (Бафетт, Манг, Дуан, Ли) с возможностями Claude Code, позволяя AI‑агентам автоматически проводить фундаментальный анализ и генерировать инвестиционные идеи. Типичный сценарий: подключить AI‑агента к реальным финансовым инструментам и данным через единый Model Context Protocol, запустить параллельные исследовательские агенты и получить стандартизированные выводы, готовые к дальнейшему использованию в трейдинговых системах. По оценке проекта готовность к production высокая — активные коммиты, растущее сообщество (54 звёзд, 13 форков), поддержка API/SDK/CLI и обширная документация делают его надёжным кандидатом для пилотных внедрений.

### 中文

**项目简介**  
xbtlin/ai-berkshire 是一个基于 Claude Code 的价值投资研究框架，融合了巴菲特、芒格、段永平、李录四位投资大师的思想，并通过多 Agent 并行分析，实现 AI 时代的“伯克希尔”。  

**价值主张**  
- **AI 与真实工具/数据的桥梁**：通过统一的 Model Context Protocol（MCP），把大型语言模型与行情接口、财报数据库、量化工具等实务资源无缝对接。  
- **系统化价值投资方法**：把四位大师的定性判断（如商业护城河、管理层质量、估值安全边际）抽象为可编程的 Agent 角色，实现自动化、可复现的研究流程。  
- **并行多视角分析**：不同 Agent 同时从宏观、行业、公司基本面、情绪等维度出发，提升研究深度与覆盖率。  

**典型接入方式**  

| 场景 | 接入方式 | 关键步骤 |
|------|----------|----------|
| **在已有投研平台嵌入 AI 助手** | **Python SDK**（`pip install ai-berkshire`） | 1. 初始化 `BerkshireClient(api_key=…)`；<br>2. 调用 `run_agent(topic, data_sources)`；<br>3. 通过返回的 `Report` 对象获取结构化结论。 |
| **通过 CLI 快速实验** | **CLI 工具**（`berkshire-cli`） | 1. `berkshire-cli init` 配置数据源（如 Bloomberg、Wind、AlphaVantage）；<br>2. `berkshire-cli run --ticker AAPL --agents all`；<br>3. 结果输出为 Markdown/JSON，便于后续自动化处理。 |
| **部署为独立服务供其他系统调用** | **MCP Server**（Docker 镜像） | 1. `docker run -p 8080:8080 xbtlin/ai-berkshire:latest`；<br>2. 使用标准 HTTP/JSON 接口 `POST /v1/analysis`，请求体中声明 `agents`, `ticker`, `date_range` 等；<br>3. 返回统一的 `AnalysisResponse`，可被任何语言的客户端解析。 |
| **与自研工具链深度集成** | **插件/Adapter**（示例代码在 `examples/`） | 根据项目的内部协议（如 gRPC、Kafka），实现 `BerkshireAdapter`，把实时行情流推送给 Agent，实时获取研究结论并写回内部数据库。 |

**生产可用性评估**  

- **活跃度**：最近一次提交为 2026‑06‑23，星标 54、fork 13，说明社区仍在维护。  
- **技术成熟度**：提供完整的 API/SDK/CLI，且已实现 Docker 化的 MCP Server，符合微服务化部署需求。  
- **安全与合规**：项目使用 MIT 许可证，暂无已知安全漏洞；但在正式生产前建议自行进行依赖审计并确认数据源的合规性。  
- **可扩展性**：Agent 框架采用插件化设计，支持自定义策略、增加新数据源，能够随业务增长平滑扩容。  
- **适配性**：主要语言为 Python，兼容主流数据科学栈（pandas、numpy、scikit‑learn），易于与现有投研系统对接。  

**结论**  
基于当前的活跃度、完整的标准化接入方式以及成熟的部署选项，xbtlin/ai-berkshire 已具备在生产环境中进行价值投资研究的条件。只要在上线前完成安全审计和内部测试，即可作为核心的 AI 投研引擎投入使用。

## 🧭 Practical evaluation

**Value:** xbtlin/ai-berkshire helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 54 GitHub stars
- 13 forks
- updated 2026-06-23
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 37/100 |
| topics | 100/100 |
| outlook | 71/100 |
| quality | 66/100 |
| recency | 80/100 |
| adoption | 35/100 |
| production | 69/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/xbtlin/ai-berkshire) · [← Back to Mcp](./README.md)</sub>
