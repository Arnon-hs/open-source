# shaxzodbek-uzb/pay-uz

[![Stars](https://img.shields.io/github/stars/shaxzodbek-uzb/pay-uz?style=flat-square&color=yellow)](https://github.com/shaxzodbek-uzb/pay-uz/stargazers) [![Forks](https://img.shields.io/github/forks/shaxzodbek-uzb/pay-uz?style=flat-square&color=blue)](https://github.com/shaxzodbek-uzb/pay-uz/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Для национальных платежных систем в Узбекистане

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 85 |
| 🍴 **Forks** | 42 |
| 💻 **Language** | PHP |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`billing` `clickuz` `laravel` `payment-gateway` `paymeuz` `paynet-uz` `uzbekistan`

## 🎯 Categories

Payments

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*shaxzodbek-uzb/pay‑uz* is an open‑source PHP library that streamlines integration with Uzbekistan’s national payment systems (e.g., Uzcard, Humo, PayMe). It provides ready‑made API/SDK wrappers and CLI helpers so developers can add billing, checkout, or PSP‑flow automation to their applications with minimal boiler‑plate. With 85 GitHub stars and recent updates (June 2026), it is a practical choice for prototypes or internal tools, though a final security and licensing audit is advisable before production use.  

**Value**  
- **Speed:** Pre‑built request/response handling, signature generation, and error mapping cut weeks of custom code.  
- **Consistency:** A single, documented interface abstracts the quirks of multiple Uzbek payment gateways, reducing bugs and maintenance overhead.  
- **Extensibility:** The library’s modular design lets you swap or chain PSPs, making it easy to experiment with different monetisation strategies.  

**Practical Adoption Path**  
1. **Evaluate:** Clone the repo, run the provided unit tests, and inspect the API docs to confirm it supports the required gateway(s).  
2. **Prototype:** Add the Composer package to a sandbox PHP project, configure credentials in a `.env` file, and use the CLI to generate a test payment request.  
3. **Integrate:** Replace the prototype’s payment calls with the library’s service classes, wiring them into your existing billing or checkout workflow.  
4. **Validate:** Perform end‑to‑end testing against the gateway’s sandbox, run static‑analysis/security scans, and review the license (MIT‑style) for compliance.  

**Production Readiness**  
- **Maturity:** Medium – the codebase is actively maintained (last commit 2026‑06‑22) and has community traction (85 ★, 42 forks).  
- **Stability:** Suitable for internal tools or low‑risk production pilots; however, a thorough security review and dependency audit are required before high‑volume deployment.  
- **Support:** No dedicated maintainer listed; rely on community issues/PRs for bug fixes.  

Overall, *pay‑uz* offers a fast, low‑friction way to hook into Uzbekistan’s national payment ecosystem, making it a solid starting point for prototypes and internal services, with the caveat that additional vetting is needed for mission‑critical production environments.

### Русский

**shaxzodbek-uzb/pay-uz** — это открытая PHP‑библиотека, ускоряющая интеграцию национальных платёжных систем Узбекистана в ваши продукты: она предоставляет готовые API/SDK/CLI‑модули для быстрой реализации биллинга, checkout‑процессов и автоматизации PSP‑операций. Типичный сценарий — подключение к локальному PSP (например, PayMe, Click) для прототипов или внутренних сервисов, где требуется быстро проверить и отладить платёжный поток. Проект находится на среднем уровне готовности к production: имеет активные коммиты, 85 звёзд и 42 форка, но перед развёртыванием в продакшн рекомендуется проверить лицензию, безопасность зависимостей и наличие поддерживающих мейнтейнеров.

### 中文

shaxzodbek-uzb/pay-uz 是一个专为乌兹别克斯坦国家支付系统设计的 PHP 库，能够快速实现计费、结算或 PSP（支付服务提供商）流程，从而加速货币化和支付操作的集成。典型的接入方式是通过其提供的 API/SDK/CLI 在项目中引入相应的支付模块，进行计费或结算流程的自动化。虽然该项目在原型或内部工作流中表现良好（已有 85 颗星、42 次 Fork，定期更新），但在生产环境使用前仍需进行依赖审查、安全评估以及维护者活跃度的确认。

## 🧭 Practical evaluation

**Value:** shaxzodbek-uzb/pay-uz helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 85 GitHub stars
- 42 forks
- updated 2026-06-22
- primary language: PHP
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 41/100 |
| topics | 88/100 |
| outlook | 69/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 41/100 |
| production | 67/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/shaxzodbek-uzb/pay-uz) · [← Back to Payments](./README.md)</sub>
