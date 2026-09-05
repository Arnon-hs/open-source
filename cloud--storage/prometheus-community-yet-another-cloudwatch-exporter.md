# prometheus-community/yet-another-cloudwatch-exporter

[![Stars](https://img.shields.io/github/stars/prometheus-community/yet-another-cloudwatch-exporter?style=flat-square&color=yellow)](https://github.com/prometheus-community/yet-another-cloudwatch-exporter/stargazers) [![Forks](https://img.shields.io/github/forks/prometheus-community/yet-another-cloudwatch-exporter?style=flat-square&color=blue)](https://github.com/prometheus-community/yet-another-cloudwatch-exporter/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Prometheus exporter for AWS CloudWatch - Discovers services through AWS tags, gets CloudWatch metrics data and provides them as Prometheus metrics with AWS tags as labels

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.2k |
| 🍴 **Forks** | 405 |
| 💻 **Language** | Go |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cloudwatch` `cloudwatch-metrics` `prometheus` `prometheus-exporter`

## 🎯 Categories

Cloud & Storage · Observability

## 📝 Summary

### English

Here's a brief summary of the project and its value proposition:

The prometheus-community/yet-another-cloudwatch-exporter is an open-source project that helps convert raw AWS CloudWatch metrics data into searchable, analyzable, or automated pipelines, enabling users to organize analytics pipelines, process datasets, and improve reporting workflows. This project offers a practical adoption path, starting with a small proof of concept and README check, to ensure seamless integration. Its high production readiness, recent activity, and strong adoption signals make it a serious candidate for a pilot deployment, with over 1,212 GitHub stars and 405 forks.

In terms of value, this project provides a solution for users to leverage their AWS CloudWatch data in a more structured and actionable way, ultimately improving their observability and decision-making capabilities. The practical adoption path involves:

1. **Small proof of concept**: Evaluate the project's feasibility by running a small-scale test to ensure it meets the user's requirements.
2. **README check**: Review the project's documentation to understand its configuration, usage, and potential pitfalls.
3. **Integration**: Gradually integrate the project into the user's existing infrastructure, starting with a small subset of metrics or data.

The production readiness of this project is high due to its:

1. **Recent

### Русский

Резюме:

Prometheus-community/yet-another-cloudwatch-exporter - это открытый проект, который позволяет конвертировать raw данные из AWS CloudWatch в поисковую, анализируемую или автоматизированную базу данных. Этот проект особенно полезен для организации аналитических потоков, обработки данных и улучшения отчетных процессов. Проект имеет высокий уровень готовности к производству, с сильными сигналами активности, приема и экосистемы, что делает его подходящим кандидатом для серьезного пилота.

### 中文

**项目简介**  
`prometheus-community/yet-another-cloudwatch-exporter` 是一款用 Go 编写的 Prometheus Exporter，能够通过 AWS Tag 自动发现云资源，抓取 CloudWatch 指标并以 Prometheus 格式暴露，同时把 AWS Tag 作为标签附加到指标上，方便在 Prometheus/Grafana 中进行统一监控和分析。

**价值**  
- **统一可观测性**：把原本只能在 CloudWatch 中查看的原始指标转化为 Prometheus 可查询、可告警的时间序列，打通 AWS 与自建监控体系。  
- **标签驱动的聚合**：利用 AWS Tag 直接作为 Prometheus 标签，实现跨服务、跨环境的灵活聚合与筛选，降低在 Grafana 中手工拼装查询的成本。  
- **自动发现**：无需手动列举资源，Exporter 会根据 Tag 动态发现 EC2、RDS、Lambda 等服务，适配弹性伸缩的云环境。

**典型接入方式**  
1. **部署**：在 Kubernetes（DaemonSet / Deployment）或作为独立的二进制/Docker 镜像运行。官方提供 Helm chart，可直接通过 `helm install` 完成部署。  
2. **配置**：在 `config.yaml` 中指定要抓取的 AWS 区域、Tag 过滤规则以及需要的 CloudWatch 命名空间/指标列表；也可以通过环境变量提供 AWS 凭证（IAM Role、AccessKey/SecretKey）。  
3. **Prometheus 抓取**：在 Prometheus 配置中加入对应的 `scrape_config`，指向 Exporter 的 `/metrics` 端点。示例：

   ```yaml
   scrape_configs:
     - job_name: 'aws-cloudwatch'
       static_configs:
         - targets: ['yet-another-cloudwatch-exporter:9106']
   ```

4. **验证**：访问 `http://<exporter-host>:9106/metrics`，确认指标已带有 `aws_tag_*` 标签；随后在 Grafana 中创建基于这些标签的仪表盘或告警规则。

**生产可用性**  
- **活跃度**：截至 2026‑07‑05，项目最近一次提交，星标 1.2k，Fork 405，持续接受 PR 与 Issue，表明社区活跃。  
- **成熟度**：使用 Go 编写，单二进制部署，依赖少；已在多个企业的生产环境中验证（社区 issue 中可见真实案例）。  
- **风险**：暂无重大安全或许可证争议，但仍建议在正式上线前完成：  
  - 审核使用的 AWS 权限（最小化 IAM Role）。  
  - 通过内部安全扫描检查二进制镜像。  
  - 在预生产环境做一次完整的 POC，验证 Tag 过滤、指标延迟和资源发现是否符合业务需求。  

综合来看，该 Exporter 已具备 **高** 的生产就绪度，适合作为 Prometheus 监控体系中接入 AWS CloudWatch 的首选桥梁。

## 🧭 Practical evaluation

**Value:** prometheus-community/yet-another-cloudwatch-exporter helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1212 GitHub stars
- 405 forks
- updated 2026-07-05
- primary language: Go
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 65/100 |
| stars | 66/100 |
| topics | 50/100 |
| outlook | 68/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 66/100 |
| production | 69/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/prometheus-community/yet-another-cloudwatch-exporter) · [← Back to Cloud--storage](./README.md)</sub>
