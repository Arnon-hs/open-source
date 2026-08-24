# drupal/drupal

[![Stars](https://img.shields.io/github/stars/drupal/drupal?style=flat-square&color=yellow)](https://github.com/drupal/drupal/stargazers) [![Forks](https://img.shields.io/github/forks/drupal/drupal?style=flat-square&color=blue)](https://github.com/drupal/drupal/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> Verbatim mirror of the git.drupal.org repository for Drupal core. Please see the https://github.com/drupal/drupal#contributing. PRs are not accepted on GitHub.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4.3k |
| 🍴 **Forks** | 2k |
| 💻 **Language** | PHP |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The **drupal/drupal** repository is a verbatim mirror of the official Drupal core codebase from git.drupal.org, kept in sync on GitHub for easy browsing and CI integration. While the mirror is kept up‑to‑date, contributions must be made through the upstream Drupal workflow—pull requests on GitHub are not accepted.

**Value Proposition**  
- **Convenient access**: Developers can clone, explore, and reference the Drupal core code from the familiar GitHub interface, benefiting from GitHub’s search, issue linking, and CI tooling without needing a direct connection to git.drupal.org.  
- **Stable reference point**: The mirror provides a reliable snapshot of the official core for scripts, Docker images, or CI pipelines that require a GitHub URL, while the authoritative development still happens upstream.  

**Practical Adoption Path**  
1. **Clone the mirror** (`git clone https://github.com/drupal/drupal.git`) for local development or CI pipelines.  
2. **Align with the upstream workflow**: For any bug fixes or feature work, follow the contribution guidelines on the upstream Drupal site (https://www.drupal.org/contribute). Create patches locally, then submit them via Drupal’s issue queue; the GitHub mirror will be updated automatically.  
3. **Integrate into tooling**: Point Composer, Dockerfiles, or CI scripts to the GitHub URL if you need a GitHub‑compatible source reference, but keep the upstream repository as the source of truth for version tags and release notes.  

**Production Readiness**  
- **Maturity**: The project has strong community adoption (4.3k stars, 2k forks) and is actively maintained (last update 2026‑07‑02).  
- **Readiness level**: **Medium** – suitable for prototypes, internal tools, or CI pipelines that need a GitHub source, but not for direct contribution or release management.  
- **Considerations before production**:  
  * Verify that your build process can tolerate the extra indirection (mirror → upstream).  
  * Ensure you have a fallback to the official git.drupal.org repo for critical patches or when the mirror lags.  
  * Perform a dependency audit—Drupal core pulls many PHP libraries via Composer, so you’ll still need the standard Composer setup.  

**Bottom Line**  
The drupal/drupal mirror is a handy, production‑viable shortcut for accessing Drupal core via GitHub, provided you treat it as a read‑only reference and follow the official Drupal contribution flow for any changes. With modest integration effort and a quick validation of sync latency, it can be safely used in internal workflows and CI pipelines.

### Русский

drupal/drupal — это официальное публичное зеркало репозитория ядра Drupal (git.drupal.org), предоставляющее готовый к использованию исходный код на PHP. Подходит для прототипов и внутренних workflow, где требуется быстрое подключение к последней версии Drupal без необходимости настраивать собственный git‑сервер; однако из‑за отсутствия подробных инструкций по интеграции и ограниченной автоматической поддержки следует провести ручную проверку совместимости и оценить затраты на настройку перед выводом в продакшн. Готовность к production — средняя: проект стабилен и активно обновляется, но требует дополнительного тестирования и контроля зависимостей.

### 中文

**项目简介**  
drupal/drupal 是 Drupal 核心代码在 GitHub 上的只读镜像，完整同步自 git.drupal.org。它提供了 Drupal 官方源码的便捷获取渠道，但所有贡献（PR）只能在原始仓库提交，GitHub 仅用于浏览和克隆。

**价值**  
- **快速获取**：开发者可以直接使用 `git clone https://github.com/drupal/drupal.git` 获得最新的 Drupal 核心代码，无需额外配置访问 git.drupal.org。  
- **生态兼容**：与 Drupal 官方文档、模块生态保持一致，适合作为 CI/CD、容器镜像或内部脚手架的基础代码库。  
- **社区认可**：拥有 4 274+ 星、1 978+ Fork，活跃度高，适合作为原型或内部项目的起点。

**典型接入方式**  
1. **代码拉取**  
   ```bash
   git clone https://github.com/drupal/drupal.git
   cd drupal
   composer install   # 安装依赖
   ```
2. **CI/CD 集成**  
   - 在 Jenkins、GitHub Actions、GitLab CI 等流水线中使用上述 `git clone` 步骤，随后执行 `composer install`、`drush site:install` 等脚本完成自动化部署。  
   - 由于仓库为只读，所有后续的补丁或自定义代码应放在独立的 fork 或子模块中。  

3. **容器化**  
   - 基于官方的 `php`/`apache` 镜像构建自定义 Dockerfile，复制 `drupal` 目录并运行 `composer install`，即可生成可部署的 Drupal 镜像。  

**生产可用性**  
- **成熟度**：Drupal 核心本身是成熟的企业级 CMS，代码库更新频繁（截至 2026‑07‑02 仍在维护），因此在功能层面具备高可靠性。  
- **风险**：GitHub 镜像仅作只读同步，所有贡献必须在官方仓库完成，这意味着：  
  - 若需要提交补丁或紧急修复，必须在 git.drupal.org 上操作后再同步。  
  - 自动化脚本应避免直接在镜像上提交 PR，以免产生冲突。  
- **适用场景**：  
  - **原型/内部系统**：快速搭建测试环境或内部工具，省去访问 git.drupal.org 的网络配置。  
  - **生产系统**：在经过依赖审计、版本锁定（Composer lock）以及充分的 CI 测试后，可用于正式上线。但仍建议将生产代码托管在自有的私有仓库或通过 Composer 包管理来确保可追溯性。  

**结论**  
drupal/drupal 为需要快速获取 Drupal 核心源码的团队提供了便利的只读入口，适合原型开发和内部工作流。通过标准的 `git clone + Composer` 流程即可接入 CI/CD 或容器化部署；在完成依赖审计和充分测试后，也可用于生产环境，但需注意其只读特性和贡献流程的限制。

## 🧭 Practical evaluation

**Value:** drupal/drupal may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 4274 GitHub stars
- 1978 forks
- updated 2026-07-02
- primary language: PHP

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 82/100 |
| stars | 77/100 |
| topics | 0/100 |
| outlook | 52/100 |
| quality | 60/100 |
| recency | 40/100 |
| adoption | 79/100 |
| production | 53/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/drupal/drupal) · [← Back to Misc](./README.md)</sub>
