# wikimedia/mediawiki

[![Stars](https://img.shields.io/github/stars/wikimedia/mediawiki?style=flat-square&color=yellow)](https://github.com/wikimedia/mediawiki/stargazers) [![Forks](https://img.shields.io/github/forks/wikimedia/mediawiki?style=flat-square&color=blue)](https://github.com/wikimedia/mediawiki/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> 🌻 The collaborative editing software that runs Wikipedia. Mirror from https://gerrit.wikimedia.org/g/mediawiki/core. See https://mediawiki.org/wiki/Developer_access for contributing.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 5.1k |
| 🍴 **Forks** | 1.5k |
| 💻 **Language** | PHP |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`mediawiki` `php` `wiki` `wikipedia`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
Wikimedia MediaWiki is the open‑source PHP platform that powers Wikipedia and thousands of other wikis. It offers a mature, actively maintained codebase (5090 ⭐, 1545 forks, recent commits) that can be leveraged to accelerate development, automate routine engineering tasks, and tighten CI feedback loops.

**Value**  
MediaWiki’s extensive API, robust extension framework, and proven scalability let engineering teams streamline daily development and review cycles—e.g., generating test data, scripting bulk edits, or integrating custom validation steps directly into CI pipelines. By reusing a battle‑tested foundation, teams avoid building a wiki engine from scratch and can focus on domain‑specific features.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repository, run the Docker‑based development environment, and verify the README instructions.  
2. **Small integration** – Add a simple custom extension or script that automates a recurring task (e.g., linting page content or pre‑populating test pages).  
3. **CI extension** – Hook the extension into your CI pipeline to provide immediate feedback on wiki‑related changes.  
4. **Scale up** – Gradually replace ad‑hoc scripts with deeper MediaWiki customizations, leveraging the extensive developer documentation and community support.

**Production readiness**  
MediaWiki is highly production‑ready: it has continuous activity, a large install base, and a vibrant ecosystem of extensions and documentation. The main risk lies in the initial setup—configuration details are scattered across Gerrit and the developer portal—so a modest investment in a pilot environment is advisable before committing to a full rollout. Once the proof‑of‑concept validates the integration cost, MediaWiki can be deployed at scale with confidence.

### Русский

Wikimedia MediaWiki — это открытая платформа для совместного редактирования, на которой работает Wikipedia; её активное сообщество и регулярные обновления (5090 звёзд, 1545 форков, последние коммиты 2026‑06‑23) делают проект готовым к использованию в продакшене. Типичный сценарий внедрения — небольшое proof‑of‑concept, в котором автоматизируются локальные задачи разработчиков и ускоряется CI‑обратная связь, после чего решение масштабируется на весь процесс разработки. Несмотря на сильные сигналы качества, следует уточнить детали интеграции и оценить затраты на настройку перед полномасштабным переходом.

### 中文

**价值**  
wikimedia/mediawiki 是支撑 Wikipedia 等维基站点的核心协作编辑平台，拥有庞大的社区、活跃的维护者以及丰富的插件生态。对内部工程团队而言，它能够：

- **加速开发与审查**：提供成熟的页面渲染、权限管理、扩展框架等功能，避免重复造轮子，显著缩短新功能的实现周期。  
- **提升 CI 效率**：内置的单元测试、代码风格检查以及可通过 CI 自动部署的扩展机制，使得代码提交后的质量反馈快速且可靠。  
- **自动化日常任务**：通过脚本化的维护工具（如 `maintenance/` 目录下的 PHP 脚本）可以批量处理数据迁移、统计、备份等工程任务。

**典型接入方式**  

| 步骤 | 说明 |
|------|------|
| 1️⃣ Clone & 环境搭建 | 使用官方镜像 `git clone https://gerrit.wikimedia.org/g/mediawiki/core.git`，参考 <https://www.mediawiki.org/wiki/Installation> 完成 PHP、MySQL、Composer 等依赖的本地部署。 |
| 2️⃣ 扩展开发 | 在 `extensions/` 目录下创建自定义扩展，遵循 MediaWiki 的钩子（Hook）机制；使用 Composer 管理依赖。 |
| 3️⃣ CI 集成 | 在项目的 CI（GitHub Actions、GitLab CI、Jenkins 等）中加入 `phpunit`、`phpcs`、`phpmd` 等检查，并通过 `maintenance/run.php` 脚本执行数据库迁移或数据导入。 |
| 4️⃣ 小范围 POC | 先在内部测试环境部署一个最小化的 MediaWiki 实例（仅核心功能 + 必要扩展），验证与现有系统的接口（如 SSO、搜索、缓存）是否顺畅。 |
| 5️⃣ 正式上线 | 完成安全审计、性能压测后，将完整实例迁移至生产环境，并开启监控（Prometheus + Grafana）与备份策略。 |

**生产可用性**  

- **活跃度**：最近一次提交（2026‑06‑23）表明项目仍在积极维护；GitHub 上 5 090+ stars、1 545+ forks，社区活跃度高。  
- **成熟度**：MediaWiki 已在全球数十万台服务器上运行，核心代码经过多年实战检验，具备高可用、横向扩展和多语言支持能力。  
- **生态与支持**：官方提供完整的开发者文档、扩展目录以及专门的开发者邮件列表；同时有专职的维基媒体工程团队提供技术支持。  
- **风险**：元数据未直接给出“一键”集成脚本，初始搭建和 CI 集成需要自行编写脚本并验证环境依赖，建议先在小规模环境进行验证后再投入生产。  

综合来看，wikimedia/mediawiki 具备 **高生产就绪度**，适合作为内部协作平台或知识库的核心组件，只要在接入前做好环境准备和小规模 POC，即可在正式环境中稳定运行。

## 🧭 Practical evaluation

**Value:** wikimedia/mediawiki helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 5090 GitHub stars
- 1545 forks
- updated 2026-06-23
- primary language: PHP
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 80/100 |
| stars | 79/100 |
| topics | 50/100 |
| outlook | 57/100 |
| quality | 68/100 |
| recency | 40/100 |
| adoption | 79/100 |
| production | 56/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/wikimedia/mediawiki) · [← Back to Misc](./README.md)</sub>
