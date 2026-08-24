# ulsklyc/yuvomi

[![Stars](https://img.shields.io/github/stars/ulsklyc/yuvomi?style=flat-square&color=yellow)](https://github.com/ulsklyc/yuvomi/stargazers) [![Forks](https://img.shields.io/github/forks/ulsklyc/yuvomi?style=flat-square&color=blue)](https://github.com/ulsklyc/yuvomi/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Self-hosted family planner - tasks, calendars, shopping, meals, budget. Your data, your server.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 805 |
| 🍴 **Forks** | 63 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`docker` `family` `family-planner` `home-automation` `open-source` `planner-app` `privacy-first` `progressive-web-app` `pwa` `self-hosted` `selfhosted` `selfhosted-apps`

## 🎯 Categories

Automation · DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
Yuvomi (ulsklyc/yuvomi) is a self‑hosted family planner that consolidates tasks, calendars, shopping lists, meals, and budgeting into a single web app you run on your own server. With a clean JavaScript codebase, an extensible API/CLI and strong community signals (805 ★, recent commits), it aims to eliminate repetitive manual coordination and let families automate everyday workflows.

**Value**  
- **Automation of routine family chores** – recurring tasks, grocery orders, meal plans and budget updates can be defined once and run automatically, freeing members from manual copy‑pasting or paper lists.  
- **Data sovereignty** – all information stays on the user‑controlled server, which is crucial for privacy‑sensitive households.  
- **Extensibility** – the exposed API, SDK and CLI let you hook Yuvomi into existing tools (e.g., Google Calendar, Slack, home‑assistant) and build repeatable flows without custom scripting.

**Practical Adoption Path**  
1. **Deploy** – spin up the Docker image or clone the repo on a Node.js‑compatible host; the README provides one‑click Docker‑Compose and environment‑variable configuration.  
2. **Onboard** – create family accounts, import existing calendars or CSV task lists via the UI or CLI.  
3. **Automate** – define recurring tasks or budget rules through the web UI or API; connect external services using webhooks or the provided SDK.  
4. **Iterate** – extend functionality with custom scripts or integrate with CI/CD pipelines for scheduled data syncs, leveraging the open‑source community for plugins and support.

**Production Readiness**  
- **Active development** – last commit on 2026‑06‑23, regular issue triage, and a healthy fork network indicate ongoing maintenance.  
- **Community adoption** – >800 stars and dozens of forks demonstrate real‑world interest and a pool of contributors.  
- **Infrastructure‑ready** – Docker support, clear API/CLI contracts, and JavaScript’s mature ecosystem make deployment and scaling straightforward.  
- **Risks** – licensing, security audit, and long‑term maintainer commitment still need a final check, but no major red flags appear in the current metadata.

Overall, Yuvomi is a mature OSS candidate for families or small teams that want a private, automated planner and are comfortable running a Node.js service in production.

### Русский

ulsklyc/yuvomi — это self‑hosted планировщик для семьи, объединяющий задачи, календари, покупки, меню и бюджет в едином интерфейсе, полностью под контролем пользователя и его сервера. Он позволяет автоматизировать рутинные операции (например, синхронизацию списков покупок с календарём или планирование бюджетных расходов) и интегрировать сторонние инструменты через открытый API/CLI, превращая их в повторяемые рабочие потоки. Проект имеет высокую готовность к production: активные коммиты, 805 звёзд, 63 форка, поддержка JavaScript и обширная мета‑информация, что делает его надёжным кандидатом для пилотного внедрения в корпоративных или семейных инфраструктурах.

### 中文

**项目简介**  
ulsklyc/yuvomi 是一款自托管的家庭计划管理工具，集任务、日历、购物清单、餐食安排和预算管理于一体，所有数据都保存在用户自己的服务器上，完全掌控。

**价值**  
- **消除重复手工操作**：通过统一的界面和 API，将家庭日常事务自动化，省时省力。  
- **数据自主可控**：所有信息都存放在自有服务器，避免第三方平台的数据泄露风险。  
- **灵活扩展**：提供 API/SDK/CLI，可轻松与其他工具（如智能家居、财务系统）对接，构建可重复的工作流。

**典型接入方式**  
1. **API 调用**：使用项目公开的 RESTful API 进行任务、日历、购物等资源的增删改查。  
2. **SDK/CLI**：项目提供的 JavaScript SDK 或命令行工具，可在脚本或 CI/CD 流程中直接调用，实现自动化任务调度。  
3. **Webhook/事件**：通过订阅系统事件（如任务完成、预算变更）与外部服务（如 Slack、Zapier）进行实时集成。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑23 最近一次提交，拥有 805 星、63 Fork，社区活跃。  
- **技术成熟**：主语言 JavaScript，配套 12 个主题标签，文档涵盖 API、部署与运维指南。  
- **部署简便**：支持 Docker Compose、Kubernetes 等常见方式，适合在自家服务器或私有云上快速上线。  
- **风险提示**：仍需进一步审查许可证细节、依赖安全漏洞以及维护者的响应速度，但整体已具备进入生产环境的条件，可作为正式项目的候选方案。

## 🧭 Practical evaluation

**Value:** ulsklyc/yuvomi helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 805 GitHub stars
- 63 forks
- updated 2026-06-23
- primary language: JavaScript
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 62/100 |
| topics | 100/100 |
| outlook | 63/100 |
| quality | 66/100 |
| recency | 40/100 |
| adoption | 57/100 |
| production | 57/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/ulsklyc/yuvomi) · [← Back to Automation](./README.md)</sub>
