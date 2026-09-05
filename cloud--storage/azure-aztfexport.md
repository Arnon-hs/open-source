# Azure/aztfexport

[![Stars](https://img.shields.io/github/stars/Azure/aztfexport?style=flat-square&color=yellow)](https://github.com/Azure/aztfexport/stargazers) [![Forks](https://img.shields.io/github/forks/Azure/aztfexport?style=flat-square&color=blue)](https://github.com/Azure/aztfexport/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> A tool to bring existing Azure resources under Terraform's management

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.9k |
| 🍴 **Forks** | 217 |
| 💻 **Language** | Go |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`azure` `devops` `iac` `terraform` `terraform-azurerm` `tool`

## 🎯 Categories

Cloud & Storage · DevOps/Infra

## 📝 Summary

### English

**Summary (2‑3 sentences)**  
Azure/aztfexport is an open‑source Go utility that scans existing Azure subscriptions and generates Terraform configuration and state files, allowing teams to bring already‑provisioned resources under Terraform management without manual recreation. With strong community traction (≈1.9 k stars, 217 forks) and recent activity, it offers a low‑friction path to standardize IaC across Azure workloads.

**Value**  
By automating the export of Azure resources to Terraform, the tool eliminates the time‑consuming, error‑prone “re‑write‑from‑scratch” process, enabling faster onboarding of legacy assets, consistent version‑controlled infrastructure, and easier integration with CI/CD pipelines. This reduces custom scripting overhead and accelerates the prototyping of database‑backed applications that rely on stable, reproducible cloud resources.

**Practical adoption path**  
1. **Proof‑of‑concept** – Run `aztfexport` against a non‑critical resource group to generate Terraform files and verify that the output matches expectations.  
2. **README validation** – Follow the provided usage guide, adjust any provider or backend settings, and perform a `terraform plan` to confirm drift detection works.  
3. **Pilot** – Select a small production workload, import the generated state into a version‑controlled repo, and integrate with existing CI pipelines for automated plan/apply cycles.  
4. **Scale** – Incrementally expand to additional subscriptions or resource groups, using the same workflow to keep the Terraform codebase in sync.

**Production readiness**  
The project scores high on production readiness: it has recent commits (as of 2026‑06‑26), active community contributions, and a mature Go codebase. While no major metadata risks have been identified, a final review of the license (MIT/Apache‑compatible) and a security audit of the generated Terraform manifests are recommended before full‑scale deployment. Overall, Azure/aztfexport is a solid OSS candidate for pilots and can be promoted to production once the brief compliance checks are completed.

### Русский

**Azure/aztfexport** — это open‑source утилита на Go, позволяющая автоматически импортировать уже существующие ресурсы Azure в Terraform, что упрощает их дальнейшее управление и инфраструктурный код. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept, проверка README и генерация Terraform‑файлов для выбранных ресурсов, после чего можно масштабировать процесс на всю среду. По показателям активности (1894 звёзд, 217 форков, обновления до 2026‑06‑26) и поддержке сообщества проект считается готовым к использованию в продакшене, хотя окончательная проверка лицензии и безопасности всё же рекомендуется.

### 中文

**项目简介**  
Azure/aztfexport 是一款开源工具，可自动将已存在的 Azure 资源导出为 Terraform 配置，使其快速纳入 Terraform 的 IaC（Infrastructure as Code）管理流程。

**价值**  
- **统一管理**：把手动创建的 Azure 资源“一键”转为 Terraform 代码，避免资源漂移，提升运维一致性。  
- **降低成本**：无需自行编写导出脚本或维护大量自定义迁移代码，节省开发与运维工时。  
- **加速交付**：生成的 HCL 文件即可以直接用于 Terraform plan/apply，快速实现资源的版本化、审计和回滚。

**典型接入方式**  
1. **准备环境**：在 CI/CD 机器或本地工作站上安装 Go（或直接使用已发布的二进制）。  
2. **授权**：为 azftexport 配置 Azure Service Principal（或使用 Azure CLI 登录），确保拥有目标订阅的只读权限。  
3. **执行导出**：`aztfexport --resource-group <rg> --output ./tfconfig`，工具会遍历资源组并生成对应的 `.tf` 与 `.tfstate` 文件。  
4. **验证 & 合并**：在生成的 Terraform 项目中运行 `terraform init && terraform plan`，确认无差异后提交到代码库。  
5. **渐进式落地**：先在一个小型资源组或单个关键资源上做 PoC，验证导出结果与现有 Terraform 模块的兼容性，再逐步扩大至全订阅。

**生产可用性**  
- **活跃度**：截至 2026‑06‑26，项目仍在持续更新，拥有 1,894 ★、217 Fork，最近一次提交仅数天前。  
- **生态兼容**：使用 Go 编写，输出标准 HCL，天然兼容 Terraform 0.13 以上版本，且已有社区案例在生产环境中使用。  
- **风险评估**：暂无重大元数据或许可证风险，但建议在正式投产前完成安全审计（依赖的 Go 包、Azure 权限最小化）并确认维护者的响应速度。  
- **结论**：在经过小规模验证后，Azure/aztfexport 完全可以作为正式生产环境的资源迁移与统一管理工具投入使用。

## 🧭 Practical evaluation

**Value:** Azure/aztfexport helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1894 GitHub stars
- 217 forks
- updated 2026-06-26
- primary language: Go
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 58/100 |
| stars | 70/100 |
| topics | 75/100 |
| outlook | 74/100 |
| quality | 76/100 |
| recency | 80/100 |
| adoption | 67/100 |
| production | 70/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/Azure/aztfexport) · [← Back to Cloud--storage](./README.md)</sub>
