# Dicklesworthstone/destructive_command_guard

[![Stars](https://img.shields.io/github/stars/Dicklesworthstone/destructive_command_guard?style=flat-square&color=yellow)](https://github.com/Dicklesworthstone/destructive_command_guard/stargazers) [![Forks](https://img.shields.io/github/forks/Dicklesworthstone/destructive_command_guard?style=flat-square&color=blue)](https://github.com/Dicklesworthstone/destructive_command_guard/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> The Destructive Command Guard (dcg) is for blocking dangerous git and shell commands from being executed by agents.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1k |
| 🍴 **Forks** | 57 |
| 💻 **Language** | Rust |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `cli` `developer-tools` `git` `rust` `safety`

## 🎯 Categories

AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The Destructive Command Guard (dcg) is an open‑source Rust library that intercepts and blocks hazardous Git and shell commands before they can be run by AI agents or automation scripts. By providing a lightweight API/CLI, it lets developers embed safety checks into agent‑driven workflows, reducing the risk of accidental data loss or system compromise. With over a thousand stars, active maintenance, and recent commits, it is ready for pilot projects and early‑stage production use.

**Value**  
- **Safety‑first guardrail**: Prevents agents from executing destructive operations (e.g., `git reset --hard`, `rm -rf`) without having to rewrite the agent’s core logic.  
- **AI‑ready integration**: The library can be called from any language that can invoke a Rust binary or through its SDK, making it easy to add “danger‑detection” to RAG pipelines, tool‑using agents, or custom LLM‑driven assistants.  
- **Speed to market**: Because the guard is pre‑built and open source, teams can prototype AI‑enhanced tooling without developing their own command‑filtering layer from scratch.

**Practical Adoption Path**  
1. **Evaluate** – Clone the repo, run the provided CLI on a sandboxed set of commands, and review the detection rules.  
2. **Integrate** – Add the `dcg` crate to a Rust project or call the compiled binary from Python/Node/Go via a subprocess/HTTP wrapper.  
3. **Customize** – Extend the rule set (JSON/YAML) to match your organization’s policy (e.g., block specific repository paths or disallow `sudo`).  
4. **Deploy** – Wrap the guard around any agent executor (e.g., LangChain tool, AutoGPT plugin) so that every generated command passes through `dcg` first.  
5. **Monitor** – Use the built‑in logging/telemetry to audit blocked attempts and refine the rule set.

**Production Readiness**  
- **Activity & Community**: 1,013 stars, 57 forks, recent commit (2026‑05‑12), and a modest but active contributor base.  
- **Maturity**: Core functionality (command parsing, rule engine) is stable; the Rust implementation offers strong performance and memory safety.  
- **Ecosystem Fit**: Exposes both an API and a CLI, making it language‑agnostic for typical AI agent stacks.  
- **Risks**: Licensing and long‑term maintainer commitment need a final check, and a formal security audit is advisable before wide‑scale rollout.  

Overall, dcg is a high‑readiness OSS component that can be quickly piloted to add a critical safety layer to AI‑driven automation, with a clear path to production deployment after minor due‑diligence steps.

### Русский

Destructive Command Guard (dcg) — это Rust‑библиотека, позволяющая агентам безопасно блокировать опасные git‑ и shell‑команды, что упрощает добавление AI‑функционала без построения модели «с нуля». Ее обычно интегрируют в прототипы RAG‑ или агентных воркфлоу, где требуется быстрый контроль над выполнением потенциально разрушительных команд через API/SDK/CLI. Проект обладает высокой готовностью к production: активные коммиты, более 1000 звёзд, значительное количество форков и сильные сигналы экосистемы, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
Destructive Command Guard（dcg）是一款用 Rust 编写的安全工具，能够在 AI 代理执行任务时拦截并阻止危险的 Git 与 Shell 命令，防止意外破坏或安全泄露。

**价值**  
- **安全防护**：在自动化工作流或 RAG/Agent 场景中实时过滤高危指令，降低因代码生成或模型误判导致的系统破坏风险。  
- **快速集成 AI 能力**：提供现成的拦截层，开发者无需从零实现安全检查，即可在现有模型或工具链上直接加入防护。  
- **社区与生态支持**：拥有 1 013+ Stars、活跃的维护者和 Rust 生态的高性能实现，适合作为生产级安全组件。

**典型接入方式**  
1. **SDK / API**：在代理的执行入口调用 `dcg::guard::check(command)`，返回拦截结果或错误信息。  
2. **CLI**：将 `dcg` 作为前置过滤器，在 CI/CD、容器启动脚本或自定义 shell 中包装实际的 Git/Shell 命令。  
3. **语言绑定**：通过官方提供的 Rust 库或社区维护的 Python/Node 绑定，将拦截逻辑嵌入任意语言的 Agent 实现中。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑05‑12，代码维护频繁，issues 响应及时。  
- **成熟度**：已有 57 个 Fork，多个项目在内部使用，证明其在真实业务场景下可运行。  
- **安全审计**：目前未发现重大许可证或安全漏洞风险，仍建议在正式上线前进行内部安全评估。  

综上，Destructive Command Guard 具备高性能、易集成的特性，是在 AI 代理或自动化脚本中实现命令安全防护的可靠 OSS 选项。

## 🧭 Practical evaluation

**Value:** Dicklesworthstone/destructive_command_guard helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1013 GitHub stars
- 57 forks
- updated 2026-05-12
- primary language: Rust
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 64/100 |
| topics | 75/100 |
| outlook | 57/100 |
| quality | 58/100 |
| recency | 20/100 |
| adoption | 58/100 |
| production | 49/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/Dicklesworthstone/destructive_command_guard) · [← Back to AI/ML](./README.md)</sub>
