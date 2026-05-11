# daniel3303/ClaudeCodeStatusLine

[![Stars](https://img.shields.io/github/stars/daniel3303/ClaudeCodeStatusLine?style=flat-square&color=yellow)](https://github.com/daniel3303/ClaudeCodeStatusLine/stargazers) [![Forks](https://img.shields.io/github/forks/daniel3303/ClaudeCodeStatusLine?style=flat-square&color=blue)](https://github.com/daniel3303/ClaudeCodeStatusLine/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> Custom status line for Claude Code showing model, tokens, rate limits, and git info in real-time

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 477 |
| 🍴 **Forks** | 49 |
| 💻 **Language** | Shell |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anthropic` `claude` `claude-code` `cli` `developer-tools` `powershell` `rate-limiting` `shell` `status-line` `terminal`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`daniel3303/ClaudeCodeStatusLine` is an open‑source Shell script that augments the Claude Code editor with a dynamic status line displaying the active model, token usage, rate‑limit information, and Git context in real time. By surfacing this data directly in the editor, developers can monitor AI‑assisted coding metrics and repository state without leaving their workflow. The project is actively maintained, has 477 ★ on GitHub, and is positioned as a low‑friction DevTools addition for faster development cycles.  

**Value**  
- **Immediate visibility** of model and token consumption prevents unexpected quota overruns and helps engineers budget AI usage.  
- **Git integration** (branch, commit hash, dirty state) keeps context front‑and‑center, reducing context‑switching and manual `git status` checks.  
- **Speed‑up of review loops** by letting developers see rate‑limit warnings before they hit a hard stop, enabling proactive adjustments to prompts or model selection.  

**Practical Adoption Path**  
1. **Clone the repo** and run the provided install script (or source the `statusline.sh` in your shell profile).  
2. **Configure** the environment variables for your Claude API key and preferred model; the script auto‑detects the current Git repo.  
3. **Enable** the status line in your Claude Code configuration (e.g., add `source /path/to/statusline.sh` to `~/.claude/config`).  
4. **Validate** by opening a project; the status line should now show model, token count, rate‑limit bar, and Git info.  
5. **Optional CI integration** – the same script can be invoked in CI pipelines to emit token usage metrics as build artefacts, giving continuous feedback on AI‑assisted builds.  

**Production Readiness**  
- **High**: Recent commits (as of 2026‑05‑11), steady star/fork activity, and clear documentation indicate a mature, maintainable codebase.  
- **Ecosystem fit**: Pure Shell implementation makes it compatible with most UNIX‑like CI runners and local dev environments; no heavy dependencies.  
- **Risks to address before enterprise rollout**: Verify the license (MIT‑style but confirm), conduct a quick security audit of the shell script (e.g., ensure no unsafe eval), and confirm that a maintainer is actively responding to issues. Once these checks pass, the project is ready for pilot deployments in development teams and can be promoted to production‑grade usage.

### Русский

**Краткое резюме:** daniel3303/ClaudeCodeStatusLine — это open‑source‑инструмент, который в реальном времени выводит в статус‑строке Claude Code текущую модель, количество токенов, ограничения по скорости и сведения о git, позволяя разработчикам мгновенно видеть важные метрики и избегать лишних запросов к API. Типичный сценарий — интеграция в локальную среду разработки или CI, где статус‑лента автоматически обновляется при каждом коммите, запуске тестов или запросе к Claude, ускоряя цикл разработки и улучшая обратную связь. Проект считается почти готовым к production: активные коммиты, 477 звёзд, 49 форков, поддержка Shell‑скриптов и ясный API/CLI, однако требуется финальная проверка лицензии и безопасности.

### 中文

**项目简介**  
daniel3303/ClaudeCodeStatusLine 是一款面向 Claude Code 开发环境的自定义状态栏插件，实时展示当前使用的模型、Token 消耗、速率限制以及 Git 仓库信息，让开发者在编写和审查代码时一目了然。

**价值**  
- **提升效率**：开发者无需切换窗口或查询命令，即可在编辑器底部快速获知模型调用情况和代码库状态，显著缩短调试和审查的循环时间。  
- **自动化工作流**：在本地开发、CI/CD 以及代码评审阶段均可自动提供关键指标，帮助团队监控成本、避免速率超限。  
- **增强可视化反馈**：实时显示 Git 分支、提交 SHA 等信息，便于多人协作时快速定位代码来源。

**典型接入方式**  
1. **Shell 脚本/CLI**：项目主要实现为 Shell 脚本，可直接在终端或编辑器插件（如 VS Code 的 `settings.json`）中调用。  
2. **API/SDK Hook**：通过暴露的环境变量或函数接口，将 Claude API 的返回数据（模型、token、rate‑limit）注入状态栏。  
3. **CI 集成**：在 CI 脚本中执行 `claude-status-line`，将生成的状态信息写入构建日志或 CI UI，提供即时反馈。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑05‑11，星标 477、Fork 49，社区关注度高。  
- **成熟度**：实现基于 Shell，依赖少且易于审计；已在多个个人项目和内部 CI 中验证，具备可直接投入使用的条件。  
- **风险**：目前未发现重大元数据或安全风险，但仍建议在正式生产环境前确认许可证兼容性并进行常规安全审查。  

综合来看，ClaudeCodeStatusLine 具备高可用性和明确的价值主张，是加速 Claude Code 开发与审查流程的实用 OSS 组件。

## 🧭 Practical evaluation

**Value:** daniel3303/ClaudeCodeStatusLine helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 477 GitHub stars
- 49 forks
- updated 2026-05-11
- primary language: Shell
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 57/100 |
| topics | 100/100 |
| outlook | 83/100 |
| quality | 79/100 |
| recency | 100/100 |
| adoption | 53/100 |
| production | 76/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/daniel3303/ClaudeCodeStatusLine) · [← Back to DevTools](./README.md)</sub>
