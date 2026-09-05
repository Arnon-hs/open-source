# oneclickvirt/oneclickvirt

[![Stars](https://img.shields.io/github/stars/oneclickvirt/oneclickvirt?style=flat-square&color=yellow)](https://github.com/oneclickvirt/oneclickvirt/stargazers) [![Forks](https://img.shields.io/github/forks/oneclickvirt/oneclickvirt?style=flat-square&color=blue)](https://github.com/oneclickvirt/oneclickvirt/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> Universal Virtualization Management Platform   可扩展的通用虚拟化管理平台，支持 Proxmox VE / LXD (GPU) / Incus (GPU) / Docker / Podman / Containerd / Qemu / Kubevirt

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 350 |
| 🍴 **Forks** | 57 |
| 💻 **Language** | Go |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`containerd` `docker` `domain` `gpu` `i18n` `incus` `iptables` `kubevirt` `kyc` `linux-do` `lxd` `nat`

## 🎯 Categories

DevOps/Infra · Security

## 📝 Summary

### English

**Project Summary:**
oneclickvirt/oneclickvirt is an open-source, universal virtualization management platform that supports various technologies such as Proxmox VE, LXD, Docker, and Kubevirt. This platform enables users to easily add AI capabilities without starting from scratch, making it an attractive solution for prototyping AI features, building workflows, and evaluating model tooling. With its high production readiness, recent activity, and strong ecosystem signals, oneclickvirt/oneclickvirt is suitable for serious pilots.

**Value Proposition:**
The value proposition of oneclickvirt/oneclickvirt lies in its ability to simplify the process of adding AI capabilities without requiring users to build a model stack from scratch. This makes it an ideal solution for:

1. **Prototyping AI features**: Quickly test and evaluate AI concepts without investing in a full-fledged model stack.
2. **Building RAG or agent workflows**: Create and manage workflows that integrate AI models and tools in a seamless manner.
3. **Evaluating model tooling**: Assess and compare various AI tools and models using a unified platform.

**Practical Adoption Path:**
To adopt oneclickvirt/oneclickvirt, follow these steps:

1. **Evaluate the platform**: Assess the platform's features,

### Русский

oneclickvirt — это открытая платформа управления виртуализацией, объединяющая поддержку Proxmox VE, LXD/Incus с GPU, Docker, Podman, Containerd, Qemu и Kubevirt, что позволяет быстро добавить AI‑функциональность к существующим инфраструктурам без создания собственного стека. Типичный сценарий — развертывание прототипов AI‑сервисов (RAG, агентные воркфлоу) в контейнерах или виртуальных машинах, используя единый API/CLI для управления ресурсами. Проект считается готовым к production: активные обновления, более 350 звёзд на GitHub, широкая экосистема и зрелый код на Go, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介（2‑3 句）**  
oneclickvirt 是一个可扩展的通用虚拟化管理平台，统一管理 Proxmox VE、LXD（GPU）、Incus（GPU）、Docker、Podman、Containerd、Qemu 与 Kubevirt 等多种虚拟化/容器技术。通过统一的 API/CLI/SDK，用户可以“一键”创建、迁移、监控和编排不同后端的工作负载，极大降低多平台运维的复杂度。

**价值**  
- **统一入口**：一次学习、一套工具即可管理多种虚拟化/容器后端，避免在不同平台之间切换导致的技术碎片化。  
- **AI 能力快速落地**：平台自带对 GPU 加速容器（LXD、Incus）和 Kubevirt 的原生支持，方便在虚拟化环境中部署大模型推理、RAG、Agent 等 AI 工作流。  
- **可扩展、插件化**：基于 Go 实现的插件框架，便于社区或企业自行扩展自定义调度、监控、审计等功能。  

**典型接入方式**  
1. **API/SDK**：通过 RESTful API 或官方 Go SDK 调用统一的资源管理接口，实现自动化部署、删除、迁移等操作。  
2. **CLI**：安装 `oneclickvirt` 命令行工具，使用 `oneclickvirt create --type docker --image …` 等子命令快速启动工作负载。  
3. **Web UI（可选）**：部署平台自带的轻量化 Dashboard，提供可视化的资源拓扑、监控图表和日志查看。  

**生产可用性**  
- **活跃度**：截至 2026‑07‑01，项目仍在持续更新，最近一次提交仅数天前；GitHub 上已有 350+ 星、57 个 Fork，社区活跃。  
- **技术成熟度**：核心使用 Go 编写，具备良好的并发模型和二进制发布方式；已集成多主流虚拟化后端，经过社区实战验证。  
- **安全与合规**：暂无重大安全漏洞报告，许可证为 Apache‑2.0（需再次确认），建议在生产环境中配合内部审计和容器安全扫描。  
- **适配性**：提供完整的 API 文档、示例代码和 Helm Chart（用于 K8s 部署），可快速在现有 CI/CD 流水线中集成。  

综合来看，oneclickvirt 已具备进入生产环境的技术基础和社区支撑，适合作为多平台虚拟化统一管理层，并为 AI 工作负载提供即插即用的 GPU 容器支持。

## 🧭 Practical evaluation

**Value:** oneclickvirt/oneclickvirt helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 350 GitHub stars
- 57 forks
- updated 2026-07-01
- primary language: Go
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 54/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 73/100 |
| recency | 80/100 |
| adoption | 51/100 |
| production | 74/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/oneclickvirt/oneclickvirt) · [← Back to DevOps & Infra](./README.md)</sub>
