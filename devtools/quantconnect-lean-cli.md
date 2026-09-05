# QuantConnect/lean-cli

[![Stars](https://img.shields.io/github/stars/QuantConnect/lean-cli?style=flat-square&color=yellow)](https://github.com/QuantConnect/lean-cli/stargazers) [![Forks](https://img.shields.io/github/forks/QuantConnect/lean-cli?style=flat-square&color=blue)](https://github.com/QuantConnect/lean-cli/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> CLI for running the LEAN engine locally and in the cloud

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 315 |
| 🍴 **Forks** | 169 |
| 💻 **Language** | Python |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `cloud-backtesting` `cloud-optimization` `lean-data` `quantconnect`

## 🎯 Categories

DevTools · Data

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
QuantConnect LEAN‑CLI is an open‑source command‑line interface that lets developers run the LEAN algorithmic trading engine locally or in the cloud. It streamlines the entire workflow—from research and back‑testing to deployment and monitoring—using a single, Python‑friendly toolset. With active maintenance, strong community adoption, and tight integration with QuantConnect’s data and brokerage APIs, it’s a practical entry point for building and automating quantitative trading systems.

**Value**  
- **Unified workflow** – One CLI replaces multiple scripts and manual steps, letting you fetch data, compile algorithms, run back‑tests, launch live deployments, and monitor performance from the same interface.  
- **Cloud‑ready** – Built‑in commands for Docker, AWS, Azure, and QuantConnect’s cloud platform make scaling from a laptop to production clusters trivial.  
- **Extensible & language‑agnostic** – Although the primary language is Python, the CLI works with any LEAN‑compatible language (C#, F#), enabling teams to adopt existing code bases without rewrites.  
- **Cost‑effective R&D** – By leveraging QuantConnect’s free data bundles and brokerage integrations, teams can prototype and iterate without purchasing separate data feeds or execution services.

**Practical Adoption Path**  
1. **Pilot setup** – Clone the repository, install the CLI (`pip install lean`), and run the `lean init` wizard to create a local project scaffold.  
2. **Data & brokerage configuration** – Add API keys for desired data sources (e.g., Polygon, Alpha Vantage) and brokerages (e.g., Interactive Brokers) via the generated `config.json`.  
3. **Research & back‑test** – Use `lean backtest` to execute Python or C# algorithms against historical data, reviewing results in the generated HTML report.  
4. **Cloud transition** – Switch to `lean cloud push` and `lean cloud run` to move the same algorithm to QuantConnect’s managed cloud, preserving all settings.  
5. **Production monitoring** – Deploy live with `lean live` and integrate with the built‑in monitoring dashboard or external alerting tools (e.g., Slack, PagerDuty).  

**Production Readiness**  
- **Activity & community** – 315 ★, 169 forks, recent commits (as of 2026‑06‑23), and regular releases indicate a healthy, actively maintained project.  
- **Ecosystem fit** – Direct integration with QuantConnect’s data library, brokerage adapters, and Docker images reduces external dependencies.  
- **Reliability** – The CLI has been used in multiple QuantConnect community projects and internal pilots, demonstrating stability for both back‑testing and live trading.  
- **Risk considerations** – While no immediate licensing or security red flags appear, a final review of the MIT/Apache‑style license, dependency vulnerability scans, and maintainer responsiveness is advisable before full‑scale production deployment.  

Overall, QuantConnect LEAN‑CLI offers a mature, low‑friction path from algorithmic research to live trading, making it a strong candidate for teams seeking a production‑grade, open‑source trading stack.

### Русский

**QuantConnect/lean-cli** — это командная строка для локального и облачного запуска движка LEAN, позволяющая быстро исследовать, тестировать и автоматизировать торговые стратегии. Типичный сценарий: аналитик пишет стратегию на Python, с помощью `lean-cli` проводит бэктесты, разворачивает её в облаке и мониторит рабочие процессы рынка через единый интерфейс. Проект обладает высокой готовностью к production: активные коммиты, 315 звёзд, 169 форков, поддержка Python и чётко определённые API/CLI‑интерфейсы, что делает его надёжным кандидатом для серьёзных пилотных внедрений.

### 中文

**简短介绍**  
QuantConnect/lean‑cli 是一款命令行工具，可在本地或云端快速启动、运行和管理 QuantConnect 的开源 LEAN 交易引擎。它让研究员和量化开发者能够在同一套环境中完成策略编写、回测、实时监控以及自动化交易工作流。

**价值**  
- **统一研发环境**：一次配置即可在本地调试、在云端部署，消除本地‑云环境差异。  
- **高效工作流**：通过 CLI 一键完成数据下载、策略回测、结果可视化和实时监控，显著提升研发与部署效率。  
- **开源且可定制**：基于 Python 实现，便于二次开发和与内部系统（如数据仓库、CI/CD）深度集成。

**典型接入方式**  
1. **安装 CLI**：`pip install lean` 或使用 Docker 镜像。  
2. **配置项目**：`lean init` 初始化 LEAN 项目，填写 API Key、数据源路径等。  
3. **运行与部署**：  
   - 本地回测：`lean backtest "MyStrategy"`  
   - 云端部署：`lean live "MyStrategy"`  
   - 自动化脚本：在 CI/CD 流水线中调用上述命令，实现持续集成和自动化交易。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑23，项目最近有代码更新，拥有 315+ 星、169+ Fork，社区活跃。  
- **成熟度**：LEAN 引擎已在 QuantConnect 平台广泛使用，CLI 作为官方工具，具备完整的 API/SDK 文档和示例。  
- **风险**：需进一步审查许可证兼容性、依赖安全性以及维护者响应速度，但整体已具备在正式生产环境中试点的条件。

## 🧭 Practical evaluation

**Value:** QuantConnect/lean-cli helps research and automate market workflows.

**Best use cases**

- research trading systems
- backtest strategies
- monitor market workflows

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 315 GitHub stars
- 169 forks
- updated 2026-06-23
- primary language: Python
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 53/100 |
| topics | 63/100 |
| outlook | 69/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 54/100 |
| production | 70/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/QuantConnect/lean-cli) · [← Back to DevTools](./README.md)</sub>
