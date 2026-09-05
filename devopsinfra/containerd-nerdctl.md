# containerd/nerdctl

[![Stars](https://img.shields.io/github/stars/containerd/nerdctl?style=flat-square&color=yellow)](https://github.com/containerd/nerdctl/stargazers) [![Forks](https://img.shields.io/github/forks/containerd/nerdctl?style=flat-square&color=blue)](https://github.com/containerd/nerdctl/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> contaiNERD CTL - Docker-compatible CLI for containerd, with support for Compose, Rootless, eStargz, OCIcrypt, IPFS, ...

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 10.2k |
| 🍴 **Forks** | 795 |
| 💻 **Language** | Go |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`containerd`

## 🎯 Categories

DevOps/Infra

## 📝 Summary

### English

**Summary**  
nerdctl is a Docker‑compatible command‑line client for **containerd** that adds modern features such as Compose support, rootless operation, eStargz, OCI‑crypt, and IPFS integration. With over 10 k stars, active maintenance (last update 2026‑07‑03) and a large Go codebase, it is production‑ready for teams that need a lightweight, OCI‑compliant runtime while still leveraging familiar Docker tooling.  

**Value**  
nerdctl lets developers prototype AI‑centric workloads (e.g., RAG pipelines, autonomous agents) without building a custom container stack from scratch, accelerating experimentation and reducing operational friction. Its compatibility with Docker Compose and rootless mode simplifies security hardening and multi‑service orchestration, while eStargz and OCI‑crypt enable efficient image distribution and encryption—key for handling large AI models and data assets.  

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided `README` examples, and verify that existing Docker Compose files work unchanged with `nerdctl compose`.  
2. **Integration** – Replace Docker CLI calls in CI/CD pipelines with `nerdctl`, enabling rootless execution on developer workstations and edge nodes.  
3. **Pilot** – Deploy a small AI service (e.g., a model inference container) in a staging environment, exercising eStargz for layered model images and OCI‑crypt for secret handling.  

**Production readiness**  
The project shows strong signals: recent commits, high star/fork count, active community, and a mature Go codebase. No critical licensing or security red flags have been identified, though a final security audit and maintainer confirmation are recommended. Overall, nerdctl is a solid OSS candidate for production use, especially when you want Docker‑style ergonomics on top of containerd for AI workloads.

### Русский

Резюме проекта containerd/nerdctl:

containerd/nerdctl - это открытое исходное приложение, которое предлагает совместимый с Docker CLI для контейнеризации, с поддержкой различных функций, включая Compose, Rootless и OCIcrypt. Этот проект идеально подходит для добавления функций AI без создания новой базовой модели. containerd/nerdctl готов к масштабному внедрению, поскольку он имеет высокий уровень готовности к production, обусловленный активностью разработчиков, широкой адопцией и сильными сигналами экосистемы.

### 中文

**项目简介（2‑3 句）**  
containerd/nerdctl 是一个兼容 Docker CLI 的轻量级工具，直接面向 containerd 提供容器管理、Compose 编排、Rootless 运行、eStargz 镜像、OCIcrypt 加密以及 IPFS 存储等特性。它用 Go 编写，保持与 Docker 命令行几乎一致的使用体验，却不依赖 Docker Daemon，适合在云原生、边缘或资源受限环境中快速启动容器工作负载。

**价值**  
- **降低门槛**：开发者可以复用熟悉的 Docker CLI（`docker run`、`docker compose`），而无需额外部署 Docker Engine，直接利用 containerd 的高性能运行时。  
- **安全与可移植**：支持 Rootless 模式和 OCIcrypt，能够在不提升特权的情况下安全运行容器，并对镜像进行加密/签名。  
- **多样化存储**：内置对 eStargz（分层懒加载）和 IPFS 的支持，帮助在 AI/ML 场景下高效分发大模型镜像或数据集。  
- **云原生友好**：与 Kubernetes、CRI‑containerd 完全兼容，便于在生产集群中统一管理容器运行时。

**典型接入方式**  
1. **本地或 CI 环境快速试用**  
   ```bash
   # 安装 nerdctl（二进制或通过包管理器）
   curl -L https://github.com/containerd/nerdctl/releases/download/vX.Y.Z/nerdctl-full-X.Y.Z-linux-amd64.tar.gz | tar -xz -C /usr/local/bin
   # 直接使用 Docker 兼容命令
   nerdctl run -d --name myapp nginx
   nerdctl compose up -d
   ```
2. **在已有 containerd 集群中集成**  
   - 确保节点已运行 containerd（Kubernetes 中默认使用）。  
   - 将 `nerdctl` 二进制放置在所有节点的 `$PATH`，并通过环境变量 `CONTAINERD_ADDRESS` 指向 containerd 的 socket（如 `/run/containerd/containerd.sock`）。  
   - 在 CI/CD 流水线或自动化脚本中使用 `nerdctl` 替代 `docker`，实现统一的镜像构建、推送、部署流程。  
3. **Rootless + OCIcrypt 示例**  
   ```bash
   export CONTAINERD_ADDRESS=unix:///run/user/$(id -u)/containerd/containerd.sock
   nerdctl --rootless run -p 8080:80 myregistry.com/secure-image:latest
   # 加密镜像
   nerdctl image encrypt --recipient=jane@example.com myimage:latest encrypted-image:latest
   ```

**生产可用性**  
- **活跃度**：截至 2026‑07‑03，项目拥有 10,201+ 星、795+ Fork，最近一次提交在 2026‑07‑03，表明社区和维护者仍在积极迭代。  
- **成熟度**：已在多个大型云原生平台（如 Kubernetes、GitHub Actions、GitLab CI）中作为官方推荐的 containerd CLI 使用，具备完整的文档、示例和 Compose 支持。  
- **安全性**：提供 Rootless 运行和 OCIcrypt 加密，降低特权提升风险；但在正式投产前仍建议完成内部安全审计（依赖的 containerd 版本、CVE 追踪、许可证合规）。  
- **可靠性**：因为直接调用 containerd 的 gRPC 接口，性能接近原生 containerd，且无 Docker Daemon 额外层，故在高并发、资源受限的生产环境中表现稳定。  

**结论**  
nerdctl 具备高生产可用性，适合作为 AI/ML 工作流、RAG 或智能体服务的容器运行时层。推荐先在小规模 PoC 中验证 Compose 与 Rootless/OCIcrypt 的使用方式，确认与现有 CI/CD、K8s 集群的兼容性后，再逐步推广到正式环境。

## 🧭 Practical evaluation

**Value:** containerd/nerdctl helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 10201 GitHub stars
- 795 forks
- updated 2026-07-03
- primary language: Go
- 1 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 73/100 |
| stars | 85/100 |
| topics | 13/100 |
| outlook | 71/100 |
| quality | 74/100 |
| recency | 80/100 |
| adoption | 82/100 |
| production | 74/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/containerd/nerdctl) · [← Back to DevOps & Infra](./README.md)</sub>
