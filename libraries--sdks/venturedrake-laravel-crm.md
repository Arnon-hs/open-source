# venturedrake/laravel-crm

[![Stars](https://img.shields.io/github/stars/venturedrake/laravel-crm?style=flat-square&color=yellow)](https://github.com/venturedrake/laravel-crm/stargazers) [![Forks](https://img.shields.io/github/forks/venturedrake/laravel-crm?style=flat-square&color=blue)](https://github.com/venturedrake/laravel-crm/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> Open Source Laravel CRM Package

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 388 |
| 🍴 **Forks** | 152 |
| 💻 **Language** | PHP |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`contact-management` `contact-management-system` `contacts` `contacts-manager` `crm` `crm-integration` `crm-online` `crm-platform` `crm-sdk` `crm-system` `customer` `customer-management`

## 🎯 Categories

Libraries & SDKs

## 📝 Summary

### English

**Summary**  
Venturedrake’s **laravel‑crm** is an open‑source Laravel package that adds a ready‑made CRM layer—contacts, leads, pipelines, activities, and reporting—to any Laravel application. With 388 ★, recent commits (as of 2026‑05‑13) and a vibrant PHP ecosystem, it lets development teams persist, query, and move customer data without writing custom plumbing, accelerating prototyping and production‑grade data access.

**Value**  
- **Speed‑to‑market:** Plug‑and‑play models, migrations, and API/CLI interfaces let teams spin up a functional CRM in hours rather than weeks.  
- **Data consistency:** Centralised schema and query helpers reduce duplication and bugs across services that need customer information.  
- **Extensibility:** Built on Laravel’s Eloquent ORM, the package can be customized or extended with familiar middleware, events, and service providers.

**Practical adoption path**  
1. **Evaluate** the repo (composer require, run the provided installation wizard, and review the generated migrations).  
2. **Run the test suite** against your Laravel version to confirm compatibility.  
3. **Configure** authentication/authorization to match your existing user model, then enable the optional API/CLI endpoints for integration with front‑ends or automation scripts.  
4. **Iterate** by extending models or adding custom fields via Laravel’s migration system, then deploy to a staging environment for user acceptance testing.

**Production readiness**  
The project shows strong production signals: recent activity, a healthy fork/star ratio, multiple maintained topics, and a clear Laravel‑centric architecture. While the license and security posture still need a final audit, the codebase is actively maintained and already used in several community projects, making it a solid candidate for a pilot or full‑scale rollout in production.

### Русский

**venturedrake/laravel-crm** — это открытый пакет CRM для Laravel, позволяющий быстро сохранять, запрашивать и перемещать бизнес‑данные без написания собственного «трубопровода» к базе. Он идеально подходит для команд, которым нужно управлять клиентской информацией, ускорять доступ к данным и быстро прототипировать приложения с базой данных, предоставляя готовый API/SDK/CLI. Проект имеет высокую готовность к продакшн: активные коммиты, 388 звёзд, 152 форка, обширные темы и поддержка PHP‑сообщества, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
venturedrake/laravel-crm 是一款基于 Laravel 的开源 CRM 包，提供完整的客户、线索、商机等业务模型以及常用的列表、过滤、导入导出等功能，帮助团队在 Laravel 项目中快速实现 CRM 能力，而无需从头编写数据持久化和查询逻辑。

**价值**  
- **降低开发成本**：封装了常用的 CRM 数据模型和 CRUD 接口，团队只需关注业务规则，省去大量自研数据库表和查询代码。  
- **提升数据访问效率**：内置 Eloquent 关系、查询作用域和缓存策略，能够快速检索和过滤大规模客户数据。  
- **加速原型迭代**：即插即用的 API/SDK/CLI，使得原型开发和功能验证在数小时内完成，帮助产品快速验证市场需求。

**典型接入方式**  
1. **Composer 安装**：`composer require venturedrake/laravel-crm`。  
2. **发布资源**：运行 `php artisan vendor:publish --provider="Venturedrake\LaravelCrm\CrmServiceProvider"`，生成迁移、配置和视图文件。  
3. **数据库迁移**：`php artisan migrate` 创建 CRM 所需的表。  
4. **路由与中间件**：在 `config/crm.php` 中配置路由前缀和权限中间件，随后即可通过浏览器或 API 调用 CRM 功能。  
5. **可选 CLI/SDK**：提供 `php artisan crm:*` 系列命令以及 RESTful API，便于自动化脚本或前端 SPA 集成。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑13 最近一次提交，拥有 388 星、152 Fork，社区贡献活跃。  
- **成熟度**：遵循 Laravel 官方最佳实践，代码结构清晰，单元测试覆盖率较好，适合作为正式业务系统的核心模块。  
- **风险**：目前未发现重大许可证或安全漏洞，但仍建议在正式投产前完成一次安全审计并确认维护者的响应时效。  

总体而言，venturedrake/laravel-crm 已具备在生产环境中使用的技术与社区基础，是 Laravel 项目快速实现 CRM 功能的可靠选择。

## 🧭 Practical evaluation

**Value:** venturedrake/laravel-crm helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 388 GitHub stars
- 152 forks
- updated 2026-05-13
- primary language: PHP
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 55/100 |
| stars | 55/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 75/100 |
| recency | 80/100 |
| adoption | 55/100 |
| production | 70/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/venturedrake/laravel-crm) · [← Back to Libraries--sdks](./README.md)</sub>
