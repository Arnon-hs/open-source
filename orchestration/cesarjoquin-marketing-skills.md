# Cesarjoquin/Marketing-Skills

[![Stars](https://img.shields.io/github/stars/Cesarjoquin/Marketing-Skills?style=flat-square&color=yellow)](https://github.com/Cesarjoquin/Marketing-Skills/stargazers) [![Forks](https://img.shields.io/github/forks/Cesarjoquin/Marketing-Skills?style=flat-square&color=blue)](https://github.com/Cesarjoquin/Marketing-Skills/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> AI agent Marketing skills for Claude Code and AI agents. CRO, copywriting, SEO, analytics, ai agent, and growth engineering, ai agent

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 51 |
| 🍴 **Forks** | 55 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `ai` `ai-agent` `ai-skills` `marketing-agent` `skills-agent`

## 🎯 Categories

Orchestration · AI/ML · Marketing

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Cesarjoquin/Marketing‑Skills is an open‑source TypeScript library that stitches together isolated prompts, tools, and APIs into repeatable, multi‑agent marketing workflows for Claude‑based AI agents. It supplies ready‑made components for CRO, copywriting, SEO, analytics, and growth‑engineering, letting you orchestrate tool‑use pipelines and maintain a shared agent memory. With 51 stars and recent activity, it’s positioned as a prototyping‑grade framework for building internal marketing automation agents.

**Value**  
- **Workflow composability:** Turns ad‑hoc prompts into structured, reusable pipelines, reducing the time spent wiring together Claude, external APIs, and data stores.  
- **Domain‑specific primitives:** Pre‑built agents for conversion‑rate optimisation, SEO audits, copy generation, and analytics let teams focus on strategy rather than low‑level integration.  
- **Standardised memory handling:** Centralises context across agents, improving consistency and enabling more sophisticated multi‑step campaigns.

**Practical Adoption Path**  
1. **Proof‑of‑concept:** Clone the repo, run the provided README examples, and replace the sample API keys with your own marketing tools (e.g., Google Analytics, Ahrefs).  
2. **Pilot workflow:** Build a small multi‑agent pipeline (e.g., SEO audit → copywriting → CRO test) and validate output quality against existing manual processes.  
3. **Iterate & extend:** Add custom tool adapters or domain‑specific prompts, and lock the workflow definition in version control.  
4. **Scale:** Containerise the agents, expose them via a lightweight API gateway, and integrate with your CI/CD pipeline for automated testing and deployment.

**Production Readiness**  
- **Maturity:** Medium. The codebase is actively maintained (last commit 2026‑07‑03) and functional for prototypes, but it still requires dependency vetting, security review, and possibly a formal CI pipeline before mission‑critical use.  
- **Risks:** Licensing and long‑term maintainer commitment need confirmation; thorough security scanning of third‑party tool integrations is advisable.  
- **Recommendation:** Suitable for internal tools, proof‑of‑concepts, or staged roll‑outs; treat it as a foundation that should be hardened and monitored before full production deployment.

### Русский

Cesarjoquin/Marketing‑Skills — это набор TypeScript‑агентов, позволяющий превратить разрозненные подсказки и отдельные инструменты (CRO, копирайтинг, SEO, аналитика и т.п.) в повторяемые многокомпонентные workflow для Claude и других AI‑агентов. Типичное внедрение начинается с небольшого proof‑of‑concept: добавьте репозиторий в проект, запустите готовый README‑пример и настройте конвейер инструментов, после чего можно масштабировать процесс координации нескольких агентов и стандартизировать их память. Готовность к production — средняя: решение уже используется в прототипах и внутренних процессах, но перед выводом в продакшн требуется проверка зависимостей, лицензии и безопасности, а также обеспечение постоянного сопровождения.

### 中文

**项目简介**  
Cesarjoquin/Marketing‑Skills 是一套基于 Claude 的 AI 代理工具库，聚焦营销全链路——从 CRO、文案、SEO 到数据分析、增长工程等场景。它把零散的 Prompt 与外部工具封装成可复用的工作流，让多代理协同、工具链调用以及记忆管理变得结构化、可编排。

**价值主张**  
- **工作流标准化**：将分散的 Prompt 与 API、数据库等工具统一包装，形成可重复、可共享的营销任务模板。  
- **多代理协同**：支持在同一流程中调度多个 Claude 代理，分别负责创意、数据分析、优化建议等职责，实现端到端的营销自动化。  
- **快速原型**：基于 TypeScript 实现，易于在现有前端/后端项目中嵌入，适合内部实验或 MVP 开发。  

**典型接入方式**  
1. **阅读 README 与示例**：项目提供了完整的快速上手指南和几段示例代码，帮助你了解如何定义 `Agent`, `Tool` 以及 `Workflow`。  
2. **在代码库中安装**：`npm i @cesarjoquin/marketing-skills`（或对应的 Yarn/Pnpm 命令），引入核心模块。  
3. **创建工作流**：使用 TypeScript 编写 `Workflow` 配置，指定各代理的 Prompt、所需工具（如 SEO API、Google Analytics）以及记忆持久化方式。  
4. **小范围 PoC**：在内部测试环境中跑一次完整的营销任务（如生成登陆页文案 → 通过 SEO 工具校验 → 输出 CRO 建议），验证结果并收集反馈。  
5. **逐步扩展**：在 PoC 成功后，可将工作流抽象为微服务或 serverless 函数，供业务系统调用，或通过 CI/CD 自动化部署。  

**生产可用性评估**  
- **成熟度**：Medium。项目已有 51 个 Star、55 个 Fork，活跃更新至 2026‑07‑03，代码基于 TypeScript，结构清晰，适合作为原型或内部工具。  
- **依赖与维护**：依赖数量适中，但在投入生产前需审查第三方库的安全报告、许可证兼容性以及长期维护计划。  
- **上线建议**：  
  1. **安全审计**：检查所有外部 API 调用的鉴权方式，确保不泄露凭证。  
  2. **监控与日志**：为每个 Agent 与 Tool 的调用添加链路追踪和错误日志，便于故障定位。  
  3. **容错设计**：为关键步骤（如 SEO 查询、数据写入）实现重试或降级策略。  
  4. **资源配额**：根据 Claude 计费模型设定并发上限，防止成本失控。  

综上，Cesarjoquin/Marketing‑Skills 适合作为营销自动化的 **原型/内部工作流** 解决方案，经过安全、监控和容错等生产化改造后，可平滑迁移到正式业务环境。

## 🧭 Practical evaluation

**Value:** Cesarjoquin/Marketing-Skills helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 51 GitHub stars
- 55 forks
- updated 2026-07-03
- primary language: TypeScript
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 37/100 |
| topics | 75/100 |
| outlook | 67/100 |
| quality | 64/100 |
| recency | 80/100 |
| adoption | 39/100 |
| production | 66/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/Cesarjoquin/Marketing-Skills) · [← Back to Orchestration](./README.md)</sub>
