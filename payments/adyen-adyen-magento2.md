# Adyen/adyen-magento2

[![Stars](https://img.shields.io/github/stars/Adyen/adyen-magento2?style=flat-square&color=yellow)](https://github.com/Adyen/adyen-magento2/stargazers) [![Forks](https://img.shields.io/github/forks/Adyen/adyen-magento2?style=flat-square&color=blue)](https://github.com/Adyen/adyen-magento2/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> Adyen Payment plugin for Magento2

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 166 |
| 🍴 **Forks** | 220 |
| 💻 **Language** | PHP |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`adyen` `adyen-plugin` `ecommerce` `hacktoberfest` `magento` `magento2` `magento2-extension` `magento2-module` `payments`

## 🎯 Categories

Payments

## 📝 Summary

### English

**Summary**  
Adyen’s adyen‑magento2 is an open‑source PHP plugin that lets Magento 2 merchants connect to the Adyen PSP for seamless checkout, billing, and payment‑operation automation. With strong community signals (166 ⭐, 220 forks, recent commits) and straightforward integration hooks (API/SDK/CLI), it’s a mature candidate for pilots or production use.

**Value**  
The plugin accelerates the implementation of Adyen’s payment suite—card, wallets, local payments, and recurring billing—by handling the heavy lifting of API calls, tokenisation, and webhook processing. This reduces development effort, shortens time‑to‑market, and gives merchants a reliable, standards‑compliant checkout experience while retaining the flexibility to customise Magento’s flow.

**Practical adoption path**  

1. **Pre‑flight** – Review the repository, confirm the MIT‑style license, and run a quick security scan of the code.  
2. **Installation** – Add the package via Composer (`composer require adyen/module-payment`) and enable the module with Magento CLI (`bin/magento module:enable Adyen_Payment`).  
3. **Configuration** – Supply your Adyen API credentials (API key, merchant account) in the Magento admin, select required payment methods, and map webhooks.  
4. **Testing** – Switch the plugin to Adyen’s test environment, run end‑to‑end checkout tests, and optionally use the provided CLI tools for sandbox token generation.  
5. **Go‑live** – Flip the environment flag to production, monitor webhook logs, and enable fraud‑prevention rules in the Adyen dashboard.

**Production readiness**  
The project shows high production readiness: it is actively maintained (last commit 2026‑05‑12), widely adopted (166 stars, 220 forks), and integrates cleanly with Magento 2’s modular architecture. While the license and security posture merit a final review, the combination of recent activity, robust community support, and clear implementation signals makes adyen‑magento2 suitable for a serious pilot and, with standard hardening, for full production deployment.

### Русский

Adyen/adyen-magento2 — это открытый PHP‑плагин, позволяющий быстро подключить платежный шлюз Adyen к Magento 2, автоматизировать процесс оплаты и упростить интеграцию billing/checkout‑функций. Типичный сценарий: разработчик добавляет модуль в магазин, настраивает API‑ключи и получает готовый к использованию PSP‑flow без написания собственного кода. Проект демонстрирует высокий уровень готовности к production: активные коммиты, более 160 звёзд, широкое принятие в сообществе и стабильный набор функций, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
Adyen/adyen-magento2 是 Adyen 官方提供的 Magento 2 支付插件，帮助商家在 Magento 平台上快速接入 Adyen 的多渠道支付、结算和风控能力。

**价值**  
- **加速支付上线**：一键配置即可支持信用卡、数字钱包、本地支付等多种支付方式，省去自行开发 PSP 接口的时间和成本。  
- **统一结算与风控**：利用 Adyen 完整的结算、对账和风险管理功能，提升收款成功率并降低欺诈损失。  
- **灵活扩展**：插件提供 API/SDK 接口，支持自定义支付流程、分期、订阅等业务场景。

**典型接入方式**  
1. 在 Magento 后台通过 Composer 安装插件 `composer require adyen/module-payment`。  
2. 在 Magento 管理后台填写 Adyen 商户账号、API 密钥等凭证并启用所需的支付方式。  
3. 如需深度定制，可在 `app/code/Adyen/Payment` 目录下使用提供的 PHP SDK 调用 Adyen API，或通过插件的事件/观察者机制拦截支付流程。

**生产可用性**  
- **活跃度高**：2026‑05‑12 最近一次提交，166 Stars、220 Forks，社区和官方均保持活跃维护。  
- **成熟度**：已在多个大型 Magento 商城上线，具备完整的单元测试和 CI，符合生产环境的可靠性要求。  
- **风险**：需进一步审查许可证（MIT）以及安全补丁的响应速度，但总体上已具备在正式业务中安全、稳定运行的条件。

## 🧭 Practical evaluation

**Value:** Adyen/adyen-magento2 helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 166 GitHub stars
- 220 forks
- updated 2026-05-12
- primary language: PHP
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 59/100 |
| stars | 47/100 |
| topics | 100/100 |
| outlook | 51/100 |
| quality | 58/100 |
| recency | 20/100 |
| adoption | 50/100 |
| production | 49/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/Adyen/adyen-magento2) · [← Back to Payments](./README.md)</sub>
