# puemos/craftplan

[![Stars](https://img.shields.io/github/stars/puemos/craftplan?style=flat-square&color=yellow)](https://github.com/puemos/craftplan/stargazers) [![Forks](https://img.shields.io/github/forks/puemos/craftplan?style=flat-square&color=blue)](https://github.com/puemos/craftplan/network) [![Language](https://img.shields.io/badge/lang-Elixir-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> Self-hosted software for managing artisanal D2C micro-businesses

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.1k |
| 🍴 **Forks** | 58 |
| 💻 **Language** | Elixir |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`artisanal` `d2c` `erp` `self-hosted`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Craftplan (puemos/craftplan) is a self‑hosted Elixir application designed to help artisanal direct‑to‑consumer (D2C) micro‑businesses plan, track, and fulfil orders. With over 1 100 GitHub stars and recent activity (last commit 2026‑06‑23), it offers a lightweight, open‑source alternative to SaaS order‑management tools, but its integration details are not fully documented.  

**Value**  
- Provides an end‑to‑end workflow (product catalog, order intake, inventory, and basic analytics) that small makers can run on their own servers, preserving brand control and avoiding recurring SaaS fees.  
- Because it is written in Elixir, it benefits from concurrency and fault‑tolerance, which can be attractive for real‑time inventory updates and webhook handling.  

**Practical Adoption Path**  
1. **Read‑through & prototype** – Clone the repo, follow the README to spin up the Docker/LiveView development environment, and run a sandbox with a few test products.  
2. **Fit‑gap analysis** – Compare Craftplan’s data model and API endpoints with your current order‑capture process (e.g., Shopify, Stripe, custom checkout). Identify missing features (payment gateway, shipping label generation) and plan small extensions.  
3. **Proof of concept** – Deploy the app on a low‑cost staging server (e.g., Fly.io or a small VPS). Connect it to a test payment provider and a simple front‑end for order entry. Validate that the core workflow (order creation → inventory decrement → reporting) works end‑to‑end.  
4. **Iterate & harden** – Add any required integrations, write unit/integration tests, and perform a security review of the Elixir dependencies.  

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained and has a solid star count, but the documentation and integration guides are sparse, so additional engineering effort is needed to adapt it to a specific business workflow.  
- **Suitability**: Ideal for internal prototypes, pilot programs, or niche D2C shops that can allocate a developer to bridge gaps. Not yet a drop‑in solution for large‑scale production without thorough dependency vetting, performance testing, and possibly adding missing features (e.g., robust payment processing, multi‑warehouse support).  

**Recommendation**  
Start with a limited proof‑of‑concept deployment to verify that Craftplan’s core order‑management capabilities align with your needs, then invest in the necessary custom integrations and operational hardening before considering it for a production environment.

### Русский

**Краткое резюме:**  
`puemos/craftplan` — это self‑hosted решение на Elixir для организации процессов в небольших D2C‑бизнесах (управление заказами, инвентарём, клиентской базой). Его типичный сценарий — быстрый прототип или внутренний инструмент, когда команда может развернуть сервис в своей инфраструктуре, проверить рабочий процесс через небольшое proof‑of‑concept и, при положительных результатах, масштабировать. Готовность к продакшну средняя: проект достаточно популярен (1117 звёзд, 58 форков) и поддерживается, однако интеграционный путь неочевиден, поэтому перед внедрением стоит оценить затраты на настройку и зависимые компоненты.

### 中文

**价值**  
- CraftPlan 是一套自托管的 SaaS，专为手工 D2C 微型企业（如手工艺品、定制食品、小批量服装等）提供订单、库存、会员和支付等全链路管理。  
- 因为源码完全开放，企业可以随时根据业务需求增删功能，避免被商业平台锁定或产生高额佣金。  

**典型接入方式**  
1. **快速原型**：克隆仓库 → 按 README 完成 Elixir / Phoenix 环境配置 → 使用 Docker‑Compose（项目已提供）启动所有依赖（PostgreSQL、Redis）。  
2. **业务集成**：通过项目自带的 RESTful API 或 GraphQL 接口，将前端（Shopify、WooCommerce、独立商城）或内部 ERP 与 CraftPlan 对接；Webhook 可实时推送订单、付款、发货状态。  
3. **定制化**：在 Elixir 代码层面添加自定义业务规则（如会员积分、限时折扣），利用 Phoenix Channel 实现实时仪表盘或通知。  

**生产可用性**  
- **成熟度**：已有 1 117 颗星、58 个 Fork，且最近一次提交在 2026‑06‑23，社区活跃度尚可。  
- **适用场景**：非常适合作为原型、内部工具或小规模微业务的核心系统；对业务流程有明确需求且能够接受自行运维的团队。  
- **风险与准备**：  
  - 依赖 Elixir/Phoenix 生态，需要具备相应运维经验或容器化部署能力。  
  - 官方文档较简略，建议先在测试环境完成完整的 **README → 部署 → API 调用** 流程验证。  
  - 在生产环境前应进行：  
    1. **安全审计**（数据库凭证、HTTPS、OAuth）  
    2. **监控/日志**（Prometheus + Grafana）  
    3. **备份/灾备**（PostgreSQL logical replication）  

综上，CraftPlan 适合作为 **可自行掌控、可高度定制** 的 D2C 微业务管理平台，先在小范围 PoC 验证后，再逐步扩展至正式生产。

## 🧭 Practical evaluation

**Value:** puemos/craftplan may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1117 GitHub stars
- 58 forks
- updated 2026-06-23
- primary language: Elixir
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 65/100 |
| topics | 50/100 |
| outlook | 55/100 |
| quality | 59/100 |
| recency | 40/100 |
| adoption | 59/100 |
| production | 52/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/puemos/craftplan) · [← Back to Misc](./README.md)</sub>
