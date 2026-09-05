# prometheus/mysqld_exporter

[![Stars](https://img.shields.io/github/stars/prometheus/mysqld_exporter?style=flat-square&color=yellow)](https://github.com/prometheus/mysqld_exporter/stargazers) [![Forks](https://img.shields.io/github/forks/prometheus/mysqld_exporter?style=flat-square&color=blue)](https://github.com/prometheus/mysqld_exporter/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Exporter for MySQL server metrics

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.5k |
| 🍴 **Forks** | 815 |
| 💻 **Language** | Go |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Database · Observability

## 📝 Summary

### English

**Brief Summary**  
Prometheus mysqld_exporter is an open‑source Go exporter that scrapes MySQL server metrics and exposes them to Prometheus for observability. With a solid community footprint (≈2.5 k stars, 800 forks) it lets teams reuse a proven monitoring component instead of building their own, accelerating API‑service delivery and standardising backend patterns.

**Value**  
- **Reusable infrastructure** – Provides a ready‑made, battle‑tested collector for MySQL, eliminating duplicate effort across services.  
- **Observability‑first** – Exposes a rich set of performance and health counters (connections, replication, InnoDB, etc.) that integrate directly with existing Prometheus dashboards and alerting rules.  
- **Speed to market** – By plugging in a common exporter, teams can focus on business logic rather than low‑level metric collection, shortening the path from prototype to production.

**Practical Adoption Path**  
1. **Prototype** – Deploy the official Docker image or binary alongside the MySQL instance; configure the exporter via environment variables or a simple `mysqld_exporter.cnf`.  
2. **Validate** – Verify the scraped metrics in Prometheus, adjust the whitelist/blacklist of collectors to match your schema, and confirm that the exported data satisfies your monitoring requirements.  
3. **Integrate** – Add the exporter target to your Prometheus scrape config, version‑pin the exporter image, and incorporate the default dashboards (e.g., Grafana MySQL dashboard).  
4. **Security & Ops review** – Perform a license check, run a vulnerability scan on the binary/container, and confirm that the MySQL user used by the exporter has the minimal required privileges.  

**Production Readiness**  
- **Maturity**: Medium – the exporter is widely used and actively maintained (last update 2026‑07‑12), but its integration signals are sparse, so a manual sanity check is required before critical deployments.  
- **Dependencies**: Minimal (Go runtime, standard MySQL client libraries); ensure compatibility with your MySQL version and any custom plugins.  
- **Operational considerations**: Monitor the exporter’s own health endpoint, set up alerts for scrape failures, and plan for periodic upgrades to keep up with security patches.  

Overall, mysqld_exporter is a production‑grade component for internal services and prototypes, provided you perform the standard security and compatibility vetting steps before rolling it out at scale.

### Русский

**prometheus/mysqld_exporter** — это open‑source‑экспортер, собирающий метрики MySQL‑серверов и отдающий их в Prometheus, что позволяет быстро добавить мониторинг баз данных без написания собственного кода. Он идеально подходит для команд, которые хотят ускорить запуск API‑сервисов, стандартизировать инфраструктуру наблюдаемости и переиспользовать готовый бекенд‑компонент, однако перед внедрением требуется ручная проверка совместимости, так как обнаруживаемые сигналы интеграции ограничены. Готовность к production — средняя: проект стабилен и популярен (≈2,5 к звёзд, 800 форков, активные обновления), но перед выводом в продакшн стоит убедиться в актуальности лицензии, безопасности и наличии активных мейнтейнеров.

### 中文

**简短介绍**  
prometheus/mysqld_exporter 是一个用 Go 编写的 Prometheus Exporter，专门采集 MySQL 服务器的运行时指标并暴露为 Prometheus 可抓取的格式。它帮助团队复用成熟的监控组件，避免自行实现 MySQL 指标采集逻辑，从而更快地交付业务服务。

**价值**  
- **复用基础设施**：提供开箱即用的 MySQL 监控实现，团队无需重复开发相同的采集代码。  
- **统一监控标准**：通过 Prometheus 统一收集、存储、告警，便于在多服务环境中保持监控一致性。  
- **加速业务交付**：在新项目或原有系统中快速接入 MySQL 监控，缩短上线时间。

**典型接入方式**  
1. **部署 Exporter**：在 MySQL 所在机器或网络可达的独立主机上运行 `mysqld_exporter`（Docker 镜像或二进制文件均可）。  
2. **配置 MySQL 账户**：在 MySQL 中创建专用的监控用户，授予 `PROCESS`, `REPLICATION CLIENT`, `SELECT` 等最小权限。  
3. **Prometheus 抓取**：在 Prometheus 配置文件 `scrape_configs` 中添加目标，例如  
   ```yaml
   - job_name: 'mysqld'
     static_configs:
       - targets: ['<exporter-host>:9104']
   ```  
4. **可选自定义**：通过环境变量或命令行参数开启/关闭特定的 metric 集（如 InnoDB、性能模式等），或使用 `--collect.auto_increment.columns` 等细粒度开关。  

**生产可用性**  
- **成熟度**：GitHub 近 2500 星、800+ Fork，活跃维护，最近一次提交在 2026‑07‑12，代码基于 Go，社区成熟度中等。  
- **适用场景**：适合原型、内部业务或对监控要求不极端的生产环境；在正式生产前建议进行依赖审计（如 MySQL 版本兼容性、网络连通性）和安全评估（审查监控用户权限、Exporter 的容器安全配置）。  
- **风险**：当前元数据较少，集成前需要手动检查指标覆盖情况；需确认许可证（Apache‑2.0）符合企业合规，并评估维护者活跃度是否满足长期支持需求。  

总体而言，mysqld_exporter 是一款 **“可直接使用、快速集成”** 的 MySQL 监控解决方案，具备中等的生产就绪度，只要做好前置审查和运维监控，即可在多数业务环境中安全投入使用。

## 🧭 Practical evaluation

**Value:** prometheus/mysqld_exporter helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 2451 GitHub stars
- 815 forks
- updated 2026-07-12
- primary language: Go

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 73/100 |
| stars | 72/100 |
| topics | 0/100 |
| outlook | 64/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 72/100 |
| production | 67/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/prometheus/mysqld_exporter) · [← Back to Database](./README.md)</sub>
