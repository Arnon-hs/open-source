# aicw-io/aicw-ai-mentions

[![Stars](https://img.shields.io/github/stars/aicw-io/aicw-ai-mentions?style=flat-square&color=yellow)](https://github.com/aicw-io/aicw-ai-mentions/stargazers) [![Forks](https://img.shields.io/github/forks/aicw-io/aicw-ai-mentions?style=flat-square&color=blue)](https://github.com/aicw-io/aicw-ai-mentions/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> AICW AI Mentions (formerly AICW Rankings) is an open-source tool that helps online marketers track how often their products are mentioned in responses from popular AI chatbots.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 22 |
| 🍴 **Forks** | 3 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `ai-observability` `ai-transparency` `brand-monitoring` `chatgpt` `claude` `competitive-intelligence` `llm-evaluation` `llm-monitoring` `marketing` `martech` `observability`

## 🎯 Categories

AI/ML · Observability · Marketing

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
AICW AI Mentions (formerly AICW Rankings) is an open‑source TypeScript utility that automatically scans responses from popular AI chatbots to count how often a brand’s products are mentioned. By turning a previously manual monitoring task into a repeatable, schedulable workflow, it helps marketers gauge AI‑driven buzz without hand‑picking each conversation.

**Value**  
- **Automation of a tedious task** – eliminates the need for marketers to manually copy‑paste chatbot logs and search for product names, freeing time for analysis and strategy.  
- **Data‑driven insights** – provides a quantitative “mention score” that can be fed into dashboards, alerting systems, or attribution models.  
- **Composable workflows** – can be linked with existing marketing stacks (e.g., Slack, HubSpot, Google Sheets) to trigger downstream actions such as notifications, lead scoring, or content updates.

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC)** – Clone the repo, run the provided README example against a single chatbot endpoint, and verify that mention extraction works for your product terminology.  
2. **Integration & Scheduling** – Wrap the core library in a small Node/TS service, add connectors to your data lake or BI tool, and schedule the job (e.g., via GitHub Actions, cron, or an orchestration platform like Airflow).  
3. **Iterate & Extend** – Refine the keyword list, add language‑specific parsers, and incorporate alerting (e.g., Slack webhook) based on threshold breaches.  
4. **Scale to Production** – Containerize the service, implement logging/metrics (the project already includes basic observability hooks), and integrate with your CI/CD pipeline for automated testing and deployment.

**Production Readiness**  
- **Maturity**: Medium. The codebase is recent (last update 2026‑05‑12), has modest community traction (22 ★, 3 forks), and is written in TypeScript, which eases maintenance.  
- **Strengths**: Clear automation focus, good documentation starter, and a modest dependency footprint.  
- **Caveats**: Requires a final security/license audit, and the maintainers’ activity level should be confirmed before a critical rollout. Dependency and version‑pinning checks are advisable, as is adding unit/integration tests for your specific chatbot endpoints.  

Overall, AICW AI Mentions is well‑suited for internal prototypes or early‑stage marketing automation, with a straightforward path to a production‑grade service once the above diligence steps are completed.

### Русский

**AICW AI Mentions** — это open‑source утилита (TypeScript), позволяющая автоматизировать мониторинг упоминаний продуктов в ответах популярных AI‑чатботов, избавляя маркетологов от рутинных ручных проверок и интегрируя данные в повторяемые рабочие потоки. Типичный сценарий: небольшая proof‑of‑concept‑интеграция через README, настройка расписания и соединение с существующими инструментами (CRM, аналитика) для автоматического сбора и анализа упоминаний. Готовность к production — средняя: проект подходит для прототипов и внутренних процессов, но перед масштабным запуском требуется проверка лицензии, безопасности и поддерживаемости зависимостей.

### 中文

**项目简介**  
AICW AI Mentions（原 AICW Rankings）是一款开源工具，能够自动抓取并统计热门 AI 聊天机器人（如 ChatGPT、Claude 等）对话中对指定产品的提及次数，帮助在线营销人员实时监控品牌曝光。

**价值**  
- **降低重复劳动**：无需人工在聊天记录中逐条搜索，工具可批量抓取、统计并生成报告。  
- **实现可编排的工作流**：可与数据库、监控平台或营销自动化系统（如 Zapier、Make）对接，形成数据采集 → 处理 → 报警的闭环。  
- **提升决策效率**：通过定时任务自动更新提及数据，为营销活动、舆情分析提供可靠的量化依据。

**典型接入方式**  
1. **快速 PoC**：克隆仓库 → 按 README 配置 API Key（对应的聊天机器人或爬虫服务） → 运行 `npm run start`，观察控制台输出的提及统计。  
2. **业务集成**：在已有的 TypeScript/Node.js 项目中通过 `npm i aicw-ai-mentions` 引入库，使用提供的 SDK 调用 `fetchMentions(productId, options)`，将结果写入内部数据库或推送到监控仪表盘。  
3. **调度执行**：结合 cron（如 `node-cron`）或云函数（AWS Lambda、Google Cloud Run）实现每日/每小时自动抓取，配合 Slack、邮件或 webhook 发送提醒。

**生产可用性**  
- **成熟度**：当前评分 68/100，适合作为原型或内部工具使用。代码基于 TypeScript，结构清晰，拥有 22 ⭐ 的社区关注。  
- **依赖与维护**：项目仍在活跃更新（截至 2026‑05‑12），但仍需自行审查第三方依赖的安全性，并确认许可证（MIT）符合企业合规。  
- **上线建议**：先在测试环境完成小规模 PoC，验证数据准确性与性能后，再通过容器化或 CI/CD 将其部署为可监控的微服务；同时加入日志、健康检查和异常报警，以满足生产级可靠性要求。

## 🧭 Practical evaluation

**Value:** aicw-io/aicw-ai-mentions helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 22 GitHub stars
- 3 forks
- updated 2026-05-12
- primary language: TypeScript
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 15/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 61/100 |
| recency | 80/100 |
| adoption | 25/100 |
| production | 65/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/aicw-io/aicw-ai-mentions) · [← Back to AI/ML](./README.md)</sub>
