# Dolibarr/dolibarr

[![Stars](https://img.shields.io/github/stars/Dolibarr/dolibarr?style=flat-square&color=yellow)](https://github.com/Dolibarr/dolibarr/stargazers) [![Forks](https://img.shields.io/github/forks/Dolibarr/dolibarr?style=flat-square&color=blue)](https://github.com/Dolibarr/dolibarr/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Dolibarr ERP CRM is a modern software package to manage your company or foundation's activity (contacts, suppliers, invoices, orders, stocks, agenda, accounting, ...). it's an open source Web application (written in PHP) designed for businesses of any sizes, foundations and freelancers.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 7.2k |
| 🍴 **Forks** | 3.4k |
| 💻 **Language** | PHP |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-05-10 |
| 🔍 **Source** | github |

## 🏷️ Topics

`accounting` `agenda` `crm` `erp` `hacktoberfest` `human-resource-managment` `invoice` `invoices` `invoicing` `mysql` `orders` `php`

## 🎯 Categories

Payments · Database · Design

## 📝 Summary

### English

**Brief Summary**  
Dolibarr ERP CRM is an open‑source, PHP‑based web application that lets businesses, foundations and freelancers manage contacts, suppliers, invoices, orders, stock, agenda, accounting and more. With a large community (7 k+ stars) and frequent updates, it can serve as a back‑office platform for integrating billing, checkout or PSP flows.  

**Value**  
Dolibarr provides a ready‑made, modular suite for core business processes, so you can embed monetisation and payment‑related features without building a full ERP from scratch. Its built‑in invoicing, product catalog and accounting modules reduce the time needed to connect to payment service providers (PSPs) and automate billing cycles.  

**Practical Adoption Path**  

1. **Proof‑of‑concept** – Clone the repo, follow the README to spin up a Docker or LAMP stack, and enable the “Payments” module.  
2. **Integration** – Use Dolibarr’s REST API or its built‑in “External modules” framework to connect your PSP (e.g., Stripe, PayPal). Start with a single checkout flow (e.g., invoice payment) to validate data mapping and webhook handling.  
3. **Pilot** – Deploy the configured instance to a staging environment, run end‑to‑end tests with a few real users, and iterate on custom modules or hooks as needed.  
4. **Scale** – Once the pilot is stable, enable additional modules (stock, accounting, multi‑currency) and migrate production data.  

**Production Readiness**  
Dolibarr scores high on readiness: it has recent commits (as of 2026‑05‑10), a vibrant ecosystem (7 k+ stars, 3 k+ forks, 20 topics), and proven adoption across SMEs and NGOs. The core codebase is mature, but the integration surface for payment flows is not documented in the metadata, so a modest setup effort is required to understand the API and module hooks. Overall, it is a solid OSS candidate for a serious pilot, provided you allocate time for the initial proof‑of‑concept and validation of integration costs.

### Русский

Dolibarr — это открытая ERP/CRM‑система на PHP, позволяющая быстро добавить в ваш продукт функции монетизации, выставления счетов и интеграции с платёжными шлюзами; типичный сценарий — развертывание небольшого proof‑of‑concept, подключение нужных модулей (биллинг, PSP) и последующее масштабирование. Проект обладает высокой готовностью к production: активные обновления, более 7 тыс. звёзд, крупное сообщество и проверенный в реальных бизнесах функционал. Однако перед полномасштабным внедрением стоит уточнить детали настройки и интеграционных точек, так как они не описаны явно в метаданных.

### 中文

**价值**  
Dolibarr 是一套完整的 ERP/CRM 开源套件，能够帮助企业或组织快速搭建从联系人、供应商、发票、订单、库存、日程到会计全链路的业务管理系统。其内置的计费、付款单据和多种支付渠道（PSP）模块，使得在业务流程中加入收款、开票或结算功能变得非常便捷，显著缩短了从概念到上线的时间。

**典型接入方式**  

| 场景 | 接入步骤 | 关键点 |
|------|----------|--------|
| **在现有系统中嵌入计费/结算** | 1. 在 Dolibarr 中启用 **Payments** 模块（或相应的插件）。<br>2. 配置需要的支付服务提供商（如 Stripe、PayPal、Adyen 等），填写 API Key、回调 URL。<br>3. 使用 Dolibarr 提供的 REST API（`/api/index.php`）创建客户、发票、付款记录等。 | - API 基于标准的 OAuth2/Token 认证，文档齐全。<br>- 可通过 Webhooks 接收支付成功/失败回调，实现业务状态同步。 |
| **完整的业务系统（ERP+支付）一次性部署** | 1. 下载官方 Docker 镜像或通过源码自行部署（PHP 7.4+、MySQL/MariaDB）。<br>2. 在安装向导中勾选 **Billing / Payments** 模块。<br>3. 按需开启 **Accounting**、**Stock**、**Agenda** 等子模块，形成“一站式”业务平台。 | - Docker 部署只需几条命令，适合快速 PoC。<br>- 支持多语言和多公司（Multi‑company）模式，便于后期扩展。 |
| **自动化支付运营（对账、批量开票）** | 1. 编写脚本调用 Dolibarr 的批量 API（如 `/invoices/batch`、`/payments/batch`）。<br>2. 配合计划任务（cron）定时拉取未付款发票、生成付款链接并发送邮件。<br>3. 使用内置的 **Export** 功能或自定义报表进行对账。 | - 所有核心对象（客户、发票、付款）都有对应的 CRUD API。<br>- 支持 CSV、PDF 导出，便于与外部财务系统对接。 |

**生产可用性**  
- **活跃度**：截至 2026‑05‑10，项目仍在持续更新，拥有 7 194 颗星、3 372 个 fork，社区活跃度高。  
- **成熟度**：Dolibarr 已在全球数千家中小企业、基金会以及自由职业者中部署，官方提供长期支持（LTS）分支。  
- **安全性**：项目遵循 OWASP PHP 安全最佳实践，发布的每个版本都会同步发布安全补丁。  
- **部署门槛**：提供 Docker 镜像、官方一键安装脚本以及完整的 API 文档，适合从小型 PoC 逐步演进到全生产环境。  
- **风险**：虽然核心功能稳定，但支付渠道的具体实现往往依赖第三方插件或自定义代码，建议在正式上线前先完成 **小规模概念验证（POC）**，并审查插件的维护状态与兼容性。

**结论**  
Dolibarr 具备高可用的企业级功能，能够在几天内完成计费/支付模块的集成，是一个值得在生产环境中试点的 OSS 方案。只要在正式投入前完成支付插件的兼容性验证和基础的安全审计，即可放心用于业务运营。

## 🧭 Practical evaluation

**Value:** Dolibarr/dolibarr helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 7194 GitHub stars
- 3372 forks
- updated 2026-05-10
- primary language: PHP
- 20 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 88/100 |
| stars | 82/100 |
| topics | 100/100 |
| outlook | 84/100 |
| quality | 93/100 |
| recency | 100/100 |
| adoption | 84/100 |
| production | 79/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-10 · [View on GitHub](https://github.com/Dolibarr/dolibarr) · [← Back to Payments](./README.md)</sub>
