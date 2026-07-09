# OthmanAdi/planning-with-files

[![Stars](https://img.shields.io/github/stars/OthmanAdi/planning-with-files?style=flat-square&color=yellow)](https://github.com/OthmanAdi/planning-with-files/stargazers) [![Forks](https://img.shields.io/github/forks/OthmanAdi/planning-with-files?style=flat-square&color=blue)](https://github.com/OthmanAdi/planning-with-files/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-78%2F100-brightgreen?style=flat-square)](#)

> Claude Code skill implementing Manus-style persistent markdown planning — the workflow pattern behind the $2B acquisition.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 21.3k |
| 🍴 **Forks** | 1.9k |
| 💻 **Language** | Python |
| 📈 **Score** | 78/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

`adal` `agent-skills` `antigravity` `claude` `claude-code` `claude-skills` `copilot` `copilot-skills` `hermes` `hermes-agent` `hermes-skill` `kilocode`

## 🎯 Categories

Orchestration · Automation · AI/ML · Frontend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
OthmanAdi/planning‑with‑files is a Claude‑Code skill that brings Manus‑style persistent markdown planning to AI agents, enabling them to store, retrieve, and evolve task plans across sessions. By treating markdown files as a shared, version‑controlled memory, the project turns ad‑hoc prompts and tool calls into reproducible, multi‑agent workflows—the same pattern that underpinned a $2 B acquisition. With over 21 k stars, active maintenance, and a Python‑centric codebase, it is ready for pilot‑level integration.

**Value**  
- **Workflow persistence:** Agents can read/write structured markdown plans, giving them a durable “brain” that survives restarts and can be audited.  
- **Tool‑use pipelines:** The skill wraps external tools (e.g., search, code execution) into the plan file, making complex pipelines declarative and reproducible.  
- **Multi‑agent coordination:** Multiple agents can converge on the same markdown document, allowing hand‑offs, task splitting, and shared memory without bespoke APIs.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept:** Clone the repo, run the provided example notebook, and verify that a Claude‑Code instance can create, update, and read a markdown plan.  
2. **Read‑me Validation:** Follow the README to integrate the skill into your existing Claude‑Code or LangChain stack, swapping a single “prompt‑only” step with the `plan_with_files` call.  
3. **Pilot Scope:** Deploy the skill in a sandboxed microservice that handles a specific workflow (e.g., ticket triage or content generation) and monitor plan files in a version‑controlled folder.  
4. **Scale‑out:** Extend the folder to a shared storage (Git repo, S3 bucket, or internal document store) and add additional agents that consume the same plan files for hand‑off or parallel execution.  

**Production Readiness**  
- **Maturity:** Recent commits (as of 2026‑05‑14), strong community signals (21 k stars, 1.9 k forks), and a well‑documented Python API indicate a stable codebase.  
- **Readiness Level:** High for an OSS candidate; the project is suitable for a serious pilot, though a final security/license audit and confirmation of active maintainers are recommended before full production rollout.  
- **Risk Mitigation:** Conduct a dependency scan, verify the MIT/Apache license compatibility, and establish a fallback plan (e.g., snapshot of the repo) in case maintainer activity wanes.  

Overall, planning‑with‑files offers a low‑friction way to give AI agents durable, shareable memory and orchestrated pipelines, making it a strong candidate for early‑stage production pilots.

### Русский

**Краткое резюме:**  
OthmanAdi/planning-with-files — open‑source библиотека на Python, реализующая стиль планирования Manus в виде постоянных markdown‑файлов, что позволяет превратить разрозненные подсказки и инструменты в воспроизводимые агентные рабочие процессы (координация нескольких агентов, построение пайплайнов с использованием инструментов, стандартизация памяти агента). Для внедрения рекомендуется начать с небольшого proof‑of‑concept: проверить README, запустить пример и интегрировать в существующий оркестрационный слой. Проект имеет высокий уровень готовности к production: активные коммиты, более 21 k звёзд, 1,9 k форков и свежие обновления, что делает его надёжным кандидатом для серьёзных пилотов.

### 中文

**项目简介（2‑3 句话）**  
OthmanAdi/planning-with-files 是基于 Claude Code Skill 实现的 Manus 风格持久化 Markdown 规划工具，提供将单个 Prompt 与外部工具组合成可重复执行的智能体工作流的能力——正是支撑 20 亿美元收购案背后的核心模式。  

**价值**  
- 将零散的 Prompt、工具调用和记忆状态统一封装为文件化的计划，使多智能体协作、工具链编排和记忆管理变得可视、可审计、可复用。  
- 通过 Markdown 语法直观表达任务、依赖与结果，降低非技术团队的上手门槛，同时保持对 AI/ML、自动化和前端系统的完整兼容。  

**典型接入方式**  
1. **快速验证**：克隆仓库 → 阅读 `README.md` 中的示例 → 在本地或容器中运行 `python -m planning_with_files example.md`，观察智能体如何读取、执行并写回计划。  
2. **CI/CD 集成**：在项目的构建流水线中加入步骤，使用 `planning-with-files` 生成的 Markdown 作为输入/输出，配合 GitHub Actions 或 Jenkins 实现自动化任务调度。  
3. **业务系统嵌入**：通过提供的 Python API（`PlanningEngine`）在现有后端服务中实例化，引入自定义工具（REST API、数据库查询等），并将生成的计划文件挂载到共享存储供前端实时展示。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑14 最近一次提交，21250+ 星、1885+ Fork，社区活跃，Issue 与 PR 反馈及时。  
- **技术成熟度**：主语言 Python，兼容主流 AI 框架（Claude、OpenAI），并提供完整的依赖声明与 Docker 镜像，易于在容器化环境中部署。  
- **风险**：目前未发现重大元数据或许可证冲突，仍需对依赖的第三方工具进行安全审计，并确认维护者的长期可用性。总体上，项目已具备 **高** 的生产候选资格，适合作为 Pilot 项目进行小范围概念验证后逐步扩大到全链路使用。

## 🧭 Practical evaluation

**Value:** OthmanAdi/planning-with-files helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 21250 GitHub stars
- 1885 forks
- updated 2026-05-14
- primary language: Python
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 82/100 |
| stars | 92/100 |
| topics | 100/100 |
| outlook | 92/100 |
| quality | 95/100 |
| recency | 100/100 |
| adoption | 89/100 |
| production | 82/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/OthmanAdi/planning-with-files) · [← Back to Orchestration](./README.md)</sub>
