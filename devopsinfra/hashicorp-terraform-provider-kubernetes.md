# hashicorp/terraform-provider-kubernetes

[![Stars](https://img.shields.io/github/stars/hashicorp/terraform-provider-kubernetes?style=flat-square&color=yellow)](https://github.com/hashicorp/terraform-provider-kubernetes/stargazers) [![Forks](https://img.shields.io/github/forks/hashicorp/terraform-provider-kubernetes?style=flat-square&color=blue)](https://github.com/hashicorp/terraform-provider-kubernetes/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> Terraform Kubernetes provider

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.7k |
| 🍴 **Forks** | 1k |
| 💻 **Language** | Go |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`kubernetes` `terraform` `terraform-provider`

## 🎯 Categories

DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
The *hashicorp/terraform-provider-kubernetes* is an open‑source Terraform provider that lets you declaratively manage Kubernetes resources (including custom resources) alongside your infrastructure code. With over 1.7 k stars, active maintenance, and recent releases, it is production‑ready for teams that want to treat Kubernetes objects as part of their IaC pipeline.

**Value**  
- **Unified control plane** – Manage clusters, namespaces, deployments, services, CRDs, and other K8s objects from the same Terraform configuration that provisions cloud resources, eliminating ad‑hoc scripts and reducing drift.  
- **Reusable, auditable state** – All changes are stored in Terraform state, giving you version‑controlled, reviewable histories of both infrastructure and application‑level resources.  
- **Accelerated prototyping** – Developers can spin up fully‑configured clusters and associated workloads with a single `terraform apply`, shortening the feedback loop for database‑backed or data‑intensive applications.

**Practical Adoption Path**  
1. **Pilot** – Fork the repo or add the provider to your existing Terraform setup, run `terraform init` and apply a minimal manifest (e.g., a namespace and a ConfigMap) to verify connectivity and RBAC.  
2. **Integration testing** – Extend the pilot to cover the critical resources you manage (Deployments, Services, Ingress, CRDs). Use `terraform plan` in CI to ensure changes are predictable.  
3. **Policy enforcement** – Pair the provider with Sentinel or Open Policy Agent to enforce security and naming conventions before promotion to production.  
4. **Scale‑out** – Gradually migrate legacy `kubectl`/Helm scripts to Terraform modules, leveraging the provider’s ability to import existing resources (`terraform import`).  

**Production Readiness**  
- **High** – The project shows strong activity (last commit 2026‑05‑14), a large community (≈1.7 k stars, >1 k forks), and is written in Go, the language of Terraform core.  
- **Risk considerations** – Perform a final review of the license (MPL‑2.0), run a security scan of the provider binary, and confirm that the maintainers are responsive to issues. Once those checks pass, the provider is suitable for a serious pilot and, subsequently, full production deployment.

### Русский

Hashicorp/terraform-provider-kubernetes — это открытый провайдер Terraform, позволяющий управлять ресурсами Kubernetes через инфраструктурный код, что упрощает автоматизацию развертывания, миграцию и поддержание согласованности кластеров без написания кастомных скриптов. Типичный сценарий внедрения — интеграция провайдера в CI/CD‑конвейер для декларативного создания и обновления объектов (Deployments, Services, ConfigMaps и т.п.) и их синхронизации с другими облачными сервисами. По уровню готовности проект считается «high production ready»: активная поддержка, регулярные обновления (последний коммит — 2026‑05‑14), более 1700 звёзд на GitHub и широкое использование в сообществе, хотя перед запуском в прод необходимо проверить лицензию, безопасность и наличие ответственных мейнтейнеров.

### 中文

**简短介绍**  
HashiCorp 官方维护的 **terraform-provider-kubernetes** 是一款 Terraform Provider，帮助用户在 Terraform 配置中直接管理 Kubernetes 资源，实现基础设施即代码（IaC）对 K8s 集群的完整生命周期管理。

**价值**  
- **统一治理**：通过 Terraform 统一管理云资源和 Kubernetes 对象，避免在不同工具之间切换，降低运维复杂度。  
- **可审计、可回滚**：所有变更都以 Terraform Plan/Apply 的形式记录，支持审计和一键回滚。  
- **加速交付**：在 CI/CD 流程中直接声明式部署 Service、Ingress、ConfigMap 等 K8s 资源，缩短从代码到集群的交付周期。

**典型接入方式**  
1. 在 Terraform 项目根目录的 `required_providers` 中声明 provider：  
   ```hcl
   terraform {
     required_providers {
       kubernetes = {
         source  = "hashicorp/kubernetes"
         version = "~> 2.30"
       }
     }
   }
   ```  
2. 配置访问凭证（常用方式）  
   - **Kubeconfig**：`config_path = "~/.kube/config"`  
   - **直接凭证**：`host`, `client_certificate`, `client_key`, `cluster_ca_certificate` 等字段。  
3. 在 Terraform 配置文件中使用资源块，如 `kubernetes_deployment`, `kubernetes_service`, `kubernetes_ingress` 等，交由 `terraform apply` 完成实际创建/更新。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑14，项目拥有 1708 Stars、1049 Forks，最近一次提交仅数天前，社区活跃且持续迭代。  
- **成熟度**：Provider 已在多个大型企业生产环境中使用，官方文档完善，支持 Terraform 1.x 及以上版本。  
- **风险**：暂无重大安全或许可证风险，但在正式投产前仍建议进行内部安全审计和对维护者活跃度的二次确认。  

总体而言，terraform-provider-kubernetes 已具备高度的生产就绪度，可在正式项目中安全使用，并通过 Terraform 的统一框架提升 DevOps 效率。

## 🧭 Practical evaluation

**Value:** hashicorp/terraform-provider-kubernetes helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1708 GitHub stars
- 1049 forks
- updated 2026-05-14
- primary language: Go
- 3 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 76/100 |
| stars | 69/100 |
| topics | 38/100 |
| outlook | 47/100 |
| quality | 57/100 |
| recency | 20/100 |
| adoption | 71/100 |
| production | 51/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/hashicorp/terraform-provider-kubernetes) · [← Back to DevOps & Infra](./README.md)</sub>
