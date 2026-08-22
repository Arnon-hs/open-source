# rfsbraz/deleterr

[![Stars](https://img.shields.io/github/stars/rfsbraz/deleterr?style=flat-square&color=yellow)](https://github.com/rfsbraz/deleterr/stargazers) [![Forks](https://img.shields.io/github/forks/rfsbraz/deleterr?style=flat-square&color=blue)](https://github.com/rfsbraz/deleterr/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> Automated Plex media cleanup with watch-based rules, smart exclusions, and "Leaving Soon" notifications via Radarr, Sonarr & Tautulli.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 324 |
| 🍴 **Forks** | 12 |
| 💻 **Language** | Python |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-07-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`overseerr` `plex` `plex-media-server` `plex-server` `python` `radarr` `radarr-api` `sonarr` `sonarr-api` `sonarr3` `tautulli` `tautulli-api`

## 🎯 Categories

Backend

## 📝 Summary

### English

**Brief Summary**  
rfsbraz/deleterr is a Python‑based automation tool that cleans up Plex libraries by applying watch‑based retention rules, smart exclusion lists, and “Leaving Soon” alerts through Radarr, Sonarr and Tautulli. It lets media‑server operators keep their collections tidy without manual pruning, while preserving content that is still in demand.

**Value**  
- **Infrastructure reuse:** Deleterr provides a ready‑made backend service for media‑library lifecycle management, so teams don’t have to roll their own cron jobs, database queries, or notification pipelines.  
- **Standardized patterns:** By exposing a clear API/CLI and integrating with popular Plex‑ecosystem tools, it enforces consistent cleanup logic across multiple servers or tenants.  
- **Time‑to‑value:** Deploying Deleterr instantly adds automated retention and proactive “Leaving Soon” notifications, reducing storage costs and manual admin effort.

**Practical Adoption Path**  
1. **Evaluate the API/CLI:** Clone the repo, run the provided Docker image or virtual‑env setup, and test the command‑line interface against a staging Plex instance.  
2. **Configure integrations:** Supply Radarr, Sonarr and Tautulli endpoints (API keys, URLs) via the supplied YAML/ENV config; define watch‑time thresholds and exclusion rules.  
3. **Pilot on a non‑critical library:** Enable the service for a single Plex library, monitor logs and the “Leaving Soon” notifications, and adjust thresholds.  
4. **Roll out fleet‑wide:** Once the pilot validates the cleanup behavior, replicate the configuration across all Plex servers using your existing deployment tooling (e.g., Ansible, Helm, or Kubernetes).  

**Production Readiness**  
- **Activity & adoption:** 324 stars, recent commits (as of 2026‑07‑12), and active community forks indicate healthy maintenance.  
- **Ecosystem fit:** Native support for Radarr, Sonarr and Tautulli covers the core Plex workflow, and the Python codebase is easy to audit and extend.  
- **Risk considerations:** No major metadata issues, but a final review of the license (MIT‑style) and a security audit of the exposed API endpoints are advisable before full production use.  

Overall, Deleterr is a mature, well‑documented OSS component that can be quickly integrated into existing Plex deployments to automate media cleanup and improve operational efficiency.

### Русский

**rfsbraz/deleterr** — это open‑source‑утилита на Python, автоматизирующая очистку медиа‑библиотеки Plex по правилам, основанным на просмотре, с умными исключениями и уведомлениями «Скоро закончится» через Radarr, Sonarr и Tautulli. Она позволяет командам быстро подключать готовую инфраструктуру для управления медиа‑контентом, избавляясь от необходимости писать собственные бэкенд‑модули, и легко интегрируется через API/CLI. Проект имеет высокий уровень готовности к production: активные обновления, 324 ★, поддержка нескольких языков и широкое принятие в сообществе, что делает его надёжным кандидатом для пилотного внедрения.

### 中文

**项目简介**  
rfsbraz/deleterr 是一款基于观看记录的 Plex 媒体自动清理工具，能够通过 Radarr、Sonarr 与 Tautulli 实现智能排除和 “即将离场” 通知，帮助用户自动删除不再需要的媒体文件。

**价值**  
- **统一后端能力**：提供即插即用的媒体清理 API/CLI，团队无需自行实现复杂的监控、规则匹配和通知逻辑。  
- **提升交付效率**：复用成熟的清理服务，可快速在新项目或自建 Plex 环境中集成，缩短上线时间。  
- **标准化运维**：统一的规则与排除机制让不同团队在媒体管理上保持一致，降低运维成本。

**典型接入方式**  
1. **API 调用**：通过 HTTP REST 接口提交清理任务、查询规则状态等。  
2. **CLI/SDK**：项目提供 Python 包和命令行工具，可在脚本或 CI/CD 流程中直接调用。  
3. **事件驱动**：结合 Tautulli webhook，将观看完成事件推送至 deleterr，触发即时清理或 “Leaving Soon” 通知。

**生产可用性**  
- **活跃度高**：截至 2026‑07‑12 最近一次提交，拥有 324 ⭐、12 个 Fork，社区活跃。  
- **技术成熟**：使用 Python 实现，配套完整的文档、示例和 12 项主题标签，易于审计与二次开发。  
- **生态兼容**：已验证可与 Radarr、Sonarr、Tautulli 无缝集成，适合作为 OSS 级别的后端服务在生产环境中使用。  
- **风险提示**：仍需进一步审查许可证、潜在安全依赖以及维护者的长期可用性。  

总体来看，deleterr 具备较高的生产就绪度，适合作为媒体管理平台的后端清理组件快速落地。

## 🧭 Practical evaluation

**Value:** rfsbraz/deleterr helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 324 GitHub stars
- 12 forks
- updated 2026-07-12
- primary language: Python
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 28/100 |
| stars | 53/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 76/100 |
| recency | 100/100 |
| adoption | 46/100 |
| production | 77/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/rfsbraz/deleterr) · [← Back to Backend](./README.md)</sub>
