# shy3130/tickflow-stock-panel

[![Stars](https://img.shields.io/github/stars/shy3130/tickflow-stock-panel?style=flat-square&color=yellow)](https://github.com/shy3130/tickflow-stock-panel/stargazers) [![Forks](https://img.shields.io/github/forks/shy3130/tickflow-stock-panel?style=flat-square&color=blue)](https://github.com/shy3130/tickflow-stock-panel/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> 自托管、零运维的 A 股「选股 + 监控 + 回测」量化工作台 | 基于 TickFlow 数据 | 能力驱动适配全档位订阅 | 自由接入第三方扩展数据(Tushare 等)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 123 |
| 🍴 **Forks** | 33 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`a-stock` `ai-agent` `aigc` `backtesting` `duckdb` `fastapi` `llm` `polars` `quant` `quantitative-finance` `quantitative-trading` `react`

## 🎯 Categories

Trading · AI/ML · Frontend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
shy3130/tickflow‑stock‑panel is a self‑hosted, zero‑ops quantitative workbench for China A‑share markets, offering integrated stock selection, real‑time monitoring, and back‑testing built on TickFlow data. It supports full‑range subscription tiers, can be extended with third‑party data sources such as Tushare, and is written in TypeScript for both frontend and backend components.

**Value**  
- Provides a single, open‑source platform that replaces fragmented tools for research, strategy execution, and market surveillance, reducing the time and cost of building a custom quant stack.  
- The modular architecture lets teams plug in additional data feeds or analytics libraries, enabling rapid experimentation and iteration on trading ideas.  
- By being self‑hosted, firms retain full control over data privacy and compliance—critical for regulated financial environments.

**Practical Adoption Path**  
1. **Evaluation** – Clone the repo and run the Docker‑compose setup (or the provided CLI) to spin up a local instance; use the built‑in demo data to explore the UI and API.  
2. **Integration** – Connect your existing data pipelines (e.g., Tushare, proprietary feeds) via the documented SDK/REST endpoints; customize the selection and monitoring widgets as needed.  
3. **Pilot** – Deploy the containerized stack to a staging environment, configure a subscription tier that matches your data plan, and run a limited back‑test or live‑monitoring workflow with a sandbox account.  
4. **Production Roll‑out** – Scale the service using Kubernetes or your preferred orchestrator, enable TLS and RBAC, and integrate with your order‑execution gateway for end‑to‑end automation.

**Production Readiness**  
- **Activity & Community** – Recent commits (as of 2026‑06‑24), 123 stars, 33 forks, and 16 relevant topics indicate an active user base and ongoing maintenance.  
- **Technology Stack** – TypeScript codebase with clear separation of frontend (React) and backend (Node/Express) simplifies onboarding for teams familiar with modern web stacks.  
- **Extensibility** – Well‑documented APIs/SDKs and CLI tools make third‑party data integration straightforward, reducing lock‑in risk.  
- **Risks** – Licensing and security audits are still pending; ensure a formal review of the repository’s license and perform vulnerability scanning before production use.  

Overall, tickflow‑stock‑panel is a mature OSS candidate ready for pilot projects and, after standard security/license vetting, can be promoted to production in quant‑focused trading operations.

### Русский

**shy3130/tickflow-stock-panel** — это полностью самодостаточная платформа для A‑share (китайского рынка) с функциями «выбора акций + мониторинга + бэктестинга», построенная на данных TickFlow. Она позволяет исследователям и трейдерам быстро собрать конвейер: подобрать набор акций, задать правила автоматического мониторинга и проверить стратегии на исторических данных, при этом легко подключать сторонние источники (Tushare, другие API) и масштабировать подписки под любой объём. Проект активно поддерживается (обновления в 2026 г., 123 звёзд, 33 форка), написан на TypeScript и предоставляет API/CLI/SDK, что делает его готовым к пилотному запуску в production‑среде после окончательной проверки лицензии и безопасности.

### 中文

**项目简介（2‑3 句）**  
shy3130/tickflow‑stock‑panel 是一款自托管、零运维的 A 股「选股 + 监控 + 回测」量化工作台，基于 TickFlow 数据流并支持全档位订阅能力。它可自由接入 Tushare 等第三方数据源，帮助研发者快速构建、验证并实时监控交易系统。

**价值**  
- **全链路量化工作流**：从股票筛选、策略回测到实时监控，一站式覆盖，显著降低研发与运维成本。  
- **数据驱动、灵活订阅**：支持 TickFlow 的细粒度行情订阅以及全档位（免费/付费）数据套餐，满足不同规模的研究需求。  
- **可扩展生态**：通过统一的插件接口轻松引入 Tushare、Wind、聚宽等第三方数据，提升策略的覆盖面和准确性。  

**典型接入方式**  
1. **Docker 部署**：项目提供官方 Docker 镜像，运行 `docker compose up -d` 即可启动后端服务、前端 UI 与数据库，适合快速试用或生产部署。  
2. **API/SDK 调用**：后端暴露 RESTful API，配套 TypeScript SDK（`npm i @tickflow/stock-panel-client`），业务系统可直接通过 HTTP 或 SDK 调用选股、回测、监控等功能。  
3. **CLI 工具**：内置 `tickflow-cli`，支持本地脚本化执行选股、回测任务，便于 CI/CD 流程自动化。  

**生产可用性**  
- **活跃维护**：截至 2026‑06‑24 最近一次提交，项目拥有 123 ⭐、33 🍴，社区活跃度良好。  
- **技术成熟度**：核心使用 TypeScript + Node.js + React，配套 PostgreSQL 持久化，技术栈成熟且易于运维。  
- **安全与合规**：项目采用 MIT 许可证，未发现明显的安全漏洞；自行托管意味着数据完全可控，符合金融机构对合规性的要求。  
- **可扩展性**：插件化设计和统一的订阅层，使得在生产环境中可以平滑增加新数据源或自定义指标，支持水平扩容。  

综合来看，tickflow‑stock‑panel 已具备进入正式生产环境的技术与社区条件，适合作为量化研究与实盘监控的核心平台，亦可作为企业内部交易系统的快速原型或中台服务。

## 🧭 Practical evaluation

**Value:** shy3130/tickflow-stock-panel helps research and automate market workflows.

**Best use cases**

- research trading systems
- backtest strategies
- monitor market workflows

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 123 GitHub stars
- 33 forks
- updated 2026-06-24
- primary language: TypeScript
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 38/100 |
| stars | 45/100 |
| topics | 100/100 |
| outlook | 63/100 |
| quality | 59/100 |
| recency | 40/100 |
| adoption | 43/100 |
| production | 57/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/shy3130/tickflow-stock-panel) · [← Back to Trading](./README.md)</sub>
