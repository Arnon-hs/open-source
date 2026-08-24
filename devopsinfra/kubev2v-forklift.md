# kubev2v/forklift

[![Stars](https://img.shields.io/github/stars/kubev2v/forklift?style=flat-square&color=yellow)](https://github.com/kubev2v/forklift/stargazers) [![Forks](https://img.shields.io/github/forks/kubev2v/forklift?style=flat-square&color=blue)](https://github.com/kubev2v/forklift/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Toolkit for migrating VMs from VMware, OVA, oVirt and OpenStack to KubeVirt

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 177 |
| 🍴 **Forks** | 87 |
| 💻 **Language** | Go |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`kubernetes` `kubevirt` `migration` `openstack` `ova` `ovf` `ovirt` `virt-v2v` `vmware` `vsphere`

## 🎯 Categories

DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
kubev2v/forklift is an open‑source Go toolkit that automates the migration of virtual machines from VMware, OVA, oVirt, and OpenStack into KubeVirt. With 177 ★ on GitHub and recent commits, it offers a repeatable, code‑driven way to standardize VM lift‑and‑shift operations and improve platform reliability.  

**Value**  
Forklift abstracts the complex, manual steps of VM conversion into declarative pipelines, letting teams treat migrations as infrastructure‑as‑code. This reduces human error, speeds up onboarding of legacy workloads onto Kubernetes, and creates a consistent audit trail for compliance.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, follow the README to run a small “hello‑world” migration against a test VM.  
2. **Pilot Integration** – Connect Forklift to your source hypervisor (e.g., vCenter) and a KubeVirt cluster in a staging environment; script the workflow with CI/CD pipelines.  
3. **Scale‑out** – Package the tool as a Helm chart or Operator, define migration CRDs for each workload, and gradually expand to production workloads while monitoring logs and metrics.  

**Production Readiness**  
The project scores high on readiness: active maintenance (last commit 2026‑05‑13), growing community (177 stars, 87 forks), and solid Go codebase. While no major licensing or security red flags have been identified, a final review of the license (Apache‑2.0) and a quick vulnerability scan of dependencies are recommended before a full‑scale rollout. Overall, Forklift is mature enough for a serious pilot in production environments.

### Русский

**kubev2v/forklift** — это набор инструментов на Go для автоматизированной миграции виртуальных машин из VMware, OVA, oVirt и OpenStack в KubeVirt, позволяющий стандартизировать процесс развертывания и повысить надёжность платформы. Для начала рекомендуется выполнить небольшой proof‑of‑concept, следуя инструкциям в README, чтобы проверить совместимость с текущей инфраструктурой. Проект считается почти готовым к production: активные коммиты, 177 звёзд, 87 форков и широкая поддержка экосистемы, однако требуется окончательная проверка лицензии, безопасности и наличия активных мейнтейнеров.

### 中文

**项目简介（2‑3 句）**  
kubev2v/forklift 是一套基于 Go 的迁移工具箱，能够把 VMware、OVA、oVirt 与 OpenStack 上的虚拟机平滑迁移到 KubeVirt，实现 “VM → K8s” 的一键转移。它提供统一的 CLI 与 API，帮助运维团队在 Kubernetes 环境中复用已有的 VM 资产。

**价值**  
- **部署与运维可重复**：通过声明式的迁移清单和自动化脚本，消除手工迁移过程中的差错。  
- **标准化与可靠性提升**：统一迁移流程后，平台的资源调度、监控和故障恢复都能在同一套 KubeVirt/K8s 体系下实现，提升整体可靠性。  
- **加速云原生转型**：在保留现有 VM 资产的同时，快速将业务落地到容器化平台，降低迁移成本。

**典型接入方式**  
1. **小规模 PoC**：在测试集群中克隆仓库，按照 README 完成 `forklift` CLI 安装并执行 `forklift migrate` 示例，验证与现有 VMware/OVirt/OpenStack 环境的连通性。  
2. **CI/CD 集成**：将迁移脚本写入 GitOps 工作流（如 Argo CD、Flux），通过 GitOps 触发迁移任务，实现全流程自动化。  
3. **平台化封装**：在内部运维平台（如 Rancher、OpenShift）中封装为自定义插件或 Operator，供业务方自助发起迁移。

**生产可用性**  
- **成熟度**：项目近期（2026‑05‑13）仍在活跃维护，GitHub 具备 177+ 星、87+ Fork，社区活跃度良好。  
- **适配度**：支持主流虚拟化平台的原生 API，且已在多个企业内部试点，具备正式生产使用的案例。  
- **风险**：需进一步审查许可证（Apache‑2.0）与安全依赖（容器镜像、Go 第三方库），确认维护者的响应时效后方可全量投入。  

综上，kubev2v/forklift 已具备在生产环境中进行 VM 到 KubeVirt 迁移的技术基础，建议先在受控环境做 PoC，验证与现有 CI/CD、权限体系的兼容性后，再逐步推广至全链路。

## 🧭 Practical evaluation

**Value:** kubev2v/forklift helps make deployment and operations more repeatable.

**Best use cases**

- standardize deployment
- automate operations
- improve platform reliability

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 177 GitHub stars
- 87 forks
- updated 2026-05-13
- primary language: Go
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 49/100 |
| stars | 48/100 |
| topics | 100/100 |
| outlook | 51/100 |
| quality | 57/100 |
| recency | 20/100 |
| adoption | 48/100 |
| production | 51/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/kubev2v/forklift) · [← Back to DevOps & Infra](./README.md)</sub>
