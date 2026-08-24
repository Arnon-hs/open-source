# hummingbot/hummingbot

[![Stars](https://img.shields.io/github/stars/hummingbot/hummingbot?style=flat-square&color=yellow)](https://github.com/hummingbot/hummingbot/stargazers) [![Forks](https://img.shields.io/github/forks/hummingbot/hummingbot?style=flat-square&color=blue)](https://github.com/hummingbot/hummingbot/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> Open source software that helps you create and deploy high-frequency crypto trading bots

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 19k |
| 🍴 **Forks** | 4.7k |
| 💻 **Language** | Python |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`algotrading` `arbitrage` `backtesting` `bitcoin` `bot` `crypto` `cryptocurrency` `cython` `dex` `docker` `ethereum` `hft`

## 🎯 Categories

Crypto · Trading · Automation · DevOps/Infra

## 📝 Summary

### English

**Summary**  
Hummingbot is an open‑source Python framework for building, testing, and deploying high‑frequency cryptocurrency trading bots. It provides ready‑to‑use connectors, a CLI/SDK, and extensive documentation, enabling developers to prototype and inspect Web3 trading workflows with full visibility into the underlying implementation. With a large community (≈19 k stars) and frequent updates, it is positioned as a production‑ready candidate for serious trading or DeFi pilots.

**Value**  
- **Transparency & Control:** All bot logic, exchange adapters, and wallet interactions are open‑source, letting teams audit security, customize strategies, and integrate new protocols without vendor lock‑in.  
- **Speed to Market:** Pre‑built connectors, strategy templates, and a unified CLI accelerate the creation of market‑making, arbitrage, or liquidity‑provision bots, reducing the time needed to move from idea to live deployment.  
- **Extensibility:** The Python SDK and modular architecture make it easy to plug in custom analytics, AI/ML models, or proprietary risk engines, supporting both rapid prototyping and production‑grade extensions.

**Practical Adoption Path**  
1. **Evaluation:** Clone the repo, run the CLI sandbox, and test existing sample strategies against paper‑trading APIs.  
2. **Prototype:** Extend a connector or strategy using the Python SDK, integrate internal wallet or DeFi contracts, and validate performance on testnets.  
3. **Pilot:** Deploy the bot in a controlled environment (e.g., a dedicated VM or container) with real‑time monitoring, logging, and alerting.  
4. **Scale:** Containerize the bot (Docker/K8s), integrate with CI/CD pipelines, and apply hardened security policies (secret management, network segmentation).  

**Production Readiness**  
- **Activity & Community:** Recent commits (as of 2026‑06‑22), >19 k stars, and thousands of forks indicate strong momentum and a vibrant contributor base.  
- **Ecosystem Fit:** Supports major crypto exchanges, DeFi protocols, and provides clear API/CLI interfaces, making integration with existing trading stacks straightforward.  
- **Risk Considerations:** While no immediate licensing or metadata red flags appear, a final security audit, license compliance check, and confirmation of active maintainers are recommended before full production rollout.

### Русский

**hummingbot/hummingbot** — это открытая платформа на Python для создания и развертывания высокочастотных ботов, торгующих криптовалютой. Она позволяет быстро прототипировать и проверять Web3‑процессы (интеграция с биржами, кошельками, DeFi‑протоколами) через готовый API/CLI/SDK, что делает её удобным фундаментом для построения кастомных торговых стратегий. Проект демонстрирует высокий уровень готовности к production: активная разработка, более 18 тыс. звёзд на GitHub, регулярные обновления и широкое принятие в сообществе, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句）**  
Hummingbot 是一款开源的高频加密交易机器人平台，提供完整的 API、SDK 与 CLI，帮助用户快速搭建、测试并部署自己的加密交易策略。它以 Python 为核心语言，社区活跃、星标超过 1.9 万，是构建 Web3、DeFi 与钱包自动化工作流的首选工具。

**价值**  
- **快速原型与审计**：完整的实现细节公开，开发者可以直接查看、修改并审计交易逻辑及区块链交互流程。  
- **多场景适配**：支持现货、永续、做市、套利等多种高频交易模式，亦可用于链上工作流（如自动化流动性提供、跨链桥接）。  
- **生态兼容**：内置对主流交易所和去中心化协议的连接器，便于在同一框架下统一管理多链资产。

**典型接入方式**  
1. **CLI**：通过 `hummingbot` 命令行工具快速启动、配置和监控机器人。  
2. **Python SDK**：在自有代码库中直接调用 Hummingbot 提供的类与函数，实现深度定制或与现有系统集成。  
3. **Docker / Kubernetes 部署**：官方提供的容器镜像可直接在容器编排平台上扩展，适合生产环境的弹性部署。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑22，项目仍在持续更新，拥有 18 959 个 GitHub 星标和 4 749 次 fork，社区贡献频繁。  
- **成熟度**：代码基于 Python，文档完整，提供丰富的示例和测试套件；已有多家交易所和 DeFi 项目在生产环境中使用。  
- **风险提示**：需进一步审查许可证兼容性、依赖安全漏洞以及维护者响应速度，但整体技术和生态成熟度足以支撑正式的业务试点。

## 🧭 Practical evaluation

**Value:** hummingbot/hummingbot helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 18959 GitHub stars
- 4749 forks
- updated 2026-06-22
- primary language: Python
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 92/100 |
| stars | 91/100 |
| topics | 100/100 |
| outlook | 68/100 |
| quality | 81/100 |
| recency | 40/100 |
| adoption | 91/100 |
| production | 67/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/hummingbot/hummingbot) · [← Back to Crypto](./README.md)</sub>
