# expo/skills

[![Stars](https://img.shields.io/github/stars/expo/skills?style=flat-square&color=yellow)](https://github.com/expo/skills/stargazers) [![Forks](https://img.shields.io/github/forks/expo/skills?style=flat-square&color=blue)](https://github.com/expo/skills/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> A collection of AI agent skills for working with Expo projects and Expo Application Services

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.1k |
| 🍴 **Forks** | 105 |
| 💻 **Language** | Shell |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Orchestration · AI/ML

## 📝 Summary

### English

**Summary**  
expo/skills is an open‑source library that bundles ready‑made AI‑agent “skills” for interacting with Expo projects and Expo Application Services. It lets you stitch isolated prompts and command‑line tools into repeatable, multi‑agent workflows, making it easier to coordinate tool‑use pipelines and maintain a shared agent memory.  

**Value**  
- **Rapid workflow composition** – Turn one‑off prompts into reusable, composable actions (e.g., building, publishing, or querying an Expo app) without writing custom glue code.  
- **Multi‑agent orchestration** – Provide a common skill set that multiple agents can call, enabling coordinated tasks such as CI/CD, diagnostics, or feature flag toggling across Expo services.  
- **Standardised memory & tooling** – By using a shared skill catalogue, agents can store and retrieve context consistently, reducing duplication and error‑prone ad‑hoc scripts.  

**Practical adoption path**  
1. **Clone & inspect** – Pull the repository, review the `skills/*.sh` scripts and their dependencies (Node, Expo CLI, etc.).  
2. **Prototype locally** – Run a few skills against a sandbox Expo project to verify expected behavior and understand required environment variables.  
3. **Integrate into your orchestration layer** – Wrap the desired skills in your agent framework (e.g., LangChain, CrewAI) using simple shell‑execution calls or a thin wrapper library.  
4. **Add validation & logging** – Because metadata is sparse, instrument each skill with explicit success/failure signals and log outputs for easier debugging.  
5. **Gradual rollout** – Deploy the new skill‑driven workflows to a staging environment, monitor for missing dependencies or permission issues, then promote to production once stable.  

**Production readiness**  
- **Maturity**: Medium. The repo is actively maintained (last update 2026‑06‑25) and has a solid community signal (2.1 k stars, 105 forks), but the integration surface is not well documented.  
- **Risk**: The path to embed the skills into an existing AI‑agent stack requires manual inspection and possibly custom wrappers; missing metadata can increase setup cost.  
- **Recommendation**: Suitable for prototypes, internal tools, or teams already comfortable with shell‑based automation. Before committing to production, perform a dependency audit, add robust error handling, and establish automated tests around the skill executions.

### Русский

**expo/skills** — набор готовых навыков AI‑агентов для автоматизации работы с проектами Expo и сервисом Expo Application Services. Он позволяет превратить разрозненные подсказки и инструменты в повторяемые многокомпонентные рабочие процессы (координация нескольких агентов, построение конвейеров с использованием инструментов, стандартизация памяти агента). Проект уже имеет 2121 звезду на GitHub и активные обновления, но из‑за скудных метаданных путь интеграции требует ручного анализа; поэтому он подходит для прототипов и внутренних процессов, а для production‑использования необходимы дополнительные проверки зависимостей и поддерживаемости.

### 中文

**项目简介（2‑3 句）**  
expo/skills 是一套面向 Expo 项目和 Expo Application Services（EAS）的 AI 代理技能库，能够把零散的 Prompt 与工具封装成可复用的工作流。它适用于多代理协同、工具链调用以及统一的代理记忆管理。

**价值**  
- 将“孤立的 Prompt + 工具”转化为结构化、可重复的 Agent 流程，显著提升开发效率和可维护性。  
- 支持在同一工作流中调度多个 AI 代理，实现复杂任务的自动化编排。  
- 为团队提供统一的技能库，降低新成员上手成本并保证业务逻辑的一致性。

**典型接入方式**  
1. **克隆或添加子模块**：将仓库 `git clone https://github.com/expo/skills.git`（或使用 Git submodule）加入项目代码库。  
2. **安装依赖**：项目根目录运行 `npm i`（或 `yarn`），确保 Shell 环境具备 `bash`、`jq` 等基础工具。  
3. **配置入口**：在业务代码中引入相应的 skill 脚本，例如 `./skills/ios-build.sh`，并通过环境变量或配置文件（`expo.skills.json`）声明所需的输入/输出。  
4. **手动验证**：首次运行时手动执行一次完整流程，检查日志并确认所有外部服务（EAS、Expo CLI、GitHub Actions 等）的凭证和权限配置正确。  
5. **集成到 CI/CD**：将验证通过的 skill 脚本嵌入到现有的 CI/CD pipeline 中，使用 `npm run skill:<name>` 或直接调用对应的 Shell 脚本。

**生产可用性**  
- **成熟度**：GitHub ★2121、Fork 105，最近一次更新为 2026‑06‑25，表明社区活跃度尚可。  
- **适用场景**：适合原型、内部工具或中小规模的自动化流程；在生产环境使用前建议进行依赖审计、版本锁定以及错误恢复机制的补充。  
- **风险**：元数据中缺乏明确的集成指引，接入成本主要在于手动检查脚本兼容性和凭证配置；因此在正式投产前需完成一次完整的端到端验证。  

总体而言，expo/skills 在提升 Expo 项目自动化水平方面具备显著价值，经过适当的审查与测试后即可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** expo/skills helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 2121 GitHub stars
- 105 forks
- updated 2026-06-25
- primary language: Shell

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 71/100 |
| topics | 0/100 |
| outlook | 52/100 |
| quality | 54/100 |
| recency | 40/100 |
| adoption | 65/100 |
| production | 51/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/expo/skills) · [← Back to Orchestration](./README.md)</sub>
