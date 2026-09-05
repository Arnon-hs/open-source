# fivetran/dbt_stripe

[![Stars](https://img.shields.io/github/stars/fivetran/dbt_stripe?style=flat-square&color=yellow)](https://github.com/fivetran/dbt_stripe/stargazers) [![Forks](https://img.shields.io/github/forks/fivetran/dbt_stripe?style=flat-square&color=blue)](https://github.com/fivetran/dbt_stripe/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-49%2F100-brightgreen?style=flat-square)](#)

> Data models for Stripe built using dbt.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 58 |
| 🍴 **Forks** | 40 |
| 💻 **Language** | Shell |
| 📈 **Score** | 49/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`dbt` `dbt-packages` `fivetran` `stripe`

## 🎯 Categories

Payments

## 📝 Summary

### English

**Summary**  
fivetran/dbt_stripe provides ready‑made dbt models that surface Stripe’s payment, billing, and checkout data in a clean, analytics‑friendly format. By dropping in the package and configuring a few connection variables, teams can quickly build dashboards or run analyses on monetisation and PSP (payment service provider) flows without hand‑crafting the underlying SQL.

**Value**  
- Accelerates the creation of a unified Stripe data warehouse, turning raw event logs into normalized tables for reporting, churn analysis, revenue recognition, and fraud monitoring.  
- Reduces engineering overhead: the models handle common Stripe objects (customers, invoices, payments, subscription schedules, etc.) and include pre‑built tests and documentation.  
- Enables data‑driven product decisions and automated billing operations by giving analysts a reliable, version‑controlled source of truth.

**Practical adoption path**  
1. **Proof‑of‑concept** – Fork the repo, run the provided `README` steps on a sandbox Snowflake/BigQuery/Redshift warehouse, and validate that the generated tables match your Stripe account.  
2. **Configuration** – Add your Stripe API credentials and set the required dbt variables (e.g., `stripe_schema`, `stripe_database`).  
3. **Selective enablement** – Enable only the models you need (e.g., `payments`, `subscriptions`) to keep the build fast and limit unnecessary data ingestion.  
4. **Testing & CI** – Leverage the built‑in dbt tests and integrate the package into your existing dbt CI pipeline.  
5. **Scale** – Once the PoC is approved, promote the same dbt project to production, schedule regular runs, and monitor model freshness.

**Production readiness**  
- **Maturity:** Medium. The repo has modest community traction (≈58 ★, 40 forks) and recent activity (updated 2026‑05‑14), indicating active maintenance but limited enterprise‑grade validation.  
- **Dependencies:** Primarily a Shell‑based setup wrapper and dbt; ensure your dbt version aligns with the package’s requirements.  
- **Risks:** The integration steps are not fully spelled out in the metadata, so initial setup may require extra investigation and a small pilot to gauge effort.  
- **Recommendation:** Suitable for internal prototypes, analytics sandboxes, or early‑stage billing dashboards. For production use, perform a controlled rollout, audit the generated SQL for compliance with your data‑governance policies, and establish monitoring around model failures and Stripe API changes.

### Русский

**fivetran/dbt_stripe** — набор готовых dbt‑моделей для аналитики данных Stripe, позволяющих быстро построить отчёты по монетизации, биллингу и процессам PSP без написания собственного ETL‑кода. Обычно проект внедряется в виде небольшого proof‑of‑concept: подключаете репозиторий, настраиваете соединение с вашими Stripe‑данными и проверяете готовые модели, после чего расширяете их под свои бизнес‑требования. Готовность к продакшну — средняя: модель подходит для прототипов и внутренних воркфлоу, но требует проверки зависимостей, обновлений и адаптации под ваш пайплайн перед масштабным запуском.

### 中文

**项目简介**  
fivetran/dbt_stripe 是一套基于 dbt 的开源数据模型，专门用于把 Stripe 的交易、账单、客户等原始数据转化为分析友好的表结构，帮助团队快速构建付款、计费和 PSP（支付服务提供商）相关的业务报表。

**价值**  
- **加速业务洞察**：预置的模型已经完成了常用的聚合、清洗和维度化，业务方无需自行编写繁琐的 SQL，即可直接在 BI 工具中查询收入、退款、订阅生命周期等关键指标。  
- **降低集成成本**：只需把 Stripe 数据通过 Fivetran（或其他 ELT 工具）同步到数据仓库，然后运行 dbt 即可得到完整的分析层，省去从头设计数据模型的时间。  
- **支持实验与迭代**：模型结构清晰、可配置，适合在原型、内部仪表盘或 A/B 测试中快速验证计费策略和支付流程。

**典型接入方式**  
1. **数据同步**：使用 Fivetran（或 Stitch、Airbyte 等）将 Stripe API 的原始事件、费用、发票等表同步到目标数据仓库（如 Snowflake、BigQuery、Redshift）。  
2. **dbt 项目引入**：在已有的 dbt 项目中添加 `fivetran/dbt_stripe` 作为子模块或 package，配置 `profiles.yml` 指向同步后的原始表。  
3. **运行 dbt**：执行 `dbt deps && dbt run`，模型会在仓库中生成 `stripe_*` 维度表和事实表。  
4. **验证 & 扩展**：通过 README 中的示例查询验证结果，随后根据业务需要在 `models` 目录下添加自定义派生表或覆盖默认变量。

**生产可用性**  
- **成熟度**：GitHub 58 星、40 Fork，最近一次更新在 2026‑05‑14，社区活跃度一般。模型已在多个企业内部原型中使用，具备 **中等** 的生产就绪度。  
- **适用场景**：非常适合原型、内部报表或对数据质量要求不是极端严格的业务流程；在正式生产环境使用前建议：  
  1. **小范围 PoC**：先在测试库跑通完整的 ELT + dbt 流程，检查字段映射和数据完整性。  
  2. **依赖审计**：确认所用的 dbt 版本、适配的仓库方言以及 Fivetran 连接器的费用和配额。  
  3. **运维准备**：为模型添加监控（如 dbt test、数据质量检查）并制定变更审查流程，以防 Stripe API 版本升级导致模型失效。  
- **风险**：项目的接入文档相对简略，具体的配置步骤需要自行探索；若对实时性或高可用有严格要求，需额外评估同步延迟和故障恢复方案。

**总结**：fivetran/dbt_stripe 能显著缩短 Stripe 数据分析的搭建时间，适合作为内部原型或中等规模的生产报表基础，只要在正式上线前完成小规模验证并做好运维监控，即可安全投入使用。

## 🧭 Practical evaluation

**Value:** fivetran/dbt_stripe helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 58 GitHub stars
- 40 forks
- updated 2026-05-14
- primary language: Shell
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 40/100 |
| stars | 38/100 |
| topics | 50/100 |
| outlook | 61/100 |
| quality | 60/100 |
| recency | 80/100 |
| adoption | 38/100 |
| production | 62/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/fivetran/dbt_stripe) · [← Back to Payments](./README.md)</sub>
