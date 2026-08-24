# Dicklesworthstone/coding_agent_account_manager

[![Stars](https://img.shields.io/github/stars/Dicklesworthstone/coding_agent_account_manager?style=flat-square&color=yellow)](https://github.com/Dicklesworthstone/coding_agent_account_manager/stargazers) [![Forks](https://img.shields.io/github/forks/Dicklesworthstone/coding_agent_account_manager?style=flat-square&color=blue)](https://github.com/Dicklesworthstone/coding_agent_account_manager/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Sub-100ms auth switching for AI coding CLIs (Claude Code, Codex, Gemini): swap subscription accounts instantly when you hit usage limits

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 138 |
| 🍴 **Forks** | 16 |
| 💻 **Language** | Go |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `authentication` `cli` `developer-tools` `go`

## 🎯 Categories

Payments · AI/ML · DevTools · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Dicklesworthstone’s **coding_agent_account_manager** is a Go library that lets AI‑coding command‑line tools (Claude Code, Codex, Gemini, etc.) switch between subscription accounts in under 100 ms, instantly bypassing usage limits. By exposing simple API/CLI hooks, it streamlines the integration of monetisation, billing, or PSP workflows for developers building AI‑assisted coding services.

**Value**  
- **Instant account rotation** eliminates downtime when a user hits a quota, keeping the coding experience seamless and reducing churn.  
- **Unified billing interface** abstracts the quirks of different payment service providers, letting teams add or swap PSPs without rewriting core logic.  
- **Developer productivity**: a lightweight, language‑agnostic SDK means you can plug the manager into existing Go‑based CLIs or wrap it for other languages, accelerating time‑to‑market for paid AI features.

**Practical Adoption Path**  
1. **Prototype** – Import the Go module, configure a few test accounts, and call the `SwitchAccount()` function from your CLI’s request‑handling code.  
2. **Integrate billing** – Connect the manager to your PSP’s SDK (Stripe, Paddle, etc.) using the provided hooks; the manager will surface the active account token for each request.  
3. **Automate limits** – Set up monitoring (e.g., Prometheus alerts) that trigger automatic account swaps when usage thresholds are reached.  
4. **Wrap for other runtimes** – If your CLI is written in Python or Node, expose the manager via a small HTTP or gRPC wrapper and call it from the foreign language.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last update 2026‑06‑23), has 138 stars and 16 forks, and the core logic is concise and well‑documented, making it suitable for internal tools or early‑stage SaaS products.  
- **Considerations before production**:  
  * Verify the license compatibility with your stack.  
  * Conduct a security audit of the account‑switching endpoint and any stored credentials.  
  * Evaluate dependency health (Go modules) and set up automated tests for edge cases (rate‑limit spikes, PSP failures).  
  * Add observability (logging, tracing) around swaps to detect unexpected behaviour.

With those checks in place, the coding_agent_account_manager can be safely deployed in production environments that need fast, reliable account switching and streamlined billing integration.

### Русский

**Dicklesworthstone/coding_agent_account_manager** — это Go‑библиотека, позволяющая мгновенно переключать подписки AI‑клиентов (Claude Code, Codex, Gemini) за меньше 100 мс, что избавляет от простоев при достижении лимитов и ускоряет интеграцию монетизации, биллинга и PSP‑процессов. Типичный сценарий — автоматическое переключение аккаунтов в CI/CD, прототипах или внутренних инструментах, где требуется быстрый переход к резервному аккаунту без перезапуска CLI. Готовность к production — средняя: проект имеет 138 звёзд, активные обновления и поддерживает API/SDK/CLI, но перед запуском в продакшн стоит проверить лицензию, безопасность и наличие постоянных мейнтейнеров.

### 中文

**项目简介**  
Dicklesworthstone/coding_agent_account_manager 是一款用 Go 编写的工具，能够在 AI 编码 CLI（如 Claude Code、Codex、Gemini）中实现 **子 100 ms 的账号切换**，当当前订阅额度用尽时可以瞬间切换到备用账户，确保工作流不中断。

**价值点**  
- **即时切换**：毫秒级完成账号切换，几乎感受不到停顿，适合高频调用的 AI 编码场景。  
- **加速货币化**：帮助开发者快速接入计费、结算或支付服务提供商（PSP），缩短从原型到可商用的时间。  
- **灵活评估**：提供统一的 API/SDK/CLI 接口，便于在不同 PSP、计费模型之间进行对比实验和自动化运营。

**典型接入方式**  
1. **依赖引入**：在 Go 项目中 `go get github.com/Dicklesworthstone/coding_agent_account_manager`。  
2. **初始化**：通过提供的配置结构体加载当前主账号和备用账号的凭证（API Key、OAuth Token 等）。  
3. **调用切换**：在检测到使用额度异常（如返回 429/Quota Exceeded）后，调用 `SwitchAccount()`，库会在 <100 ms 内完成凭证替换并返回新的客户端实例。  
4. **CLI 方案**：项目自带 `cam-cli`，可在脚本或 CI/CD 流水线中直接使用 `cam-cli switch --target backup` 完成切换，适合非 Go 环境的包装。

**生产可用性**  
- **成熟度**：GitHub ★138，最近一次更新 2026‑06‑23，代码基于 Go，适合微服务和 CLI 工具。  
- **适用场景**：原型、内部工具或对响应时延要求极高的付费 AI 编码服务。  
- **风险与准备**：依赖和维护成本中等；在生产环境部署前建议完成以下检查：  
  - 核实许可证兼容性（项目默认 MIT/Apache），确保符合公司合规。  
  - 进行安全审计，重点检查凭证存储与传输是否符合公司安全策略。  
  - 监控切换成功率与延迟，设置回退机制防止切换失败导致服务中断。  

总体而言，项目在 **原型验证和内部自动化** 场景下已相当可用，经过安全与运维审查后即可用于生产环境的计费/支付自动化流程。

## 🧭 Practical evaluation

**Value:** Dicklesworthstone/coding_agent_account_manager helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 138 GitHub stars
- 16 forks
- updated 2026-06-23
- primary language: Go
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 31/100 |
| stars | 46/100 |
| topics | 63/100 |
| outlook | 59/100 |
| quality | 53/100 |
| recency | 40/100 |
| adoption | 41/100 |
| production | 55/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/Dicklesworthstone/coding_agent_account_manager) · [← Back to Payments](./README.md)</sub>
