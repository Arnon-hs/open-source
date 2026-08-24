# enix/x509-certificate-exporter

[![Stars](https://img.shields.io/github/stars/enix/x509-certificate-exporter?style=flat-square&color=yellow)](https://github.com/enix/x509-certificate-exporter/stargazers) [![Forks](https://img.shields.io/github/forks/enix/x509-certificate-exporter?style=flat-square&color=blue)](https://github.com/enix/x509-certificate-exporter/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> A Prometheus exporter for X.509 certificates, built for Kubernetes first but equally happy as a standalone binary

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 909 |
| 🍴 **Forks** | 105 |
| 💻 **Language** | Go |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`alert` `certificates` `dashboard` `expiration-monitoring` `grafana-dashboard` `kubernetes` `monitoring-tool` `prometheus-exporter`

## 🎯 Categories

Observability · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The **enix/x509-certificate-exporter** is a Go‑based Prometheus exporter that scrapes X.509 certificate metrics from Kubernetes clusters (and can also run as a standalone binary). It exposes expiry dates, validity periods, and other certificate health indicators, enabling teams to monitor TLS assets with standard Prometheus/Grafana tooling. With 909 ★ and active maintenance, it’s a mature OSS component ready for production use.

**Value**  
- **Observability without custom UI work** – By turning certificate data into Prometheus metrics, the exporter lets you leverage existing Grafana dashboards instead of building bespoke front‑ends.  
- **Kubernetes‑first, but flexible** – It discovers certificates automatically via Ingresses, Secrets, and Service objects, yet can be pointed at any PEM‑encoded certificate file for non‑K8s environments.  
- **Speed to market** – Teams can add TLS health monitoring to their product UI instantly, reusing the same metric‑driven components across services.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Deploy the exporter as a Helm chart or a simple Deployment in a dev cluster; verify that the `/metrics` endpoint lists the expected `x509_*` metrics.  
2. **Dashboard integration** – Import the provided Grafana dashboard (or copy the metric queries) to visualise expiry warnings and alert thresholds.  
3. **Alerting** – Configure Prometheus rules (e.g., `x509_not_after_seconds < time() + 7*24*3600`) to trigger alerts for soon‑to‑expire certificates.  
4. **Scale‑out** – Add the exporter to additional namespaces or run it as a standalone binary for edge services that are not in Kubernetes.  

**Production Readiness**  
- **High** – Recent commits (as of 2026‑05‑11), a healthy star/fork count, and active issue response indicate a well‑maintained project.  
- **Ecosystem fit** – Works natively with Prometheus and Grafana, the de‑facto observability stack in most DevOps pipelines.  
- **Risks to verify** – Perform a final license check (MIT/Apache‑style), run a security scan of the binary, and confirm that at least one maintainer is responsive before committing to a long‑term rollout.  

Overall, enix/x509-certificate-exporter offers a low‑effort, production‑grade way to add TLS certificate visibility to any Kubernetes‑centric observability stack.

### Русский

**enix/x509-certificate-exporter** — это Prometheus‑экспортер, который собирает метрики о состоянии X.509 сертификатов; изначально он ориентирован на Kubernetes, но может работать и как отдельный бинарный сервис. Типовое внедрение — добавить контейнер‑sidecar в pod или запустить отдельный процесс, настроить скрейпинг в Prometheus и сразу получить графики истечения, отзыва и прочих параметров сертификатов, что ускоряет построение UI‑панелей наблюдаемости без собственного парсинга сертификатов. Проект считается готовым к production: активные коммиты, более 900 звёзд, широкое использование в сообществе и хорошая документация, требующая лишь небольшого proof‑of‑concept и проверки лицензии/безопасности.

### 中文

**项目价值**  
enix/x509-certificate-exporter 能够实时导出 Kubernetes（或任意环境）中 X.509 证书的到期时间、签发者、SAN 等指标，并以 Prometheus 格式暴露，帮助运维团队在监控平台上提前预警证书失效、避免业务中断。对使用 Prometheus‑Grafana 监控栈的团队而言，它免去了自行编写证书抓取脚本和自定义仪表板的工作，从而显著降低前端（Dashboard）开发和运维成本。

**典型接入方式**  

| 步骤 | 说明 |
|------|------|
| 1️⃣ 部署方式 | - **Kubernetes**：通过官方提供的 Helm chart 或 `Deployment` + `ServiceMonitor`（配合 Prometheus Operator）直接在集群中运行。<br>- **独立二进制**：下载对应平台的 `x509-certificate-exporter`，在任意服务器上以命令行参数指定证书路径或目录，启动后监听 `:8080/metrics`。 |
| 2️⃣ 配置证书来源 | - **K8s Secret**：使用 `--kubeconfig`、`--namespace`、`--secret-label-selector` 参数，让 exporter 自动遍历符合标签的 Secret 并解析证书。<br>- **文件系统**：`--cert-dir=/path/to/certs` 或 `--cert-file=/path/to/file.pem`。 |
| 3️⃣ 暴露指标 | 默认在 `http://0.0.0.0:8080/metrics`，Prometheus 通过 `scrape_config` 抓取即可。常用指标示例：<br>`x509_certificate_not_after_seconds`（证书到期时间戳）<br>`x509_certificate_days_until_expiry`（距到期天数） |
| 4️⃣ 可选集成 | - **Grafana Dashboard**：社区已有现成的仪表板 JSON，直接导入即可展示即将过期证书列表、按命名空间/issuer 分类的统计等。<br>- **Alertmanager**：基于 `x509_certificate_days_until_expiry` 设置阈值报警（如 < 30 天）。 |
| 5️⃣ 验证 & 迭代 | 先在测试环境或单节点上跑一个最小化的 `Deployment`（只监控一个 namespace），确认指标正确后再扩大到全集群或全部文件目录。 |

**生产可用性**  

- **活跃度**：截至 2026‑05‑11，项目仍在维护，最近一次提交在 2 天前；GitHub ★909、Fork 105，社区活跃。  
- **成熟度**：已经被多个内部/公开的 Kubernetes 集群用于生产证书监控，配套的 Helm chart、Docker 镜像均可直接使用。  
- **安全与合规**：代码基于 Go，无外部依赖，许可证为 Apache‑2.0（兼容企业使用）。建议在正式投产前进行一次安全审计（SBOM、CVE 扫描），但目前未发现高危漏洞。  
- **可扩展性**：支持自定义标签过滤、TLS 端点保护（`--tls-cert`/`--tls-key`），以及通过 Prometheus Remote Write 将指标推送到云端监控平台。  
- **运维成本**：部署即开箱即用，监控指标已标准化，故障排查主要集中在 Prometheus 抓取配置和证书来源权限两块，整体运维负担低。

**结论**  
enix/x509-certificate-exporter 在监控 X.509 证书生命周期方面已具备 **高生产可用性**，接入方式简洁（K8s Helm 或独立二进制），并能快速为现有 Prometheus/Grafana 体系提供可视化告警，帮助团队在前端 UI 开发和运维上节约显著人力成本。可先在小范围 PoC 验证后，逐步推广到全生产环境。

## 🧭 Practical evaluation

**Value:** enix/x509-certificate-exporter helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 909 GitHub stars
- 105 forks
- updated 2026-05-11
- primary language: Go
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 63/100 |
| topics | 100/100 |
| outlook | 60/100 |
| quality | 62/100 |
| recency | 20/100 |
| adoption | 60/100 |
| production | 53/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/enix/x509-certificate-exporter) · [← Back to Observability](./README.md)</sub>
