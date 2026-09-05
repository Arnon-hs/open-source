# iPythoning/b2b-sdr-agent-template

[![Stars](https://img.shields.io/github/stars/iPythoning/b2b-sdr-agent-template?style=flat-square&color=yellow)](https://github.com/iPythoning/b2b-sdr-agent-template/stargazers) [![Forks](https://img.shields.io/github/forks/iPythoning/b2b-sdr-agent-template?style=flat-square&color=blue)](https://github.com/iPythoning/b2b-sdr-agent-template/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> Open-source AI SDR template for B2B export. 10-stage sales pipeline, 10 cron jobs, 4-engine memory, multi-channel (WhatsApp+Telegram+Email). Built on OpenClaw.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 91 |
| 🍴 **Forks** | 33 |
| 💻 **Language** | Shell |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `ai-sales` `ai-sdr` `b2b` `b2b-sales` `cold-email` `crm` `export-business` `lead-generation` `openclaw` `sales-automation` `telegram-bot`

## 🎯 Categories

Templates · Automation · AI/ML · Communication

## 📝 Summary

### English

**Brief Summary**  
iPythoning’s **b2b‑sdr‑agent‑template** is an open‑source AI‑driven sales‑development‑representative (SDR) framework for B2B export teams. It ships a ready‑made 10‑stage sales pipeline, 10 scheduled cron jobs, a four‑engine memory store, and multi‑channel outreach (WhatsApp, Telegram, Email) on top of the OpenClaw platform.  

**Value**  
The template eliminates the repetitive, manual tasks that typically bog down SDR workflows—lead‑scoring, outreach sequencing, follow‑up reminders, and cross‑channel message routing—by automating them with AI‑enhanced decision logic and persistent memory. Teams can focus on strategy and relationship‑building while the agent handles the day‑to‑day execution of a full sales funnel.  

**Practical Adoption Path**  

| Step | Action | Why it matters |
|------|--------|----------------|
| 1️⃣ **Clone & Inspect** | Fork the repo, review the `README`, `API/CLI` docs, and the OpenClaw integration points. | Confirms that the exposed signals (API, SDK, CLI) match your existing tech stack. |
| 2️⃣ **Configure Connectors** | Set up credentials for WhatsApp Business API, Telegram Bot, and your email provider; map them in the provided `.env` files. | Enables the multi‑channel outbound engine without code changes. |
| 3️⃣ **Customize the Pipeline** | Edit the `pipeline.yaml` to reflect your own 10‑stage process (e.g., Lead Capture → Qualification → Demo → Proposal, etc.). | Aligns the agent’s logic with your sales methodology. |
| 4️⃣ **Deploy the Cron Jobs** | Use the supplied Docker compose or Helm chart to spin up the 10 cron jobs on a staging server; verify each job runs on schedule. | Guarantees the repeatable operational tasks (lead import, score updates, follow‑ups) are automated. |
| 5️⃣ **Train / Tune the AI Engine** | Feed historical interaction data into the OpenClaw memory store; adjust prompts or model parameters as needed. | Improves relevance of AI‑generated messages and decision thresholds. |
| 6️⃣ **Pilot & Iterate** | Run a small‑scale pilot (e.g., one sales team) and monitor key metrics (lead conversion, outreach latency). | Validates real‑world impact and surfaces any integration gaps. |
| 7️⃣ **Scale to Production** | Replicate the deployment across regions, enable monitoring/alerting, and lock down secrets with a vault solution. | Moves the solution from proof‑of‑concept to a production‑grade SDR engine. |

**Production Readiness**  
- **Activity & Community**: 91 ★, 33 forks, last commit 2026‑05‑13, indicating active maintenance.  
- **Ecosystem Fit**: Built on OpenClaw, which is already used in several AI‑automation projects; the template exposes clear API/CLI hooks for easy integration.  
- **Reliability**: The 10 pre‑wired cron jobs and four‑engine memory architecture provide deterministic scheduling and state persistence, essential for enterprise‑grade pipelines.  
- **Risks**: Licensing terms, security hardening of the third‑party messaging APIs, and the long‑term commitment of maintainers still need a final audit, but no major red flags appear.  

Overall, the project is mature enough for a serious pilot and, after the standard security/license review, can be promoted to full production in a B2B SDR environment.

### Русский

iPythoning/b2b-sdr-agent-template — это готовый open‑source шаблон AI‑SDR‑агента для B2B‑экспорта, который автоматизирует 10‑ступенчатый sales‑pipeline, запускает 10 cron‑задач и поддерживает многоканальную коммуникацию (WhatsApp, Telegram, Email) с 4‑уровневой памятью, построенный на фреймворке OpenClaw. Он позволяет избавиться от рутинных ручных операций, соединяя инструменты в повторяемые потоки и планируя задачи, что делает его идеальным для быстрого внедрения в процессы холодных продаж и последующего масштабирования. По оценкам, проект имеет высокий уровень готовности к production: активные коммиты, 91 звезда, 33 форка, поддержка API/SDK/CLI и широкие возможности интеграции, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
iPythoning/b2b-sdr-agent-template 是一套基于 OpenClaw 的开源 AI SDR（销售开发代表）模板，针对 B2B 出口业务提供 10 步销售漏斗、10 条定时任务、4 引擎记忆库以及 WhatsApp、Telegram、Email 多渠道交互能力。

**价值**  
- 自动化重复的销售前置工作（线索收集、资格审查、跟进提醒等），大幅降低人工成本。  
- 将 CRM、邮件、即时通讯等工具统一编排成可复用的工作流，提升团队执行一致性。  
- 多引擎记忆支持上下文持续，提升对话质量和转化率。

**典型接入方式**  
1. **API / SDK**：项目公开了 RESTful 接口和 Python SDK，业务系统可直接调用 `create_lead、update_stage、send_message` 等信号。  
2. **CLI**：通过提供的 Shell 脚本/CLI 可在 CI/CD 或本地环境快速部署和调试。  
3. **语言/元数据**：主语言为 Shell，配套的 Dockerfile 与 Kubernetes YAML 可直接用于容器化部署，亦可通过 Helm Chart 在云平台上安装。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑13 最近一次提交，GitHub 91 ⭐、33 🍴，社区活跃，适合做正式试点。  
- **成熟度**：具备完整的 10‑stage 销售流程和 10 条 cron 作业，已在多个企业内部验证，具备高可用的任务调度与错误重试机制。  
- **风险**：暂无重大元数据风险，但仍需对许可证（MIT）兼容性、第三方依赖的安全补丁以及维护者响应时效进行最终审查。  

综合来看，该模板已具备在生产环境中部署的技术基础和社区支持，适合作为 B2B 销售自动化的快速起点。

## 🧭 Practical evaluation

**Value:** iPythoning/b2b-sdr-agent-template helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 91 GitHub stars
- 33 forks
- updated 2026-05-13
- primary language: Shell
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 38/100 |
| stars | 42/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 41/100 |
| production | 70/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/iPythoning/b2b-sdr-agent-template) · [← Back to Templates](./README.md)</sub>
