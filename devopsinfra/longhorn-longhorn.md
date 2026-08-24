# longhorn/longhorn

[![Stars](https://img.shields.io/github/stars/longhorn/longhorn?style=flat-square&color=yellow)](https://github.com/longhorn/longhorn/stargazers) [![Forks](https://img.shields.io/github/forks/longhorn/longhorn?style=flat-square&color=blue)](https://github.com/longhorn/longhorn/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Cloud-Native distributed storage built on and for Kubernetes

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 7.8k |
| 🍴 **Forks** | 710 |
| 💻 **Language** | Shell |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cncf` `distributed-systems` `high-availability` `k8s-sig-storage` `kubernetes` `longhorn` `storage`

## 🎯 Categories

DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
Longhorn (longhorn/longhorn) is a cloud‑native, distributed block storage system designed specifically for Kubernetes. It provides highly available, fault‑tolerant volumes that can be dynamically provisioned, replicated, and backed up directly from the cluster, making persistent storage as easy to manage as any other Kubernetes resource.  

**Value**  
Longhorn turns raw Kubernetes nodes into a resilient, software‑defined storage layer, eliminating the need for external SAN/NAS solutions and reducing operational overhead. By exposing storage as native Kubernetes objects, it enables developers and operators to automate data lifecycle (creation, snapshot, backup, restore) through familiar CI/CD pipelines and GitOps workflows, thereby accelerating cloud‑native application delivery and improving data reliability.  

**Practical Adoption Path**  

| Phase | Goal | Key Activities |
|-------|------|----------------|
| **Proof‑of‑Concept** | Validate basic functionality on a test cluster | Deploy the official Helm chart or `longhorn` manifest on a small multi‑node cluster; run the built‑in UI to create a volume, attach it to a pod, and test snapshot/backup. |
| **Integration Pilot** | Assess operational fit and performance | Connect Longhorn to existing backup targets (e.g., S3, NFS); configure replication factor; run load tests with representative workloads; document the process in a README for the team. |
| **Production Rollout** | Deploy at scale across production namespaces | Use GitOps (ArgoCD/Flux) to manage Longhorn CRDs; set up monitoring (Prometheus + Grafana) and alerting; define RBAC policies; establish backup retention policies and disaster‑recovery drills. |
| **Continuous Improvement** | Optimize and extend | Tune replica counts, node selectors, and storage class parameters; integrate with CSI drivers for other platforms if needed; contribute back any custom patches. |

**Production Readiness**  
Longhorn scores high on readiness: it has >7,800 stars, 710 forks, frequent commits (last update 2026‑06‑23), and active community support. The project is mature enough for a serious pilot—its CSI implementation is GA, it offers built‑in UI, backup/restore, and disaster‑recovery features, and it is already deployed in many production Kubernetes environments. Before full adoption, perform a final review of licensing (Apache‑2.0), run a security audit of the container images, and verify that core maintainers are responsive, but overall the risk profile is low and the platform is ready for production use.

### Русский

Longhorn — это cloud‑native распределённое хранилище, разработанное специально для Kubernetes, которое позволяет быстро и надёжно создавать блок‑уровневые тома с поддержкой резервного копирования, восстановления и репликации. Типичный сценарий внедрения — развертывание небольшого proof‑of‑concept в кластере, проверка README и базовых функций, а затем масштабирование до продакшн‑окружения для обеспечения постоянного доступа к данным приложений. Проект обладает высокой готовностью к production: активные коммиты, более 7 800 звёзд, широкое принятие в сообществе и стабильный набор функций, однако перед полномасштабным запуском рекомендуется окончательная проверка лицензии, безопасности и наличия активных мейнтейнеров.

### 中文

**项目简介（2‑3 句话）**  
Longhorn 是一个面向 Kubernetes 的云原生分布式块存储系统，提供高可用、快照、备份和跨集群复制等企业级功能，能够在裸机或公有云环境中直接为容器化工作负载提供持久化磁盘。

**价值**  
- **统一存储层**：在 Kubernetes 上即插即用，消除传统存储与容器编排之间的兼容性障碍。  
- **数据安全**：内置快照、备份和容灾复制，帮助业务实现 RPO/RTO 目标。  
- **成本可控**：基于本地磁盘或云块存储构建，无需额外采购专有存储硬件，降低运维开销。  

**典型接入方式**  
1. **Helm / kubectl 安装**：通过官方 Helm Chart 或 `kubectl apply -f https://raw.githubusercontent.com/longhorn/longhorn/master/deploy/longhorn.yaml` 快速部署 Longhorn 控制平面和节点驱动。  
2. **StorageClass 配置**：创建 `StorageClass`（如 `longhorn`），在 PVC 中指定，即可让应用自动使用 Longhorn 提供的卷。  
3. **备份/快照集成**：利用 Longhorn UI 或 CRD（`LonghornVolumeSnapshot`、`BackupTarget`）实现自动化备份到 S3、NFS 等外部存储。  

**生产可用性**  
- **活跃社区**：GitHub ★7800+、Fork ★710，最近一次提交在 2026‑06‑23，维护者响应及时。  
- **成熟度**：已在多个大规模生产环境（如 Rancher、K3s）中验证，提供 HA 控制平面、节点故障自愈和跨集群复制。  
- **安全与合规**：项目采用 Apache‑2.0 许可证，代码审计记录良好；建议在正式上线前进行安全依赖扫描和 RBAC 最小化配置。  

综上，Longhorn 具备高可用、易集成、成本友好的特性，是在 Kubernetes 上构建持久化存储的可靠 OSS 选型，可先通过小规模 PoC 验证，再逐步推广至生产环境。

## 🧭 Practical evaluation

**Value:** longhorn/longhorn helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 7802 GitHub stars
- 710 forks
- updated 2026-06-23
- primary language: Shell
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 71/100 |
| stars | 83/100 |
| topics | 88/100 |
| outlook | 64/100 |
| quality | 74/100 |
| recency | 40/100 |
| adoption | 80/100 |
| production | 60/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/longhorn/longhorn) · [← Back to DevOps & Infra](./README.md)</sub>
