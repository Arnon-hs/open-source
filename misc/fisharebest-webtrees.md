# fisharebest/webtrees

[![Stars](https://img.shields.io/github/stars/fisharebest/webtrees?style=flat-square&color=yellow)](https://github.com/fisharebest/webtrees/stargazers) [![Forks](https://img.shields.io/github/forks/fisharebest/webtrees?style=flat-square&color=blue)](https://github.com/fisharebest/webtrees/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-49%2F100-brightgreen?style=flat-square)](#)

> Online genealogy

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 780 |
| 🍴 **Forks** | 347 |
| 💻 **Language** | PHP |
| 📈 **Score** | 49/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`family-history` `family-tree` `gedcom` `genealogy` `webtrees`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
fisharebest/webtrees is an open‑source PHP application for building and publishing online genealogy trees. With a solid community (≈780 ★, 347 forks) and recent activity, it can serve as a quick way to host collaborative family‑history data, especially when its README aligns with your workflow. It is best suited for prototypes, internal tools, or low‑risk production use after a small proof‑of‑concept implementation.

**Value**  
- Provides a ready‑made, feature‑rich platform for storing, visualising, and sharing genealogical data without building a system from scratch.  
- Extensible via plugins and themes, allowing you to tailor the UI and data model to specific research or organisational needs.  
- Active community and regular updates reduce the effort required for bug fixes and security patches.

**Practical Adoption Path**  
1. **Read the README & Docs** – Confirm that the installation steps (Docker, Composer, or shared‑hosting) match your environment.  
2. **Proof‑of‑Concept** – Deploy a sandbox instance (e.g., using the official Docker image) and import a small GEDCOM sample to verify core features and integration points (authentication, API, data export).  
3. **Integration Tests** – Hook the instance into your existing workflow (e.g., single‑sign‑on, CI pipelines, or custom data pipelines) and evaluate any required customisations.  
4. **Gradual Roll‑out** – Expand the dataset and enable the instance for a limited user group; monitor performance and maintenance overhead.  

**Production Readiness**  
- **Maturity:** Medium – the codebase is mature and actively maintained, but the project is primarily targeted at genealogy use‑cases, not generic CMS workloads.  
- **Stability:** Suitable for internal tools or prototypes; for public‑facing services, perform a thorough security review (PHP version, dependencies, hardening).  
- **Dependencies:** PHP + MySQL/MariaDB; ensure your stack matches the supported versions and that you have a process for applying Composer updates.  
- **Maintenance:** Monitor the upstream repository for security patches; plan periodic upgrades and backup strategies for the underlying database.  

Overall, fisharebest/webtrees can be adopted quickly for low‑risk genealogy or data‑catalogue projects, provided you validate the installation effort and perform a small pilot before committing to production use.

### Русский

**fisharebest/webtrees** — это открытая веб‑программа на PHP для построения и публикации генеалогических деревьев. При наличии подходящего README и активного репозитория её удобно внедрять в виде небольшого прототипа: установить на тестовый сервер, импортировать GEDCOM‑файл и предоставить доступ сотрудникам или членам семьи, после чего оценить требования к зависимостям и обслуживанию. Проект имеет средний уровень готовности к production (780 звёзд, регулярные обновления), но перед масштабным запуском следует проверить сложность интеграции и планировать поддержку.

### 中文

**项目简介**  
fisharebest/webtrees 是一个基于 PHP 的开源在线族谱系统，提供网页化的家谱管理、树形展示、事件搜索和多用户协作等功能，适合个人或小型组织搭建自己的族谱平台。

**价值**  
- **集中管理**：所有族谱数据通过 Web 界面统一存储，支持 GEDCOM 导入/导出，便于数据迁移和备份。  
- **多用户协作**：细粒度的权限控制让家族成员可以自行编辑、添加或审核信息，提升信息的完整性和准确性。  
- **可扩展**：插件机制和丰富的主题支持，使其能够根据特定需求（如地图展示、DNA 关联等）进行二次开发。

**典型接入方式**  
1. **环境准备**：在支持 PHP 7.4+、MySQL/MariaDB 的服务器上部署（可使用 Docker 官方镜像快速搭建）。  
2. **代码获取**：`git clone https://github.com/fisharebest/webtrees.git`，或直接下载发行版。  
3. **配置**：运行安装向导，填写数据库连接、管理员账户等信息；可通过 `.env` 文件或 `config.ini.php` 进行进一步自定义。  
4. **集成**：  
   - **内部系统**：通过 SSO（LDAP、OAuth）对接企业身份库，实现单点登录。  
   - **外部服务**：利用 RESTful API（或自建插件）将族谱数据同步到 CRM、文档管理或移动端 App。  
   - **CI/CD**：将代码放入私有仓库，使用 GitHub Actions 自动构建 Docker 镜像并推送至 Kubernetes / Docker‑Compose 环境。

**生产可用性**  
- **成熟度**：已有 780+ 星、347+ Fork，活跃社区，每月都有代码更新，说明项目在维护中。  
- **适用场景**：适合原型、内部工具或面向特定家族/组织的生产环境；若要支撑大规模并发访问，需要配合负载均衡、缓存（Redis）和数据库分片等措施。  
- **风险与准备**：  
  - **依赖管理**：确保 PHP、数据库及扩展版本与项目兼容，定期审计第三方库的安全性。  
  - **运维成本**：需要监控备份、日志和安全更新；建议在正式上线前完成一次完整的灾备演练。  
  - **集成难度**：官方文档提供基本安装与插件开发指南，但复杂业务（如深度 SSO、跨系统数据同步）仍需自行实现或社区插件支持。  

综上，fisharebest/webtrees 在功能完整性和社区活跃度上具备中等到高的生产可用性，适合作为内部族谱系统或原型项目的基础平台；在大规模或高安全要求的生产环境中，建议先进行小规模 PoC 验证并做好运维准备后再全面推广。

## 🧭 Practical evaluation

**Value:** fisharebest/webtrees may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 780 GitHub stars
- 347 forks
- updated 2026-06-26
- primary language: PHP
- 5 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 64/100 |
| stars | 62/100 |
| topics | 63/100 |
| outlook | 54/100 |
| quality | 62/100 |
| recency | 40/100 |
| adoption | 62/100 |
| production | 53/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/fisharebest/webtrees) · [← Back to Misc](./README.md)</sub>
