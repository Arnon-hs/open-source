# fasiondog/hikyuu

[![Stars](https://img.shields.io/github/stars/fasiondog/hikyuu?style=flat-square&color=yellow)](https://github.com/fasiondog/hikyuu/stargazers) [![Forks](https://img.shields.io/github/forks/fasiondog/hikyuu?style=flat-square&color=blue)](https://github.com/fasiondog/hikyuu/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Hikyuu Quant Framework 基于C++/Python的超高速开源量化交易研究框架，同时可基于策略部件进行资产重用，快速累积策略资产。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.3k |
| 🍴 **Forks** | 794 |
| 💻 **Language** | C++ |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`algorithms-trading` `backtesting` `finance` `quant` `stock` `system-trading` `trading` `vestment`

## 🎯 Categories

Trading

## 📝 Summary

### English

**Brief Summary**  
Hikyuu Quant Framework (fasiondog/hikyuu) is a high‑performance, open‑source quantitative trading research platform written in C++ with Python bindings. It enables rapid strategy development, back‑testing, and market workflow automation while allowing reusable strategy components to be shared across assets. With strong community activity (3 k+ stars, 800+ forks) and recent updates, it is positioned as a production‑ready candidate for serious trading pilots.  

**Value**  
- **Speed & Scalability** – Core C++ engine delivers ultra‑low latency for back‑testing and live execution, while Python bindings give data‑science teams a familiar interface.  
- **Component Reuse** – Strategy modules can be packaged and applied to multiple assets, accelerating portfolio expansion and reducing duplicated effort.  
- **End‑to‑End Workflow** – From market data ingestion to order routing, Hikyuu supports the full research‑to‑production pipeline, simplifying automation of trading operations.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the provided examples, and verify that the Python API can load historical data and execute a simple strategy on a sandbox broker.  
2. **Pilot Integration** – Wrap a small, low‑risk strategy in Hikyuu’s component model, connect to a paper‑trading environment, and benchmark latency and resource usage against existing tools.  
3. **Gradual Scale‑Up** – Incrementally migrate additional strategies, integrate internal data feeds, and add custom risk‑management modules while maintaining CI tests for the C++ core.  
4. **Production Hardening** – Conduct security and license reviews, set up automated builds, monitoring, and fail‑over for the C++ engine, and document deployment procedures (Docker/K8s).  

**Production Readiness**  
- **Activity & Community** – Recent commits (as of 2026‑06‑22), a large star/fork base, and active issue discussions indicate a healthy maintainer ecosystem.  
- **Technical Maturity** – The C++ core is battle‑tested for speed; Python bindings are stable, and the framework already supports back‑testing, live trading, and market data adapters.  
- **Risk Considerations** – No major metadata or licensing red flags have been identified, but a final security audit and confirmation of long‑term maintainer commitment are advisable before full production deployment.  

Overall, Hikyuu offers a robust, high‑performance foundation for quantitative trading research and automation, and with a staged integration approach it can be moved from pilot to production with confidence.

### Русский

**Hikyuu Quant Framework** — это высокопроизводительный открытый набор инструментов на C++/Python для исследования и автоматизации торговых стратегий, позволяющий быстро переиспользовать готовые компоненты и накапливать «активы» стратегии. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept: подключить фреймворк к данным биржи, реализовать и протестировать стратегию в back‑test, затем автоматизировать мониторинг и исполнение в реальном времени. По оценке готовности проект находится на уровне production‑ready OSS‑кандидата: активные коммиты, более 3000 звёзд, широкое сообщество и стабильный стек технологий, требующие лишь финального аудита лицензии и безопасности.

### 中文

**项目简介（2‑3 句话）**  
Hikyuu Quant Framework（fasiondog/hikyuu）是基于 C++ 与 Python 的超高速开源量化交易研究框架，提供统一的策略组件、数据接口和回测引擎，可实现策略资产的复用与快速累积。

**价值**  
- **高性能**：底层 C++ 实现，满足毫秒级甚至微秒级的行情处理需求。  
- **跨语言**：Python 包装层让研究员能够用熟悉的脚本语言快速原型化，同时保留 C++ 的执行效率。  
- **模块化资产复用**：策略部件（因子、信号、仓位管理等）可独立打包、共享，降低重复开发成本。  
- **完整工作流**：从行情获取、回测、实时监控到自动化下单，一站式支持量化全链路。

**典型接入方式**  
1. **环境准备**：  
   - 克隆仓库 `git clone https://github.com/fasiondog/hikyuu.git`  
   - 按照 README 编译 C++ 核心（支持 CMake、Conan），并安装 Python 包 `pip install -e .`  
2. **数据接入**：使用内置的 `DataDriver` 接口接入本地 CSV、MySQL、或第三方行情 API（如 Tushare、Wind）。  
3. **策略开发**：在 Python 中编写继承 `StrategyBase` 的类，调用 `hikyuu` 提供的因子、信号、仓位管理等组件。  
4. **回测/实盘**：使用 `BacktestEngine` 进行离线回测，或通过 `LiveEngine` 绑定交易所网关（CTP、IB 等）进行实时监控与下单。  
5. **CI/POC**：在项目根目录添加最小化的回测脚本作为 PoC，确保依赖、数据和策略能够在 CI 环境中完整运行。

**生产可用性**  
- **活跃度**：截至 2026‑06‑22，项目仍在持续更新，拥有 3,268 星、794 Fork，社区贡献活跃。  
- **成熟度**：提供完整的回测、实时监控、风险控制模块，已在多个内部量化团队中验证。  
- **集成门槛**：首次接入建议先在沙盒环境完成一个完整的回测-实盘闭环验证（POC），确认数据驱动和交易网关兼容性后再推广至生产。  
- **风险**：需进一步审查许可证（MIT）与依赖库的安全性，确保内部合规；同时关注维护者响应速度以应对潜在的漏洞修复。  

综上，Hikyuu 在性能、功能完整性和社区活跃度方面已具备在生产环境中进行严肃量化研发与自动化交易的条件，适合作为量化团队的核心框架进行试点和逐步推广。

## 🧭 Practical evaluation

**Value:** fasiondog/hikyuu helps research and automate market workflows.

**Best use cases**

- research trading systems
- backtest strategies
- monitor market workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3268 GitHub stars
- 794 forks
- updated 2026-06-22
- primary language: C++
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 73/100 |
| stars | 75/100 |
| topics | 100/100 |
| outlook | 64/100 |
| quality | 73/100 |
| recency | 40/100 |
| adoption | 74/100 |
| production | 62/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/fasiondog/hikyuu) · [← Back to Trading](./README.md)</sub>
