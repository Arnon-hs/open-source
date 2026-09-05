# atilladeniz/Kubeli

[![Stars](https://img.shields.io/github/stars/atilladeniz/Kubeli?style=flat-square&color=yellow)](https://github.com/atilladeniz/Kubeli/stargazers) [![Forks](https://img.shields.io/github/forks/atilladeniz/Kubeli?style=flat-square&color=blue)](https://github.com/atilladeniz/Kubeli/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> A modern Kubernetes GUI management desktop app for macOS & Windows. Multi-cluster support, real-time monitoring, AI assistant, terminal access, and more.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 363 |
| 🍴 **Forks** | 32 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cloud-native` `devops` `k8s` `kubectl` `kubernetes` `kubernetes-dashboard` `kubernetes-monitoring` `kubernetes-ui` `pods`

## 🎯 Categories

Cloud & Storage · Productivity · Frontend · Observability · DevOps/Infra

## 📝 Summary

### English

Here's a brief summary of the project:

Kubeli is an open-source, modern Kubernetes GUI management desktop app that supports multi-cluster management, real-time monitoring, AI assistance, and terminal access. This project offers a valuable proposition by providing AI capability without requiring a custom model stack, making it an ideal choice for prototyping AI features, building workflows, and evaluating model tooling. With its recent activity, adoption, and strong ecosystem signals, Kubeli is production-ready for serious pilots.

**Value:**
Kubeli's primary value proposition lies in its ability to add AI capability without requiring a custom model stack, making it an ideal choice for various use cases such as prototyping AI features, building workflows, and evaluating model tooling.

**Practical Adoption Path:**
To adopt Kubeli, users can start by evaluating its feasibility through a small proof of concept and reviewing the README documentation. This will help them understand the project's functionality, integration requirements, and potential risks. Once they're confident, they can proceed with integrating Kubeli into their existing infrastructure.

**Production Readiness:**
Kubeli is considered production-ready for serious pilots due to its recent activity, adoption, and strong ecosystem signals. With 363 GitHub stars, 32 forks, and an active primary language (Type

### Русский

**Kubeli** — это современное кроссплатформенное десктоп‑приложение (macOS/Windows) для визуального управления Kubernetes‑кластерами с поддержкой мультикластеров, мониторинга в реальном времени, AI‑ассистента и встроенного терминала. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept: подключить существующие кластеры, протестировать AI‑функциональность (например, RAG‑агенты) и оценить интеграцию через README, после чего расширять использование в продакшн‑процессы. Проект считается готовым к production‑pilot: активные коммиты, 363 звезды, TypeScript‑база и сильные сигналы экосистемы, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
Kubeli（atilladeniz/Kubeli）是一款面向 macOS 与 Windows 的现代化 Kubernetes 桌面管理 GUI，支持多集群、实时监控、AI 助手、内置终端等功能，让运维和开发者能够在本地以可视化方式高效管理 K8s 环境。

**价值主张**  
- **AI 能力即插即用**：内置 AI 助手，可直接在 UI 中查询集群状态、生成 kubectl 命令或提供故障排查建议，无需自行搭建模型堆栈。  
- **全链路可观测**：实时监控、日志、指标一体化展示，帮助快速定位性能瓶颈。  
- **跨平台与多集群**：一次安装即可在 macOS 与 Windows 上使用，轻松切换和管理多个集群，提升团队协作效率。

**典型接入方式**  
1. **快速试用**：从 GitHub Release 下载对应平台的二进制安装包，运行后通过 UI 添加 kubeconfig 即可连接集群。  
2. **CI/CD 与自研插件**：项目提供 `kubeli-cli` 与插件机制，开发者可在脚本或自定义插件中调用其 API，实现自动化部署或与内部工具链的深度集成。  
3. **AI 功能实验**：在设置页启用 AI 助手，配置 OpenAI/Claude 等模型的 API Key，即可在 UI 中直接使用自然语言交互，实现原型 RAG、Agent 工作流或模型评估。

**生产可用性**  
- **活跃度**：截至 2026‑07‑05 最近一次提交，仓库拥有 363 星、32 Fork，社区活跃，具备持续维护的迹象。  
- **技术成熟度**：使用 TypeScript 开发，代码结构清晰，已覆盖常用的集群管理与监控场景，适合作为内部运维工具的正式入口。  
- **风险与注意事项**：仍需对许可证（MIT）进行合规确认；建议在生产环境前进行安全审计（依赖的 Electron 与 Node 包），并通过小范围 PoC（如单集群、只启用监控）验证兼容性。  
- **总体评估**：在完成上述安全与合规检查后，Kubeli 可视为 OSS 级别的高可用候选，适合在正式业务中推广使用。

## 🧭 Practical evaluation

**Value:** atilladeniz/Kubeli helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 363 GitHub stars
- 32 forks
- updated 2026-07-05
- primary language: TypeScript
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 38/100 |
| stars | 55/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 50/100 |
| production | 71/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/atilladeniz/Kubeli) · [← Back to Cloud--storage](./README.md)</sub>
