# oneshot-agent/oneshot-gtm

[![Stars](https://img.shields.io/github/stars/oneshot-agent/oneshot-gtm?style=flat-square&color=yellow)](https://github.com/oneshot-agent/oneshot-gtm/stargazers) [![Forks](https://img.shields.io/github/forks/oneshot-agent/oneshot-gtm?style=flat-square&color=blue)](https://github.com/oneshot-agent/oneshot-gtm/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> GTM agent for technical founders. Pay-per-result. Signed receipts. Two surfaces: terminal CLI + local web dashboard.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 453 |
| 🍴 **Forks** | 10 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `bun` `cli` `cold-email` `dashboard` `founder-led-sales` `gtm` `mit-license` `oneshot` `react` `signed-receipts` `typescript`

## 🎯 Categories

AI/ML · Communication · Frontend · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
oneshot‑agent/oneshot‑gtm is an open‑source GTM (go‑to‑market) agent that lets technical founders embed AI capabilities via a simple terminal CLI or a local web dashboard, charging only on successful outcomes and providing signed receipts for transparency. It streamlines the creation of RAG pipelines, autonomous agents, and other AI‑driven features without requiring a custom model stack, and is built in TypeScript with active community backing (453 ★, recent commits).

**Value**  
- **Speed to market** – Developers can prototype and ship AI‑enhanced products in hours rather than weeks, thanks to ready‑made CLI/web interfaces and pre‑wired integration hooks.  
- **Pay‑per‑result model** – Costs are incurred only when the agent delivers the promised outcome, reducing financial risk for early‑stage teams.  
- **Auditability** – Signed receipts give founders verifiable proof of performance, useful for compliance and investor reporting.  

**Practical Adoption Path**  
1. **Install** the npm package and run the CLI to generate a starter project or launch the local dashboard.  
2. **Configure** your data source(s) and select a pre‑built RAG or agent workflow from the provided templates.  
3. **Iterate** locally, using the dashboard to monitor signals (API calls, latency, success metrics) and tweak prompts or data pipelines.  
4. **Deploy** the agent to your production environment (e.g., Docker, Vercel) and switch on pay‑per‑result billing; the signed receipt API can be hooked into your invoicing or monitoring stack.  

**Production Readiness**  
- **Activity & Adoption** – Recent commits (as of 2026‑06‑24), 453 GitHub stars, and a growing user base indicate healthy momentum.  
- **Technical Maturity** – Written in TypeScript, the codebase follows modern patterns, exposes clear SDK/CLI entry points, and includes metadata for easy integration.  
- **Risk Profile** – No glaring licensing or security red flags have been identified, though a final audit of the license and maintainer responsiveness is advisable before mission‑critical roll‑outs. Overall, the project is a strong OSS candidate for pilot deployments and can be scaled to production with standard DevOps hardening.

### Русский

**oneshot-agent/oneshot-gtm** — это open‑source GTM‑агент, позволяющий техническим основателям быстро добавить AI‑функциональность (RAG, агентные воркфлоу, прототипы) без необходимости строить собственный стек моделей. Агент работает в двух режимах — через терминальный CLI и локальную веб‑дашборд‑панель, поддерживает pay‑per‑result и подписанные квитанции, а также предоставляет API/SDK и метаданные языка для лёгкой интеграции. По оценке готовности проекта (453★, активные коммиты, TypeScript‑база, широкая экосистема) он считается «high‑ready» для пилотного внедрения в продакшн, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句）**  
oneshot‑agent/oneshot‑gtm 是面向技术创始人的 GTM（Go‑to‑Market）智能代理，采用“按结果付费+签名收据”的商业模式，提供终端 CLI 与本地 Web 仪表盘两种交互方式。它让开发者无需从零搭建模型堆栈，即可快速为产品原型或业务流程注入 AI 能力。

**价值**  
- **即插即用**：通过封装好的 API/SDK 与 CLI，开发者只需几行代码即可在现有系统中集成 RAG、智能客服或自动化工作流。  
- **成本可控**：按实际产出付费，避免了大规模预付算力或模型训练的费用。  
- **可审计**：所有调用均生成签名收据，便于合规审计和费用结算。  

**典型接入方式**  
1. **CLI**：在本地终端运行 `oneshot gtm <command>`，快速调用预置的 AI 功能或自定义脚本。  
2. **Web Dashboard**：启动本地服务器（`npm run dashboard`），在浏览器中通过可视化界面配置模型、管理工作流、查看调用日志。  
3. **SDK/API**：在 TypeScript/JavaScript 项目中引入 `@oneshot/gtm-sdk`，使用 `gtmClient.invoke()` 等方法进行编程式调用，支持自定义 Prompt、数据源绑定等高级特性。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑24 最近一次提交，GitHub ★453，Fork 10，12 个主题标签，表明社区活跃且持续维护。  
- **技术成熟度**：核心实现使用 TypeScript，提供完整的类型声明和 CI/CD 流水线，易于集成到现代前端/后端项目。  
- **风险**：目前未发现重大元数据风险，但仍需对许可证（MIT/Apache 等）和安全审计（依赖漏洞）进行最终确认。总体而言，作为 OSS 候选，已具备在生产环境中进行试点的条件。

## 🧭 Practical evaluation

**Value:** oneshot-agent/oneshot-gtm helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 453 GitHub stars
- 10 forks
- updated 2026-06-24
- primary language: TypeScript
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 26/100 |
| stars | 57/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 48/100 |
| production | 71/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/oneshot-agent/oneshot-gtm) · [← Back to AI/ML](./README.md)</sub>
