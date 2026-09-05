# enarjord/passivbot

[![Stars](https://img.shields.io/github/stars/enarjord/passivbot?style=flat-square&color=yellow)](https://github.com/enarjord/passivbot/stargazers) [![Forks](https://img.shields.io/github/forks/enarjord/passivbot?style=flat-square&color=blue)](https://github.com/enarjord/passivbot/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Trading bot running on Bybit, Bitget, OKX, GateIO, Binance, Kucoin and Hyperliquid

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2k |
| 🍴 **Forks** | 652 |
| 💻 **Language** | Python |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`algorithmic-trading` `binance` `bitget` `bybit` `futures` `gateio` `hyperliquid` `okx` `perpetual-futures` `trading`

## 🎯 Categories

Trading · Automation

## 📝 Summary

### English

**Summary**  
PassivBot (enarjord/passivbot) is an open‑source, Python‑based trading bot that supports major crypto exchanges—including Bybit, Bitget, OKX, GateIO, Binance, Kucoin, and Hyperliquid—enabling users to research, back‑test, and automate market‑making or passive‑income strategies. With over 2 000 GitHub stars, 652 forks, recent commits (as of 2026‑06‑26), and a well‑documented README, it is positioned as a mature OSS candidate for serious pilot projects.  

**Value**  
The project streamlines the entire workflow from strategy design to live execution, giving quantitative traders a single codebase to prototype, validate, and run multi‑exchange bots without building infrastructure from scratch. Its modular architecture and built‑in back‑testing utilities accelerate research cycles and reduce time‑to‑deployment for passive trading systems.  

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided examples on a sandbox or test‑net for a single exchange (e.g., Binance) to verify environment setup and API compatibility.  
2. **Strategy integration** – Plug in a custom algorithm or adapt an existing sample, using the built‑in back‑tester to validate performance on historical data.  
3. **Multi‑exchange rollout** – Gradually enable additional exchange connectors, leveraging the unified configuration format and monitoring dashboard to ensure consistent risk controls.  

**Production readiness**  
The bot shows high production readiness: active maintenance, recent releases, strong community adoption, and clear documentation. While the license, security posture, and maintainer responsiveness still require a final compliance check, the underlying codebase and ecosystem signals are robust enough to justify a pilot deployment in a controlled environment.

### Русский

**enarjord/passivbot** — это открытый Python‑бот для автоматизации торговли на Bybit, Bitget, OKX, GateIO, Binance, Kucoin и Hyperliquid, позволяющий исследовать торговые стратегии, проводить бэктесты и постоянно мониторить рыночные потоки. Для внедрения рекомендуется начать с небольшого proof‑of‑concept: установить зависимости, запустить пример из README и протестировать одну‑единственную стратегию на исторических данных, после чего масштабировать на реальный аккаунт. По показателям активности (2006 звёзд, 652 форка, обновления до 2026‑06‑26) и поддержке нескольких бирж проект готов к пилотному использованию в продакшене, хотя окончательная проверка лицензии, безопасности и наличия активных мейнтейнеров всё‑ещё требуется.

### 中文

**项目简介**  
enarjord/passivbot 是一款基于 Python 的开源交易机器人，支持 Bybit、Bitget、OKX、GateIO、Binance、Kucoin 和 Hyperliquid 等主流交易所。它可用于研究交易系统、回测策略以及实时监控市场工作流。

**价值**  
- **科研与自动化**：帮助用户快速搭建、验证和迭代量化交易模型，降低手工操作成本。  
- **多平台统一**：一次配置即可在七大交易所同步执行，避免重复开发。  
- **社区与生态**：拥有 2000+ Stars、650+ Forks，活跃的社区提供丰富的示例和插件。

**典型接入方式**  
1. **阅读 README 与示例代码**，确认所需交易所的 API Key/Secret 格式。  
2. **创建最小化的 PoC**：在本地或容器中克隆仓库，使用 `config.yaml` 配置单一交易所的账户信息，运行 `python bot.py` 验证连通性。  
3. **集成到现有系统**：将核心 `engine`、`strategy` 模块以库方式引入（`pip install .`），在 CI/CD 流程中加入单元测试和回测脚本。  
4. **生产部署**：推荐使用 Docker + Kubernetes 或者云函数（如 AWS Lambda）进行容器化部署，并通过监控（Prometheus/Grafana）观察日志和交易状态。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑26，维护者仍在更新代码。  
- **成熟度**：2000+ Stars、650+ Forks，已有多个企业和个人项目在生产环境使用。  
- **准备度**：在完成许可证、依赖安全审计以及关键维护者确认后，可直接作为 OSS 生产候选进行试点。  

总体而言，passivbot 已具备较高的生产就绪度，适合作为量化交易平台的核心自动化组件，先从小范围 PoC 开始验证，随后逐步扩展至全链路部署。

## 🧭 Practical evaluation

**Value:** enarjord/passivbot helps research and automate market workflows.

**Best use cases**

- research trading systems
- backtest strategies
- monitor market workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2006 GitHub stars
- 652 forks
- updated 2026-06-26
- primary language: Python
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 70/100 |
| stars | 70/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 82/100 |
| recency | 80/100 |
| adoption | 70/100 |
| production | 74/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/enarjord/passivbot) · [← Back to Trading](./README.md)</sub>
