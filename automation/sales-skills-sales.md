# sales-skills/sales

[![Stars](https://img.shields.io/github/stars/sales-skills/sales?style=flat-square&color=yellow)](https://github.com/sales-skills/sales/stargazers) [![Forks](https://img.shields.io/github/forks/sales-skills/sales?style=flat-square&color=blue)](https://github.com/sales-skills/sales/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Claude Code skills for sales, marketing, and GTM — CRM, outbound, note-takers, enrichment, email marketing, influencer marketing, social   listening, directories, and more. Install: npx skills add sales-skills/sales

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 57 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | Python |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-skills` `claude` `claude-code` `cold-email` `conversion-intelligence` `crm` `email-marketing` `gtm` `helpdesk` `influencer-marketing` `lead-generation` `martech`

## 🎯 Categories

Automation · AI/ML · Communication · Marketing

## 📝 Summary

### English

**Project Summary:**
The sales-skills/sales project is an open-source initiative that provides Claude Code skills for sales, marketing, and go-to-market (GTM) operations, automating tasks such as CRM management, email marketing, and social listening. This project aims to remove repetitive manual operations from workflows, connecting tools into repeatable flows and scheduling operational tasks. With a score of 61/100, it is considered production-ready but requires further evaluation and dependency checks.

**Value:**
The primary value proposition of sales-skills/sales lies in automating repetitive tasks, freeing up resources for more strategic and high-value activities. By connecting tools and scheduling operational tasks, businesses can streamline their workflows, improve efficiency, and reduce manual errors.

**Practical Adoption Path:**
To adopt sales-skills/sales, follow these steps:

1. **Install the project**: Use the command `npx skills add sales-skills/sales` to install the project.
2. **Evaluate and test**: Perform a small proof of concept and review the README documentation to ensure the project meets your requirements.
3. **Integrate with your tools**: Connect the project with your existing tools and workflows to automate tasks and schedule operational tasks.
4. **Monitor and maintain**: Regularly check for updates,

### Русский

`sales-skills/sales` — набор открытых Claude‑кодов для автоматизации продаж, маркетинга и GTM: CRM, аутбаунд‑кампании, нотатки, обогащение данных, email‑ и influencer‑маркетинг, соц‑прослушивание и др. Проект позволяет избавиться от рутинных ручных операций, связав разрозненные инструменты в повторяемые потоки и запланировать регулярные задачи (например, синхронизация лидов из директории в CRM и автоматическая рассылка — выполняется одной командой `npx skills add sales-skills/sales`). Готовность к продакшену — средняя: код подходит для прототипов и внутренних процессов, но перед масштабным запуском требуется проверка README, небольшое POC‑внедрение, аудит лицензии, безопасности и поддержка зависимостей.

### 中文

**项目简介**  
`sales-skills/sales` 是一套基于 Claude Code 的开源技能库，涵盖 CRM、外呼、笔记、数据补全、邮件营销、网红营销、社交监听、目录查询等销售与营销场景。只需运行 `npx skills add sales-skills/sales` 即可将这些功能快速装入你的工作流。

**价值**  
- **自动化重复任务**：把手动的客户信息抓取、邮件发送、线索分配等工作交给代码执行，显著提升效率。  
- **可组合的工具桥梁**：提供统一的 API，方便将不同 SaaS（如 HubSpot、Salesforce、Mailchimp 等）串联成可重复的业务流程。  
- **快速原型与内部工具**：适合在内部团队中快速搭建销售自动化原型，验证业务假设。

**典型接入方式**  
1. **安装**：`npx skills add sales-skills/sales`（或在项目的 `requirements.txt` 中加入对应 Python 包）。  
2. **配置**：在项目根目录创建 `sales_config.yaml`，填写 API Key、CRM 实例 URL、邮件服务器等凭证。  
3. **调用**：在 Python 脚本或 Claude Code 工作流中引入 `sales` 包，例如：  
   ```python
   from sales import crm, email

   leads = crm.search_contacts(industry="FinTech")
   email.send_batch(leads, template="welcome")
   ```  
4. **调试**：先在小规模数据集上跑一次，确认业务规则与外部系统的兼容性。

**生产可用性**  
- **成熟度**：当前评分 61/100，属于 **中等** 稳定性。代码已更新至 2026‑06‑27，拥有 57 颗星和 8 个 fork，社区活跃度一般。  
- **适用场景**：非常适合作为 **原型** 或 **内部工具** 使用；在正式生产环境部署前建议进行：  
  1. **安全审计**（检查依赖库的许可证与已知漏洞）。  
  2. **可靠性验证**（在预生产环境做完整的端到端回归测试）。  
  3. **监控与告警**（为关键 API 调用添加日志与异常上报）。  
- **风险**：暂无重大元数据风险，但仍需确认许可证兼容性、维护者活跃度以及潜在的安全漏洞后再投入关键业务。

综上，`sales-skills/sales` 能显著降低销售运营中的手工成本，适合作为内部自动化的起点；在完成小规模 PoC 并通过安全/可靠性检查后，即可考虑在生产环境中正式使用。

## 🧭 Practical evaluation

**Value:** sales-skills/sales helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 57 GitHub stars
- 8 forks
- updated 2026-06-27
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 38/100 |
| topics | 100/100 |
| outlook | 68/100 |
| quality | 65/100 |
| recency | 80/100 |
| adoption | 34/100 |
| production | 66/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/sales-skills/sales) · [← Back to Automation](./README.md)</sub>
