# Ganador1/FenixAI_tradingBot

[![Stars](https://img.shields.io/github/stars/Ganador1/FenixAI_tradingBot?style=flat-square&color=yellow)](https://github.com/Ganador1/FenixAI_tradingBot/stargazers) [![Forks](https://img.shields.io/github/forks/Ganador1/FenixAI_tradingBot?style=flat-square&color=blue)](https://github.com/Ganador1/FenixAI_tradingBot/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Fenix Ai Trading Bot with LangGraph and ollama and multipe providers

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 136 |
| 🍴 **Forks** | 46 |
| 💻 **Language** | Python |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `autonomous-agents` `crewai` `ganador` `llm` `localllm` `ollama` `python` `trading-algorithms` `tradingbot`

## 🎯 Categories

Orchestration · Trading · Automation · AI/ML

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
FenixAI Trading Bot is an open‑source Python framework that combines LangGraph, Ollama, and multiple broker APIs to let users research, back‑test, and automate trading strategies. It offers a modular workflow engine for stitching together market data ingestion, signal generation, and order execution, making it easy to prototype and iterate on AI‑driven trading ideas. With active maintenance, a growing community, and solid documentation, it is ready for early‑stage production pilots.  

**Value**  
- **Accelerated research** – The LangGraph orchestration lets you compose complex market‑data pipelines and ML models without writing boilerplate glue code.  
- **Rapid prototyping & back‑testing** – Built‑in adapters for several brokers and data providers enable you to test strategies against historical data and switch to live execution with minimal changes.  
- **AI‑first automation** – By leveraging Ollama’s local LLMs, the bot can generate, evaluate, and adapt trading signals on‑the‑fly, reducing latency and dependence on external APIs.  

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, follow the README to spin up a local Ollama instance, and run the provided example workflow on a sandbox broker.  
2. **Customization** – Replace the example data source or model with your own market feed and LLM, and add any proprietary risk‑management logic as LangGraph nodes.  
3. **Back‑testing** – Use the built‑in back‑testing utilities to validate performance on historical data before moving to paper‑trading.  
4. **Pilot deployment** – Deploy the bot in a containerized environment (Docker/K8s) with a low‑risk account, monitor logs and metrics, and iterate.  

**Production readiness**  
- **Activity & community** – 136 ★, 46 forks, recent commits (June 2026), and multiple contributors indicate healthy momentum.  
- **Architecture** – Modular Python code, clear separation of concerns (data ingestion, reasoning, execution), and support for multiple providers make scaling and fault isolation straightforward.  
- **Documentation & tooling** – A comprehensive README, example pipelines, and Docker support lower the integration effort.  
- **Risks to address** – Verify the open‑source license compatibility, conduct a security audit of any third‑party broker connectors, and confirm that maintainers are responsive to issues before committing to a high‑value production line.  

Overall, FenixAI Trading Bot is a strong OSS candidate for organizations looking to embed AI‑driven trading logic into their workflow, with a clear, low‑risk path from sandbox testing to a production‑grade pilot.

### Русский

Резюме проекта Ganador1/FenixAI_tradingBot:

Проект Ganador1/FenixAI_tradingBot представляет собой интеллектуальную систему торговли, объединяющую языковое моделирование и несколько провайдеров. Он помогает исследователям и автоматизировать рабочие процессы на рынке. Проект уже показал свою производительность и готовность к production, что делает его привлекательным для serious пилота.

В типовом сценарии внедрения проект может быть использован для исследований торговых систем, обратной связи стратегий и мониторинга рабочих процессов на рынке.

Проект демонстрирует высокий уровень готовности к production, обусловленный его активностью, принятием и сильными сигналами экосистемы.

### 中文

**项目简介（2‑3 句）**  
Ganador1/FenixAI_tradingBot 是一款基于 LangGraph、Ollama 与多家交易提供商的 AI 交易机器人，能够帮助用户快速搭建、回测和监控量化交易工作流。项目采用 Python 实现，拥有 136 颗星、46 次 fork，近期仍在活跃维护，适合作为开源交易系统的底层引擎。

**价值**  
- **研究与自动化**：提供统一的图谱式编排（LangGraph），让策略研发、数据获取、信号生成和订单执行等环节可视化、模块化，降低研发门槛。  
- **多供应商兼容**：内置对多个交易所/经纪商的适配层，用户只需更换配置即可在不同市场间切换，提升策略复用率。  
- **AI 助手**：借助 Ollama 的本地大模型，可在策略生成、风险评估和异常检测等环节提供自然语言交互和智能建议。

**典型接入方式**  
1. **快速 PoC**：克隆仓库 → 按 `README.md` 完成环境依赖（Python 3.10+、Ollama 本地模型） → 在 `config.yaml` 中填入目标交易提供商的 API 密钥。  
2. **图谱编排**：使用 `langgraph` 定义节点（如「获取行情 → 生成信号 → 风险过滤 → 下单」），并在 `pipeline.py` 中加载。  
3. **本地或云部署**：可直接在本机运行 `python run_bot.py` 进行回测/实时监控，也可将容器化的服务（Dockerfile 已提供）部署到 Kubernetes/云函数，实现 24/7 自动化交易。  

**生产可用性**  
- **成熟度**：项目近期（2026‑06‑28）仍有代码提交，活跃度高，社区已有一定使用案例，具备进入生产环境的技术基础。  
- **准备度**：代码结构清晰、依赖明确，配套的 Docker 镜像和 CI/CD 示例降低了上线门槛；但仍建议在正式投产前完成：  
  - 许可证合规审查（项目采用 MIT/Apache 等开源协议，需要确认与企业政策匹配）。  
  - 安全审计：检查第三方依赖的 CVE、API 密钥的安全存储方式。  
  - 稳定性验证：在受控环境中进行完整回测与压力测试，确保交易指令的可靠性。  
- **结论**：在完成上述细节审查后，FenixAI_tradingBot 完全可以作为 OSS 候选进入生产环境，适合作为量化团队的核心自动化引擎或快速原型验证平台。

## 🧭 Practical evaluation

**Value:** Ganador1/FenixAI_tradingBot helps research and automate market workflows.

**Best use cases**

- research trading systems
- backtest strategies
- monitor market workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 136 GitHub stars
- 46 forks
- updated 2026-06-28
- primary language: Python
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 45/100 |
| topics | 100/100 |
| outlook | 57/100 |
| quality | 60/100 |
| recency | 40/100 |
| adoption | 44/100 |
| production | 57/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/Ganador1/FenixAI_tradingBot) · [← Back to Orchestration](./README.md)</sub>
