# LuKresXD/claw-skeleton

[![Stars](https://img.shields.io/github/stars/LuKresXD/claw-skeleton?style=flat-square&color=yellow)](https://github.com/LuKresXD/claw-skeleton/stargazers) [![Forks](https://img.shields.io/github/forks/LuKresXD/claw-skeleton?style=flat-square&color=blue)](https://github.com/LuKresXD/claw-skeleton/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> 🪼 A personal AI assistant that lives in Telegram — every topic is its own isolated Claude Code agent with layered persistent memory and proactive cron heartbeats. Open skeleton of a real, running system.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 64 |
| 🍴 **Forks** | 14 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-assistant` `anthropic` `chatbot` `claude` `claude-code` `grammy` `llm-agent` `personal-assistant` `telegram-bot` `typescript`

## 🎯 Categories

Automation · AI/ML

## 📝 Summary

### English

LuKresXD/claw-skeleton is an open-source AI assistant framework that deploys isolated Claude Code agents within Telegram, each handling a specific topic with persistent memory and automated scheduled tasks (“cron heartbeats”) to reduce repetitive manual work. Its value lies in automating workflow operations, connecting tools into repeatable flows, and enabling proactive task scheduling—ideal for personal productivity or internal team automation. While production-ready for prototypes and internal use, adoption should begin with a small PoC due to medium production readiness: users must verify dependencies, licensing, security, and maintainer activity before scaling, as the project is actively updated but lacks full enterprise-grade assurances.

### Русский

LuKresXD/claw‑skeleton — это открытый скелет персонального AI‑ассистента в Telegram, где каждый топик реализован как отдельный изолированный агент Claude с постоянной памятью и активными cron‑heartbeat’ами, позволяющий автоматизировать повторяющиеся операции и связывать инструменты в повторяемые потоки. Для внедрения рекомендуется начать с небольшого proof‑of‑concept: развернуть бота, протестировать один‑два топика и настроить расписание задач, проверив README и зависимости. Готовность к production — средняя: проект подходит для прототипов и внутренних процессов, но перед запуском в продакшн требуется проверка лицензии, безопасности и поддерживаемости зависимостей.

### 中文

**项目简介**  
LuKresXD/claw‑skeleton 是一个基于 Telegram 的个人 AI 助手框架，使用 Claude Code 为每个话题创建独立的代码代理，并配备分层持久记忆与主动的 cron 心跳，实现自动化的对话与任务调度。它提供了真实可运行系统的骨架，方便开发者快速构建自己的 AI 工作流。

**价值**  
- **消除重复操作**：把日常的手动指令、查询和数据处理交给 AI 代理执行，显著提升工作效率。  
- **可组合的工具链**：通过 Telegram 消息即可调用外部 API、触发脚本或调度任务，实现跨工具的可复用流程。  
- **持久记忆与主动提醒**：分层记忆让每个话题拥有上下文记忆，cron 心跳能够主动推送提醒或执行例行任务。

**典型接入方式**  
1. **阅读 README**，确认所需的 Telegram Bot Token、Claude API Key 以及 Node.js/TypeScript 环境。  
2. **Fork 项目**，在 `config` 中填入自己的凭证并根据业务需求添加或修改 “topic” 配置（每个话题对应一个独立的 Claude Code 代理）。  
3. **本地运行或容器化部署**，先在测试群组里验证 Bot 的基本指令和 cron 任务是否按预期工作。  
4. **逐步集成**：从单一话题的简单自动化开始，随后在代码中引入自定义插件或外部服务，实现完整的业务流程。

**生产可用性**  
- **成熟度**：当前评分 62/100，适合作为原型或内部工具使用。代码已在 2026‑06‑30 更新，拥有 64 星、14 Fork，社区活跃度一般。  
- **准备度**：中等（Medium）。在生产环境部署前，需要完成以下检查：  
  - 许可证兼容性与合规审查。  
  - 第三方依赖的安全审计（尤其是 Claude API 与 Telegram Bot）。  
  - 持续监控和日志收集，以捕获 cron 心跳或代理异常。  
  - 设定灰度发布或 A/B 测试，确保业务关键路径的可靠性。  

综上，claw‑skeleton 为希望在 Telegram 中快速实现 AI 自动化的团队提供了一个可定制、可扩展的起点，适合先做小规模 PoC，确认稳定后再逐步推向生产环境。

## 🧭 Practical evaluation

**Value:** LuKresXD/claw-skeleton helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 64 GitHub stars
- 14 forks
- updated 2026-06-30
- primary language: TypeScript
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 39/100 |
| topics | 100/100 |
| outlook | 55/100 |
| quality | 56/100 |
| recency | 40/100 |
| adoption | 36/100 |
| production | 53/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/LuKresXD/claw-skeleton) · [← Back to Automation](./README.md)</sub>
