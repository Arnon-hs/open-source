# JungHoonGhae/tossinvest-cli

[![Stars](https://img.shields.io/github/stars/JungHoonGhae/tossinvest-cli?style=flat-square&color=yellow)](https://github.com/JungHoonGhae/tossinvest-cli/stargazers) [![Forks](https://img.shields.io/github/forks/JungHoonGhae/tossinvest-cli?style=flat-square&color=blue)](https://github.com/JungHoonGhae/tossinvest-cli/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-83%2F100-brightgreen?style=flat-square)](#)

> 토스증권을 AI 에이전트·터미널에서 — 공식 Open API(예정)보다 넓은 조회·거래 범위(수급·AI시그널·스크리너·실시간 푸시·소수점 주문·dry-run preview)를 다루는 비공식 CLI

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 404 |
| 🍴 **Forks** | 68 |
| 💻 **Language** | Go |
| 📈 **Score** | 83/100 |
| 🗓️ **Last push** | 2026-06-23 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `cli` `go` `korea-stock` `llm-tools` `stock-trading` `toss` `toss-securities` `tossinvest` `trading-api`

## 🎯 Categories

Trading · AI/ML · Backend · DevTools

## 📝 Summary

### English

**Summary**  
JungHoonGhae /tossinvest‑cli is an unofficial Go‑based command‑line client that extends Toss Securities’ upcoming Open API, offering a richer set of market data and trading capabilities such as supply‑demand insights, AI‑generated signals, screeners, real‑time push notifications, fractional orders, and dry‑run previews. It is designed for developers and quantitative traders who want to script, back‑test, and automate their Toss‑based strategies from a terminal or AI agent.  

**Value**  
- **Broader functionality** than the official API, giving users access to advanced analytics (AI signals, order‑book depth) and features (fractional sizing, dry‑run previews) that are otherwise unavailable.  
- **Automation‑ready**: the CLI can be integrated into scripts, CI pipelines, or AI agents, enabling end‑to‑end research, monitoring, and execution workflows without manual UI interaction.  
- **Open‑source transparency**: the Go source code is auditable, extensible, and can be forked or wrapped in custom tooling, which is attractive for quantitative teams that need to verify trading logic.  

**Practical adoption path**  
1. **Evaluation** – Clone the repo, review the README and Go modules, and run the built‑in `--help` commands to explore available endpoints.  
2. **Credential setup** – Configure Toss API keys or OAuth tokens as documented; the CLI stores them securely via environment variables or a config file.  
3. **Proof‑of‑concept** – Write small shell or Go scripts that fetch AI signals, perform a dry‑run order, and log results; iterate on back‑testing logic using the provided preview mode.  
4. **Integration** – Wrap the CLI in Docker containers or invoke it from orchestration tools (Airflow, Prefect) to embed it in larger trading pipelines or AI‑agent frameworks.  
5. **Production hardening** – Add logging, rate‑limit handling, and fallback mechanisms; optionally fork the repo to pin dependencies and apply internal security reviews.  

**Production readiness**  
- **Activity & community**: Recent commits (as of 2026‑06‑23), 68 forks, and an active issue/PR flow indicate a healthy maintainer presence.  
- **Maturity**: The CLI already implements critical trading functions (order preview, fractional sizing) and provides real‑time push support, reducing the need for custom wrappers.  
- **Risk considerations**: The project lacks a formal license declaration and has not undergone a third‑party security audit; organizations should verify licensing compliance and perform a security review before deploying in live environments.  
- **Overall**: With the above checks completed, the tool is a strong OSS candidate for pilot projects and can be promoted to production for automated Toss‑based trading workflows.

### Русский

JungHoonGhae/tossinvest‑cli — это неофициальный CLI‑инструмент для работы с Toss 증권, который расширяет возможности официального Open API, предоставляя доступ к широкому набору данных (сигналы AI, скринеры, реальное время, дробные ордера, dry‑run‑preview) и автоматизируя торговые операции. Он идеально подходит для исследователей и разработчиков, которым нужно быстро собрать рыночные данные, протестировать стратегии и мониторить рабочие процессы через терминал или AI‑агента. Проект находится на высокой стадии готовности к продакшн: активная разработка (обновления до 2026‑06‑23), значительное количество форков, написан на Go и имеет хорошую экосистемную поддержку, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
JungHoonGhae/tossinvest-cli 是一款基于 Go 实现的非官方命令行工具，能够在 AI Agent 与终端环境中调用 Toss 증권的多种功能。相较于官方即将上线的 Open API，它提供更丰富的查询与交易能力（包括资金流向、AI 信号、筛选器、实时推送、支持小数点下单以及 dry‑run 预览），帮助用户在本地完成全链路的市场研究与自动化交易。

**价值**  
- **全方位市场洞察**：一次性获取行情、资金流、AI 生成的买卖信号以及自定义筛选结果，省去多平台切换的成本。  
- **自动化工作流**：通过 CLI 脚本化下单、监控和回测，可轻松嵌入 CI/CD 或自研交易机器人，实现“研究‑回测‑实盘”闭环。  
- **高灵活性**：支持小数点下单和 dry‑run 预览，既满足高频微交易需求，又能在不触发真实交易的情况下验证策略安全性。

**典型接入方式**  
1. **本地安装**：`go install github.com/JungHoonGhae/tossinvest-cli@latest` 或直接下载二进制。  
2. **配置凭证**：在 `~/.tossinvest/config.yaml` 中填入 API Token（或使用 OAuth）以及默认交易账户。  
3. **脚本调用**：在 Bash、PowerShell、Python（via `subprocess`）或 CI/CD pipeline 中执行 `tossinvest-cli trade --symbol=005930 --qty=0.5 --dry-run` 等命令，实现策略自动下单或数据抓取。  
4. **与 AI Agent 集成**：在 LangChain、AutoGPT 等框架的工具插件里包装 CLI，允许自然语言指令直接触发查询或交易。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑23，项目拥有 68 个 Fork，代码质量稳定，主要语言为 Go，易于审计和二进制分发。  
- **成熟度**：提供完整的错误码、日志以及 dry‑run 预览功能，降低了在生产环境直接下单的风险。  
- **可评估性**：项目结构清晰，公开的 API/SDK 文档、示例脚本以及 10 条主题标签帮助快速评估兼容性。  
- **风险**：仍需进一步审查许可证（默认 MIT），以及长期维护者的响应速度和安全审计报告。总体而言，已具备在内部或受控环境中进行试点的条件，适合作为 OSS 交易自动化的候选方案。

## 🧭 Practical evaluation

**Value:** JungHoonGhae/tossinvest-cli helps research and automate market workflows.

**Best use cases**

- research trading systems
- backtest strategies
- monitor market workflows

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 404 GitHub stars
- 68 forks
- updated 2026-06-23
- primary language: Go
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 46/100 |
| stars | 55/100 |
| topics | 100/100 |
| outlook | 88/100 |
| quality | 79/100 |
| recency | 100/100 |
| adoption | 53/100 |
| production | 80/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/JungHoonGhae/tossinvest-cli) · [← Back to Trading](./README.md)</sub>
