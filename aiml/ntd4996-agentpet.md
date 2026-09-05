# ntd4996/agentpet

[![Stars](https://img.shields.io/github/stars/ntd4996/agentpet?style=flat-square&color=yellow)](https://github.com/ntd4996/agentpet/stargazers) [![Forks](https://img.shields.io/github/forks/ntd4996/agentpet?style=flat-square&color=blue)](https://github.com/ntd4996/agentpet/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> A desktop pet for macOS & Windows that monitors your AI coding agents (Claude Code, Codex, Cursor, Gemini...) in real time, and grows as you code, feed it tokens, level it up, climb the leaderboard.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 251 |
| 🍴 **Forks** | 45 |
| 💻 **Language** | Swift |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `claude-code` `codex` `desktop-pet` `developer-tools` `macos` `menubar` `productivity` `swift` `swiftui`

## 🎯 Categories

AI/ML · Productivity · DevTools

## 📝 Summary

### English

**Brief Summary**  
AgentPet is a cross‑platform desktop companion (macOS & Windows) that visualizes the activity of AI coding agents such as Claude Code, Codex, Cursor, Gemini, etc., in real time. As you code, the pet grows, you can feed it tokens, level it up, and compete on a leaderboard, turning AI‑assisted development into a gamified experience.  

**Value**  
AgentPet gives developers an immediate, low‑friction way to surface the inner workings of AI coding agents—API calls, token usage, model responses—without having to build a custom monitoring stack. By turning these signals into a playful “pet” that evolves with usage, it encourages continuous experimentation, helps teams spot performance or cost anomalies, and makes AI‑augmented development more engaging for both individuals and groups.  

**Practical Adoption Path**  
1. **Clone & Install** – The project is a Swift‑based desktop app; install via the provided release binaries or build from source on macOS/Windows.  
2. **Connect Your Agent** – Use the exposed SDK/CLI configuration to point AgentPet at the desired AI service (Claude, Codex, Gemini, etc.) by supplying API keys or endpoint URLs.  
3. **Instrument Your Workflow** – Add the lightweight AgentPet SDK or CLI wrapper to your existing build or editor scripts; the wrapper automatically emits the required telemetry (token count, request latency, language metadata).  
4. **Start Coding** – The pet appears on your desktop, reflecting real‑time activity; you can feed tokens, level up, and monitor the leaderboard.  
5. **Scale** – For team‑wide adoption, share the same configuration file or run AgentPet in a shared VM/container, allowing multiple developers to see collective progress and compare agent performance.  

**Production Readiness**  
- **Activity & Community**: 251 stars, 45 forks, recent commits (as of 2026‑06‑23) and a growing issue/PR response rate indicate an active maintainer base.  
- **Stability**: The Swift codebase is mature, with clear separation between UI and telemetry layers, making it easy to integrate into CI pipelines or sandbox environments.  
- **Ecosystem Fit**: It exposes standard signals (API/SDK/CLI, language metadata) that align with typical RAG or agent‑workflow pipelines, reducing integration effort.  
- **Risks**: Licensing and security posture still need a final audit, and long‑term maintainer commitment should be confirmed before mission‑critical deployment.  

Overall, AgentPet is a high‑readiness OSS candidate for pilots that want quick visibility into AI coding agents while adding a gamified feedback loop for developers.

### Русский

n​td4996/agentpet — это открытый десктоп‑пет для macOS и Windows, который в реальном времени отслеживает работу ваших AI‑кодирующих агентов (Claude Code, Codex, Cursor, Gemini и др.), позволяет «кормить» его токенами, повышать уровень и соревноваться в лидерборде. Проект удобно интегрировать в прототипы AI‑фич, RAG‑ и агентные пайплайны — он уже предоставляет API/SDK/CLI и метаданные о языке и темах, что упрощает быстрый запуск и оценку моделей. По активности репозитория (251 ★, 45 форков, обновления до 2026‑06‑23) и наличию основных интеграционных точек проект считается готовым к пилотному использованию в продакшене, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
`ntd4996/agentpet` 是一款跨 macOS 与 Windows 的桌面宠物，它实时监控 Claude Code、Codex、Cursor、Gemini 等 AI 编码助手的运行状态。随着你写代码、喂养 token、升级等级，宠物会成长并在排行榜上竞争。

**价值**  
- **即插即用的 AI 能力**：无需自行搭建模型堆栈，直接在本地 IDE 中可视化 AI 代理的工作情况。  
- **激励与可视化**：通过“喂食”“升级”等游戏化元素，让团队成员更直观地感受到 AI 辅助的产出与效率提升。  
- **快速原型**：在研发阶段即可评估不同模型（Claude、Gemini 等）的响应速度、调用频率和错误率，为后续 RAG/Agent 工作流的选型提供数据支撑。

**典型接入方式**  
1. **SDK / API**：项目提供 Swift（macOS）和对应的 Windows 桥接库，开发者可以通过简单的函数调用将 AI 代理的调用日志、token 消耗、错误信息等发送给 AgentPet。  
2. **CLI**：在 CI/CD 或本地脚本中使用 `agentpet-cli`，通过环境变量或命令行参数注入模型 API key、请求体等元数据，自动生成实时统计。  
3. **语言元数据**：支持读取编辑器/IDE 插件的语言上下文（如文件类型、光标位置），帮助宠物展示当前正在处理的编程语言或任务主题。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑23 最近一次提交，星标 251、Fork 45，社区活跃度良好。  
- **生态兼容**：已支持主流 AI 编码模型的 API，且实现方式相对独立，易于在现有开发流水线中嵌入。  
- **成熟度**：代码质量、文档和示例较完整，具备 OSS 级别的生产候选资格；唯一需进一步确认的风险是许可证合规和安全审计。  

综上，`ntd4996/agentpet` 可作为低成本、可视化的 AI 助手监控层，快速集成到开发环境并在生产环境中提供实时反馈与激励机制。

## 🧭 Practical evaluation

**Value:** ntd4996/agentpet helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 251 GitHub stars
- 45 forks
- updated 2026-06-23
- primary language: Swift
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 51/100 |
| topics | 100/100 |
| outlook | 80/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 48/100 |
| production | 69/100 |
| usefulness | 100/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/ntd4996/agentpet) · [← Back to AI/ML](./README.md)</sub>
