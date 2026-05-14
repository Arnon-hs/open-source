# officecli/officecli

[![Stars](https://img.shields.io/github/stars/officecli/officecli?style=flat-square&color=yellow)](https://github.com/officecli/officecli/stargazers) [![Forks](https://img.shields.io/github/forks/officecli/officecli?style=flat-square&color=blue)](https://github.com/officecli/officecli/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> AI agent skills for Claude Code and Codex to create PPTX, DOCX, XLSX, and report workflows with OfficeCLI.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 38 |
| 🍴 **Forks** | 2 |
| 💻 **Language** | Shell |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-tools` `ai-agents` `automation` `claude-code` `codex` `docx` `gpt` `office` `office-documents` `officecli` `openclaw` `pptx`

## 🎯 Categories

Orchestration · Automation · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
OfficeCLI is an open‑source AI‑agent framework that equips Claude Code and Codex with reusable “skills” for generating PowerPoint, Word, Excel, and custom report artifacts. By stitching together isolated prompts and tool calls, it lets developers define repeatable, multi‑agent workflows that can be invoked via an API, SDK, or CLI.

**Value**  
- **Turn ad‑hoc prompts into pipelines** – What normally requires a manual copy‑paste of prompts and scripts becomes a declarative workflow that can be version‑controlled and shared.  
- **Multi‑agent orchestration** – Agents can hand off work (e.g., a content‑generation agent writes a DOCX, then a formatting agent converts it to PPTX) without custom glue code.  
- **Standardised memory & tool use** – Built‑in support for persisting context and invoking external tools (file I/O, data pulls) reduces boiler‑plate and improves consistency across projects.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided shell CLI locally, and experiment with the sample “create‑pptx” and “generate‑report” skills.  
2. **Integrate** – Wrap the CLI or call the exposed SDK from your CI/CD pipelines or internal services; the language‑agnostic API makes it easy to embed in Python, Node, or Bash workflows.  
3. **Extend** – Add new skills by defining prompt templates and tool wrappers; the repository’s topic tags and clear folder layout simplify contribution.  
4. **Govern** – Pin the repository version, audit the license, and run a security scan on the shell scripts before promoting to a shared internal registry.

**Production Readiness**  
- **Maturity** – Medium. The project is actively maintained (last commit 2026‑05‑14) and has a modest but growing community (38 ★, 2 forks).  
- **Dependencies** – Relies on Claude Code/Codex APIs and standard shell tooling; these need version locking and monitoring for breaking changes.  
- **Risks** – License and long‑term maintainership have not been fully vetted; security posture of the shell scripts should be reviewed.  
- **Suitability** – Ideal for prototypes, internal automation, or as a “glue” layer in larger AI‑augmented pipelines, but requires a final security and compliance audit before mission‑critical production use.

### Русский

**officecli/officecli** — это набор AI‑агентских навыков для Claude Code и Codex, позволяющих автоматически генерировать презентации (PPTX), документы (DOCX), таблицы (XLSX) и сложные отчётные пайплайны через единый интерфейс OfficeCLI. Типичный сценарий — интеграция в существующие CI/CD или внутренние боты, где несколько агентов последовательно используют инструменты Office, стандартизируя их память и упрощая повторяемость рабочих процессов. Проект находится на среднем уровне готовности к production: достаточно стабилен для прототипов и внутренних автоматизаций, но требует проверки лицензии, безопасности и поддержки зависимостей перед масштабным развертыванием.

### 中文

**项目简介**  
officecli 是一个基于 Claude Code 与 Codex 的 AI Agent 技能集合，能够在命令行下自动生成 PPTX、DOCX、XLSX 文档以及完整的报告工作流。它把零散的 Prompt 与工具封装成可重复执行的 Agent 流程，帮助团队实现 Office 文档的批量化、可编程化处理。

**价值**  
- **统一工作流**：将多 Agent、多工具的交互抽象为可复用的流水线，避免手动切换和重复操作。  
- **提升效率**：通过 AI 自动撰写、排版、数据填充等步骤，显著缩短 PPT、报告、表格的产出周期。  
- **标准化记忆**：内置 Agent memory，保证上下文在同一工作流内持续，可用于审计和二次迭代。

**典型接入方式**  
1. **CLI**：直接在终端调用 `officecli <subcommand> [options]` 完成文档生成。  
2. **SDK/API**：项目公开了 REST‑like 接口（`/generate/pptx`, `/generate/docx` 等），可在 CI/CD、内部服务或前端页面中嵌入调用。  
3. **脚本编排**：配合 Shell、Makefile 或 GitHub Actions，构建自动化流水线，例如：  
   ```bash
   officecli generate pptx --prompt "季度业绩报告" --data data.xlsx -o output.pptx
   ```

**生产可用性**  
- **成熟度**：当前评分 71/100，适合作为原型或内部业务流程的快速实现。  
- **依赖与维护**：项目主要使用 Shell 编写，依赖少，易于审计；但仍需自行检查许可证兼容性、第三方 AI 服务的安全与成本。  
- **准备度**：已更新至 2026‑05‑14，拥有 38 星、2 次 fork，社区活跃度一般。建议在正式生产前进行：  
  - 安全审计（API 密钥、网络访问）  
  - 性能基准（大批量文档生成时的响应时间）  
  - 监控与回滚机制（Agent 失败时的补偿策略）  

总体而言，officecli 能够帮助企业快速搭建可重复的 Office 文档自动化流程，适合内部工具或原型项目；在完成上述生产检查后即可投入更大规模的业务使用。

## 🧭 Practical evaluation

**Value:** officecli/officecli helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 38 GitHub stars
- 2 forks
- updated 2026-05-14
- primary language: Shell
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 12/100 |
| stars | 34/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 67/100 |
| recency | 100/100 |
| adoption | 28/100 |
| production | 72/100 |
| usefulness | 100/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/officecli/officecli) · [← Back to Orchestration](./README.md)</sub>
