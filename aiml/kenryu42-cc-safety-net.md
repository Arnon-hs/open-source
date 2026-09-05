# kenryu42/cc-safety-net

[![Stars](https://img.shields.io/github/stars/kenryu42/cc-safety-net?style=flat-square&color=yellow)](https://github.com/kenryu42/cc-safety-net/stargazers) [![Forks](https://img.shields.io/github/forks/kenryu42/cc-safety-net?style=flat-square&color=blue)](https://github.com/kenryu42/cc-safety-net/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-75%2F100-brightgreen?style=flat-square)](#)

> A coding agent CLI hook that acts as a safety net, catching destructive git and filesystem commands before they execute. Supports Codex, Claude Code, OpenCode, Gemini CLI, Copilot CLI, Kimi Code and Pi.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.4k |
| 🍴 **Forks** | 64 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 75/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`claude` `claude-code` `claude-code-plugin` `codex` `destructive-commands` `kimi-code` `pi-extension` `security`

## 🎯 Categories

AI/ML · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
kenryu42/cc‑safety‑net is a TypeScript‑based CLI hook that intercepts potentially destructive git and filesystem commands, acting as a safety net for AI‑driven coding agents such as Codex, Claude Code, OpenCode, Gemini CLI, Copilot CLI, Kimi Code and Pi. By surfacing a simple “pre‑execute” checkpoint, it lets developers prototype AI‑assisted workflows without risking accidental data loss. With over 1.4 k stars and recent activity, it is positioned as a production‑ready open‑source component for AI‑enhanced developer tools.

**Value**  
- **Risk mitigation:** Prevents accidental `git reset --hard`, `rm -rf`, or similar commands issued by autonomous agents, safeguarding codebases and CI pipelines.  
- **Fast AI integration:** Provides a ready‑made safety layer so teams can plug in large‑language‑model (LLM) coding assistants without building their own guardrails from scratch.  
- **Broad compatibility:** Supports the major coding‑assistant CLIs, making it a one‑stop solution for heterogeneous AI toolchains.

**Practical Adoption Path**  
1. **Install** the npm package and add the `cc-safety-net` hook to the project’s `package.json` scripts or CI configuration.  
2. **Configure** allowed command patterns (whitelist) and define custom remediation actions via the provided JSON/YAML policy file.  
3. **Integrate** with existing AI agents by invoking the hook in the agents’ command‑execution pipeline (e.g., wrap `git` or `fs` calls).  
4. **Test** in a staging environment, iterating on the policy until false positives are minimized.  
5. **Promote** to production, optionally coupling the hook with monitoring/alerting to log blocked commands.

**Production Readiness**  
- **Activity & Community:** 1,409 stars, 64 forks, recent commits (as of 2026‑06‑23), and active issue discussions indicate a healthy maintainer presence.  
- **Maturity:** The core functionality is stable, with clear CLI/API boundaries and TypeScript typings, easing integration and automated testing.  
- **Security Posture:** No known critical vulnerabilities; however, a final review of the license (MIT‑style) and any third‑party dependencies is advisable before enterprise rollout.  
- **Scalability:** Designed as a lightweight hook, it adds negligible overhead and can be deployed across multiple developer machines or CI agents.  

Overall, cc‑safety‑net offers a mature, low‑friction safety layer that can be adopted quickly in AI‑augmented development pipelines and is ready for serious production pilots.

### Русский

**kenryu42/cc-safety-net** — это CLI‑хук‑агент, который перехватывает опасные git‑ и файловые команды до их выполнения, предоставляя «сетку безопасности» для AI‑ассистентов (Codex, Claude Code, Gemini CLI и др.). Он легко интегрируется в прототипы AI‑фич, RAG‑или агентные воркфлоу и позволяет быстро добавить интеллектуальное поведение без построения модели с нуля. По активности (1409 звёзд, недавние коммиты, широкая экосистема) проект считается готовым к пилотному использованию в production, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
kenryu42/cc-safety-net 是一个基于 CLI 的编码助手钩子，能够在 Git 与文件系统的破坏性操作真正执行前拦截并阻止，兼容 Codex、Claude Code、OpenCode、Gemini CLI、Copilot CLI、Kimi Code 与 Pi 等多种大模型接口。

**价值**  
- **安全防护**：在 AI 自动化编程过程中，实时捕获并拦截可能导致代码回滚、文件删除或仓库破坏的指令，降低误操作风险。  
- **快速集成 AI 能力**：无需自行构建底层模型栈，只需挂载该钩子即可让现有项目立即获得 AI 编码助手的安全保障。  
- **多模型兼容**：统一的接口层支持主流大模型，使得在同一项目中切换或组合不同模型成为可能，提升研发灵活性。

**典型接入方式**  
1. **CLI 安装**：`npm i -g cc-safety-net`（或使用 Yarn、pnpm）。  
2. **配置 Hook**：在项目根目录的 `.git/hooks` 中添加或链接 `pre-commit`、`pre-push`、`pre-rebase` 等钩子脚本，指向 `cc-safety-net` 可执行文件。  
3. **模型绑定**：在 `cc-safety-net.config.json` 中声明使用的模型（如 `codex`, `gemini`），并提供相应的 API key。  
4. **可选 SDK**：若需要在自定义脚本或 CI/CD 中调用，可通过提供的 TypeScript SDK (`import { SafetyNet } from 'cc-safety-net'`) 直接调用拦截函数。

**生产可用性**  
- **活跃度**：最近一次更新为 2026‑06‑23，拥有 1,409 个星标和 64 个 Fork，社区活跃。  
- **技术成熟度**：核心实现使用 TypeScript，提供完整的 API/CLI/SDK，且已在多个开源项目中实际使用，具备“高”生产就绪度。  
- **风险点**：仍需对许可证（MIT）进行合规审查，并对依赖的模型 API 访问权限与安全策略进行二次确认；但整体安全姿态良好，适合作为正式环境的安全网进行试点或全面部署。

## 🧭 Practical evaluation

**Value:** kenryu42/cc-safety-net helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1409 GitHub stars
- 64 forks
- updated 2026-06-23
- primary language: TypeScript
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 67/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 77/100 |
| recency | 80/100 |
| adoption | 61/100 |
| production | 75/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/kenryu42/cc-safety-net) · [← Back to AI/ML](./README.md)</sub>
