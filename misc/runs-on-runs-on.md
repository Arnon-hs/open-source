# runs-on/runs-on

[![Stars](https://img.shields.io/github/stars/runs-on/runs-on?style=flat-square&color=yellow)](https://github.com/runs-on/runs-on/stargazers) [![Forks](https://img.shields.io/github/forks/runs-on/runs-on?style=flat-square&color=blue)](https://github.com/runs-on/runs-on/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> Self-hosted GitHub Actions runners made simple. For AWS. 10x cheaper, 40% faster, and unlimited caching. Best alternative to Actions Runner Controller.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.2k |
| 🍴 **Forks** | 44 |
| 💻 **Language** | Unknown |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`aws` `ci` `cicd` `cloudformation` `continuous-delivery` `continuous-deployment` `continuous-integration` `ec2-spot` `github-actions` `github-runners` `on-premise` `self-hosted`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary**  
Runs‑on (runs‑on/runs‑on) is an open‑source tool that simplifies the deployment of self‑hosted GitHub Actions runners on AWS, delivering up to 10× lower cost, ~40 % faster job execution, and unlimited build‑cache storage. It positions itself as a leaner, faster alternative to the Actions Runner Controller for teams that want to run CI/CD workloads on their own infrastructure.

**Value proposition**  
- **Cost & speed** – By leveraging spot instances and native AWS networking, runs‑on reduces the per‑job expense dramatically while cutting latency compared with the default GitHub‑hosted runners.  
- **Unlimited caching** – Persistent EBS/EFS volumes give you unbounded cache size, which speeds up dependency installation and artifact reuse across workflows.  
- **Simplicity** – A small set of Terraform modules and a CLI handle provisioning, registration, and lifecycle management, so you don’t need to maintain a full Kubernetes‑based controller stack.

**Practical adoption path**  
1. **Pilot** – Clone the repo, run the provided Terraform scripts in a sandbox AWS account, and register a runner with a test repository. Verify that jobs complete faster and at lower cost.  
2. **Integration** – Add the runner’s ARN to your GitHub organization/repo settings, update your workflow files to target the custom runner label, and optionally enable the shared cache volume.  
3. **Scale** – Adjust the Terraform variables (instance type, spot vs. on‑demand, autoscaling thresholds) to match your workload. Use the built‑in health‑check Lambda to automatically replace unhealthy instances.  
4. **Governance** – Incorporate the Terraform state into your IaC pipeline, apply IAM least‑privilege policies, and set up CloudWatch alarms for cost and performance monitoring.

**Production readiness**  
- **Maturity** – 1,181 ★ and recent activity (last update 2026‑05‑12) indicate a healthy community, but the project is still categorized as “medium” readiness.  
- **Risks** – Integration documentation is sparse; you’ll need to manually verify networking (VPC, security groups) and cache persistence. Dependency management (Terraform version, AWS SDK) should be locked down before production rollout.  
- **Recommendation** – Suitable for internal tools, prototypes, or teams that can allocate engineering time to validate the setup and monitor costs. With proper testing and a clear maintenance plan, runs‑on can be promoted to production for most CI/CD workloads.

### Русский

**runs‑on/runs‑on** — это open‑source решение для простого развертывания собственных GitHub Actions runners в AWS, которое снижает затраты в 10 раз, ускоряет выполнение задач ≈ 40 % и предоставляет неограниченный кэш. Типичный сценарий: команда настраивает несколько EC2‑инстансов, подключает их к репозиторию и использует кэш для ускорения сборок и тестов, получая при этом полный контроль над инфраструктурой. Проект имеет среднюю готовность к production: достаточное количество звёзд и активные обновления делают его пригодным для прототипов и внутренних пайплайнов, но перед масштабным внедрением требуется проверить интеграцию и оценить затраты на поддержку.

### 中文

**项目简介**  
runs‑on/runs‑on 为 AWS 环境提供了极简化的 Self‑hosted GitHub Actions Runner。相较于官方 Runner，成本降低约 10 倍、执行速度提升约 40%，并且支持无限制缓存，是 Actions Runner Controller 的高性价比替代方案。  

**价值**  
- **成本优势**：利用按需 EC2 实例或 Spot 实例，运行费用远低于 GitHub 托管的 Runner。  
- **性能提升**：在同一 VPC 内部署，可直接访问私有网络资源，避免跨域网络延迟，实现约 40% 的作业加速。  
- **无限缓存**：通过 EFS/EBS 实现持久化缓存，显著缩短依赖下载与编译时间。  
- **运维简化**：提供 Terraform/CloudFormation 模块和 CLI，一键创建、扩容、销毁，无需自行维护底层实例。  

**典型接入方式**  
1. **准备基础设施**：在 AWS 上使用提供的 Terraform 模块创建 VPC、子网、IAM 角色以及用于 Runner 的 EC2（或 Auto Scaling Group）。  
2. **部署 Runner**：运行 `runs-on install` CLI，自动在实例上安装并注册 GitHub Runner，支持自定义标签（如 `linux-x86`, `gpu`）。  
3. **配置工作流**：在 `.github/workflows/*.yml` 中通过 `runs-on: self-hosted` 并添加对应标签，即可把作业调度到自建 Runner。  
4. **缓存使用**：在工作流中使用标准的 `actions/cache`，缓存目录会自动映射到共享的 EFS，实现跨实例复用。  

**生产可用性**  
- **成熟度**：项目已有 1,181 颗星、44 个 Fork，近期（2026‑05‑12）仍在维护，社区活跃度中等。  
- **适用场景**：适合内部工具、原型开发以及对成本/速度有明确要求的团队；在生产环境使用前建议进行以下检查：  
  - **依赖审计**：确认所使用的 EC2 镜像、IAM 权限与组织安全策略兼容。  
  - **运维流程**：建立实例更新、日志收集（CloudWatch）和故障自动恢复（ASG）机制。  
  - **集成验证**：由于元数据中缺少完整的集成指引，需在小范围内进行手动验证，确保 CI/CD 流水线能够正确发现并使用自建 Runner。  
- **风险**：集成路径不够透明，初始部署需要一定的手动调试；一旦确认设置成本可接受，系统在中等规模（数十台实例）下已可稳定运行。  

综上，runs‑on/runs‑on 为需要在 AWS 上自建 GitHub Actions Runner 的团队提供了低成本、高性能、易扩展的解决方案，适合作为原型或内部 CI/CD 环境的首选；在完成依赖审查和运维自动化后，也可平滑迁移至生产环境。

## 🧭 Practical evaluation

**Value:** runs-on/runs-on helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1181 GitHub stars
- 44 forks
- updated 2026-05-12
- 13 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 65/100 |
| topics | 100/100 |
| outlook | 56/100 |
| quality | 61/100 |
| recency | 20/100 |
| adoption | 59/100 |
| production | 48/100 |
| usefulness | 74/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/runs-on/runs-on) · [← Back to Misc](./README.md)</sub>
