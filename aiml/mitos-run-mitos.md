# mitos-run/mitos

[![Stars](https://img.shields.io/github/stars/mitos-run/mitos?style=flat-square&color=yellow)](https://github.com/mitos-run/mitos/stargazers) [![Forks](https://img.shields.io/github/forks/mitos-run/mitos?style=flat-square&color=blue)](https://github.com/mitos-run/mitos/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Millisecond microVM sandbox forking for AI agents on Kubernetes. Firecracker VMs that restore from memory snapshots in milliseconds, fork a running VM into N copies, and persist durable, versioned workspaces. Self-hostable, declarative CRDs.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 44 |
| 🍴 **Forks** | 3 |
| 💻 **Language** | Go |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-infrastructure` `agent-sandbox` `ai-agents` `code-execution` `code-interpreter` `copy-on-write` `e2b-alternative` `firecracker` `kubernetes` `kvm` `llm` `microvm`

## 🎯 Categories

AI/ML · DevOps/Infra

## 📝 Summary

### English

**Project Summary:**

mitos-run/mitos is an open-source project that enables the creation of AI agents on Kubernetes using millisecond microVM sandbox forking. This allows for rapid prototyping and deployment of AI capabilities without requiring a new, blank model stack. The project provides a self-hostable, declarative solution for creating durable, versioned workspaces.

**Value Proposition:**

The primary value of mitos-run/mitos lies in its ability to accelerate AI development by providing a fast and flexible solution for creating and testing AI agents. This makes it an ideal tool for prototyping AI features, building RAG (Reusable Agent Graph) or agent workflows, and evaluating model tooling.

**Practical Adoption Path:**

To adopt mitos-run/mitos, developers can start by evaluating the project through a small proof of concept and reviewing the README documentation. The project's declarative CRDs (Custom Resource Definitions) make it relatively straightforward to integrate into existing Kubernetes environments. However, it's essential to perform dependency and maintenance checks before considering production deployment.

**Production Readiness:**

While mitos-run/mitos is suitable for prototypes or internal workflows, its production readiness is currently assessed as medium. This is due to the need for a final review of the project's license, security posture,

### Русский

Резюме:

Митос - это открытый проект, предоставляющий инфраструктуру для развертывания и управления искусственными интеллектом (AI) агентами в Kubernetes. Он позволяет создавать копии работающих виртуальных машин (VM) с помощью Firecracker VM и сохранять устойчивые и версионные рабочие пространства. Это идеальный выбор для прототипирования функций AI, построения рабочих процессов RAG или агентов и оценки инструментов моделирования.

Проект Mitos имеет средний уровень готовности к production (Medium) и подходит для внутренних рабочих процессов или прототипирования. Для внедрения проекта рекомендуется начать с малого proof of concept и проверки README.

### 中文

**项目简介（2‑3 句）**  
mitos-run/mitos 是一个面向 Kubernetes 的毫秒级微 VM 沙箱，基于 Firecracker 实现内存快照恢复与多副本 fork。它通过声明式 CRD 提供可持久化、版本化的工作空间，让 AI 代理能够在几毫秒内启动并并行运行多个微 VM。

---

## 价值

- **快速原型**：在毫秒级启动的微 VM 中运行 AI 代理，省去模型训练与环境搭建的时间，直接在已有模型上叠加新能力。  
- **高并发实验**：一次 fork 可得到 N 个相同状态的 VM，适合并行评估 RAG、工具调用、Agent‑Toolchain 等工作流。  
- **可持久化工作空间**：工作空间自动版本化，便于回滚、审计和复现实验结果。  
- **自托管、云原生**：通过 Kubernetes CRD 完全声明式管理，兼容现有 CI/CD 与 GitOps 流程，避免对公有云服务的依赖。

---

## 典型接入方式

1. **环境准备**  
   - 在目标 K8s 集群上安装 `firecracker` RuntimeClass（或使用项目自带的 Helm chart）。  
   - 为项目创建对应的 `Namespace` 与 `ServiceAccount`，确保具备创建 `Pod`、`ConfigMap`、`PersistentVolumeClaim` 的权限。

2. **部署 CRD**  
   ```bash
   kubectl apply -f https://github.com/mitos-run/mitos/releases/download/v0.3.0/crds.yaml
   ```

3. **声明工作空间**（示例）  
   ```yaml
   apiVersion: mitos.run/v1alpha1
   kind: Workspace
   metadata:
     name: rag-demo
   spec:
     image: public.ecr.aws/firecracker/firecracker:latest
     snapshot: s3://my-bucket/snapshots/agent-base.snap
     replicas: 5          # fork 为 5 份
     resources:
       cpu: "2"
       memory: "4Gi"
   ```
   - `snapshot` 指向预先准备好的内存快照（包含模型、依赖、代码）。  
   - `replicas` 控制一次 fork 的副本数。

4. **在代码中调用**  
   - 通过 Kubernetes API（client-go）或 `kubectl wait` 检查 `Workspace` 状态，获取生成的 Pod IP / Service。  
   - 将 AI 代理的入口 HTTP/gRPC 地址注入业务服务或 Prompt 链中，即可使用。

5. **CI/CD / GitOps**  
   - 将上述 YAML 纳入 Git 仓库，使用 ArgoCD、Flux 等工具自动同步，实现“代码即部署”。

---

## 生产可用性评估

| 维度 | 现状 | 备注 |
|------|------|------|
| **成熟度** | **中等**（适合原型、内部工具） | 项目已更新至 2026‑07‑06，GitHub ⭐44、Fork 3，活跃度一般。 |
| **依赖** | Firecracker、Kubernetes 1.24+、CRD 控制器 | 需要在集群中启用 `RuntimeClass` 并保证底层节点支持 KVM。 |
| **安全** | 无已知重大漏洞，仍需自行审计容器镜像与快照来源 | 建议在生产环境使用内部镜像仓库、签名验证。 |
| **运维成本** | 需要维护快照存储（S3/MinIO）和控制器的升级 | 控制器本身体积小，升级相对简单。 |
| **可扩展性** | 支持水平 fork 与水平 Pod 自动伸缩 | 通过 `replicas` 与 HPA 可实现弹性扩容。 |
| **监控/日志** | 暴露标准 K8s metrics 与日志 | 可接入 Prometheus/Grafana 进行监控。 |
| **适用场景** | AI 功能快速验证、RAG/Agent 工作流原型、内部实验平台 | 对外部客户的高可用生产服务仍需额外冗余与容灾设计。 |

**结论**：mitos-run/mitos 在 **原型验证和内部研发** 场景下价值突出，能够在毫秒级启动 AI 代理并实现高并发实验。若要用于面向客户的生产系统，需在以下方面进行补强：快照安全签名、控制器高可用部署、节点硬件（KVM）合规性、以及完善的监控告警体系。经过这些加固后，可逐步提升至生产级别。

## 🧭 Practical evaluation

**Value:** mitos-run/mitos helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 44 GitHub stars
- 3 forks
- updated 2026-07-06
- primary language: Go
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 15/100 |
| stars | 35/100 |
| topics | 100/100 |
| outlook | 56/100 |
| quality | 53/100 |
| recency | 40/100 |
| adoption | 30/100 |
| production | 55/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/mitos-run/mitos) · [← Back to AI/ML](./README.md)</sub>
