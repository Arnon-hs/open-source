# tailscale/terraform-provider-tailscale

[![Stars](https://img.shields.io/github/stars/tailscale/terraform-provider-tailscale?style=flat-square&color=yellow)](https://github.com/tailscale/terraform-provider-tailscale/stargazers) [![Forks](https://img.shields.io/github/forks/tailscale/terraform-provider-tailscale?style=flat-square&color=blue)](https://github.com/tailscale/terraform-provider-tailscale/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> Terraform provider for Tailscale

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 353 |
| 🍴 **Forks** | 64 |
| 💻 **Language** | Go |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`tailscale` `terraform-provider`

## 🎯 Categories

DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The *tailscale/terraform-provider-tailscale* project supplies a Terraform provider that lets you manage Tailscale resources (ACLs, devices, routes, etc.) directly from IaC code. Written in Go and actively maintained (last update 2026‑05‑11), it has gathered modest community interest (≈ 350 ★, 64 forks). While it isn’t a turnkey AI solution, it enables you to embed Tailscale networking into AI‑centric pipelines (e.g., RAG or agent workflows) without building a custom integration from scratch.

**Value**  
- **Rapid networking integration** – Provision and update Tailscale ACLs, auth‑keys, and devices declaratively, letting AI‑driven services spin up secure, private networks on demand.  
- **Consistent IaC workflow** – Leverages existing Terraform tooling and state management, reducing context‑switching for DevOps and data‑science teams.  
- **Lower operational overhead** – Avoids hand‑crafted API calls or custom scripts, cutting the risk of drift between code and actual Tailscale configuration.

**Practical Adoption Path**  
1. **Pilot** – Add the provider to a sandbox Terraform workspace, configure a minimal set of resources (e.g., a single ACL and auth‑key) and run `terraform plan/apply`.  
2. **CI/CD integration** – Include the provider in your pipeline (GitHub Actions, GitLab CI, etc.) to automatically provision Tailscale networks for AI model containers or inference endpoints.  
3. **Policy & security review** – Verify the generated ACLs align with your organization’s zero‑trust policies; add required `depends_on` relationships to ensure ordering with other resources (e.g., cloud VMs).  
4. **Scale** – Extend the configuration to cover multi‑tenant ACLs, device tags, and route advertisements as your AI workloads grow.

**Production Readiness**  
- **Maturity**: Medium. The provider is up‑to‑date and functional, but the surrounding ecosystem (e.g., official Tailscale Terraform docs) is still thin, so manual validation of generated configurations is recommended.  
- **Dependencies**: Relies on the Tailscale API and a Go runtime; ensure the API version used matches your Tailscale account settings.  
- **Maintenance**: Monitor the repository for new releases and security advisories; consider pinning a specific provider version in production to avoid breaking changes.  
- **Risk**: No glaring licensing or security red flags, but a final review of the maintainer activity and any open CVEs is advisable before full production deployment.  

In short, the provider is a solid building block for integrating Tailscale networking into AI‑focused infrastructure, suitable for prototypes and internal services, with a straightforward path to production once you perform the usual IaC validation and dependency checks.

### Русский

**tailscale/terraform-provider-tailscale** — это открытый Terraform‑провайдер, позволяющий управлять ресурсами Tailscale через инфраструктурный код. Он удобен для быстрого прототипирования AI‑сервисов, построения RAG‑или агентных воркфлоу и интеграции сетевых политик в CI/CD‑пайплайны, однако перед внедрением требуется ручная проверка конфигураций из‑за ограниченной метаданных‑интеграции. Готовность к продакшну — средняя: проект стабилен и активно поддерживается (353★, обновлён 2026‑05‑11), но перед масштабным использованием следует оценить лицензирование, безопасность и нагрузку на зависимости.

### 中文

**项目简介**  
`tailscale/terraform-provider-tailscale` 是一款官方 Terraform Provider，用于在 Terraform 配置中直接管理 Tailscale 网络、ACL、设备和共享路由等资源，实现基础设施即代码（IaC）对 Tailscale 的完整编排。

**价值**  
- **统一化管理**：把 Tailscale 的网络拓扑、访问控制列表（ACL）和设备注册等操作纳入 Terraform，配合已有的云资源实现统一的声明式管理。  
- **可重复、可审计**：所有网络配置都以代码形式保存，支持版本控制、审计和 CI/CD 自动化部署，减少手工操作导致的错误。  
- **加速原型与内部工具**：在内部研发或原型项目中快速搭建安全的点对点网络，配合 AI/ML 工作流（如 RAG、Agent）时无需额外手动配置 VPN。

**典型接入方式**  
1. **在 Terraform 项目中声明 Provider**  
   ```hcl
   terraform {
     required_providers {
       tailscale = {
         source  = "tailscale/tailscale"
         version = "~> 0.15"
       }
     }
   }

   provider "tailscale" {
     api_key = var.tailscale_api_key   # 或者使用 TAILSCALE_API_KEY 环境变量
   }
   ```
2. **使用资源定义网络、ACL、设备等**  
   ```hcl
   resource "tailscale_acl" "example" {
     acl = <<-EOT
       {
         "ACLs": [
           {
             "Action": "accept",
             "Users": ["*"],
             "Ports": ["*:22"]
           }
         ]
       }
     EOT
   }

   resource "tailscale_device" "server" {
     hostname = "my-server"
     tags     = ["tag:prod"]
   }
   ```
3. **在 CI/CD 流水线中执行 `terraform init/apply`**，实现自动化部署与变更审计。

**生产可用性**  
- **成熟度**：GitHub ★353、Forks 64，最近一次更新在 2026‑05‑11，活跃度尚可。  
- **适用场景**：适合内部工具、原型项目以及对网络安全有统一管理需求的中小规模生产环境。  
- **风险与注意事项**：  
  - 仍需自行审查 Provider 的安全更新和许可证合规性。  
  - 在大规模多租户环境或对高可用性有严格要求时，建议进行额外的容错和监控测试。  
  - 依赖 Tailscale API，确保 API Key 的安全存储与轮换机制。

总体而言，`tailscale/terraform-provider-tailscale` 在 **“中等”** 生产准备度下，可放心用于内部或中等规模的生产环境，但在正式上线前应完成依赖审计、权限最小化和灾备演练。

## 🧭 Practical evaluation

**Value:** tailscale/terraform-provider-tailscale helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 353 GitHub stars
- 64 forks
- updated 2026-05-11
- primary language: Go
- 2 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 54/100 |
| topics | 25/100 |
| outlook | 62/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 52/100 |
| production | 65/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/tailscale/terraform-provider-tailscale) · [← Back to DevOps & Infra](./README.md)</sub>
