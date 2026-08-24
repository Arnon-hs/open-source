# kubernetes-csi/csi-driver-nfs

[![Stars](https://img.shields.io/github/stars/kubernetes-csi/csi-driver-nfs?style=flat-square&color=yellow)](https://github.com/kubernetes-csi/csi-driver-nfs/stargazers) [![Forks](https://img.shields.io/github/forks/kubernetes-csi/csi-driver-nfs?style=flat-square&color=blue)](https://github.com/kubernetes-csi/csi-driver-nfs/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> This driver allows Kubernetes to access NFS server on Linux node.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.3k |
| 🍴 **Forks** | 318 |
| 💻 **Language** | Go |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`csi` `k8s-sig-storage` `kubernetes` `nfs`

## 🎯 Categories

DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The `kubernetes-csi/csi-driver-nfs` project provides a Container Storage Interface (CSI) driver that enables Kubernetes clusters to mount and use NFS shares on Linux nodes as persistent volumes. With a mature codebase (≈1.3 k stars, active maintenance, and broad community adoption), it offers a reliable way to expose existing NFS infrastructure to containerized workloads.  

**Value**  
- **Searchable internal knowledge** – By exposing NFS‑backed data through the standard Kubernetes PVC model, the driver lets AI assistants and other tooling query, index, and retrieve files stored on legacy NFS servers without custom scripts.  
- **Unified storage abstraction** – Teams can treat NFS shares like any other CSI‑managed volume, simplifying backup, migration, and policy enforcement across cloud‑native and on‑prem environments.  
- **Ecosystem compatibility** – Works with the native Kubernetes storage stack, Helm charts, and popular CI/CD pipelines, making it easy to incorporate into existing DevOps workflows.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Deploy the driver using the official Helm chart or the provided YAML manifests in a non‑critical namespace. Create a simple `PersistentVolume`/`PersistentVolumeClaim` that points to a test NFS export and verify pod access.  
2. **Documentation Review** – Follow the README and the CSI driver guidelines to configure required security settings (e.g., NFS export permissions, SELinux, and network policies).  
3. **Integration Tests** – Add automated e2e tests that spin up a temporary NFS server (e.g., using `nfs-ganesha` in a container) and validate read/write semantics under load.  
4. **Scale‑out** – Roll the driver to production namespaces, enable monitoring (Prometheus metrics are exposed), and configure alerts for mount failures or latency spikes.  

**Production Readiness**  
- **High** – The repository shows recent activity (last commit 2026‑07‑01), a healthy contributor base (1294 stars, 318 forks), and is written in Go, the language of choice for Kubernetes components.  
- **Maturity** – The driver is already used in many production clusters, and the CSI spec it implements is stable.  
- **Risk Considerations** – Before a full rollout, perform a final review of the license (Apache‑2.0), run a security scan of the container images, and confirm that maintainers are responsive (open issues are addressed within a reasonable timeframe).  

Overall, `csi-driver-nfs` is a production‑grade, well‑supported solution for exposing NFS storage to Kubernetes, making it a strong candidate for pilots that aim to make internal NFS‑based knowledge searchable and consumable by AI assistants.

### Русский

`kubernetes-csi/csi-driver-nfs` — это CSI‑драйвер, позволяющий Kubernetes монтировать файловые системы NFS с Linux‑узлов, что упрощает интеграцию существующих NFS‑хранилищ в контейнерные workloads. Типичный сценарий внедрения — установка драйвера в кластере, создание `StorageClass` и `PersistentVolume`/`PersistentVolumeClaim` для автоматического provision‑инга NFS‑томов, после чего приложения могут использовать их как обычные PVC. Проект имеет высокий уровень готовности к production: активные коммиты, более 1200 звёзд, широкое принятие в сообществе и стабильный Go‑код, однако перед масштабным rollout рекомендуется проверить лицензию, провести базовый security‑аудит и выполнить небольшой proof‑of‑concept.

### 中文

**项目简介**  
kubernetes‑csi/csi‑driver‑nfs 是一个基于 CSI（Container Storage Interface）的插件，能够让 Kubernetes 集群在 Linux 节点上直接挂载并使用 NFS（Network File System）共享存储。该驱动实现了标准的 CSI 接口，支持动态卷创建、快照以及卷扩容等特性。

**价值**  
- **统一存储抽象**：在 Kubernetes 中使用统一的 CSI 接口管理 NFS，避免了手动编写 `hostPath`、`nfs-client` DaemonSet 等杂项配置。  
- **提升运维效率**：通过声明式的 `StorageClass`、`PersistentVolumeClaim`，实现自动化的 NFS 卷创建与回收，降低运维成本。  
- **生态兼容**：兼容所有遵循 CSI 标准的调度器、备份工具和监控系统，方便在多云或混合云环境中统一管理 NFS 存储。

**典型接入方式**  
1. **部署驱动**：使用官方提供的 Helm chart 或直接 `kubectl apply -f deploy/kubernetes` 将 CSI driver 的 controller、node plugin 和相关 RBAC 资源部署到集群。  
2. **创建 StorageClass**：定义一个指向 NFS 服务器的 `StorageClass`（如 `nfs-csi`），并在 `parameters` 中填写 `server`、`share` 等信息。  
3. **使用 PVC**：在工作负载的 PVC 中引用该 StorageClass，Kubernetes 会自动调用 CSI driver 在指定 NFS 服务器上创建子目录并挂载到 Pod。  

```yaml
apiVersion: storage.k8s.io/v1
kind: StorageClass
metadata:
  name: nfs-csi
provisioner: nfs.csi.k8s.io
parameters:
  server: 10.0.0.10
  share: /export/data
```

**生产可用性**  
- **活跃度**：项目最近一次提交在 2026‑07‑01，拥有 1.3k+ Stars、300+ Forks，社区活跃且已有多家企业在生产环境使用。  
- **成熟度**：实现了 CSI 必要的 CreateVolume、DeleteVolume、NodePublishVolume 等接口，支持动态卷、卷扩容和快照（可选插件），符合 CNCF 推荐的生产级存储插件标准。  
- **安全与运维**：代码基于 Go，遵循安全审计流程；可配合 PodSecurityPolicy / OPA 进行权限控制；提供详细的监控指标（Prometheus）和日志。  

综合来看，csi‑driver‑nfs 已具备成熟的功能、活跃的社区和良好的安全姿态，是在 Kubernetes 中使用 NFS 存储的可靠生产级解决方案，适合作为内部知识库或文档存储的底层文件系统。

## 🧭 Practical evaluation

**Value:** kubernetes-csi/csi-driver-nfs helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1294 GitHub stars
- 318 forks
- updated 2026-07-01
- primary language: Go
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 63/100 |
| stars | 66/100 |
| topics | 50/100 |
| outlook | 57/100 |
| quality | 62/100 |
| recency | 40/100 |
| adoption | 65/100 |
| production | 58/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/kubernetes-csi/csi-driver-nfs) · [← Back to DevOps & Infra](./README.md)</sub>
