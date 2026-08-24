# Charlie85270/Dorothy

[![Stars](https://img.shields.io/github/stars/Charlie85270/Dorothy?style=flat-square&color=yellow)](https://github.com/Charlie85270/Dorothy/stargazers) [![Forks](https://img.shields.io/github/forks/Charlie85270/Dorothy?style=flat-square&color=blue)](https://github.com/Charlie85270/Dorothy/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Dorothy, the wife your AI agents needs.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 312 |
| 🍴 **Forks** | 59 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-agents` `ai-tools` `orchestration`

## 🎯 Categories

Orchestration · AI/ML

## 📝 Summary

### English

**Brief Summary**  
Dorothy (Charlie85270/Dorothy) is an open‑source TypeScript framework that stitches together isolated prompts, tools, and memory stores into repeatable, orchestrated AI‑agent workflows. It lets developers coordinate multi‑agent pipelines, add tool‑use steps, and standardize agent memory without writing boilerplate orchestration code.

**Value**  
- **Workflow unification** – Turns ad‑hoc prompt calls into reusable, composable agents, reducing duplication and speeding up experimentation.  
- **Tool integration** – Provides a simple pipeline model for attaching external tools (APIs, databases, retrieval systems) to agents, making complex tasks achievable with minimal glue code.  
- **Memory standardization** – Offers a common interface for persisting and retrieving agent state, improving consistency across projects and teams.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, run the example scripts, and verify that the README steps work in your environment.  
2. **Pilot integration** – Replace a single existing prompt‑to‑tool call with a Dorothy‑defined workflow, using the built‑in memory adapters to test state handling.  
3. **Scale incrementally** – Gradually migrate additional agents and tools into Dorothy’s pipeline model, leveraging its TypeScript typings for type‑safe expansion.  
4. **Internal documentation** – Capture the new workflow patterns in team docs to ensure consistent usage across future projects.

**Production Readiness**  
Dorothy sits at a **medium** readiness level. It is mature enough for prototypes and internal tooling—evidenced by 312 ★, recent updates (June 2026), and an active TypeScript codebase—but it still requires due‑diligence before production deployment: verify the open‑source license, perform a security audit of its dependencies, and confirm that maintainers are responsive for critical bug fixes. With those checks in place, Dorothy can be safely promoted to production for controlled, internal workloads.

### Русский

Резюме проекта Charlie85270/Dorothy:

Charlie85270/Dorothy - это open-source проект, который помогает превратить изолированные наборы команд и инструменты в повторяемые рабочие процессы для агентов AI. Этот проект особенно полезен для координации рабочих процессов между несколькими агентами, добавления линий обработки инструментов и стандартизации памяти агентов. Charlie85270/Dorothy готов к внедрению в прототипах или внутренних рабочих процессах, но требует проверки зависимостей и поддержки перед выпуском в производство.

### 中文

**项目简介**  
Dorothy（Charlie85270/Dorothy）是一款面向 AI 代理的编排框架，能够把零散的 Prompt 与工具组合成可重复、可管理的多代理工作流。它让开发者轻松实现代理间的协同、工具调用流水线以及统一的记忆管理。

**价值点**  
- **工作流化**：把单个 Prompt 或工具封装成可复用的节点，快速搭建复杂的多代理流程。  
- **工具链集成**：内置工具使用管道，支持在不同代理之间无缝传递数据。  
- **记忆标准化**：提供统一的记忆模型，避免不同代理之间的状态不一致。  

**典型接入方式**  
1. **阅读 README**，确认项目的依赖（Node.js、TypeScript）以及示例代码。  
2. **创建小型 PoC**：在本地或沙盒环境中复制示例仓库，改写 Prompt 与工具配置，验证工作流能否按预期运行。  
3. **逐步迁移**：将已有的单体 Prompt 或工具调用迁入 Dorothy 的节点定义，使用其 Orchestration API 进行调度。  
4. **CI/CD 集成**：将 TypeScript 编译、单元测试和部署脚本加入现有流水线，确保每次改动都通过自动化验证。  

**生产可用性**  
- **成熟度**：Medium。已有 312 ⭐、59 🍴，活跃更新至 2026‑06‑27，适合作为原型或内部业务的核心编排层。  
- **准备工作**：在正式上线前需要完成以下检查：  
  - 许可证兼容性（确认是否为 MIT/Apache 等开源许可证）。  
  - 安全审计：审查依赖的 npm 包是否存在已知漏洞。  
  - 维护者沟通：确认项目维护者的响应速度，以便在出现问题时能及时获得支持。  
- **运维建议**：在生产环境部署时，建议使用容器化（Docker）或 serverless 平台，配合监控和日志收集，以便快速定位工作流异常。  

综上，Dorothy 能显著提升多代理系统的可组合性与可维护性，适合作为原型或内部工具的编排引擎；在完成许可证、依赖安全和运维准备后，即可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** Charlie85270/Dorothy helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 312 GitHub stars
- 59 forks
- updated 2026-06-27
- primary language: TypeScript
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 53/100 |
| topics | 50/100 |
| outlook | 56/100 |
| quality | 55/100 |
| recency | 40/100 |
| adoption | 51/100 |
| production | 53/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/Charlie85270/Dorothy) · [← Back to Orchestration](./README.md)</sub>
