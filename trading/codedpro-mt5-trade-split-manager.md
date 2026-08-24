# codedpro/mt5-trade-split-manager

[![Stars](https://img.shields.io/github/stars/codedpro/mt5-trade-split-manager?style=flat-square&color=yellow)](https://github.com/codedpro/mt5-trade-split-manager/stargazers) [![Forks](https://img.shields.io/github/forks/codedpro/mt5-trade-split-manager?style=flat-square&color=blue)](https://github.com/codedpro/mt5-trade-split-manager/network) [![Language](https://img.shields.io/badge/lang-MQL5-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> 🤖 AI-Agent Friendly MT5 Expert Advisor with intelligent order splitting, automatic trailing stops, and REST API. Perfect for Gold/Silver trading with Claude AI integration. Split orders 60/10/10/10/10 for maximum profit optimization.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 53 |
| 🍴 **Forks** | 15 |
| 💻 **Language** | MQL5 |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `algorithmic-trading` `automated-trading` `claude-ai` `expert-advisor` `fastapi` `forex-bot` `gold-trading` `metatrader5` `mql5` `mt5` `python-trading`

## 🎯 Categories

Trading · Automation · AI/ML · Backend

## 📝 Summary

### English

**Project Summary**

The codedpro/mt5-trade-split-manager is an open-source project that provides an AI-Agent Friendly MT5 Expert Advisor for optimizing gold and silver trading with Claude AI integration. This project enables users to split orders for maximum profit optimization, featuring intelligent order splitting, automatic trailing stops, and a REST API. It is suitable for researchers and traders who want to automate market workflows.

**Value Proposition**

The codedpro/mt5-trade-split-manager offers several values to users, including:

* Research and automation of market workflows
* Ability to backtest trading strategies and monitor market workflows
* Integration with Claude AI for optimized trading decisions

**Practical Adoption Path**

To adopt this project, users can follow these steps:

1. Evaluate the project's implementation signals, such as API/SDK/CLI, language metadata, or focused topics.
2. Review the project's code and documentation to understand its functionality and potential use cases.
3. Test the project's features, such as intelligent order splitting and automatic trailing stops, to ensure they meet their needs.
4. Integrate the project with their existing trading systems and Claude AI setup.
5. Monitor and adjust the project's settings as needed to optimize their trading performance.

**Production Readiness**

The codedpro/mt5-trade-split

### Русский

**codedpro/mt5-trade-split-manager** — это открытый MT5‑EA, оптимизированный для торговли золотом и серебром, который автоматически разбивает ордера по схеме 60/10/10/10/10, применяет интеллектуальные трейлинг‑стопы и предоставляет REST‑API для интеграции с Claude AI и другими системами. Типичный сценарий: исследователь или трейдер подключает EA к MetaTrader 5, задаёт параметры стратегии, а менеджер автоматически распределяет позиции, отслеживает их и позволяет управлять процессом через API/CLI для бэктестов, мониторинга и автоматизации торговых воркфлоу. Проект имеет высокую готовность к production (активные коммиты, 53 звёзды, 15 форков, свежие обновления), но перед развертыванием следует проверить лицензию, безопасность и наличие поддерживающих мейнтейнеров.

### 中文

**项目简介（2‑3 句话）**  
codedpro/mt5‑trade‑split‑manager 是一款面向 AI‑Agent 的 MT5 Expert Advisor，具备智能订单拆分（60/10/10/10/10）、自动跟踪止损和 REST API，专为金银交易并集成 Claude AI 进行决策优化。

**价值**  
- **提升盈亏比**：通过预设的 60/10/10/10/10 拆单比例，实现更细粒度的仓位管理和利润最大化。  
- **AI 驱动**：直接调用 Claude（或其他 LLM）生成交易信号，降低人工干预成本。  
- **全链路自动化**：从信号生成、下单、止损到监控均可通过 REST API 完全编程化，适合研究、回测和实时生产环境。

**典型接入方式**  
1. **REST API**：在自己的后端或交易机器人中调用 `/signal、/order、/trail` 等端点，实现信号下发与订单管理。  
2. **MQL5 脚本**：将仓位拆分逻辑直接嵌入 MT5 客户端，适合对延迟要求极高的场景。  
3. **CLI/SDK**：项目提供的命令行工具或 Python SDK（通过 `requests` 调用）可快速在 CI/CD 流程或研究笔记本中集成。  

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑07‑05，星标 53、fork 15，社区关注度较高。  
- **成熟度**：核心功能（拆单、Trailing Stop、REST API）已实现并通过基本回测验证，具备在真实账户中进行小额试运行的条件。  
- **风险**：仍需进一步审查许可证兼容性、代码安全（尤其是 API 鉴权）以及维护者响应速度；但整体技术栈（MQL5 + 标准 HTTP）易于审计。  

**结论**：该项目在功能完整性、社区活跃度和技术实现上已具备进入生产环境的基本条件，适合作为金银交易的 AI‑驱动自动化实验平台或正式部署的候选组件。

## 🧭 Practical evaluation

**Value:** codedpro/mt5-trade-split-manager helps research and automate market workflows.

**Best use cases**

- research trading systems
- backtest strategies
- monitor market workflows

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 53 GitHub stars
- 15 forks
- updated 2026-07-05
- primary language: MQL5
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 30/100 |
| stars | 37/100 |
| topics | 100/100 |
| outlook | 61/100 |
| quality | 56/100 |
| recency | 40/100 |
| adoption | 35/100 |
| production | 58/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/codedpro/mt5-trade-split-manager) · [← Back to Trading](./README.md)</sub>
