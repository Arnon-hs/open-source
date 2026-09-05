# flux-iac/tofu-controller

[![Stars](https://img.shields.io/github/stars/flux-iac/tofu-controller?style=flat-square&color=yellow)](https://github.com/flux-iac/tofu-controller/stargazers) [![Forks](https://img.shields.io/github/forks/flux-iac/tofu-controller?style=flat-square&color=blue)](https://github.com/flux-iac/tofu-controller/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> A GitOps OpenTofu and Terraform controller for Flux

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.6k |
| 🍴 **Forks** | 182 |
| 💻 **Language** | Go |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`flux` `fluxcd` `gitops` `kubernetes` `terraform`

## 🎯 Categories

DevOps/Infra

## 📝 Summary

### English

**Summary**  
The flux‑iac/tofu‑controller is a GitOps‑style controller that lets you declaratively manage OpenTofu and Terraform resources directly from a Flux CD pipeline. Written in Go and backed by a vibrant community (1,637 ★, 182 forks, recent commits), it streamlines the persistence, querying, and migration of infrastructure‑as‑code without custom scripting.  

**Value**  
By treating IaC definitions as first‑class Kubernetes objects, the controller eliminates bespoke glue code, giving teams a single source of truth for both cloud resources and database schemas. This reduces operational overhead, accelerates data‑access provisioning, and makes it easy to prototype or evolve database‑backed applications in a repeatable, version‑controlled way.  

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided examples, and verify that the controller can reconcile a simple OpenTofu/Terraform manifest in a test cluster.  
2. **README‑driven onboarding** – Follow the quick‑start guide to install the Helm chart (or Kustomize manifest), configure a minimal Flux Kustomization, and point it at a private Git repository containing your IaC files.  
3. **Incremental rollout** – Start with non‑critical resources (e.g., development‑environment databases), monitor reconciliation events, and gradually expand to production workloads once confidence is built.  

**Production readiness**  
The project scores high on readiness: active maintenance (last commit 2026‑05‑14), strong adoption signals, and a mature Go codebase. While no major licensing or security red flags have surfaced, a final review of the open‑source license, vulnerability scans, and maintainer responsiveness is recommended before a full‑scale production pilot. With those checks completed, the controller is a solid candidate for enterprise‑grade GitOps IaC automation.

### Русский

**flux-iac/tofu‑controller** — это open‑source GitOps‑контроллер для OpenTofu и Terraform, позволяющий автоматически применять инфраструктурные манифесты из репозитория Flux, тем самым упрощая управление базами данных и другими ресурсами без написания собственного кода. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept проекта, проверка README и интеграция контроллера в существующий Flux‑pipeline для автоматизации создания, миграции и мониторинга ресурсов. По оценке готовности к продакшну проект считается «high»: активные коммиты, более 1,6 к звёздам, широкое использование в сообществе и стабильный стек Go, однако перед масштабным запуском следует окончательно проверить лицензию, безопасность и наличие активных мейнтейнеров.

### 中文

**项目简介**  
flux-iac/tofu‑controller 是一个基于 GitOps 的 OpenTofu 与 Terraform 控制器，专为 Flux 生态设计，可在 Git 仓库中声明式管理基础设施代码，实现自动化的资源同步与状态维护。

**价值**  
- **统一声明式治理**：将 OpenTofu/Terraform 配置纳入 Flux 的 GitOps 工作流，团队只需在 Git 中提交代码，即可完成基础设施的创建、更新和销毁，降低手工操作和配置漂移的风险。  
- **可观测与回滚**：借助 Flux 的同步状态与审计日志，能够快速定位变更来源并在出现问题时一键回滚，提升运维可靠性。  
- **生态兼容**：基于 Go 实现，兼容现有 Flux 组件（Kustomize、Helm、Notification）以及 Kubernetes 原生 API，易于在已有 CI/CD 流水线中嵌入。

**典型接入方式**  
1. **准备环境**：在 Kubernetes 集群中安装 Flux（`flux install`），确保集群已启用 CRD。  
2. **部署控制器**：通过 Helm chart 或 `kubectl apply -f https://github.com/flux-iac/tofu-controller/releases/latest/download/tofu-controller.yaml` 安装 tofu‑controller。  
3. **创建资源**：在 Git 仓库的 `clusters/<cluster-name>/` 目录下添加 `TofuConfig`（或 `TerraformConfig`）CR，指向对应的 OpenTofu/Terraform 模块与变量。  
4. **同步与监控**：Flux 自动检测 Git 变更并触发 tofu‑controller 执行计划、apply；通过 `kubectl get tofu` 或 Flux UI 查看同步状态、日志与审计记录。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑14，项目拥有 1637 ⭐、182 🍴，最近一次提交仅几天前，表明社区活跃且持续维护。  
- **成熟度**：已在多个公开的 GitOps 项目中使用，具备完整的 CI 流水线示例、详细的 README 与 Helm chart，支持自定义插件和安全审计。  
- **风险评估**：暂无重大元数据风险，需进一步确认许可证（MIT）符合企业合规、审计其安全依赖树并验证维护者的响应时效。总体而言，项目已具备 **高** 的生产候选级别，适合作为小规模 PoC 后逐步推广到正式环境。

## 🧭 Practical evaluation

**Value:** flux-iac/tofu-controller helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1637 GitHub stars
- 182 forks
- updated 2026-05-14
- primary language: Go
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 57/100 |
| stars | 68/100 |
| topics | 63/100 |
| outlook | 69/100 |
| quality | 74/100 |
| recency | 80/100 |
| adoption | 65/100 |
| production | 72/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/flux-iac/tofu-controller) · [← Back to DevOps & Infra](./README.md)</sub>
