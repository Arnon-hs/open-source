# acip/slack-claude-agent

[![Stars](https://img.shields.io/github/stars/acip/slack-claude-agent?style=flat-square&color=yellow)](https://github.com/acip/slack-claude-agent/stargazers) [![Forks](https://img.shields.io/github/forks/acip/slack-claude-agent?style=flat-square&color=blue)](https://github.com/acip/slack-claude-agent/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-36%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 36/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Automation

## 📝 Summary

### English

Here's a brief summary of the open-source project:

**Show HN: Self-hosted Slack bot to mention Claude, with plan-gated file writes**

This self-hosted Slack bot automates repetitive manual operations by integrating with tools and scheduling operational tasks, reducing manual work and increasing workflow efficiency. To adopt this project, users should perform a manual inspection before integration and verify the project's quality signals, including license, maintenance, documentation, issues, and release cadence. With medium production readiness, it's suitable for prototypes or internal workflows after thorough dependency and maintenance checks.

**Value:**
The project provides a solution to automate repetitive manual operations, helping users remove manual work and connect tools into repeatable flows. This increases workflow efficiency and reduces the time spent on manual tasks.

**Practical Adoption Path:**

1. Manual inspection: Verify the project's quality signals, including license, maintenance, documentation, issues, and release cadence.
2. Integration: Integrate the Slack bot with your tools and schedule operational tasks.
3. Testing: Test the bot to ensure it meets your requirements and automates tasks correctly.
4. Maintenance: Regularly check for updates and dependencies, and perform necessary maintenance tasks.

**Production Readiness:**
The project has medium production readiness, making it suitable for

### Русский

Резюме проекта:

Show HN: Self-hosted Slack bot to mention Claude, с план-ограниченным доступом к файлам, представляет собой инструмент, позволяющий автоматизировать повторяющиеся задачи и задачи, связанные с управлением потоками. Примерным сценарием использования является удаление ручного труда и интеграция инструментов в повторяющиеся потоки. Проект готов к использованию в прототипах или внутренних потоках, но требует дополнительной проверки и поддержки перед внедрением в производство.

### 中文

**项目简介（2‑3 句）**  
Show HN: Self‑hosted Slack bot to mention Claude, with plan‑gated file writes 是一个可自行部署的 Slack 机器人，能够在对话中直接 @Claude 并根据用户的订阅计划控制文件写入权限。它通过自动化 Slack 与 Claude（Anthropic 大语言模型）的交互，帮助团队消除重复的手工操作。

**价值**  
- **降低人工成本**：把手动调用 Claude、保存结果、分配文件权限等步骤自动化，减少点击和复制粘贴。  
- **提升流程可重复性**：可将 Slack 消息触发的任务（如生成报告、代码审查摘要）串联成可调度的工作流。  
- **细粒度权限控制**：基于用户或团队的订阅计划决定是否允许写文件，避免未经授权的写入操作。

**典型接入方式**  
1. **部署**：在自有服务器或容器平台（Docker、K8s）上拉取源码，配置 `SLACK_BOT_TOKEN`、`CLAUDE_API_KEY` 与计划管理服务的凭证。  
2. **Slack App 注册**：在 Slack API 控制台创建 App，开启 `chat:write`、`commands`、`files:write`（受计划限制）等权限，并将 Bot Token 填入环境变量。  
3. **事件订阅**：在 Slack App 中订阅 `app_mention` 事件，或使用 Slash Command（如 `/claude`）触发机器人。  
4. **计划检查**：机器人在收到请求后先查询内部计划服务（可自行实现或使用 Stripe 等），判断是否满足写文件的条件；不满足时仅返回 Claude 的文本回复。  
5. **文件写入**：满足条件后，调用 Slack Files API 或本地存储，将 Claude 生成的内容保存为文件并共享到指定频道。  

**生产可用性**  
- **成熟度**：当前评分 45/100，属于 **中等** 级别，适合原型、内部工具或团队内部的自动化需求。  
- **依赖与维护**：项目最近一次更新为 2026‑07‑01，代码库仅包含两类主题，缺乏完整的 CI/CD、单元测试和详细文档。部署前需自行审查许可证、依赖安全性以及维护者的活跃度。  
- **上线建议**：  
  1. 在受控的测试环境中运行，验证 Slack 事件、Claude 调用和计划检查的完整链路。  
  2. 为关键路径（如文件写入）添加审计日志和回滚机制。  
  3. 若计划服务或 Claude API 频率受限，考虑加入速率限制和重试逻辑。  
  4. 在生产环境前进行安全审计，确保文件写入权限不会被滥用。  

综上，该项目可显著提升 Slack 中对 Claude 的使用效率，适合作为内部自动化的起点，但在投入生产前需要完成依赖检查、权限审计以及稳健的运维方案。

## 🧭 Practical evaluation

**Value:** Show HN: Self-hosted Slack bot to mention Claude, with plan-gated file writes helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-07-01
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 36/100 |
| quality | 26/100 |
| recency | 40/100 |
| adoption | 0/100 |
| production | 38/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/acip/slack-claude-agent) · [← Back to Automation](./README.md)</sub>
