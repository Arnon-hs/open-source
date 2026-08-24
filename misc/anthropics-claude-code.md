# anthropics/claude-code

[![Stars](https://img.shields.io/github/stars/anthropics/claude-code?style=flat-square&color=yellow)](https://github.com/anthropics/claude-code/issues/62476/stargazers) [![Forks](https://img.shields.io/github/forks/anthropics/claude-code?style=flat-square&color=blue)](https://github.com/anthropics/claude-code/issues/62476/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-31%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 31/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Project Summary:**
"Beware, Claude Code deletes >30 day old transcripts. Anthropic won't fix it" is an open-source project that alerts users about a known issue with the Claude Code, a tool developed by Anthropic, which deletes transcripts older than 30 days without a fix in sight. This project can be useful for specific workflows, but its adoption requires manual verification.

**Value Proposition:**
The project provides a warning about a potential issue with the Claude Code, allowing users to make informed decisions about their workflow. This can be particularly valuable for teams or individuals who rely on Claude Code for critical tasks.

**Practical Adoption Path:**
To adopt this project, users should first verify its quality signals, including the license, maintenance, documentation, issues, and release cadence. Once verified, users can manually inspect the project's README and activity to ensure it matches their specific workflow. This project may be suitable for prototypes or internal workflows, but its production readiness is medium due to the need for dependency and maintenance checks.

**Production Readiness:**
The project's production readiness is medium, indicating that it can be used in production environments with some caution. Users should carefully evaluate the project's quality signals and dependencies before integrating it into their workflow.

### Русский

Резюме проекта "Beware, Claude Code deletes >30 day old transcripts. Anthropic won't fix it":

Этот проект предназначен для предостережения о потенциальной потере транскриптов, превышающих 30 дней, в системе Claude Code, которая не поддерживается компанией Anthropic. Он может быть полезен для определенных рабочих процессов, когда README и активность проекта соответствуют конкретной цели. Проект готов для использования в прототипах или внутренних рабочих процессах, но требует проверки лицензии, поддержки, документации, проблем и релизного графика перед внедрением в производство.

### 中文

**项目简介**  
Beware, Claude Code deletes >30 day old transcripts. Anthropic won't fix it 是一个在 Hacker News（github‑mentions）上被发现的开源警示项目，旨在提醒用户 Claude Code 会自动删除超过 30 天的对话记录，并且官方暂未计划修复。该项目适用于需要了解或规避此行为的工作流。

**价值**  
- **风险预警**：帮助开发者在使用 Claude Code 前意识到历史对话会被自动清除，避免因数据丢失导致的业务中断或合规问题。  
- **工作流安全**：可作为内部审计或合规检查的前置步骤，确保关键对话在需要时已被备份或转存。  

**典型接入方式**  
1. **手动审查**：在项目 README 与活跃度符合你的具体业务需求后，先在本地或测试环境克隆仓库。  
2. **集成脚本**：编写简单的 CI 步骤或 pre‑commit hook，调用项目提供的检测脚本（如有），在每次提交前检查 Claude Code 配置是否开启自动删除。  
3. **监控告警**：结合现有的日志/监控平台（Prometheus、Grafana 等），使用项目中可能提供的 API 或自定义脚本，定期查询对话存储状态并触发告警。  

**生产可用性**  
- **成熟度**：评分 41/100，属于 **中等** 级别。适合原型验证、内部工具或对风险容忍度较高的场景。  
- **依赖与维护**：项目更新于 2026‑06‑30，元数据较少，需自行检查许可证、活跃度、issue 处理情况以及发布节奏。  
- **上线建议**：在正式生产环境使用前，务必完成以下检查：  
  1. 确认开源许可证兼容公司政策；  
  2. 评估维护者响应速度，确保出现 bug 能得到及时修复；  
  3. 编写备份/持久化方案，以防对话被自动删除；  
  4. 在受控环境中进行功能验证，确保告警或拦截逻辑可靠。  

总体而言，该项目在 **原型阶段或内部合规审计** 中价值突出，但在 **大规模生产环境** 使用前仍需进行充分的依赖审查和风险缓解。

## 🧭 Practical evaluation

**Value:** Beware, Claude Code deletes >30 day old transcripts. Anthropic won't fix it may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-06-30
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 33/100 |
| quality | 26/100 |
| recency | 40/100 |
| adoption | 0/100 |
| production | 38/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/anthropics/claude-code/issues/62476) · [← Back to Misc](./README.md)</sub>
