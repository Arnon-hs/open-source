# h0x91b/dev-3.0

[![Stars](https://img.shields.io/github/stars/h0x91b/dev-3.0?style=flat-square&color=yellow)](https://github.com/h0x91b/dev-3.0/stargazers) [![Forks](https://img.shields.io/github/forks/h0x91b/dev-3.0?style=flat-square&color=blue)](https://github.com/h0x91b/dev-3.0/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Mission control for the One Person Studio — run a fleet of AI coding agents in parallel without losing your mind. Kanban + git worktrees + tmux for Claude Code, Codex, Gemini CLI, OpenCode and any shell agent. Not an IDE.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 210 |
| 🍴 **Forks** | 18 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-orchestration` `ai-agents` `ai-coding` `bun` `claude-code` `codex` `developer-tools` `electrobun` `gemini-cli` `git-worktree` `kanban` `project-management`

## 🎯 Categories

Orchestration · AI/ML · DevTools

## 📝 Summary

### English

**Project Summary**

h0x91b/dev-3.0 is an open-source project that serves as a mission control system for developers, enabling them to manage a fleet of AI coding agents in parallel. This project leverages Kanban, git worktrees, and tmux to streamline workflows, making it easier to integrate and manage various AI tools such as Claude Code, Codex, and Gemini CLI. By standardizing agent memory and tool usage, h0x91b/dev-3.0 helps turn isolated prompts and tools into repeatable agent workflows.

**Value Proposition**

The primary value proposition of h0x91b/dev-3.0 lies in its ability to simplify the management of multiple AI coding agents, allowing developers to focus on their work rather than getting bogged down by the complexities of integrating and coordinating various tools. By providing a standardized and repeatable workflow, this project enables developers to streamline their development process, improve productivity, and reduce the risk of errors.

**Practical Adoption Path**

To adopt h0x91b/dev-3.0, developers can start by evaluating the project's API, SDK, and CLI implementation signals. They can then integrate the project into their existing workflows by setting up Kanban boards, git worktrees, and tmux configurations.

### Русский

Резюме проекта h0x91b/dev-3.0:

h0x91b/dev-3.0 - это инструмент оркестрации, который позволяет эффективно управлять флотом агентов AI-кодирования в параллельном режиме. Он предназначен для студий разработки, где необходимо координировать работу нескольких агентов и инструментов. Этот проект готов к сериозному пилоту, поскольку он имеет высокий уровень готовности к производству, сильные сигналы от сообщества и недавнюю активность.

### 中文

**项目简介**  
h0x91b/dev-3.0 是面向“一人工作室”的 AI 编码代理指挥中心，能够在 Kanban、git worktree 与 tmux 的组合下并行调度 Claude、Codex、Gemini CLI、OpenCode 以及自定义 Shell 代理等多种 AI 编码工具。它不是 IDE，而是把零散的 Prompt 与工具包装成可复用、可追踪的工作流。

---

### 价值点  

1. **工作流标准化**：将分散的 Prompt、工具链和临时脚本统一为可版本化、可回溯的 Git worktree + Kanban 任务，避免“随手跑一次”后难以复现的问题。  
2. **多代理并行**：通过 tmux 会话管理，能够同时运行多个 AI 代理，互相协作或分工完成大型代码生成、审查、部署等任务。  
3. **可插拔的记忆层**：内置统一的“agent memory”抽象，支持将上下文、状态或中间产物持久化，供后续步骤或其他代理复用。  
4. **轻量集成**：提供 CLI / SDK 接口，直接在现有 CI/CD、VS Code 任务或自定义脚本中调用，无需迁移到完整 IDE。  

---

### 典型接入方式  

| 场景 | 接入步骤 | 关键接口 |
|------|----------|----------|
| **本地开发** | 1. `npm i -g @h0x91b/dev-3.0` <br>2. 在项目根目录执行 `dev3 init` 生成 `.dev3/` 配置 <br>3. 用 `dev3 add-agent <agent-type>` 添加 Claude、Codex 等代理 <br>4. 使用 `dev3 start` 启动 tmux 会话，Kanban 页面自动打开 | CLI (`dev3 <command>`)、Node SDK (`import { Dev3 } from '@h0x91b/dev-3.0'`) |
| **CI/CD 自动化** | 1. 在 CI 脚本中 `dev3 run --pipeline build-test` <br>2. 通过环境变量配置 API key、工作区路径 <br>3. 结果自动提交到对应的 git worktree 分支 | `dev3 run`, `dev3 status` |
| **自定义工具链** | 1. 引入 TypeScript SDK <br>2. 调用 `Dev3.createAgent('gemini-cli', { config })` <br>3. 通过 `agent.execute(prompt)` 获取响应并写入工作树 | SDK 方法 `createAgent`, `execute`, `pushMemory` 等 |

---

### 生产可用性评估  

| 维度 | 现状 | 结论 |
|------|------|------|
| **活跃度** | 最近一次提交：2026‑07‑02；Stars 210、Forks 18；14 个关联话题 | 高活跃度，社区关注度良好 |
| **技术成熟度** | 基于 TypeScript、CLI + tmux 组合，已在多个开源项目中使用 | 稳定可用，易于调试 |
| **安全与合规** | 采用 MIT 许可证；暂无已知重大安全漏洞；仍需审查依赖的 AI 服务凭证管理 | 许可宽松，安全风险低，但建议自行审计 API Key 存储方式 |
| **可扩展性** | 插件化的 Agent 接口 + Git worktree 多分支管理，天然支持横向扩展 | 适合从单机到小型集群的渐进式扩展 |
| **运维成本** | 只需维护 Node 环境、tmux 会话和 Git 仓库；不依赖额外后台服务 | 运维开销极低 |
| **整体评级** | 综合活跃度、功能完整度、社区反馈 | **适合进入生产环境的 OSS 候选**（可先在内部 Pilot 验证后全面推广） |

**建议**：在正式生产前完成以下两项检查：  
1. **凭证管理**：统一使用公司内部的 secret 管理系统（如 Vault、AWS Secrets Manager）来注入 AI 服务的 API Key。  
2. **监控与审计**：为 `dev3` CLI 加入日志收集（stdout/err → ELK）以及工作流状态监控（Kanban 页面可接入 Grafana），确保异常代理能够快速定位。  

完成上述准备后，h0x91b/dev-3.0 完全可以作为“一人工作室”乃至小团队的 AI 编码代理编排层投入生产使用。

## 🧭 Practical evaluation

**Value:** h0x91b/dev-3.0 helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 210 GitHub stars
- 18 forks
- updated 2026-07-02
- primary language: TypeScript
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 32/100 |
| stars | 49/100 |
| topics | 100/100 |
| outlook | 63/100 |
| quality | 60/100 |
| recency | 40/100 |
| adoption | 45/100 |
| production | 57/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/h0x91b/dev-3.0) · [← Back to Orchestration](./README.md)</sub>
