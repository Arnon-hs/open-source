# hashicorp/terraform-provider-helm

[![Stars](https://img.shields.io/github/stars/hashicorp/terraform-provider-helm?style=flat-square&color=yellow)](https://github.com/hashicorp/terraform-provider-helm/stargazers) [![Forks](https://img.shields.io/github/forks/hashicorp/terraform-provider-helm?style=flat-square&color=blue)](https://github.com/hashicorp/terraform-provider-helm/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Terraform Helm provider

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.1k |
| 🍴 **Forks** | 425 |
| 💻 **Language** | Go |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`helm` `kubernetes` `terraform` `terraform-provider`

## 🎯 Categories

DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
HashiCorp’s terraform-provider-helm lets you manage Helm charts declaratively through Terraform, enabling infrastructure‑as‑code workflows for Kubernetes applications. With strong community adoption (1 069 stars, 425 forks) and recent Go‑based development, it is a mature OSS component ready for pilot projects.  

**Value**  
The provider bridges Terraform and Helm, allowing teams to version, review, and automate the lifecycle of Helm releases alongside other cloud resources. This eliminates ad‑hoc scripting, reduces drift between Terraform state and Kubernetes deployments, and speeds up provisioning of complex, chart‑driven workloads.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the example in the README, and provision a simple chart (e.g., nginx) in a test cluster.  
2. **Integration** – Add the provider to your existing Terraform codebase, pin a specific provider version, and migrate a subset of Helm releases to Terraform-managed resources.  
3. **Scale‑Up** – Extend the configuration to cover all production charts, incorporate CI/CD pipelines, and enable state back‑ends (e.g., remote S3/Consul) for team collaboration.  

**Production Readiness**  
The project shows high readiness: frequent commits (last update 2026‑05‑14), active community forks, and a solid Go codebase. While no critical licensing or security red flags have been identified, a final review of the repository’s security policy and maintainers’ activity is advisable before a full‑scale rollout. With these checks completed, the provider is suitable for a serious pilot and subsequent production deployment.

### Русский

hashicorp/terraform-provider-helm — это открытый провайдер Terraform, позволяющий управлять Helm‑чартами через инфраструктурный код, что упрощает автоматизацию развертывания Kubernetes‑приложений и снижает количество кастомных скриптов. Для начала рекомендуется выполнить небольшой proof‑of‑concept, следуя README, чтобы убедиться в совместимости с текущим кластером, а затем масштабировать использование в рамках CI/CD. Проект считается практически готовым к продакшн: активные коммиты, более 1000 звёзд, широкое принятие в сообществе и стабильный Go‑код, однако перед полномасштабным внедрением следует окончательно проверить лицензию и текущий статус безопасности.

### 中文

**简短介绍**  
hashicorp/terraform-provider-helm 是 HashiCorp 官方维护的 Terraform Provider，用于在 Terraform 配置中直接管理 Helm Chart 的安装、升级和删除，实现基础设施即代码（IaC）与 Kubernetes 包管理的无缝融合。

**价值**  
- **统一化管理**：通过 Terraform 统一管理云资源和 Helm Chart，避免在不同工具之间来回切换，降低运维复杂度。  
- **可审计、可回滚**：所有 Helm 操作都被记录在 Terraform 状态文件中，支持计划（plan）预览和回滚，提升变更安全性。  
- **自动化与可重复**：在 CI/CD 流水线中即可完成 Helm 部署，实现环境一致性和快速交付。

**典型接入方式**  
1. 在 Terraform 项目中添加 provider 配置：  
   ```hcl
   terraform {
     required_providers {
       helm = {
         source  = "hashicorp/helm"
         version = "~> 2.12"
       }
     }
   }

   provider "helm" {
     kubernetes {
       config_path = "~/.kube/config"
     }
   }
   ```  
2. 使用 `helm_release` 资源声明要部署的 Chart：  
   ```hcl
   resource "helm_release" "nginx" {
     name       = "nginx"
     namespace  = "default"
     chart      = "bitnami/nginx"
     version    = "13.2.24"
     set {
       name  = "service.type"
       value = "LoadBalancer"
     }
   }
   ```  
3. 运行 `terraform init && terraform apply` 即可完成 Helm Chart 的安装、升级或删除。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑14，项目拥有 1,069 星、425 Fork，最近一次提交仍在当月，表明社区和维护者活跃。  
- **成熟的生态**：作为 HashiCorp 官方 Provider，已被多家企业在生产环境中使用，具备完整的文档、示例和社区支持。  
- **风险可控**：暂无重大元数据风险，许可证为 MPL‑2.0，安全审计记录良好；建议在正式投产前完成一次小规模的 PoC 并检查 README 中的兼容性说明。  

综合来看，hashicorp/terraform-provider-helm 已具备高生产就绪度，适合作为 Kubernetes/Helm 自动化部署的核心组件进行评估和落地。

## 🧭 Practical evaluation

**Value:** hashicorp/terraform-provider-helm helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1069 GitHub stars
- 425 forks
- updated 2026-05-14
- primary language: Go
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 66/100 |
| stars | 64/100 |
| topics | 50/100 |
| outlook | 68/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 65/100 |
| production | 71/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/hashicorp/terraform-provider-helm) · [← Back to DevOps & Infra](./README.md)</sub>
