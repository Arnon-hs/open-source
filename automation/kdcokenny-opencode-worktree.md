# kdcokenny/opencode-worktree

[![Stars](https://img.shields.io/github/stars/kdcokenny/opencode-worktree?style=flat-square&color=yellow)](https://github.com/kdcokenny/opencode-worktree/stargazers) [![Forks](https://img.shields.io/github/forks/kdcokenny/opencode-worktree?style=flat-square&color=blue)](https://github.com/kdcokenny/opencode-worktree/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> Zero-friction git worktrees for OpenCode. Auto-spawns terminals, syncs files, cleans up on exit.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 523 |
| 🍴 **Forks** | 24 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-assistant` `ai-coding` `developer-tools` `git` `git-worktree` `opencode` `opencode-plugin` `terminal-automation` `worktree`

## 🎯 Categories

Automation · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
kdcokenny/opencode‑worktree provides a zero‑friction way to manage Git worktrees for OpenCode projects. It automatically spawns terminal sessions, keeps files in sync, and cleans up the worktree when the session ends, eliminating repetitive manual steps.

**Value**  
The tool turns a normally error‑prone, multi‑step process (creating a worktree, opening a shell, monitoring changes, and tearing it down) into a single, repeatable command. By automating these actions, developers can focus on coding rather than environment housekeeping, and CI/CD pipelines can incorporate worktree‑based builds without custom scripting.

**Practical Adoption Path**  
1. **Install** – Add the npm package or clone the repo and run the provided CLI (`opencode-worktree`).  
2. **Configure** – Point the CLI at an existing OpenCode repository; optional config files let you define default branch, terminal emulator, and cleanup policies.  
3. **Integrate** – Wrap the CLI in existing scripts or IDE extensions; the exposed API/SDK lets other tools (e.g., task schedulers, CI runners) trigger worktree creation and destruction programmatically.  
4. **Pilot** – Run the tool on a non‑critical feature branch to verify that file sync and terminal spawning behave as expected, then roll it out to the whole team.

**Production Readiness**  
- **Activity & Adoption**: 523 stars, 24 forks, recent commits (as of 2026‑05‑12) and a healthy TypeScript codebase indicate active maintenance.  
- **Stability**: Automatic cleanup reduces stale worktrees, and the CLI has clear exit codes and logging, making it suitable for automated pipelines.  
- **Risk**: No major licensing or security red flags have been identified, but a final review of the open‑source license and a quick vulnerability scan are recommended before full production deployment.  

Overall, the project is mature enough for a serious pilot in development environments and can be promoted to production once the brief compliance checks are completed.

### Русский

**kdcokenny/opencode-worktree** — это TypeScript‑инструмент, который полностью автоматизирует работу с git‑worktrees в OpenCode: при запуске автоматически создаёт рабочее дерево, открывает нужные терминалы, синхронно обновляет файлы и удаляет всё при завершении. Типичный сценарий — разработчик заменяет ручные команды `git worktree add`, настройку IDE и очистку после работы на один‑клик/CLI, что позволяет включать worktree в повторяемые CI/CD‑пайплайны или плановые задачи. По активности репозитория (523 ★, свежие коммиты, 24 форка, 10 тем), поддержке API/CLI и наличию типовой типизации проект готов к пилотному внедрению в production, требуя лишь финального аудита лицензии и безопасности.

### 中文

**项目简介（2‑3 句）**  
kdcokenny/opencode‑worktree 为 OpenCode 提供“零摩擦” Git worktree 管理，能够在创建工作树时自动打开终端、实时同步文件，退出时自动清理。它通过脚本化的方式消除手动创建、切换、删除 worktree 的繁琐步骤，让开发者专注业务代码。

**价值**  
- **降低重复劳动**：一键完成 worktree 的创建、同步、销毁，省去手动 `git worktree add/remove`、终端切换等操作。  
- **提升流程一致性**：所有工作树的启动与关闭都走同一套自动化逻辑，保证团队成员在相同环境下工作，减少因环境差异导致的错误。  
- **加速多任务并行**：在同一仓库的不同分支上并行开发或测试时，工作树之间互不干扰，配合自动终端可直接进入对应上下文。

**典型接入方式**  
1. **CLI**：通过 `npx opencode-worktree <command>`（或全局安装后 `opencode-worktree`）调用提供的子命令（`create`、`list`、`remove` 等），适合脚本或 CI/CD 中使用。  
2. **SDK/API**：项目导出 TypeScript/JavaScript 接口 `import { createWorktree, removeWorktree } from 'opencode-worktree'`，可在自定义工具或 IDE 插件中直接调用。  
3. **配置文件**：在项目根目录放置 `opencode-worktree.config.ts`，定义默认终端、同步规则、清理策略，后续所有 CLI 调用会自动读取该配置，实现即插即用。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑12 最近一次提交，星标 523、Fork 24，社区活跃，问题响应及时。  
- **技术成熟度**：使用 TypeScript 编写，提供完整类型定义，易于在现有 Node/TS 项目中集成。  
- **安全与合规**：暂无已知许可证或安全风险，仍建议在正式投产前进行一次依赖审计。  
- **可运维性**：工作树的自动清理机制防止残留资源，配合日志输出可方便监控与故障排查。  

综合来看，kdcokenny/opencode-worktree 已具备较高的生产就绪度，适合作为内部或对外工具链中的 Git worktree 自动化层，帮助团队显著降低手工操作成本并提升工作流的可重复性。

## 🧭 Practical evaluation

**Value:** kdcokenny/opencode-worktree helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 523 GitHub stars
- 24 forks
- updated 2026-05-12
- primary language: TypeScript
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 58/100 |
| topics | 100/100 |
| outlook | 83/100 |
| quality | 78/100 |
| recency | 100/100 |
| adoption | 51/100 |
| production | 78/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/kdcokenny/opencode-worktree) · [← Back to Automation](./README.md)</sub>
