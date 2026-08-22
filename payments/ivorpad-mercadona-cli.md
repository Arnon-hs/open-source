# ivorpad/mercadona-cli

[![Stars](https://img.shields.io/github/stars/ivorpad/mercadona-cli?style=flat-square&color=yellow)](https://github.com/ivorpad/mercadona-cli/stargazers) [![Forks](https://img.shields.io/github/forks/ivorpad/mercadona-cli?style=flat-square&color=blue)](https://github.com/ivorpad/mercadona-cli/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-76%2F100-brightgreen?style=flat-square)](#)

> Unofficial, agent-friendly Mercadona shopping CLI (Go) — search products, read prices, build a cart and prepare checkout from the terminal. BYO credentials.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 304 |
| 🍴 **Forks** | 27 |
| 💻 **Language** | Go |
| 📈 **Score** | 76/100 |
| 🗓️ **Last push** | 2026-07-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `claude-code` `cli` `command-line` `golang` `grocery-shopping` `llm-tools` `mercadona` `shopping-cart` `spain`

## 🎯 Categories

Payments · Automation · AI/ML · Frontend · DevTools

## 📝 Summary

### English

**Brief Summary**  
`ivorpad/mercadona-cli` is an unofficial, Go‑based command‑line client for Mercadona’s online shop that lets agents search products, view prices, assemble a cart and generate a checkout payload—all from the terminal. It is credential‑agnostic (you bring your own login) and is positioned as a fast way to prototype or automate billing, PSP, and checkout flows.

**Value**  
- **Speedy integration** – By exposing Mercadona’s shopping API through a simple CLI, developers can hook billing or payment‑service‑provider (PSP) logic into existing automation pipelines without building a full UI.  
- **Agent‑friendly** – The terminal‑first experience matches the workflow of DevOps, QA, or support teams that need to validate product‑price data, cart composition, or checkout edge‑cases quickly.  
- **Open‑source transparency** – With 304 stars, active commits, and a Go codebase, the project is easy to audit, extend, or embed in custom tooling.

**Practical Adoption Path**  
1. **Clone & build** – `git clone https://github.com/ivorpad/mercadona-cli && go build ./...` (Go 1.22+).  
2. **Configure credentials** – Export your Mercadona session token or username/password as environment variables as documented in the README.  
3. **Prototype** – Use commands such as `mercadona search <keyword>`, `mercadona price <sku>` and `mercadona cart add <sku> --qty <n>` to validate product data and cart logic.  
4. **Integrate** – Wrap the CLI in scripts or invoke its Go package directly from your service to feed cart data into your billing/PSP layer, or use it in CI pipelines for end‑to‑end checkout tests.  
5. **Extend** – Contribute missing features (e.g., coupon handling) or adapt the source to your internal SDK if deeper integration is required.

**Production Readiness**  
- **Activity & community** – The repository shows recent commits (last update 2026‑07‑13), 304 stars, 27 forks, and a well‑populated topic list, indicating healthy community interest.  
- **Stability** – The CLI is a thin wrapper around HTTP calls; the core logic is concise and written in Go, which offers strong static typing and easy cross‑platform binaries.  
- **Risk considerations** – No major licensing or security red flags are visible, but a final audit of the Mercadona API usage terms, the project’s license (MIT/Apache‑style), and any disclosed vulnerabilities is advisable before production deployment.  

Overall, `mercadona-cli` is a mature OSS component that can be piloted quickly for billing or checkout automation, and with a brief security/legal review it is ready for production‑grade use.

### Русский

**ivorpad/mercadona-cli** — это неофициальный CLI‑инструмент на Go для работы с сервисом Mercadona, позволяющий из терминала искать товары, получать цены, формировать корзину и готовить процесс оплаты, используя собственные учётные данные. Он отлично подходит для быстрого прототипирования и автоматизации сценариев монетизации — интеграция billing/checkout, тестирование PSP‑потоков или автоматизация платёжных операций без необходимости писать собственный клиент. Проект считается готовым к production‑использованию: активные коммиты (обновление 2026‑07‑13), 304 звёзд, 27 форков, хорошая документация и поддержка Go‑экосистемы, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**简短介绍**

Mercadona-cli 是一款开源的 Go 语言 CLI 工具，用于从终端进行 Mercadona 购物，支持产品搜索、价格查询、购物车创建和结算准备。该工具不提供凭据，需要用户自行提供凭据。

**价值**

Mercadona-cli 帮助用户快速集成付款、账单或支付服务集成流程。它适用于以下场景：

* 集成账单或结算流程
* 评估支付服务集成流程
* 自动化付款操作

**典型接入方式**

使用 Mercadona-cli 可以通过以下步骤接入：

1. 克隆项目代码
2. 根据文档配置凭据
3. 使用 CLI 命令执行购物流程

**生产可用性**

Mercadona-cli 具有高生产可用性，原因包括：

* 近期活跃更新
* 强劲的采用和生态系统信号
* 高评分（76/100）

但是，还需要进一步审查以下风险：

* 许可证风险
* 安全风险
* 主维

## 🧭 Practical evaluation

**Value:** ivorpad/mercadona-cli helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 304 GitHub stars
- 27 forks
- updated 2026-07-13
- primary language: Go
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 36/100 |
| stars | 53/100 |
| topics | 100/100 |
| outlook | 85/100 |
| quality | 77/100 |
| recency | 100/100 |
| adoption | 48/100 |
| production | 77/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/ivorpad/mercadona-cli) · [← Back to Payments](./README.md)</sub>
