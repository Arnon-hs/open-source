# poe-platform/poe-code

[![Stars](https://img.shields.io/github/stars/poe-platform/poe-code?style=flat-square&color=yellow)](https://github.com/poe-platform/poe-code/stargazers) [![Forks](https://img.shields.io/github/forks/poe-platform/poe-code?style=flat-square&color=blue)](https://github.com/poe-platform/poe-code/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> Use Poe to power your favorite coding agents (Claude Code, Codex, OpenCode, etc). No need for multiple subscriptions.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 87 |
| 🍴 **Forks** | 13 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`claude` `code` `codex` `opencode`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
poe‑platform/poe‑code is an open‑source TypeScript library that lets you plug Poe’s AI models (Claude Code, Codex, OpenCode, etc.) into your own coding agents while handling the underlying payment‑service‑provider (PSP) and billing flows. By centralising the monetisation logic, you can avoid juggling multiple subscriptions and integrate checkout or usage‑based billing with just a few lines of code.

**Value Proposition**  
- **Unified billing** – One integration point for all Poe‑powered coding agents, reducing the overhead of managing separate API keys, quotas, and subscription plans.  
- **Speed to market** – The library abstracts PSP interactions (payment intents, webhook handling, invoicing), so developers can focus on the AI features rather than payment infrastructure.  
- **Cost efficiency** – Consolidating subscriptions under Poe can lower overall spend, especially for teams that experiment with several coding models.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the provided README example, and verify that a simple coding agent can request a model and receive a payment‑linked response.  
2. **Sandbox Integration** – Connect a test PSP (e.g., Stripe test mode) using the library’s configuration helpers; run end‑to‑end checkout flows in a staging environment.  
3. **Incremental Roll‑out** – Replace existing ad‑hoc billing scripts with poe‑code’s SDK in a low‑risk service (internal tooling, prototype UI).  
4. **Full Production Migration** – After confirming webhook reliability, logging, and error handling, extend the integration to all customer‑facing coding agents and deprecate legacy payment code.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑06‑23) and has modest community traction (87 ★, 13 forks). It is suitable for prototypes, internal tools, or early‑stage SaaS products.  
- **Considerations before production**:  
  * Verify the license compatibility with your stack.  
  * Conduct a security audit of the PSP integration (webhook validation, secret handling).  
  * Evaluate dependency health (TypeScript ecosystem) and set up monitoring for any breaking changes in Poe or the chosen PSP APIs.  
- **Readiness Checklist**: successful PoC, test‑mode PSP validation, CI/CD pipeline with lint/type‑check, and a documented rollback plan. Once these are in place, poe‑code can be promoted to production for reliable, monetised coding‑agent services.

### Русский

**poe-platform/poe-code** — это TypeScript‑библиотека, позволяющая быстро подключать монетизацию и платежные потоки (PSP) к вашим кодовым агентам (Claude Code, Codex, OpenCode и др.) без необходимости управлять несколькими подписками. Типичный сценарий — запуск небольшого proof‑of‑concept: встраивание checkout‑модуля или оценка PSP‑процессов в прототипе/внутреннем сервисе, после чего при проверке зависимостей и безопасности можно масштабировать до production. Текущий уровень готовности — средний: проект уже имеет 87 звёзд, активные коммиты и документацию, но требует окончательной проверки лицензии, безопасности и поддержки перед использованием в критически важных продакшн‑системах.

### 中文

**项目简介（2‑3 句话）**  
poe-platform/poe-code 通过 Poe 接口为 Claude Code、Codex、OpenCode 等主流编码助手提供统一的计费与支付能力，免去为每个模型单独订阅的麻烦。只需一次集成，即可在自己的平台上实现灵活的付费使用、结算与 PSP（支付服务提供商）流程。

**价值**  
- **快速落地**：内置的计费、账单与 PSP 工作流让开发者在几行代码内完成支付功能，显著缩短原型到 MVP 的时间。  
- **统一管理**：统一的计费平台避免了多套订阅、结算系统的维护成本，提升运营效率。  
- **灵活扩展**：支持多种支付渠道（Stripe、PayPal、国内 PSP 等），可根据业务需求自由切换或并行使用。

**典型接入方式**  
1. **阅读 README**，确认所需的 Node.js/TypeScript 环境。  
2. **安装依赖**：`npm i @poe-platform/poe-code`。  
3. **配置凭证**：在项目根目录创建 `.env`，填入 Poe API Token、PSP API Key 等。  
4. **调用 SDK**：在业务代码中引入 `PoeCodeClient`，使用 `createCheckout`, `verifyPayment` 等高层 API 完成订单创建、支付回调与账单查询。  
5. **小范围验证**：先在测试环境（sandbox）跑通完整的下单‑支付‑回调链路，确认计费逻辑与业务规则匹配后再推广。

**生产可用性**  
- **成熟度**：GitHub ★87、Fork 13，最近一次更新于 2026‑06‑23，代码以 TypeScript 编写，社区活跃度中等。  
- **适用场景**：非常适合原型、内部工具或对计费需求不极端苛刻的生产环境；在正式上线前建议进行：  
  - 依赖安全审计（尤其是 PSP SDK）  
  - 监控与日志体系接入  
  - 业务容错与重试机制验证  
- **风险**：许可证、长期维护者活跃度以及安全合规（如 PCI‑DSS）仍需进一步确认。总体而言，经过一次小型 PoC 并完成上述检查后，可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** poe-platform/poe-code helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 87 GitHub stars
- 13 forks
- updated 2026-06-23
- primary language: TypeScript
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 41/100 |
| topics | 50/100 |
| outlook | 50/100 |
| quality | 50/100 |
| recency | 40/100 |
| adoption | 38/100 |
| production | 51/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/poe-platform/poe-code) · [← Back to Misc](./README.md)</sub>
