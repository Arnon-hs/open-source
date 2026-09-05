# terraform-google-modules/terraform-google-gcloud

[![Stars](https://img.shields.io/github/stars/terraform-google-modules/terraform-google-gcloud?style=flat-square&color=yellow)](https://github.com/terraform-google-modules/terraform-google-gcloud/stargazers) [![Forks](https://img.shields.io/github/forks/terraform-google-modules/terraform-google-gcloud?style=flat-square&color=blue)](https://github.com/terraform-google-modules/terraform-google-gcloud/network) [![Language](https://img.shields.io/badge/lang-HCL-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Executes Google Cloud CLI commands within Terraform

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 176 |
| 🍴 **Forks** | 98 |
| 💻 **Language** | HCL |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cft-terraform` `developer-tools`

## 🎯 Categories

Cloud & Storage · DevTools · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The **terraform-google-modules/terraform-google-gcloud** module lets you run Google Cloud CLI (`gcloud`) commands directly from Terraform configurations, streamlining the bridge between infrastructure-as-code and ad‑hoc cloud operations. It is aimed at speeding up daily development, code‑review loops, and CI feedback by automating local engineering tasks that would otherwise require manual CLI invocations. With 176 ⭐ on GitHub and recent updates (as of 2026‑07‑01), it is a mature, community‑driven tool for prototype‑level or internal workflows.

**Value**  
- **Time savings** – Engineers can embed `gcloud` actions (e.g., data imports, service enablement, temporary resource tweaks) inside Terraform plans, eliminating context‑switching between Terraform and the shell.  
- **Consistent CI feedback** – CLI steps become part of the Terraform run, so failures surface early in pull‑request pipelines, improving review quality.  
- **Reduced manual errors** – By codifying routine `gcloud` commands, the module enforces repeatable, version‑controlled operations.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the provided examples, and verify that the `gcloud` commands you need are supported.  
2. **README & CI validation** – Follow the module’s README to add a small wrapper module to an existing Terraform workspace; run it in a feature branch and observe CI results.  
3. **Incremental rollout** – Replace ad‑hoc scripts with the module for a single service (e.g., enabling APIs or seeding Cloud SQL), then expand to other repetitive tasks.  
4. **Governance** – Add the module to your internal Terraform registry, pin a specific version, and document required IAM scopes for the service account that executes the `gcloud` calls.

**Production Readiness**  
- **Maturity**: Medium. The module is actively maintained (last update 2026‑07‑01) and has a modest community footprint (176 ⭐, 98 forks). It is suitable for prototypes, internal tools, and non‑critical pipelines.  
- **Considerations before production**:  
  * Verify the license compatibility with your organization.  
  * Conduct a security audit of the embedded `gcloud` commands and the service‑account permissions they require.  
  * Establish a version‑pinning and update policy to avoid breaking changes.  
  * Test dependency handling (e.g., required `gcloud` SDK version) in your CI environment.  

Once these checks are completed, the module can be promoted to production for stable internal workflows, while keeping an eye on upstream updates and community issue tracking.

### Русский

**Краткое резюме:**  
`terraform-google-modules/terraform-google-gcloud` позволяет запускать команды Google Cloud CLI прямо из Terraform‑конфигураций, ускоряя ежедневные циклы разработки, автоматизируя локальные задачи инженеров и улучшая обратную связь в CI. Для внедрения рекомендуется начать с небольшого proof‑of‑concept, проверив README и интегрировав модуль в один из существующих пайплайнов. Проект имеет средний уровень готовности к production: подходит для прототипов и внутренних процессов, но требует предварительной проверки лицензии, безопасности и активности мейнтейнеров.

### 中文

**项目简介**  
terraform-google-modules/terraform-google-gcloud 是一个 Terraform 模块，能够在 Terraform 计划/应用阶段直接调用 Google Cloud CLI（gcloud）命令，从而把本地或 CI 环境的 GCP 操作自动化并纳入基础设施即代码的工作流。

**价值**  
- **提升开发效率**：在 Terraform 代码中即能完成资源创建、配置查询、权限检查等常见 gcloud 操作，避免在 IDE、终端和 Terraform 之间来回切换。  
- **加速 CI 反馈**：CI 流水线里可以直接运行 gcloud 命令验证资源状态或执行一次性脚本，使审查和回滚更快。  
- **统一治理**：所有 GCP 操作都通过 Terraform 受控，便于审计、版本化和团队协作。

**典型接入方式**  
1. **在 Terraform 项目中引用模块**  
   ```hcl
   module "gcloud" {
     source  = "terraform-google-modules/gcloud/google"
     version = "~> 1.0"

     # 必要的输入变量，例如要执行的命令和环境
     command = "gcloud compute instances list --project=${var.project_id}"
   }
   ```
2. **在本地或 CI 环境准备**  
   - 安装 `gcloud` 并确保已有有效的 Service Account JSON（或使用 `gcloud auth activate-service-account`）。  
   - 在 Terraform 执行前通过 `export GOOGLE_APPLICATION_CREDENTIALS=/path/to/key.json` 让模块能够调用 gcloud。  
3. **运行 Terraform**  
   - `terraform init && terraform apply` 时，模块会在 `null_resource` 的 `provisioner "local-exec"` 中执行指定的 gcloud 命令，输出可通过 `terraform output` 或日志查看。

**生产可用性评估**  
- **成熟度**：GitHub 176⭐、98 forks，最近一次提交在 2026‑07‑01，活跃度尚可。  
- **适用场景**：非常适合原型、内部工具或需要频繁执行 gcloud 脚本的 CI 流程；在生产环境使用前建议：  
  1. **小范围 PoC**：先在单个模块或测试环境验证命令的幂等性和错误处理。  
  2. **依赖审计**：检查所调用的 gcloud 子命令是否有隐藏的副作用或配额消耗。  
  3. **维护与安全**：确认项目有活跃维护者、遵循 Apache‑2.0（或相应）许可证，并对 Service Account 权限进行最小化授权。  
- **结论**：在做好依赖、权限和错误处理的前置工作后，可在生产环境安全使用，尤其适用于需要把“一次性 gcloud 操作”纳入 Terraform 生命周期的场景。

## 🧭 Practical evaluation

**Value:** terraform-google-modules/terraform-google-gcloud helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 176 GitHub stars
- 98 forks
- updated 2026-07-01
- primary language: HCL
- 2 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 50/100 |
| stars | 48/100 |
| topics | 25/100 |
| outlook | 67/100 |
| quality | 61/100 |
| recency | 80/100 |
| adoption | 48/100 |
| production | 67/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/terraform-google-modules/terraform-google-gcloud) · [← Back to Cloud--storage](./README.md)</sub>
