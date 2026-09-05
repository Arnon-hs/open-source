# scaling-group/eve

[![Stars](https://img.shields.io/github/stars/scaling-group/eve?style=flat-square&color=yellow)](https://github.com/scaling-group/eve/stargazers) [![Forks](https://img.shields.io/github/forks/scaling-group/eve?style=flat-square&color=blue)](https://github.com/scaling-group/eve/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> EvE is an open-source framework for co-evolving ensembles of coding agents. Wrap any coding agent — Codex, Claude Code — into an evolutionary loop that co-evolves solvers and agent guidance.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 33 |
| 🍴 **Forks** | 3 |
| 💻 **Language** | Python |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-framework` `alpha-evolve` `autoresearch` `claude-code` `codex` `coding-agent` `evolutionary-optimization` `llm-agents` `multi-agent` `self-evolving` `tokenmaxxing`

## 🎯 Categories

Orchestration · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
EvE (scaling-group/eve) is an open‑source Python framework that places any coding agent—such as OpenAI Codex or Anthropic Claude Code—inside an evolutionary loop, co‑evolving both problem‑solving agents and the guidance that steers them. By turning ad‑hoc prompts and tool calls into repeatable, self‑optimising workflows, EvE lets teams build coordinated multi‑agent pipelines with built‑in memory and tool‑use patterns.

**Value**  
- **From isolated prompts to systematic pipelines** – EvE abstracts away the glue code required to chain LLM‑based coding agents, turning one‑off experiments into reusable, version‑controlled workflows.  
- **Co‑evolutionary optimisation** – The framework automatically mutates both the solver agents and their “coach” prompts, surfacing better solutions without manual trial‑and‑error.  
- **Standardised agent memory & tooling** – Built‑in support for persistent state and external tool integration (e.g., linters, test runners) reduces duplication across projects and accelerates prototyping.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Fork the repo, run the README example, and replace the default Codex agent with your own model or API key. Verify that the evolutionary loop produces improved code snippets on a small benchmark (e.g., a set of coding kata).  
2. **Pilot Integration** – Wrap existing internal coding agents or CI tools into EvE’s `Agent` interface, and define a simple fitness function (e.g., passing unit tests, lint score). Run the loop on a limited code‑base to gauge convergence speed and resource consumption.  
3. **Scale & Harden** – Add custom memory back‑ends, integrate with your CI/CD pipeline, and configure logging/monitoring. Document the workflow in internal wikis and expose a thin CLI or API for other teams to reuse.  

**Production Readiness**  
- **Maturity** – Medium. The project is actively maintained (last commit 2026‑06‑25) and has a modest community (≈33 stars, 3 forks). It is suitable for prototypes, internal tooling, or “sandbox” environments.  
- **Dependencies & Maintenance** – Primarily Python; review the dependency tree for known CVEs and pin versions before shipping.  
- **Risks** – License and long‑term maintainer commitment need confirmation; security posture of the evolutionary loop (e.g., sandboxing generated code) must be evaluated.  
- **Recommendation** – Deploy first as a controlled proof‑of‑concept, perform a security audit, and establish an internal maintainer before promoting EvE to production‑critical pipelines.

### Русский

**scaling-group/eve** — это Python‑фреймворк, позволяющий превратить отдельные запросы к кодирующим моделям (Codex, Claude Code и др.) в эволюционный цикл, где одновременно развиваются решения и стратегии их управления. Типичный сценарий внедрения — создание небольшого proof‑of‑concept, в котором несколько агентов координируют работу, используют инструменты и сохраняют контекст через стандартный механизм памяти, после чего workflow интегрируется в существующий пайплайн. Готовность к production — средняя: проект подходит для прототипов и внутренних процессов, но перед выводом в продакшн требуется проверка лицензии, безопасности и стабильности зависимостей.

### 中文

**项目简介**  
EvE（scaling-group/eve）是一个开源框架，用于在进化循环中共同演化一组编码代理（如 Codex、Claude Code 等），实现求解器与代理指引的协同进化。它把单个 Prompt 或工具包装成可重复的代理工作流，帮助构建可扩展的多代理系统。

**价值**  
- **统一工作流**：把零散的 Prompt、工具和记忆机制统一进可编排的进化循环，降低了多代理协同的实现成本。  
- **快速原型**：通过标准化的接口即可把任意代码生成模型接入，快速搭建“求解器 + 指导者”组合，适合探索新算法或业务场景。  
- **可扩展性**：支持自定义进化策略、适应度函数和工具链，便于在复杂任务（如代码审查、自动重构、工具调用）中迭代优化。

**典型接入方式**  
1. **准备环境**：克隆仓库，使用 `requirements.txt` 安装 Python 依赖（Python ≥ 3.9）。  
2. **封装代理**：实现 `BaseAgent` 子类，提供 `generate(prompt, context)` 接口，内部调用目标模型的 API（如 OpenAI、Anthropic）。  
3. **定义进化配置**：在 `config.yaml` 中指定种群大小、适应度评估方式、交叉/变异策略以及需要的外部工具（如代码执行器、单元测试框架）。  
4. **启动循环**：运行 `python run_evolution.py --config config.yaml`，框架会自动创建种群、执行评估、更新代理并记录日志。  
5. **集成到现有系统**：通过 REST/gRPC 包装 `run_evolution.py`，或直接在 CI/CD 流水线中调用，以实现持续的代码生成与优化。

**生产可用性**  
- **成熟度**：目前处于 **Medium** 级别，适合原型开发、内部工具或实验性业务。代码库活跃（最近更新 2026‑06‑25），但星标和 fork 数较少，社区和维护者规模有限。  
- **依赖风险**：依赖外部大模型 API，需要关注费用、配额以及服务可用性；同时建议对模型调用进行速率控制和异常重试。  
- **安全与合规**：项目本身无显著元数据风险，但仍需审查许可证（MIT/Apache 等）以及对外部工具的安全姿态（如代码执行沙箱）。  
- **上线建议**：先在小范围 PoC 中验证进化策略和模型表现，完成 README、单元测试和 CI 检查后，再逐步推广至生产环境；同时加入监控、日志和回滚机制，以应对模型服务异常或进化过程失控的情况。

总体而言，EvE 为构建可进化的多代理代码生成系统提供了一个轻量级、可定制的起点，适合对创新性 AI 编码工作流有需求的团队在可控风险下快速实验并迭代。

## 🧭 Practical evaluation

**Value:** scaling-group/eve helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 33 GitHub stars
- 3 forks
- updated 2026-06-25
- primary language: Python
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 15/100 |
| stars | 33/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 28/100 |
| production | 65/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/scaling-group/eve) · [← Back to Orchestration](./README.md)</sub>
