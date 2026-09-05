# cisco-open/forge

[![Stars](https://img.shields.io/github/stars/cisco-open/forge?style=flat-square&color=yellow)](https://github.com/cisco-open/forge/stargazers) [![Forks](https://img.shields.io/github/forks/cisco-open/forge?style=flat-square&color=blue)](https://github.com/cisco-open/forge/network) [![Language](https://img.shields.io/badge/lang-HCL-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> ForgeMT is a secure, scalable GitHub Actions runner platform for ephemeral workloads. Designed for multi-tenant environments, it automates isolated runner provisioning on Kubernetes or EC2, with built-in OIDC, IAM, cost optimization, and deep observability.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 208 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | HCL |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`actions-runner-controller` `automation` `aws` `aws-eks` `ci` `ci-cd` `devops` `devsecops` `ec2` `ephemeral` `github-actions` `infrastructure-as-code`

## 🎯 Categories

Automation · Cloud & Storage · Observability · DevOps/Infra · Security

## 📝 Summary

### English

**Brief Summary**  
ForgeMT (cisco-open/forge) is an open‑source platform that automates the provisioning of secure, isolated GitHub Actions runners for transient workloads. It supports multi‑tenant deployments on Kubernetes or EC2, adds native OIDC/IAM integration, cost‑optimisation controls, and extensive observability out‑of‑the‑box.

**Value**  
- **Eliminates repetitive runner‑setup tasks** – developers no longer need to manually spin up, configure, and tear down runners for each CI/CD job.  
- **Security‑by‑design** – each runner runs in its own isolated environment with AWS IAM/OIDC credentials, reducing the attack surface for multi‑tenant use cases.  
- **Cost efficiency** – runners are provisioned only when needed and automatically terminated, preventing idle compute spend.  
- **Observability** – built‑in metrics and logs give teams insight into runner utilisation, failures, and performance bottlenecks.

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC)** – clone the repo, follow the README to spin up a minimal ForgeMT instance on a test Kubernetes cluster or a single EC2 node. Verify that a simple GitHub Actions workflow can request a runner and that the runner is created, used, and destroyed automatically.  
2. **Integration & Customisation** – map your existing CI/CD pipelines to ForgeMT’s runner‑request API, configure tenant‑specific IAM roles, and enable the observability stack (Prometheus/Grafana or CloudWatch).  
3. **Pilot Deployment** – roll out the service to a small team or a subset of repositories, monitor cost and latency, and iterate on resource‑quota policies.  
4. **Full Rollout** – after confirming stability, security posture, and cost‑savings, scale the deployment across all required clusters/regions and integrate with your internal tooling (e.g., ticketing, secret management).

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last update 2026‑06‑22) and has modest community traction (208 ⭐, 8 forks).  
- **Strengths**: Strong security features, multi‑tenant design, and good observability support make it suitable for internal or prototype‑level production workloads.  
- **Caveats**: Before production use, perform a thorough review of the license, conduct a security audit of the underlying HCL/Terraform modules, and verify that the maintainers can respond to issues. Additionally, evaluate dependency health (e.g., Kubernetes version compatibility, AWS SDK updates) and establish monitoring for the controller components.  

With those checks in place, ForgeMT can be a reliable foundation for automated, cost‑effective CI/CD runner provisioning in medium‑to‑large organisations.

### Русский

ForgeMT — это открытая платформа для безопасного и масштабируемого запуска GitHub Actions‑раннеров в эпемерных средах (Kubernetes или EC2). Она автоматизирует изолированное provision‑инг раннеров в мульти‑тенантных инфраструктурах, предоставляя OIDC/IAM‑интеграцию, оптимизацию затрат и глубокую наблюдаемость, что позволяет избавиться от ручных операций и построить повторяемые рабочие потоки. Готовность к продакшну — уровень Medium: проект подходит для прототипов и внутренних задач, но перед запуском в продакшн стоит проверить лицензирование, актуальность безопасности и наличие активных мейнтейнеров.

### 中文

**项目简介**  
ForgeMT（cisco-open/forge）是一个面向多租户环境的安全、可弹性扩展的 GitHub Actions Runner 平台。它能够在 Kubernetes 或 EC2 上自动化创建隔离的短暂 Runner，内置 OIDC、IAM 权限管理、成本优化和深度可观测性。

**价值**  
- **消除手工重复**：自动化 Runner 的创建、销毁和权限配置，免去运维人员在 CI/CD 流程中频繁的手动操作。  
- **安全合规**：通过 OIDC 与云原生 IAM 集成，实现最小权限原则和审计追踪。  
- **成本控制**：按需启动短暂 Runner，使用完即销毁，配合成本监控可显著降低云资源开支。  
- **可观测**：提供统一的日志、指标和追踪，帮助团队快速定位构建问题。

**典型接入方式**  
1. **准备工作**：在目标 Kubernetes 集群或 AWS 环境中配置好网络、IAM 角色以及 OIDC 提供者。  
2. **部署 ForgeMT**：使用官方提供的 Helm chart（K8s）或 Terraform 模块（EC2）进行一键部署。  
3. **GitHub 关联**：在 GitHub 仓库的 Settings → Actions → Runners 中添加对应的自托管 Runner，填写生成的注册令牌或使用 OIDC 自动注册。  
4. **验证 & 试运行**：提交一次工作流，确认 Runner 能被自动调度、执行并在完成后自动回收。  

**生产可用性**  
- **成熟度**：当前得分 67/100，适合作为原型或内部业务流程的自动化工具。  
- **依赖与维护**：项目活跃度一般（208 星，8 Fork，最近更新于 2026‑06‑22），但仍需自行评估其依赖库的安全性与长期维护计划。  
- **上线建议**：先在小范围（例如单个团队或特定 CI 流）进行 PoC，验证与现有 CI/CD、IAM、监控体系的兼容性后，再逐步推广至生产环境。  

总体而言，ForgeMT 能显著提升 CI/CD 的自动化程度与安全合规性，适合作为内部或中小规模生产环境的 Runner 解决方案，但在大规模生产部署前建议完成安全审计和运维流程的成熟度评估。

## 🧭 Practical evaluation

**Value:** cisco-open/forge helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 208 GitHub stars
- 8 forks
- updated 2026-06-22
- primary language: HCL
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 49/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 42/100 |
| production | 68/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/cisco-open/forge) · [← Back to Automation](./README.md)</sub>
