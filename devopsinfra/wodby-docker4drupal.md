# wodby/docker4drupal

[![Stars](https://img.shields.io/github/stars/wodby/docker4drupal?style=flat-square&color=yellow)](https://github.com/wodby/docker4drupal/stargazers) [![Forks](https://img.shields.io/github/forks/wodby/docker4drupal?style=flat-square&color=blue)](https://github.com/wodby/docker4drupal/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> Docker-based Drupal stack

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.3k |
| 🍴 **Forks** | 531 |
| 💻 **Language** | Shell |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`alpine` `arm64` `docker` `docker-compose` `drupal`

## 🎯 Categories

DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
wodby/docker4drupal is an open‑source, Docker‑based stack that bundles Drupal, PHP, Nginx/Apache, MariaDB, Redis, and other common services into ready‑to‑run containers. By providing a single, well‑documented `docker-compose.yml` and a set of helper scripts, it makes Drupal deployments repeatable, portable, and easier to automate. The project is actively maintained (last commit 2026‑07‑02), has strong community adoption (1.2 k ★, 531 forks), and is positioned as a production‑ready foundation for both small sites and large, multi‑environment Drupal farms.

**Value**  
- **Repeatable deployments:** All services are defined as code, eliminating “works on my machine” issues and enabling true infrastructure‑as‑code for Drupal.  
- **Standardized operations:** Common tasks (install, rebuild, cache clear, DB dump) are exposed via the wodby CLI, reducing manual error and speeding up onboarding.  
- **Improved reliability:** Container isolation and built‑in health checks make it easier to monitor and recover services, increasing platform uptime.

**Practical Adoption Path**  
1. **Evaluation:** Clone the repo, run `docker compose up -d` on a dev machine, and verify that the sample site boots.  
2. **Customization:** Replace the example codebase with your own Drupal project, adjust environment variables (e.g., DB credentials, PHP version) in the `.env` file, and add/remove services via the provided compose overrides.  
3. **CI/CD integration:** Incorporate the `docker-compose` commands into your pipeline (e.g., GitHub Actions, GitLab CI) to build images, run tests, and deploy to staging/production environments.  
4. **Scaling:** For production, transition from the default Docker Compose to Docker Swarm or Kubernetes using the same images; wodby already publishes official images on Docker Hub, simplifying the move.

**Production Readiness**  
- **Active maintenance:** Recent commits, a healthy issue/PR turnover, and a vibrant community indicate ongoing support.  
- **Ecosystem fit:** The stack uses widely‑adopted base images and follows best‑practice configurations, making it compatible with most hosting providers and orchestration platforms.  
- **Risk considerations:** While no major licensing or security red flags appear, a final review of the Dockerfile base images and a routine vulnerability scan are recommended before full production rollout.  

Overall, wodby/docker4drupal offers a mature, low‑friction foundation for Drupal teams seeking to modernize their deployment workflow and achieve reliable, repeatable operations at scale.

### Русский

**wodby/docker4drupal** — это готовый Docker‑стек для Drupal, позволяющий стандартизировать процесс развертывания и автоматизировать операции, что повышает надёжность платформы и упрощает её поддержку. Типичный сценарий — создание единой инфраструктуры для разработки, тестирования и продакшн‑окружений, где контейнеры собираются из готовых образов и управляются через Docker‑Compose/CLI. Проект имеет высокий уровень готовности к production: активные коммиты, более 1200 звёзд на GitHub, широкое принятие в сообществе и стабильную экосистему, однако перед окончательным внедрением рекомендуется проверить лицензию и текущий статус безопасности.

### 中文

**项目简介**  
wodby/docker4drupal 是一个基于 Docker 的 Drupal 全栈解决方案，提供预配置好的容器镜像（Nginx、PHP‑FPM、MariaDB、Redis、Solr 等），帮助团队在本地、CI/CD 或生产环境中快速搭建、复制和管理 Drupal 网站。

**价值**  
- **部署可重复**：所有服务都通过 Docker‑Compose 统一声明，环境一致性高，避免“在我机器上可以跑”的问题。  
- **运维自动化**：内置常用工具（Drush、Drupal Console、Xdebug、Mailhog 等），配合脚本即可完成数据库迁移、缓存刷新、代码同步等日常操作。  
- **平台可靠性**：容器隔离、可水平扩展，配合健康检查和日志收集，提升站点的可用性与故障定位效率。

**典型接入方式**  
1. **克隆仓库**或直接在项目根目录创建 `docker-compose.yml`，引用官方镜像（`wodby/drupal-nginx`, `wodby/php`, `wodby/mariadb` 等）。  
2. 通过 `docker compose up -d` 启动完整环境；使用 `docker compose exec php drush …`、`docker compose exec php drupal …` 等 CLI 与 Drupal 交互。  
3. 在 CI/CD（GitHub Actions、GitLab CI、Jenkins 等）中复用同一套 Compose 配置，实现自动化构建、测试与部署。  

**生产可用性**  
- **活跃度**：截至 2026‑07‑02，项目拥有 1,263 ⭐、531 🍴，最近一次提交在同一天，说明维护活跃。  
- **成熟度**：提供完整的生产级组件（HTTPS、日志、备份、监控），并在多个公开案例中用于线上站点。  
- **风险**：暂无重大许可证或安全漏洞报告，但仍建议在正式投产前完成一次安全审计并确认维护者的响应时效。  

综合来看，wodby/docker4drupal 已具备高可用的生产就绪度，适合作为标准化 Drupal 部署的首选 OSS 方案。

## 🧭 Practical evaluation

**Value:** wodby/docker4drupal helps make deployment and operations more repeatable.

**Best use cases**

- standardize deployment
- automate operations
- improve platform reliability

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1263 GitHub stars
- 531 forks
- updated 2026-07-02
- primary language: Shell
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 68/100 |
| stars | 66/100 |
| topics | 63/100 |
| outlook | 69/100 |
| quality | 74/100 |
| recency | 80/100 |
| adoption | 67/100 |
| production | 72/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/wodby/docker4drupal) · [← Back to DevOps & Infra](./README.md)</sub>
