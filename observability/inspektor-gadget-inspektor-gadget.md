# inspektor-gadget/inspektor-gadget

[![Stars](https://img.shields.io/github/stars/inspektor-gadget/inspektor-gadget?style=flat-square&color=yellow)](https://github.com/inspektor-gadget/inspektor-gadget/stargazers) [![Forks](https://img.shields.io/github/forks/inspektor-gadget/inspektor-gadget?style=flat-square&color=blue)](https://github.com/inspektor-gadget/inspektor-gadget/network) [![Language](https://img.shields.io/badge/lang-C-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Inspektor Gadget is a set of tools and framework for data collection and system inspection on Kubernetes clusters and Linux hosts using eBPF

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.8k |
| 🍴 **Forks** | 341 |
| 💻 **Language** | C |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bpf` `bpf-programs` `cncf-project` `ebpf` `ebpf-programs` `inspektor-gadget` `kinvolk` `kubernetes` `prometheus-exporter` `prometheus-metrics`

## 🎯 Categories

Observability · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Inspektor Gadget is an open‑source framework that leverages eBPF to collect deep telemetry from Kubernetes clusters and Linux hosts, turning raw kernel‑level data into searchable, analyzable streams. It ships a toolbox of ready‑made probes (e.g., network, security, performance) and a unified API that lets you build custom observability pipelines without writing low‑level eBPF code yourself. With strong community traction (2.8 k stars, active releases) it is ready for pilot deployments in production environments.

**Value**  
- **Rich, low‑overhead visibility**: eBPF probes run in the kernel, delivering high‑resolution metrics and traces with minimal performance impact.  
- **Turnkey analytics**: Built‑in gadgets (trace, top, dump, etc.) convert raw events into structured output that can be ingested by log/metric platforms, dashboards, or automated remediation scripts.  
- **Extensible pipeline**: The framework’s Go/C APIs let you pipe data into Prometheus, Loki, OpenTelemetry, or custom ML pipelines, enabling end‑to‑end observability and security use cases.

**Practical Adoption Path**  
1. **Proof‑of‑Concept**: Clone the repo, run the `gadget` binary on a test node, and follow the README examples (e.g., `kubectl gadget top cpu`). Verify that the collected data matches your monitoring expectations.  
2. **Integration Layer**: Choose an export format (JSON, protobuf, Prometheus metrics) and connect the gadget output to your existing observability stack (Grafana, Thanos, Elastic).  
3. **Pilot Deployment**: Deploy the gadget as a DaemonSet with the official Helm chart, enable only the probes you need, and monitor resource usage.  
4. **Scale & Harden**: Gradually roll out to all nodes, add custom eBPF programs if required, and integrate with CI/CD for automated policy enforcement.

**Production Readiness**  
- **Activity & Community**: Recent commits (as of 2026‑05‑11), >2.8 k stars, 341 forks, and multiple active contributors indicate a healthy project.  
- **Stability**: Core gadgets are battle‑tested in many CNCF and enterprise clusters; the DaemonSet deployment model is production‑grade.  
- **Risk Considerations**: Verify the Apache‑2.0 license compatibility, run a security scan of the container images, and confirm that maintainers are responsive to CVEs. Once those checks are completed, Inspektor Gadget is suitable for a serious pilot and can be promoted to full production use.

### Русский

**Inspektor Gadget** — это набор eBPF‑инструментов и фреймворк для сбора телеметрии и инспекции систем в кластерах Kubernetes и на Linux‑хостах, превращающий сырые данные в легко‑просматриваемые и автоматизируемые потоки. Типичный сценарий — запуск небольшого proof‑of‑concept, подключение к существующей наблюдательной стек‑pipeline (Prometheus, Loki, Grafana) и построение аналитических или отчётных процессов без изменения приложений. Проект считается готовым к production: активные коммиты, более 2800 звёзд, широкое принятие в сообществе и стабильный набор функций, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句）**  
Inspektor Gadget 是一套基于 eBPF 的工具与框架，能够在 Kubernetes 集群和 Linux 主机上进行高效的数据采集与系统检查。它提供丰富的预置 Gadget（如网络、进程、文件、调度等），帮助运维和开发团队实时获取底层运行时信息。  

**价值**  
- 将原始的 eBPF 采集数据直接转化为可搜索、可分析、可自动化的输出，极大简化监控、审计和故障排查的工作流。  
- 支持构建自定义的数据处理管道，提升报表、告警和容量规划的准确性与时效性。  

**典型接入方式**  
1. **快速 POC**：按照项目 README，在目标节点上安装 `gadgetctl`，使用 `kubectl gadget` 或 `gadget` 命令运行单个 Gadget，验证数据采集是否满足需求。  
2. **CI/CD 集成**：将 `gadgetctl` 作为容器镜像或二进制文件加入监控/日志采集的 DaemonSet，配合 Prometheus、Grafana 或 Loki 将输出的指标/日志推送到已有观测平台。  
3. **自定义管道**：利用内置的 JSON/CSV 输出或 eBPF map，将数据流向 Kafka、Fluent Bit、或自研的 ETL 作业，实现端到端的分析与自动化处理。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑11，项目拥有 2 810+ Stars、341 Forks，最近一次提交在当日，表明社区仍在积极维护。  
- **成熟度**：已在多个大型 Kubernetes 环境（如 CNCF、云原生社区）中采用，文档完整，提供 Helm Chart 与 Operator 便于大规模部署。  
- **风险**：暂无重大元数据或许可证风险，但仍建议在正式投产前完成安全审计（检查 eBPF 程序的权限模型）并确认维护者响应速度。  

综合来看，Inspektor Gadget 具备高可用的生产级特性，适合作为监控、审计和故障诊断的底层数据源，在小范围 POC 验证后即可在全量环境中推广使用。

## 🧭 Practical evaluation

**Value:** inspektor-gadget/inspektor-gadget helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2810 GitHub stars
- 341 forks
- updated 2026-05-11
- primary language: C
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 63/100 |
| stars | 73/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 67/100 |
| recency | 20/100 |
| adoption | 71/100 |
| production | 52/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/inspektor-gadget/inspektor-gadget) · [← Back to Observability](./README.md)</sub>
