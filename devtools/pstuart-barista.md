# pstuart/Barista

[![Stars](https://img.shields.io/github/stars/pstuart/Barista?style=flat-square&color=yellow)](https://github.com/pstuart/Barista/stargazers) [![Forks](https://img.shields.io/github/forks/pstuart/Barista?style=flat-square&color=blue)](https://github.com/pstuart/Barista/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> A modular statusline for Claude Code CLI - real-time context usage, rate limits, costs, git status, and 20+ customizable modules

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 27 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | Shell |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anthropic` `bash` `claude` `claude-code` `cli` `developer-tools` `macos` `shell` `statusline` `terminal`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Project Summary:**

Barista is an open-source, modular statusline for Claude Code CLI that provides real-time context usage, rate limits, costs, git status, and customizable modules. This project aims to save engineers' time in daily development and review loops by automating local engineering tasks and improving CI feedback. By integrating Barista, developers can speed up their workflows and focus on more critical tasks.

**Value Proposition:**

Barista offers significant value to engineers by streamlining their daily development and review processes. By automating tasks and providing real-time feedback, engineers can save time and focus on high-priority tasks. This leads to improved productivity and reduced development time.

**Practical Adoption Path:**

To adopt Barista, developers can follow these steps:

1. Evaluate the project's documentation and implementation signals to ensure it meets their requirements.
2. Integrate Barista with their existing Claude Code CLI setup.
3. Configure the customizable modules to suit their specific needs.
4. Monitor and adjust the project as needed to ensure it continues to meet their requirements.

**Production Readiness:**

Barista is considered production-ready with medium readiness. While it is useful for prototypes or internal workflows, it requires dependency and maintenance checks before being used in production environments. Additionally, a final review of the

### Русский

**Barista** (pstuart/Barista) — это модульный статус‑лайн для Claude Code CLI, который в реальном времени показывает контекст использования, ограничения запросов, затраты, состояние git и более 20 настраиваемых модулей. Он позволяет ускорить ежедневные циклы разработки и ревью, автоматизировать локальные задачи инженера и улучшить обратную связь в CI, при этом легко интегрируется через API/SDK/CLI. Готовность к production — средняя: проект подходит для прототипов и внутренних воркфлоу, но перед развёртыванием в продакшн требуется проверка лицензии, безопасности и активности поддержки.

### 中文

**项目简介**  
Barista（pstuart/Barista）是一个面向 Claude Code CLI 的模块化状态栏插件，实时展示上下文使用量、速率限制、费用、Git 状态等信息，并提供 20+ 可自定义模块，帮助开发者在终端中一目了然地掌握关键指标。

**价值**  
- **提升效率**：在编码、审查和 CI 反馈环节实时看到费用和速率限制，避免因超额而中断工作流。  
- **自动化本地任务**：通过内置 Git、路径、文件变化等模块，省去手动查询的时间。  
- **可定制**：支持 Shell 脚本层面的自由组合，满足不同团队的工作流需求。

**典型接入方式**  
1. **CLI 集成**：在 Claude Code CLI 启动脚本中加载 `barista.sh`，即可在每次命令执行后自动刷新状态栏。  
2. **SDK/API 调用**：项目暴露了 `barista_status` 函数，其他 Shell 脚本或 CI 步骤可直接调用获取结构化的状态信息（JSON），便于二次加工。  
3. **模块配置**：通过 `~/.barista/config.yml` 选择需要的模块并设置显示顺序，支持环境变量覆盖，适配本地或 CI 环境。

**生产可用性**  
- **成熟度**：当前为 **Medium** 级别，适合原型、内部工具或 CI 辅助使用。  
- **依赖与维护**：仅依赖标准 Shell 与少量外部 CLI（git、curl），但在正式生产前建议审查许可证、潜在安全漏洞并锁定依赖版本。  
- **社区活跃度**：27 Stars、5 Forks，最近一次提交在 2026‑06‑27，活跃度一般。  

总体而言，Barista 能显著缩短开发者在上下文管理和本地任务上的等待时间，接入成本低，适合作为内部工作流的加速器；在投入正式生产前，建议完成安全审计和维护者确认。

## 🧭 Practical evaluation

**Value:** pstuart/Barista helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 27 GitHub stars
- 5 forks
- updated 2026-06-27
- primary language: Shell
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 31/100 |
| topics | 100/100 |
| outlook | 56/100 |
| quality | 52/100 |
| recency | 40/100 |
| adoption | 28/100 |
| production | 52/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/pstuart/Barista) · [← Back to DevTools](./README.md)</sub>
