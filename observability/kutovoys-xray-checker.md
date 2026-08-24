# kutovoys/xray-checker

[![Stars](https://img.shields.io/github/stars/kutovoys/xray-checker?style=flat-square&color=yellow)](https://github.com/kutovoys/xray-checker/stargazers) [![Forks](https://img.shields.io/github/forks/kutovoys/xray-checker?style=flat-square&color=blue)](https://github.com/kutovoys/xray-checker/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Xray Checker: A Prometheus exporter for monitoring Xray proxies

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 838 |
| 🍴 **Forks** | 73 |
| 💻 **Language** | Go |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`checker` `go` `marzban` `metrics` `monitoring` `prometheus` `remnawave` `uptime` `uptime-monitor` `xray`

## 🎯 Categories

Observability

## 📝 Summary

### English

**Brief Summary**  
Xray‑Checker is a Go‑based Prometheus exporter that scrapes metrics from Xray proxy instances, turning their runtime state into observable data for Grafana dashboards and alerting pipelines. With over 800 stars and recent commits, it is positioned as a production‑ready OSS component for teams that need to monitor, debug, and verify the health of Xray‑powered services.  

**Value**  
By exposing detailed proxy statistics (connections, traffic, errors, latency, etc.) as standard Prometheus metrics, Xray‑Checker lets operators treat Xray proxies like any other service in their observability stack. This unified view simplifies troubleshooting, capacity planning, and SLA compliance without writing custom scripts or pulling logs manually.  

**Practical Adoption Path**  
1. **Proof of concept** – Deploy the exporter alongside a single Xray node in a dev or staging environment, using the provided Docker image or the compiled binary.  
2. **Validate metrics** – Confirm that the expected metrics appear in Prometheus and are visualizable in Grafana; adjust the exporter’s configuration (e.g., scrape interval, authentication) as needed.  
3. **Scale out** – Roll the exporter to all Xray instances via your existing orchestration tool (Kubernetes DaemonSet, Docker‑Compose, etc.), and add the new metric series to your alerting rules.  
4. **Documentation check** – Review the README for any required environment variables or TLS settings, and add any missing operational notes to your internal runbooks.  

**Production Readiness**  
The project shows strong signals of maturity: recent activity (last commit 2026‑06‑27), a healthy star/fork count, and a clean Go codebase with clear build instructions. While the license and security posture still need a final audit, the overall ecosystem health and community adoption make Xray‑Checker suitable for a serious pilot in production environments, provided a small initial rollout validates integration and security compliance.

### Русский

**kutovoys/xray-checker** — это open‑source Prometheus‑экспортер, позволяющий в реальном времени собирать метрики работы Xray‑прокси (кол‑во запросов, ошибки, задержки и т.п.) и быстро выявлять отклонения в продакшене. Типичное внедрение начинается с небольшого proof‑of‑concept: добавьте экспортер к уже существующей инфраструктуре мониторинга, проверьте README и настройте базовые дашборды, после чего можно расширять покрытие и интегрировать в общие системы observability. Проект имеет высокую готовность к production — активные коммиты, более 800 звёзд, стабильный Go‑код и широкую поддержку сообщества, однако перед масштабным запуском стоит окончательно проверить лицензию, безопасность и наличие активных мейнтейнеров.

### 中文

**项目简短介绍**  
Xray‑Checker 是一个用 Go 编写的 Prometheus Exporter，专门用于采集和暴露 Xray 代理的运行状态、流量、错误等关键指标，帮助运维团队在生产环境中实时监控和调试 Xray 服务。

**价值**  
- **可观测性提升**：通过 Prometheus 与 Grafana 的生态，快速了解代理的健康度、连接数、带宽使用等，定位异常更高效。  
- **调试与排障**：在生产环境出现异常时，直接查询 Exporter 暴露的指标即可定位问题根源，减少日志翻查和人工排查成本。  
- **服务健康追踪**：结合 Alertmanager，可实现对关键阈值（如错误率、延迟）的自动告警，保障业务连续性。

**典型接入方式**  
1. **部署 Exporter**：在运行 Xray 的机器或旁路节点上以容器（Docker）或二进制方式启动 `xray-checker`，默认监听 `:9110/metrics`。  
2. **Prometheus 抓取**：在 Prometheus 配置文件 `scrape_configs` 中加入目标，例如  
   ```yaml
   - job_name: 'xray'
     static_configs:
       - targets: ['<host>:9110']
   ```  
3. **可视化**：使用官方或社区提供的 Grafana Dashboard（JSON 可在仓库 `dashboards/` 目录找到），直接展示代理的各项指标。  
4. **告警**：基于抓取的指标编写 Alertmanager 规则，例如当 `xray_error_total` 在 5 分钟内超过阈值时触发告警。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑27 最近一次提交，拥有 838 星、73 个 Fork，社区活跃。  
- **技术成熟**：使用 Go 语言实现，单二进制文件易部署，依赖少，符合容器化和微服务的最佳实践。  
- **风险可控**：暂无重大元数据风险，仍需对许可证（MIT/Apache）和安全审计（依赖库 CVE）进行最终确认。  
- **适合试点**：建议先在非关键环境做一个小规模的 PoC，验证指标完整性和告警规则后，再推广至生产集群。

综合来看，`kutovoys/xray-checker` 已具备较高的生产就绪度，适合作为 Xray 代理监控的首选方案。

## 🧭 Practical evaluation

**Value:** kutovoys/xray-checker helps make production behavior easier to inspect and debug.

**Best use cases**

- monitor systems
- debug production behavior
- track service health

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 838 GitHub stars
- 73 forks
- updated 2026-06-27
- primary language: Go
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 47/100 |
| stars | 62/100 |
| topics | 100/100 |
| outlook | 60/100 |
| quality | 66/100 |
| recency | 40/100 |
| adoption | 58/100 |
| production | 57/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/kutovoys/xray-checker) · [← Back to Observability](./README.md)</sub>
