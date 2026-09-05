# openshift/hypershift

[![Stars](https://img.shields.io/github/stars/openshift/hypershift?style=flat-square&color=yellow)](https://github.com/openshift/hypershift/stargazers) [![Forks](https://img.shields.io/github/forks/openshift/hypershift?style=flat-square&color=blue)](https://github.com/openshift/hypershift/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Hyperscale OpenShift - clusters with hosted control planes

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 527 |
| 🍴 **Forks** | 506 |
| 💻 **Language** | Go |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
Hypershift (openshift/hypershift) is an open‑source project that enables “hyperscale” OpenShift deployments by hosting control planes as separate, lightweight clusters. Written in Go and actively maintained (527 ★, 506 forks, last update 2026‑06‑26), it lets you spin up and manage many OpenShift clusters from a single management plane.

**Value**  
- **Scalability:** By decoupling control‑plane workloads from worker nodes, you can provision dozens or hundreds of OpenShift clusters without the overhead of a full control‑plane per cluster.  
- **Operational simplicity:** Hosted control planes are managed centrally, reducing the operational burden of upgrades, backups, and security patches.  
- **Flexibility:** Works with existing OpenShift tooling and can be integrated into CI/CD pipelines to spin up temporary clusters for testing or multi‑tenant environments.

**Practical Adoption Path**  
1. **Evaluate the README and demos:** Verify that the supported workflow (e.g., creating a hosted cluster via `hypershift create cluster`) matches your use case.  
2. **Prototype:** Deploy a single hosted control plane in a sandbox environment; exercise cluster creation, scaling, and upgrade processes.  
3. **Security & compliance review:** Scan the codebase, check the license (Apache 2.0), and run vulnerability scans on the generated images.  
4. **Integrate with your CI/CD:** Wrap the `hypershift` CLI or controller‑manager into your pipeline to automate cluster lifecycle.  
5. **Operational hand‑off:** Document required RBAC, monitoring, and backup procedures; train the team on troubleshooting hosted‑control‑plane components.

**Production Readiness**  
The project is at a **medium** readiness level. It is mature enough for internal prototypes and controlled production workloads, but you should perform the following before full‑scale adoption:  
- Confirm active maintainers are responding to issues/PRs.  
- Validate that the version you plan to use aligns with your OpenShift release cycle.  
- Implement dependency pinning and regular upgrade testing.  
- Establish monitoring and alerting for the hosted control‑plane components.  

With these checks in place, Hypershift can be safely used in production for multi‑cluster, high‑density OpenShift environments.

### Русский

**openshift/hypershift** — это open‑source решение для создания гипермасштабных кластеров OpenShift с размещёнными (hosted) control‑plane, позволяющее быстро разворачивать изолированные рабочие среды без необходимости управлять инфраструктурой control‑plane вручную. Типичный сценарий — автоматизация разработки, тестирования или внутренних CI/CD‑конвейеров, где требуется гибко масштабировать кластеры и быстро переключаться между версиями OpenShift. Уровень готовности — средний: проект активно поддерживается (обновления до 2026‑06‑26, 527 ★, 506 fork), но перед выводом в продакшн рекомендуется провести детальный аудит лицензий, безопасности и зависимости, а также убедиться в наличии ответственных мейнтейнеров.

### 中文

**项目简介（2‑3 句）**  
Hypershift 是 OpenShift 的超大规模实现，提供“托管控制平面”模式，让每个租户或工作负载都可以在同一底层集群上独立运行自己的 OpenShift 控制平面，从而实现多租户、弹性伸缩和资源隔离。

**价值**  
- **多租户即服务**：通过在同一物理集群上快速创建/销毁完整的 OpenShift 控制平面，降低了运营成本并提升资源利用率。  
- **弹性伸缩**：控制平面本身也可以按需扩容或收缩，适配突发流量或大规模测试。  
- **统一运维**：底层基础设施统一管理，用户只需要关注自己的控制平面和工作负载，运维复杂度大幅下降。

**典型接入方式**  
1. **准备底层集群**：在已有的 OpenShift 或 Kubernetes 集群上安装 `hypershift` Operator（通过 OperatorHub 或 `oc apply -f`）。  
2. **创建托管控制平面**：使用 `hypershift create cluster` CLI 或自定义资源 `HostedCluster`，指定网络、节点池、身份认证等参数。  
3. **接入 CI/CD**：将生成的 kubeconfig（托管控制平面的 kubeconfig）交给现有的 GitOps/ArgoCD 流水线，即可在该控制平面上部署业务。  
4. **监控与治理**：通过 Prometheus、Alertmanager 以及 OpenShift Console 的多集群视图统一监控所有托管控制平面。

**生产可用性**  
- **成熟度**：GitHub 527 ⭐、506 Fork，活跃维护，最近一次提交在 2026‑06‑26，代码主要使用 Go 编写。  
- **适用场景**：适合内部原型、研发测试平台以及需要大规模多租户的私有云/混合云环境。  
- **风险与准备**：在正式投产前需完成以下检查  
  - 许可证兼容性（Apache‑2.0）和第三方依赖的安全审计；  
  - 控制平面与底层集群的网络隔离、RBAC 策略是否符合企业合规；  
  - 监控、备份与灾难恢复流程的验证；  
  - 与现有 CI/CD、身份提供者（OIDC、LDAP）集成的兼容性测试。  

综上，Hypershift 在多租户 OpenShift 场景下提供了高效、弹性的解决方案，经过适当的安全与运维审查后，可在生产环境中用于原型验证或内部平台，具备向全量生产迁移的潜力。

## 🧭 Practical evaluation

**Value:** openshift/hypershift may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 527 GitHub stars
- 506 forks
- updated 2026-06-26
- primary language: Go

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 68/100 |
| stars | 58/100 |
| topics | 0/100 |
| outlook | 62/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 61/100 |
| production | 65/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/openshift/hypershift) · [← Back to Misc](./README.md)</sub>
