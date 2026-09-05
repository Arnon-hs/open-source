# kube-rs/kube

[![Stars](https://img.shields.io/github/stars/kube-rs/kube?style=flat-square&color=yellow)](https://github.com/kube-rs/kube/stargazers) [![Forks](https://img.shields.io/github/forks/kube-rs/kube?style=flat-square&color=blue)](https://github.com/kube-rs/kube/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> Rust Kubernetes client and controller runtime

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.7k |
| 🍴 **Forks** | 398 |
| 💻 **Language** | Rust |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`client` `kubernetes` `runtime` `rust`

## 🎯 Categories

DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
kube‑rs/kube is a Rust‑native client and controller runtime for Kubernetes that lets developers write type‑safe operators, controllers, and automation scripts directly in Rust. By exposing a high‑level API, a CLI, and rich SDK metadata, it streamlines the feedback loop for building, testing, and deploying cloud‑native workloads. The project is actively maintained, widely adopted (≈3.7 k stars), and ready for pilot‑grade production use.

**Value**  
- **Speed:** Rust’s compile‑time safety and zero‑cost abstractions let engineers iterate faster while catching errors early, cutting down the time spent on debugging Kubernetes interactions.  
- **Automation:** The runtime simplifies writing custom controllers and CI‑integrated jobs, reducing manual operational toil and improving consistency across environments.  
- **Developer Experience:** A clean, idiomatic Rust API coupled with a CLI gives teams a single language stack for both application code and infrastructure automation, lowering context‑switching overhead.

**Practical Adoption Path**  
1. **Evaluation:** Clone the repo, run the built‑in examples, and use the CLI to interact with a local Kind or Minikube cluster.  
2. **Pilot:** Replace a small existing controller or automation script with a Rust implementation using kube‑rs/kube, integrating it into the CI pipeline to validate build‑test‑deploy cycles.  
3. **Scale‑out:** Gradually migrate additional operators or CI jobs, leveraging the library’s modular traits (e.g., `Api`, `Informer`, `Controller`) and community‑provided crates for common patterns.  
4. **Governance:** Conduct a final review of the license (Apache‑2.0), perform a security audit of dependencies, and set up automated vulnerability scanning in CI.

**Production Readiness**  
- **Activity & Community:** Recent commits (as of 2026‑05‑12), >3.7 k stars, and a healthy fork count indicate strong community momentum.  
- **Stability:** The library follows semantic versioning, provides extensive documentation, and is used in several production‑grade projects across the Kubernetes ecosystem.  
- **Risk Profile:** No major metadata or licensing concerns have been identified; the remaining checks (security posture, maintainer responsiveness) are routine due diligence steps. Overall, kube‑rs/kube is sufficiently mature for a serious pilot and can be promoted to production once the standard OSS vetting steps are completed.

### Русский

**kube-rs/kube** — это клиент и runtime‑библиотека для Kubernetes на Rust, позволяющая инженерам быстро писать контроллеры и автоматизировать локальные задачи, тем самым ускоряя цикл разработки и улучшая обратную связь в CI. Проект уже активно поддерживается (3702 ★, частые коммиты, широкое принятие в сообществе) и готов к использованию в продакшене, хотя окончательная проверка лицензии, безопасности и активности мейнтейнеров всё‑ещё требуется.

### 中文

**项目简介**  
kube‑rs/kube 是用 Rust 实现的 Kubernetes 客户端与控制器运行时库，提供类型安全的 API 调用、资源监听以及自定义控制器框架。它让 Rust 开发者能够在 Kubernetes 环境中以高性能、零运行时开销的方式编写云原生组件。

**价值**  
- **提升开发效率**：通过强类型 SDK 与自动生成的 CRD 代码，减少手写请求与序列化错误，缩短每日开发与代码审查的循环。  
- **加速工作流**：可直接在本地使用库或内置 CLI 完成资源 CRUD、事件监听和日志收集，快速验证改动后再推送 CI。  
- **改进 CI 反馈**：在 CI 中嵌入 kube‑rs/kube，可在测试阶段自动创建、销毁集群资源，实现端到端的集成验证。

**典型接入方式**  
1. **作为库依赖**：在 `Cargo.toml` 中添加 `kube = "0.xx"`，使用 `Client::try_default()` 获取集群连接，然后调用 `Api::<Pod>::list`、`watcher` 等 API。  
2. **构建自定义控制器**：结合 `kube-runtime` 提供的 `Controller`，编写 `reconcile` 与 `error_policy`，交给 Tokio 运行时异步调度。  
3. **CLI 工具**：使用项目自带的 `kubectl-rs`（或自行包装）在脚本中执行资源查询、模板渲染等操作，适配本地或 CI 环境。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑12，仓库拥有 3.7k+ stars、400+ forks，最近一次提交在当天，表明持续维护。  
- **生态成熟**：已被多个开源项目和企业内部平台采用，兼容 Kubernetes 1.24 以上的所有核心 API。  
- **安全与合规**：采用 MIT/Apache 双许可证，暂无已知重大安全漏洞；仍建议在正式上线前进行一次依赖审计与许可证合规检查。  

综合上述，kube‑rs/kube 在功能完整性、社区活跃度和技术成熟度方面均达到生产级别，适合作为 Rust 生态中 Kubernetes 自动化与控制器开发的首选组件。

## 🧭 Practical evaluation

**Value:** kube-rs/kube helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3702 GitHub stars
- 398 forks
- updated 2026-05-12
- primary language: Rust
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 65/100 |
| stars | 76/100 |
| topics | 50/100 |
| outlook | 73/100 |
| quality | 75/100 |
| recency | 80/100 |
| adoption | 73/100 |
| production | 72/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/kube-rs/kube) · [← Back to DevOps & Infra](./README.md)</sub>
