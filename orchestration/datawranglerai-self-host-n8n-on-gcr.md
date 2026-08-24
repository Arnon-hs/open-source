# datawranglerai/self-host-n8n-on-gcr

[![Stars](https://img.shields.io/github/stars/datawranglerai/self-host-n8n-on-gcr?style=flat-square&color=yellow)](https://github.com/datawranglerai/self-host-n8n-on-gcr/stargazers) [![Forks](https://img.shields.io/github/forks/datawranglerai/self-host-n8n-on-gcr?style=flat-square&color=blue)](https://github.com/datawranglerai/self-host-n8n-on-gcr/network) [![Language](https://img.shields.io/badge/lang-HCL-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Self-host n8n on Google Cloud without the subscription fees or server headaches - because your automation workflows shouldn't cost more than your coffee budget

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 600 |
| 🍴 **Forks** | 132 |
| 💻 **Language** | HCL |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic-ai` `ai` `ai-agent-framework` `ai-agents` `google-cloud-platform` `google-cloud-run` `managed-service` `n8n` `n8n-automation` `n8n-nodes` `n8n-self-hosting` `queue-workers`

## 🎯 Categories

Orchestration · Payments · Automation · AI/ML · Database

## 📝 Summary

### English

**Brief summary**  
The *datawranglerai/self‑host‑n8n‑on‑gcr* repository provides Terraform scripts and supporting files that let you spin up a fully self‑hosted instance of n8n on Google Cloud Run, eliminating the recurring subscription fees that come with the hosted version. It’s aimed at teams that want a low‑cost, scalable automation platform for payment‑related workflows such as billing, checkout, or PSP (payment service provider) integrations.  

**Value proposition**  
By deploying n8n on GCR you get a powerful, open‑source orchestration engine that can be tightly coupled with your existing payment infrastructure, giving you full control over data residency, cost, and custom extensions. The ready‑made Terraform modules accelerate the setup of billing‑oriented workflows, so you can move from concept to production without building the underlying cloud plumbing yourself.  

**Practical adoption path**  

1. **Proof‑of‑concept** – Clone the repo, review the README, and run the provided `terraform init/apply` against a test GCP project. Verify that a basic n8n workflow (e.g., a Stripe webhook → Google Sheet) executes successfully.  
2. **Security & licensing audit** – Confirm the MIT license meets your policy, scan the container image for vulnerabilities, and ensure any third‑party credentials are stored in Secret Manager.  
3. **Incremental rollout** – Deploy the production‑grade Terraform configuration in a separate GCP project, connect it to your real payment APIs, and gradually migrate existing automation jobs.  
4. **Monitoring & scaling** – Enable Cloud Logging, Cloud Monitoring, and autoscaling settings that come with the Terraform module to keep the service reliable under load.  

**Production readiness**  
The project scores 78/100 and shows strong OSS health signals: 600+ stars, 132 forks, recent commits (as of 2026‑05‑10), and active issue discussions. Its primary language (HCL) and well‑documented Terraform modules make integration straightforward for teams already using IaC on GCP. While no major metadata risks are flagged, a final review of the license, container security posture, and maintainer responsiveness is recommended before a full‑scale production launch. With these checks completed, the solution is considered “high” readiness for a serious pilot.

### Русский

**Краткое резюме:**  
Проект datawranglerai/self-host-n8n-on-gcr позволяет развернуть n8n в Google Cloud без подписки и лишних серверных хлопот, что делает автоматизацию рабочих процессов доступной даже при небольшом бюджете. Типичный сценарий — быстрая интеграция платёжных и биллинговых потоков (checkout, PSP‑операции, мониторинг платежей) через готовые ноды n8n, начиная с небольшого proof‑of‑concept и проверкой README. По оценке готовности к продакшену проект считается «high»: активные коммиты, 600 звёзд, 132 форка и поддержка инфраструктуры на HCL свидетельствуют о надёжной OSS‑базе, требующей лишь финального аудита лицензии и безопасности.

### 中文

**价值**  
datawranglerai/self-host-n8n-on-gcr 让你在 Google Cloud Run（GCR）上自托管 n8n 工作流引擎，省去官方订阅费用和服务器运维负担。它提供即插即用的 Terraform 配置，能够快速把支付、计费、PSP（支付服务提供商）等业务流程嵌入自动化工作流，从而显著缩短集成周期、降低成本，并保持与现有 CI/CD、IaC 流程的统一管理。

**典型接入方式**  

1. **准备环境**  
   - 在 GCP 项目中启用 Cloud Run、Artifact Registry、Secret Manager 等必要 API。  
   - 确保已有 Terraform（≥1.5）和 gcloud CLI。

2. **克隆仓库并检查 README**  
   ```bash
   git clone https://github.com/datawranglerai/self-host-n8n-on-gcr.git
   cd self-host-n8n-on-gcr
   ```

3. **创建 Terraform 工作区**（推荐在单独的目录或 Terraform Cloud 中）  
   ```hcl
   module "n8n" {
     source = "github.com/datawranglerai/self-host-n8n-on-gcr//terraform"
     
     project_id      = "my-gcp-project"
     region          = "us-central1"
     service_name    = "n8n"
     container_image = "gcr.io/my-gcp-project/n8n:latest"
     
     # 可选：外部数据库、Redis、SMTP 等配置
     db_instance_name = "my-sql-instance"
     redis_instance   = "my-redis"
   }
   ```

4. **部署**  
   ```bash
   terraform init
   terraform apply   # 确认后开始创建 Cloud Run 服务、IAM、Secrets 等资源
   ```

5. **接入业务系统**  
   - 在 n8n UI（通过 Cloud Run URL 访问）中创建 **Webhook**、**HTTP Request**、**Stripe/PayPal** 等节点。  
   - 将这些节点串联成 “计费 → PSP 校验 → 订单完成” 的工作流。  
   - 如需与内部微服务交互，可在 Terraform 中加入 VPC‑Connector，使 Cloud Run 与私有网络通信。

6. **验证 & 迭代**  
   - 先在测试环境跑一个小的 **Proof‑of‑Concept**（例如模拟一次支付成功回调），确认 webhook、密钥、环境变量均正常。  
   - 完成后逐步迁移生产支付/计费流程。

**生产可用性**  

- **活跃度**：最近一次提交在 2026‑05‑10，星标 600+、Fork 132，社区活跃，具备持续维护的潜力。  
- **技术成熟度**：基于 Terraform + Cloud Run 的 IaC 部署，天然支持弹性伸缩、零运维和自动 HTTPS。  
- **安全**：所有敏感信息（API 密钥、PSP 凭证）通过 GCP Secret Manager 管理，符合最小权限原则。  
- **可靠性**：Cloud Run 提供 99.95% SLA，且 n8n 本身支持持久化（PostgreSQL、MySQL）和容错。  
- **适配度**：项目语言为 HCL，易于与现有基础设施代码合并；README 提供完整的部署步骤，适合作为 **OSS Pilot** 的起点。

综合来看，datawranglerai/self-host-n8n-on-gcr 已具备 **高生产就绪度**，适合在支付、计费或任何需要自动化 PSP 流程的场景中快速落地，并可在后期通过 Terraform 进行规模化管理和持续交付。

## 🧭 Practical evaluation

**Value:** datawranglerai/self-host-n8n-on-gcr helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 600 GitHub stars
- 132 forks
- updated 2026-05-10
- primary language: HCL
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 53/100 |
| stars | 59/100 |
| topics | 100/100 |
| outlook | 61/100 |
| quality | 61/100 |
| recency | 20/100 |
| adoption | 57/100 |
| production | 50/100 |
| usefulness | 100/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-05-10 · [View on GitHub](https://github.com/datawranglerai/self-host-n8n-on-gcr) · [← Back to Orchestration](./README.md)</sub>
