# ray-project/kuberay

[![Stars](https://img.shields.io/github/stars/ray-project/kuberay?style=flat-square&color=yellow)](https://github.com/ray-project/kuberay/stargazers) [![Forks](https://img.shields.io/github/forks/ray-project/kuberay?style=flat-square&color=blue)](https://github.com/ray-project/kuberay/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> A toolkit to run Ray applications on Kubernetes

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.6k |
| 🍴 **Forks** | 784 |
| 💻 **Language** | Go |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`apache` `deep-learning` `kubernetes` `machine-learning` `ray`

## 🎯 Categories

AI/ML · DevOps/Infra

## 📝 Summary

### English

**Summary**  
KubeRay (ray-project/kuberay) is an open‑source toolkit that lets you package, deploy, and manage Ray workloads on Kubernetes clusters, turning complex distributed‑compute setups into repeatable, declarative resources. With strong community adoption (2.5 k ★, 784 forks), recent activity, and a Go‑centric codebase, it is ready for a serious pilot in production environments.

**Value** – KubeRay standardizes Ray deployments, automates routine ops (scaling, health‑checks, upgrades) and improves platform reliability by leveraging Kubernetes’ native scheduling, observability, and RBAC mechanisms.

**Adoption path** – Start with a small proof‑of‑concept: follow the README to spin up a minimal KubeRay operator in a test cluster, deploy a simple Ray job, and validate integration with your CI/CD pipeline. Once the workflow is verified, expand to staging and then production, adding custom Helm charts or Kustomize overlays to match your organization’s deployment policies.

**Production readiness** – The project shows high readiness: recent commits (as of 2026‑06‑26), active maintainers, growing ecosystem integrations, and solid usage signals make it a viable OSS candidate for production, pending final license, security, and maintainer reviews.

### Русский

**ray-project/kuberay** — это открытый набор инструментов, позволяющий легко и последовательно развёртывать приложения Ray в кластерах Kubernetes, автоматизируя операции и повышая надёжность платформы. Типичный сценарий внедрения — небольшое proof‑of‑concept, основанное на README, после чего проект масштабируется для стандартизации деплоймента и автоматизации управления рабочими нагрузками. По уровню готовности к production проект считается «high»: активные коммиты, широкое принятие (2562 звёзды, 784 форка), поддержка Go и сильные сигналы экосистемы, хотя окончательная проверка лицензии, безопасности и активности мейнтейнеров всё‑ещё требуется.

### 中文

**项目简介**  
ray-project/kuberay 是一个开源工具包，旨在帮助用户在 Kubernetes 上部署、管理和扩展 Ray 分布式计算应用。它提供了原生的 K8s CRD、Operator 与 Helm Chart，使 Ray 集群的创建、伸缩和监控与 Kubernetes 的生态保持一致。

**价值**  
- **部署可复用**：通过声明式的 CRD 与 Helm Chart，实现一次编写、在多环境中重复使用的部署流程。  
- **运维自动化**：Operator 自动处理 Ray 集群的生命周期（创建、滚动升级、故障恢复），大幅降低人工干预。  
- **平台可靠性提升**：借助 Kubernetes 的调度、弹性伸缩与监控能力，提升 Ray 作业的可用性与资源利用率。

**典型接入方式**  
1. **快速试验**：克隆仓库或直接使用官方 Helm Chart（`helm repo add kuberay https://ray-project.github.io/kuberay-helm/`），在本地或测试集群上部署一个示例 RayCluster。  
2. **POC 验证**：按照 README 中的步骤创建自定义资源（`RayCluster`、`RayJob`），并在 CI/CD 流水线中加入 `kubectl apply -f` 进行自动化部署。  
3. **正式集成**：在已有的 Kubernetes 平台上通过 Helm 或 Kustomize 将 KubeRay Operator 纳入平台的基础设施代码，结合平台的监控（Prometheus/Grafana）与日志（EFK）完成统一治理。

**生产可用性**  
- **活跃度**：截至 2026‑06‑26，项目拥有 2,562 ⭐、784 🍴，最近一次提交在同日，表明社区活跃。  
- **成熟度**：提供完整的 Operator、CRD、Helm Chart 与详细文档，已被多家企业在生产环境中采用，具备高可用部署模式（多副本、故障转移）。  
- **准备度**：在 OSS 候选列表中评分为 **High**，适合作为正式生产 pilot。唯一待确认的事项是许可证合规、漏洞扫描结果以及维护者的长期可用性，建议在正式上线前完成最终审查。  

综上，KubeRay 为在 Kubernetes 上运行 Ray 提供了标准化、自动化的解决方案，接入门槛低，且已具备足够的社区与技术成熟度，可直接用于生产环境的试点与推广。

## 🧭 Practical evaluation

**Value:** ray-project/kuberay helps make deployment and operations more repeatable.

**Best use cases**

- standardize deployment
- automate operations
- improve platform reliability

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2562 GitHub stars
- 784 forks
- updated 2026-06-26
- primary language: Go
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 72/100 |
| stars | 73/100 |
| topics | 63/100 |
| outlook | 74/100 |
| quality | 77/100 |
| recency | 80/100 |
| adoption | 72/100 |
| production | 73/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/ray-project/kuberay) · [← Back to AI/ML](./README.md)</sub>
