# nextcloud/news

[![Stars](https://img.shields.io/github/stars/nextcloud/news?style=flat-square&color=yellow)](https://github.com/nextcloud/news/stargazers) [![Forks](https://img.shields.io/github/forks/nextcloud/news?style=flat-square&color=blue)](https://github.com/nextcloud/news/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> 📰 RSS/Atom feed reader

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 986 |
| 🍴 **Forks** | 195 |
| 💻 **Language** | PHP |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`atom-feed` `feed` `feed-reader` `hacktoberfest` `news` `nextcloud` `nextcloud-news` `rss` `rss-reader`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
Nextcloud News is an open‑source RSS/Atom feed reader built as a Nextcloud app (PHP). With a solid community (≈1 k stars, active commits, and many forks) it is production‑ready for pilots, though the integration steps are not fully documented and should be validated with a small proof‑of‑concept.  

**Value**  
The app lets teams centralise news feeds inside an existing Nextcloud deployment, providing a single sign‑on, shared storage, and collaborative tagging/reading experience without needing a separate feed service. This can streamline information sharing for project groups, support desks, or any workflow that already relies on Nextcloud for file and communication management.  

**Practical adoption path**  
1. **Proof of concept** – Deploy the app on a test Nextcloud instance, follow the README to configure a few feeds, and verify that users can add, read, and tag items.  
2. **Integration check** – Review the app’s settings, API endpoints, and any required background jobs (cron/occ) to ensure they fit your infrastructure and security policies.  
3. **Pilot rollout** – Enable the app for a limited user group, collect feedback on UI, performance, and any needed customisations (e.g., LDAP groups, notification hooks).  
4. **Full deployment** – After confirming low setup cost and acceptable maintenance overhead, roll the app out to all users and integrate it with existing Nextcloud workflows (e.g., automating feed updates via Nextcloud Flow).  

**Production readiness**  
The project scores high on readiness: recent commits (as of 2026‑06‑28), active community, and strong adoption signals make it suitable for a serious pilot. The main risk lies in the lack of explicit integration documentation, so a small‑scale test is essential to gauge configuration effort and any hidden dependencies before committing to a production environment.

### Русский

**nextcloud/news** — это open‑source RSS/Atom‑читалка, интегрируемая в экосистему Nextcloud, позволяющая пользователям централизованно собирать, просматривать и делиться новостными лентами прямо из собственного облака. Типичный сценарий внедрения — установка приложения в тестовом Nextcloud‑инстансе, проверка README и базовых функций (подписка на ленты, групповой доступ, уведомления), а затем масштабирование на продакшн‑окружение для команд, которым нужен безопасный внутренний агрегатор новостей. Проект считается готовым к production: активные обновления (последний — 2026‑06‑28), более 980 звёзд, 195 форков и широкая поддержка PHP‑сообщества, однако перед полным rollout стоит уточнить детали интеграции и оценить затраты на настройку.

### 中文

**项目简介**  
nextcloud/news 是一款基于 Nextcloud 的 RSS/Atom 订阅阅读器，提供在私有云环境中统一管理、聚合和离线阅读各类信息流的功能。  

**价值**  
- **数据自主可控**：所有订阅内容都存储在自己的 Nextcloud 实例中，避免将阅读记录托管在第三方服务。  
- **统一协作平台**：与 Nextcloud 的文件、共享、通知等模块深度集成，用户可以直接在已有的云盘工作空间里打开、标记或转发文章。  
- **企业级安全**：继承 Nextcloud 的身份验证、访问控制和端到端加密，满足企业对内部信息流的合规需求。  

**典型接入方式**  
1. **部署 Nextcloud**（Docker、Snap、APT 等官方方式）并确保已启用 App Store。  
2. 在 Nextcloud 后台的「应用」页面搜索并安装 **News** 应用。  
3. 使用管理员账号登录 Nextcloud，进入「News」应用完成首次配置：  
   - 添加 RSS/Atom 源（手动或通过 OPML 导入）  
   - 设置同步间隔、缓存大小等参数  
   - 如需对外部用户开放，只需在 Nextcloud 中创建相应用户并赋予 News 权限。  
4. （可选）通过 Nextcloud 的 **OAuth2** 或 **SAML** 与企业身份中心集成，实现单点登录。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑28，项目拥有 986 ★、195 Fork，最近一次提交在同一天，说明维护者仍在积极更新。  
- **生态兼容**：基于 PHP，兼容 Nextcloud 主流版本（23+），并已在多个社区和企业实例中部署。  
- **风险点**：虽然功能完整，但具体的部署和升级流程需要参考官方 README 与社区文档，建议先在测试环境进行一次完整的安装‑配置‑升级演练，以评估运维成本。  

综上，nextcloud/news 在安全、可控和与现有 Nextcloud 基础设施的无缝集成方面具备显著优势，适合作为企业内部信息流的生产级解决方案。

## 🧭 Practical evaluation

**Value:** nextcloud/news may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 986 GitHub stars
- 195 forks
- updated 2026-06-28
- primary language: PHP
- 9 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 57/100 |
| stars | 64/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 78/100 |
| recency | 80/100 |
| adoption | 62/100 |
| production | 69/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/nextcloud/news) · [← Back to Misc](./README.md)</sub>
