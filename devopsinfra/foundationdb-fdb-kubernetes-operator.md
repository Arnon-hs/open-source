# FoundationDB/fdb-kubernetes-operator

[![Stars](https://img.shields.io/github/stars/FoundationDB/fdb-kubernetes-operator?style=flat-square&color=yellow)](https://github.com/FoundationDB/fdb-kubernetes-operator/stargazers) [![Forks](https://img.shields.io/github/forks/FoundationDB/fdb-kubernetes-operator?style=flat-square&color=blue)](https://github.com/FoundationDB/fdb-kubernetes-operator/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> A kubernetes operator for FoundationDB

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 310 |
| 🍴 **Forks** | 117 |
| 💻 **Language** | Go |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

DevOps/Infra

## 📝 Summary

### English

**Project Overview:**

The FoundationDB/fdb-kubernetes-operator is an open-source project that provides a Kubernetes operator for FoundationDB, aiming to standardize deployment and automate operations, thereby improving platform reliability.

**Value Proposition:**

This project offers a repeatable deployment process, reducing manual effort and increasing efficiency. It enables standardization of deployment and automation of operations, ultimately improving platform reliability.

**Practical Adoption Path:**

To adopt this project, follow these steps:

1. **Manual Inspection**: Review the project's integration signals, license, security posture, and active maintainers to ensure they align with your organization's requirements.
2. **Dependency and Maintenance Checks**: Verify the project's dependencies and maintenance requirements to ensure they fit your production environment.
3. **Prototype or Internal Workflow**: Use the project in a controlled environment, such as a prototype or internal workflow, to test its effectiveness and identify potential issues.
4. **Production Deployment**: Once validated, integrate the project into your production environment, following best practices for deployment and monitoring.

**Production Readiness:**

The project is rated as "Medium" in terms of production readiness, indicating that it is useful for prototypes or internal workflows but requires careful evaluation and validation before deployment in a production environment.

### Русский

**FoundationDB/fdb‑kubernetes‑operator** — это оператор Kubernetes, автоматизирующий развертывание и управление кластерами FoundationDB, делая процесс более повторяемым и стандартизированным. Он подходит для сценариев, где требуется автоматизация операций, повышение надёжности платформы и унификация деплоймента (например, в тестовых средах, прототипах или внутренних CI/CD‑конвейерах). Готовность к production — средняя: проект имеет активную поддержку (310 ★, 117 forks, последний коммит 2026‑07‑01), но перед внедрением в продакшн рекомендуется провести дополнительный аудит лицензии, безопасности и обеспечить наличие ответственного мейнтейнера.

### 中文

**项目简介**  
FoundationDB/fdb‑kubernetes‑operator 是一款用 Go 编写的 Kubernetes Operator，专门用于在 K8s 集群上部署、升级和管理 FoundationDB 集群。它把手动的安装、配置、扩容、备份等工作封装为声明式的 CRD，使得数据库的生命周期管理更加可重复、可自动化。

**价值**  
- **标准化部署**：通过自定义资源（CR）统一描述集群拓扑，避免了不同团队或环境之间的配置漂移。  
- **自动化运维**：Operator 能感知 Pod、PVC、Service 等状态变化，自动完成节点扩容、故障恢复、滚动升级等任务，显著降低运维成本。  
- **提升平台可靠性**：内置的健康检查、备份/恢复流程以及对 FoundationDB 事务日志的管理，帮助构建更稳健的生产数据库服务。

**典型接入方式**  
1. **准备环境**：在目标 Kubernetes 集群中安装 `cert-manager`（用于 Operator 的 webhook）和 `kubectl`。  
2. **部署 Operator**：使用官方提供的 Helm chart 或直接 `kubectl apply -f https://github.com/FoundationDB/fdb-kubernetes-operator/releases/latest/download/fdb-operator.yaml`。  
3. **创建集群声明**：编写 `FoundationDBCluster` CR，定义副本数、存储类、网络策略等，然后 `kubectl apply -f my-fdb.yaml`。Operator 会根据声明自动创建 StatefulSet、Service、PodDisruptionBudget 等资源。  
4. **运维集成**：可通过 Prometheus Exporter 暴露监控指标，结合 GitOps（ArgoCD、Flux）实现声明式的持续交付。

**生产可用性**  
- **成熟度**：GitHub 目前拥有约 310 ★、117 Fork，最近一次提交在 2026‑07‑01，活跃度尚可，适合作为内部或原型环境的基础设施。  
- **就绪度**：属于 **Medium** 级别。对生产使用建议在正式上线前完成：  
  - 完整的备份/恢复演练；  
  - 与现有 CI/CD、监控、RBAC 流程的兼容性验证；  
  - 对 Operator 的升级路径和依赖（如 cert‑manager、Kubernetes 版本）进行评估。  
- **风险**：当前元数据中缺少详细的安全与许可证审计信息，需进一步确认开源许可证兼容性以及是否有已知的 CVE。  

总体而言，fdb‑kubernetes‑operator 能显著简化 FoundationDB 在云原生环境中的部署与运维，适合作为内部平台的标准化数据库交付层，在完成必要的安全与运维审查后即可投入生产使用。

## 🧭 Practical evaluation

**Value:** FoundationDB/fdb-kubernetes-operator helps make deployment and operations more repeatable.

**Best use cases**

- standardize deployment
- automate operations
- improve platform reliability

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 310 GitHub stars
- 117 forks
- updated 2026-07-01
- primary language: Go

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 52/100 |
| stars | 53/100 |
| topics | 0/100 |
| outlook | 46/100 |
| quality | 49/100 |
| recency | 40/100 |
| adoption | 53/100 |
| production | 53/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/FoundationDB/fdb-kubernetes-operator) · [← Back to DevOps & Infra](./README.md)</sub>
