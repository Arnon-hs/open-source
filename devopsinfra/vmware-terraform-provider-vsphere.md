# vmware/terraform-provider-vsphere

[![Stars](https://img.shields.io/github/stars/vmware/terraform-provider-vsphere?style=flat-square&color=yellow)](https://github.com/vmware/terraform-provider-vsphere/stargazers) [![Forks](https://img.shields.io/github/forks/vmware/terraform-provider-vsphere?style=flat-square&color=blue)](https://github.com/vmware/terraform-provider-vsphere/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> Terraform Provider for VMware vSphere

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 672 |
| 🍴 **Forks** | 482 |
| 💻 **Language** | Go |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`terraform` `terraform-provider` `vmware` `vmware-vsphere` `vsphere`

## 🎯 Categories

DevOps/Infra

## 📝 Summary

### English

**Summary**  
The *vmware/terraform-provider-vsphere* project is an open‑source Terraform provider that enables teams to declaratively provision, configure, and manage VMware vSphere resources. With over 600 GitHub stars, frequent updates (last 2026‑06‑30) and a healthy fork count, it is considered production‑ready for serious pilot projects.  

**Value**  
By exposing vSphere APIs as native Terraform resources, the provider eliminates custom scripting and manual plumbing, letting infrastructure‑as‑code pipelines handle VM, network, storage, and datacenter lifecycle consistently and repeatably. This accelerates provisioning, reduces drift, and makes it easy to version‑control and audit vSphere environments.  

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the example configurations in the README, and validate that the provider can authenticate to your vCenter.  
2. **Pilot** – Add the provider to an existing Terraform workspace, start with a small, non‑critical workload (e.g., a single VM or a test network) and store the state in a remote backend.  
3. **Scale** – Gradually migrate more resources (datastores, clusters, tags, etc.) while codifying best‑practice modules and incorporating CI/CD checks.  

**Production readiness**  
The project shows strong signals: active maintenance, recent releases, a sizable community, and mature Go codebase. While no major licensing or security red flags were found, a final review of the Apache‑2.0 license compliance and a scan of disclosed vulnerabilities is recommended before full rollout. With those checks completed, the provider is fit for production use in any VMware‑centric DevOps pipeline.

### Русский

**Краткое резюме:**  
`vmware/terraform-provider-vsphere` — это официальный провайдер Terraform для управления инфраструктурой VMware vSphere, позволяющий автоматически создавать, изменять и удалять ресурсы кластера без написания собственного кода. Типовой сценарий внедрения — запуск небольшого proof‑of‑concept (по примеру README) для управления виртуальными машинами, сетями и хранилищем, а затем масштабирование на полное управление дата‑центром. Провайдер считается готовым к production: активные коммиты, более 600 звёзд, широкое использование в сообществе и стабильная экосистема, хотя окончательная проверка лицензии и вопросов безопасности всё‑ещё требуется.

### 中文

**项目简介**  
vmware/terraform-provider-vsphere 是官方维护的 Terraform Provider，能够让用户使用 Terraform 代码直接管理 VMware vSphere 环境中的计算、网络、存储等资源，实现基础设施即代码（IaC）的全流程自动化。

**价值**  
- **统一管理**：通过 Terraform 的声明式语法，跨团队统一管理 vSphere 资源，降低人为操作错误。  
- **可重复部署**：将 vSphere 环境抽象为代码，可在不同数据中心或测试/生产环境之间快速复制、回滚。  
- **与生态集成**：天然兼容 Terraform 生态（模块、工作流、CI/CD），便于在现有 DevOps 流程中加入 vSphere 管理。

**典型接入方式**  
1. **准备环境**：在本地或 CI 环境中安装 Terraform（≥1.0）和 Go（用于编译 Provider，若直接使用二进制则不必）。  
2. **配置 Provider**：在 `terraform` 配置文件中声明 `vsphere` Provider，提供 vCenter 地址、用户名、密码或使用凭证管理（如 Vault、Environment Variables）。  
   ```hcl
   provider "vsphere" {
     user           = var.vc_user
     password       = var.vc_password
     vsphere_server = var.vc_host
     allow_unverified_ssl = true
   }
   ```
3. **编写资源**：使用官方文档中的资源类型（`vsphere_virtual_machine`、`vsphere_datacenter`、`vsphere_network` 等）描述所需的虚拟机、网络、存储等。  
4. **执行 Terraform**：`terraform init` → `terraform plan` → `terraform apply`，即可在 vSphere 上创建或修改资源。  
5. **CI/CD 集成**：将上述步骤嵌入 Jenkins、GitHub Actions、GitLab CI 等流水线，实现自动化部署和变更审计。

**生产可用性**  
- **活跃度**：截至 2026‑06‑30，项目最近一次提交，星标 672，Fork 482，社区活跃，已发布多个稳定版本。  
- **成熟度**：Provider 已在多个企业级生产环境中使用，官方文档和社区示例丰富，兼容 Terraform 1.x 主流特性。  
- **风险**：暂无重大安全或许可证问题，但建议在正式投产前完成一次小规模的 PoC，审查依赖的 vSphere API 兼容性，并开启审计日志。  

综上，**vmware/terraform-provider-vsphere** 具备高生产就绪度，适合作为企业在 VMware 环境中实现基础设施即代码的核心组件。

## 🧭 Practical evaluation

**Value:** vmware/terraform-provider-vsphere helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 672 GitHub stars
- 482 forks
- updated 2026-06-30
- primary language: Go
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 67/100 |
| stars | 60/100 |
| topics | 63/100 |
| outlook | 54/100 |
| quality | 62/100 |
| recency | 40/100 |
| adoption | 62/100 |
| production | 56/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/vmware/terraform-provider-vsphere) · [← Back to DevOps & Infra](./README.md)</sub>
