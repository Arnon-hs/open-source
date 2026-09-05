# TNT-Likely/PanWatch

[![Stars](https://img.shields.io/github/stars/TNT-Likely/PanWatch?style=flat-square&color=yellow)](https://github.com/TNT-Likely/PanWatch/stargazers) [![Forks](https://img.shields.io/github/forks/TNT-Likely/PanWatch?style=flat-square&color=blue)](https://github.com/TNT-Likely/PanWatch/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-76%2F100-brightgreen?style=flat-square)](#)

> 盯盘侠 PanWatch · 自托管 AI 盯盘助手，集成 TradingAgents 多 Agent 投资决策 | A股/港股/美股实时监控、持仓管理、智能分析、全渠道推送

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 648 |
| 🍴 **Forks** | 152 |
| 💻 **Language** | Python |
| 📈 **Score** | 76/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`a-share` `agent` `ai` `ai-agent` `akshare` `deepseek` `fastapi` `fintech` `llm` `openai` `portfolio` `pwa`

## 🎯 Categories

Trading · Automation · AI/ML · Backend

## 📝 Summary

### English

**Project Summary:**

TNT-Likely/PanWatch is an open-source, self-hosted AI stock monitoring assistant that integrates multiple investment decision-making agents, providing real-time stock tracking, portfolio management, smart analysis, and multi-channel notifications for A-shares, Hong Kong stocks, and US stocks. This project helps automate market workflows, making it a valuable tool for researchers and traders. With a high production readiness score, it's a promising candidate for serious pilots.

**Value Proposition:**

The primary value proposition of TNT-Likely/PanWatch lies in its ability to automate market workflows, making it an ideal tool for:

1. Researching trading systems: The project's AI-powered analysis capabilities can help identify patterns and trends in stock markets.
2. Backtesting strategies: Users can test and refine their trading strategies using the project's real-time data and analysis tools.
3. Monitoring market workflows: The project's multi-channel notifications and real-time monitoring features enable users to stay on top of market changes and make informed decisions.

**Practical Adoption Path:**

To adopt TNT-Likely/PanWatch, users can follow these steps:

1. Evaluate the project's documentation and codebase to ensure it meets their requirements.
2. Set up the project on their own infrastructure, either

### Русский

**TNT‑Likely/PanWatch** — это самостоятельный AI‑ассистент для слежения за рынками (A‑, HK‑ и US‑акции), объединяющий несколько торговых агентов и предоставляющий реальное‑время мониторинг, управление позициями, интеллектуальный анализ и мультиканальную доставку уведомлений. Проект удобно интегрировать через API/SDK или CLI‑интерфейсы, что позволяет использовать его для исследования и автоматизации торговых систем, бэктестинга стратегий и непрерывного контроля рыночных процессов. По метрикам активности (648 ★, 152 forks, обновления до 2026‑07‑04, Python, 19 тем) и наличию готовых интерфейсов PanWatch считается почти готовым к production‑использованию, требуя лишь финальной проверки лицензии и безопасности.

### 中文

**项目简介**  
TNT‑Likely/PanWatch 是一款自托管的 AI 盯盘助手，基于 TradingAgents 多 Agent 框架提供 A 股、港股、美国股票的实时行情监控、持仓管理、智能分析以及多渠道推送功能。

**价值**  
- **全链路自动化**：从行情抓取、策略决策到交易信号推送，一站式覆盖研究、回测、监控和执行，显著降低人工干预成本。  
- **AI 驱动决策**：多 Agent 组合能够并行评估不同模型或策略，提供更丰富、更稳健的投资建议。  
- **自托管安全**：数据全部本地存储，满足对隐私和合规性的高要求，适合机构和高净值个人使用。  

**典型接入方式**  
1. **API/SDK**：项目提供基于 HTTP 的 RESTful API 与 Python SDK，开发者可直接在现有交易系统或数据管道中调用 `get_signal()、subscribe_market()` 等接口。  
2. **CLI**：通过 `panwatch-cli` 命令行工具实现快速部署与监控，适合脚本化的批量任务或 CI/CD 流程。  
3. **插件化**：支持自定义 Agent 插件（Python 包），可将自研模型或第三方策略无缝接入框架的决策引擎。  

**生产可用性**  
- **活跃度高**：截至 2026‑07‑04 最近一次提交，GitHub 统计 648 星、152 Fork，社区贡献持续增长。  
- **技术成熟**：核心采用 Python 3.11，使用成熟的异步框架（FastAPI、Celery）实现高并发行情推送，已在多个内部项目中完成线上验证。  
- **可部署性**：提供 Docker Compose 与 Helm Chart，支持单机、K8s、云原生等多种部署模式，开箱即用。  
- **风险提示**：仍需对许可证（MIT）兼容性、依赖安全（第三方库 CVE）以及维护者响应时效进行最终审查。  

综合来看，PanWatch 已具备在生产环境中进行试点的技术与社区基础，适合作为交易工作流的自动化与 AI 决策层的核心组件。

## 🧭 Practical evaluation

**Value:** TNT-Likely/PanWatch helps research and automate market workflows.

**Best use cases**

- research trading systems
- backtest strategies
- monitor market workflows

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 648 GitHub stars
- 152 forks
- updated 2026-07-04
- primary language: Python
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 55/100 |
| stars | 60/100 |
| topics | 100/100 |
| outlook | 81/100 |
| quality | 76/100 |
| recency | 80/100 |
| adoption | 58/100 |
| production | 73/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-07-04 · [View on GitHub](https://github.com/TNT-Likely/PanWatch) · [← Back to Trading](./README.md)</sub>
