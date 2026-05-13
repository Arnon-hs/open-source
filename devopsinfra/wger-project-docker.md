# wger-project/docker

[![Stars](https://img.shields.io/github/stars/wger-project/docker?style=flat-square&color=yellow)](https://github.com/wger-project/docker/stargazers) [![Forks](https://img.shields.io/github/forks/wger-project/docker?style=flat-square&color=blue)](https://github.com/wger-project/docker/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-75%2F100-brightgreen?style=flat-square)](#)

> Docker compose stack for wger deployment

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 304 |
| 🍴 **Forks** | 130 |
| 💻 **Language** | Python |
| 📈 **Score** | 75/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`django` `docker` `docker-compose` `fitness` `hacktoberfest` `self-hosted` `self-hosting` `wger` `workout`

## 🎯 Categories

DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
wger-project/docker provides a ready‑to‑use Docker‑Compose stack that bundles all the services required to run the wger fitness‑tracking application. By containerising the database, web server, and auxiliary components, it makes deployments repeatable, automates routine operations, and improves overall platform reliability.  

**Value**  
- **Consistency:** A single `docker-compose.yml` defines the exact versions, network topology, and environment variables, eliminating “it works on my machine” gaps.  
- **Speed:** New instances can be spun up with a single `docker compose up`, reducing setup time from days to minutes.  
- **Reliability:** Containers isolate failures, simplify scaling, and enable straightforward health‑check monitoring, which translates to higher uptime for production workloads.  

**Practical Adoption Path**  
1. **Evaluation:** Clone the repository and run `docker compose up -d` in a sandbox environment; the stack exposes the wger API and web UI out‑of‑the‑box.  
2. **Customization:** Override default settings via `.env` or additional compose files (e.g., to connect to an existing PostgreSQL instance or to add a reverse proxy).  
3. **CI/CD Integration:** Incorporate the compose file into your pipeline (GitHub Actions, GitLab CI, etc.) to automate testing and staging deployments.  
4. **Production Roll‑out:** Deploy the stack to a managed container host (Docker Swarm, Kubernetes via Kompose, or a cloud VM) and enable persistence for the database volume.  

**Production Readiness**  
The project scores 75/100 and shows strong OSS credentials: 304 GitHub stars, 130 forks, recent commits (last updated 2026‑05‑13), and active community engagement across nine topics. The primary language is Python, matching the wger codebase, and the Docker stack is well‑documented, making it suitable for a serious pilot. While no critical metadata risks are evident, a final review of the license, security scan results, and maintainer activity is recommended before full production adoption.

### Русский

**wger-project/docker** — это готовый Docker‑Compose стек, позволяющий быстро и воспроизводимо развернуть приложение wger, автоматизировать его обслуживание и повысить надёжность инфраструктуры. Типичный сценарий — стандартизация деплоя в тестовых, staging‑ и продакшн‑окружениях, где требуется единый набор контейнеров (веб‑сервер, база данных, очередь и т.п.) без ручных настроек. Проект демонстрирует высокий уровень готовности к production: активная поддержка (обновления до 2026‑05‑13), 304 звёзд, 130 форков, широкая экосистема Python и наличие всех необходимых API/CLI‑интерфейсов, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
wger-project/docker 是为开源健身管理系统 **wger** 提供的 Docker‑Compose 部署套件，能够一键启动完整的服务栈（Web、数据库、缓存等），让部署和运维过程高度可重复、可自动化。

**价值**  
- **标准化部署**：统一的 Compose 文件消除了手工配置差异，团队成员只需运行 `docker compose up` 即可得到一致的运行环境。  
- **自动化运维**：配合 CI/CD 流水线，可实现镜像构建、环境滚动升级和灾备恢复，显著降低人为错误。  
- **提升平台可靠性**：容器化隔离、健康检查和日志收集等机制，使服务更易监控、故障更快定位，从而提高整体可用性。

**典型接入方式**  
1. **本地开发/测试**：克隆仓库后执行 `docker compose up -d`，即可在本机获得完整的 wger 环境。  
2. **CI/CD 流水线**：在 GitHub Actions、GitLab CI 或 Jenkins 中调用 `docker compose`，实现代码推送即自动部署到预检或生产集群。  
3. **Kubernetes 迁移**：Compose 文件可通过 `kompose` 或手动转换为 Helm Chart，便于在云原生平台上进一步扩展。

**生产可用性**  
- **活跃度**：截至 2026‑05‑13，项目最近一次提交，拥有 304 星、130 Fork，社区活跃。  
- **技术成熟度**：基于 Python 主体服务，使用官方镜像和常见的 PostgreSQL、Redis 等后端，符合业界最佳实践。  
- **风险评估**：暂无重大元数据风险，唯一待确认的是许可证（MIT）合规性、容器镜像的安全扫描结果以及维护者的长期可用性。总体上，项目已具备 **高** 级别的生产候选可行性，适合作为正式业务的 pilot 或全量上线。

## 🧭 Practical evaluation

**Value:** wger-project/docker helps make deployment and operations more repeatable.

**Best use cases**

- standardize deployment
- automate operations
- improve platform reliability

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 304 GitHub stars
- 130 forks
- updated 2026-05-13
- primary language: Python
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 53/100 |
| stars | 53/100 |
| topics | 100/100 |
| outlook | 80/100 |
| quality | 79/100 |
| recency | 100/100 |
| adoption | 53/100 |
| production | 83/100 |
| usefulness | 58/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/wger-project/docker) · [← Back to DevOps & Infra](./README.md)</sub>
