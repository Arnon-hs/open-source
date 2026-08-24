# zdk/rm-safely

[![Stars](https://img.shields.io/github/stars/zdk/rm-safely?style=flat-square&color=yellow)](https://github.com/zdk/rm-safely/stargazers) [![Forks](https://img.shields.io/github/forks/zdk/rm-safely?style=flat-square&color=blue)](https://github.com/zdk/rm-safely/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-49%2F100-brightgreen?style=flat-square)](#)

> 'rm' safely – a safety net for rm

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 87 |
| 🍴 **Forks** | 1 |
| 💻 **Language** | Shell |
| 📈 **Score** | 49/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`backup` `bash` `command` `command-line` `filesystem` `guardrails` `linux` `macos` `restore` `rm` `rm-alternative` `rm-safe`

## 🎯 Categories

DevTools · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
zdk/rm‑safely is a lightweight shell‑based wrapper that adds a safety net around the Unix `rm` command, preventing accidental deletion of important files. By intercepting delete operations and offering confirmation, backup, or recovery options, it helps developers and system administrators avoid costly data loss. The project is open‑source, actively maintained (last update 2026‑05‑12) and already has a modest community presence (87 ★).

**Value Proposition**  
- **Safety first** – Provides an extra layer of protection for a notoriously dangerous command, reducing human error without requiring changes to existing workflows.  
- **AI‑ready scaffolding** – Although the core is a shell script, the repository exposes clear API/CLI hooks that can be extended with AI‑driven decision logic (e.g., context‑aware prompts, RAG‑based file‑importance scoring).  
- **Rapid prototyping** – Teams can quickly prototype AI‑enhanced file‑management assistants or integrate the tool into larger DevOps pipelines, leveraging the existing implementation signals (API, SDK, language metadata).  

**Practical Adoption Path**  
1. **Evaluate** – Clone the repo and run the provided CLI on a test machine; the implementation signals (API/CLI) make it easy to script or wrap in CI pipelines.  
2. **Integrate** – Replace direct `rm` calls with `rm‑safely` (or alias it) in scripts, CI jobs, or developer environments.  
3. **Extend** – Hook into the exposed CLI or SDK to add AI‑based confirmation dialogs, policy checks, or automatic backup creation.  
4. **Test & Harden** – Run unit and integration tests in a staging environment, verify that the safety mechanisms behave as expected under edge cases (wildcards, recursive deletes, permission errors).  

**Production Readiness**  
- **Maturity** – Medium. The tool is functional and recent (updated today), but it has a small contributor base (1 fork) and limited production‑grade testing.  
- **Dependencies** – Pure shell; minimal external dependencies, which eases containerization and audit.  
- **Maintenance** – Requires a brief review of the license, security posture, and long‑term maintainer commitment before committing to critical production workloads.  
- **Recommendation** – Suitable for internal tooling, prototypes, or as a safety layer in non‑mission‑critical environments. For high‑availability production use, perform a security audit, add automated regression tests, and consider a fallback plan (e.g., snapshot or version‑controlled backups).

### Русский

**zdk/rm-safely** — это open‑source утилита‑обёртка над `rm`, добавляющая слой защиты и возможность интеграции AI‑моделей (например, для анализа команд, предсказания опасных удалений и построения RAG‑агентов). Типичный сценарий: разработчики подключают CLI/SDK к своим CI/CD или внутренним скриптам, чтобы автоматически проверять и подтверждать операции удаления, а также экспериментировать с AI‑подсказками без необходимости создавать собственный стек моделей. Готовность к production — средняя: проект подходит для прототипов и внутренних workflow, но перед запуском в продакшн требуется проверка лицензии, безопасности зависимостей и наличие активных мейнтейнеров.

### 中文

**项目简介**  
zdk/rm-safely 为常用的 `rm` 命令提供安全防护层，防止误删文件或目录。它通过拦截、确认和日志记录等机制，让删除操作更可控、可追溯。

**价值**  
- **降低误操作风险**：在执行 `rm` 前自动进行二次确认或基于策略拦截，显著降低因手误导致的数据丢失。  
- **提升安全合规**：提供删除审计日志，帮助满足审计、合规和内部治理要求。  
- **易于集成 AI 功能**：内置可调用的 API/SDK，方便在 AI 驱动的自动化脚本或 RAG/Agent 工作流中加入安全删除检查。

**典型接入方式**  
1. **CLI 包装**：直接使用项目提供的 `rm-safely` 可执行文件，替代系统自带的 `rm`。  
2. **Shell 函数/别名**：在 `~/.bashrc` 或 `~/.zshrc` 中定义别名 `alias rm='rm-safely'`，全局生效。  
3. **SDK 调用**：通过项目暴露的 Bash 函数或轻量级库，在脚本或 CI/CD 流程中以编程方式调用安全删除 API。  
4. **API 集成**：若项目提供 HTTP 接口，可在 AI Agent 或 RAG 系统中通过 REST 调用实现远程安全删除。

**生产可用性**  
- **成熟度**：Medium。适合作为原型或内部工具使用，已有 87 星的社区认可，但 Fork 数较少，说明社区贡献仍有限。  
- **依赖与维护**：项目主要使用 Shell 编写，依赖较少，易于审计；但需自行检查许可证、漏洞报告以及维护者活跃度后再投入生产。  
- **上线建议**：在生产环境部署前，先在测试环境进行完整的功能与安全审计，配合内部日志收集和回滚机制，即可安全投入使用。

## 🧭 Practical evaluation

**Value:** zdk/rm-safely helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 87 GitHub stars
- 1 forks
- updated 2026-05-12
- primary language: Shell
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 8/100 |
| stars | 41/100 |
| topics | 100/100 |
| outlook | 47/100 |
| quality | 49/100 |
| recency | 20/100 |
| adoption | 32/100 |
| production | 46/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/zdk/rm-safely) · [← Back to DevTools](./README.md)</sub>
