# forcedotcom/sf-skills

[![Stars](https://img.shields.io/github/stars/forcedotcom/sf-skills?style=flat-square&color=yellow)](https://github.com/forcedotcom/sf-skills/stargazers) [![Forks](https://img.shields.io/github/forks/forcedotcom/sf-skills?style=flat-square&color=blue)](https://github.com/forcedotcom/sf-skills/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Salesforce's curated collection of agent skills for building applications. Optimized for Agentforce Vibes, compatible with all AI tools.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 599 |
| 🍴 **Forks** | 211 |
| 💻 **Language** | Python |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Orchestration · AI/ML

## 📝 Summary

### English

**Brief Summary**  
forcedotcom/sf‑skills is a Python library that bundles Salesforce’s curated “agent skills” – reusable prompt and tool‑wrappers – to help developers compose multi‑agent, tool‑driven workflows. It is optimized for Agentforce Vibes, works with any LLM‑orchestrator, and is intended to turn ad‑hoc prompts into repeatable, shareable pipelines.

**Value**  
- **Standardisation** – Provides a common library of well‑documented skills (memory handling, tool invocation, context stitching) so teams don’t reinvent the same prompt logic for each project.  
- **Orchestration‑ready** – Skills are designed to be chained, enabling coordinated multi‑agent flows and complex tool‑use pipelines with minimal glue code.  
- **Speed to prototype** – With 599 stars and active recent commits, the library gives a ready‑made toolbox that accelerates proof‑of‑concepts and internal demos.

**Practical Adoption Path**  
1. **Explore & vet** – Clone the repo, run the example notebooks, and review the skill definitions to ensure they match your domain (e.g., CRM, case routing).  
2. **Integrate** – Wrap the chosen skills in your Agentforce Vibes or other orchestration framework, adding any required authentication or API adapters.  
3. **Manual inspection** – Because metadata on integration signals is sparse, perform a code‑review focused on security (dependency versions, secret handling) and licensing compliance.  
4. **Test & iterate** – Build unit‑tests for each skill in your pipeline, run end‑to‑end simulations, and adjust prompts or tool wrappers to your data.  
5. **Deploy** – Package the vetted skills as a pip‑installable wheel or Docker layer, and roll them out to a staging environment before production.

**Production Readiness**  
- **Maturity**: Medium – the library is stable enough for internal prototypes and controlled production use, but it requires dependency checks and a final security/license audit.  
- **Maintenance**: Active (last update 2026‑06‑23) with a healthy fork/star count, yet the core maintainers are not officially listed as “active” by Salesforce, so you may need to plan for internal upkeep.  
- **Risk**: No critical metadata issues, but you should verify the open‑source license (likely BSD/Apache) and perform a vulnerability scan of its transitive dependencies before a full production rollout.  

In short, sf‑skills can quickly give your team a reusable skill set for multi‑agent orchestration; with a brief validation and security review, it is ready for internal production or as the foundation of a larger, maintainable AI workflow stack.

### Русский

**forcedotcom/sf-skills** — это открытая библиотека на Python, собирающая готовые «навыки» агентов Salesforce и позволяющая превратить разрозненные запросы и инструменты в повторяемые, оркестрируемые рабочие процессы (мульти‑агентные сценарии, пайплайны с использованием внешних сервисов, стандартизированная память агентов). Типичное внедрение подразумевает ручную проверку метаданных и настройку интеграции с Agentforce Vibes или другими AI‑инструментами, после чего библиотеку можно использовать в прототипах и внутренних проектах; для продакшн‑окружения требуется дополнительный аудит зависимостей, лицензий и безопасности. По текущим показателям (599 звёзд, 211 форков, активные обновления) готовность к production оценивается как средняя – подходит для быстрого пилотного запуска, но нуждается в проверке перед масштабным внедрением.

### 中文

**项目简介**  
forcedotcom/sf‑skills 是 Salesforce 官方维护的 **Agent Skills 库**，提供一套可直接在 Agentforce Vibes 中使用的、面向多种 AI 工具的技能集合（Python 实现），帮助把零散的 Prompt 与工具封装成可复用的智能体工作流。

**价值**  
- **工作流标准化**：把孤立的 Prompt、工具调用和记忆管理抽象为统一的 Skill，降低多智能体协作的实现成本。  
- **快速原型**：内置的技能覆盖常见业务场景（数据查询、表单填充、外部 API 调用等），可直接在 Vibes 或其他 LLM 框架中挂载，显著缩短开发周期。  
- **跨平台兼容**：虽然以 Agentforce Vibes 为主，但所有 Skill 都是纯 Python 实现，几乎可以在任何支持 Python 的 AI 平台上使用。

**典型接入方式**  
1. **代码依赖**：`pip install sf-skills`（或直接克隆仓库并添加到项目的 `PYTHONPATH`）。  
2. **技能注册**：在 Agentforce Vibes（或自建的 Orchestration 层）中通过 `SkillRegistry.register(<SkillClass>)` 将所需 Skill 加入智能体。  
3. **手动审查**：因为项目的元数据（集成信号）较少，建议在正式使用前阅读每个 Skill 的实现和依赖，确认安全与合规性后再上线。  

**生产可用性**  
- **成熟度**：GitHub ★599、Fork 211，最近一次更新为 2026‑06‑23，代码质量较好，适合作为 **原型或内部业务流程** 的基础。  
- **风险**：许可证、长期维护者活跃度以及安全审计仍需进一步确认；在生产环境部署前建议进行依赖安全扫描、单元/集成测试以及性能评估。  
- **就绪度**：**Medium**。在完成上述审查和必要的运维准备（如 CI/CD、监控、回滚机制）后，可投入生产使用；若对可靠性要求极高，建议先在影子环境验证。

## 🧭 Practical evaluation

**Value:** forcedotcom/sf-skills helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 599 GitHub stars
- 211 forks
- updated 2026-06-23
- primary language: Python

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 58/100 |
| stars | 59/100 |
| topics | 0/100 |
| outlook | 54/100 |
| quality | 51/100 |
| recency | 40/100 |
| adoption | 59/100 |
| production | 52/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/forcedotcom/sf-skills) · [← Back to Orchestration](./README.md)</sub>
