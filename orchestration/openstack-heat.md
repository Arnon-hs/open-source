# openstack/heat

[![Stars](https://img.shields.io/github/stars/openstack/heat?style=flat-square&color=yellow)](https://github.com/openstack/heat/stargazers) [![Forks](https://img.shields.io/github/forks/openstack/heat?style=flat-square&color=blue)](https://github.com/openstack/heat/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> OpenStack Orchestration (Heat). Mirror of code maintained at opendev.org.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 411 |
| 🍴 **Forks** | 345 |
| 💻 **Language** | Python |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`service`

## 🎯 Categories

Orchestration

## 📝 Summary

### English

**Brief Summary**  
OpenStack Heat is the official orchestration service for OpenStack, providing a declarative language (Heat templates) to define and manage complex, multi‑component cloud environments. The project is actively maintained in Python and serves as a foundation for turning isolated prompts and tools into repeatable, agent‑driven workflows.

**Value**  
Heat enables teams to model infrastructure, application stacks, and tool‑use pipelines as code, allowing agents to execute coordinated, multi‑step tasks with built‑in state tracking (agent memory) and standardized hand‑offs. By encapsulating orchestration logic in reusable templates, organizations can reduce manual effort, increase reproducibility, and accelerate the creation of sophisticated AI/ML workflows that span multiple services.

**Practical Adoption Path**  

| Step | Action | Why |
|------|--------|-----|
| 1. **Initial Evaluation** | Clone the repo, run the unit test suite, and spin up a minimal Heat deployment (e.g., using DevStack or a Docker‑compose stack). | Confirms compatibility with your OpenStack version and validates that the code builds cleanly. |
| 2. **Template Pilot** | Convert an existing manual provisioning process into a Heat template and execute it in a non‑production tenant. | Demonstrates the template language, validates resource mappings, and surfaces any missing provider plugins. |
| 3. **Agent Integration** | Wrap the Heat CLI/REST API calls in your agent framework (e.g., LangChain, CrewAI) to trigger stack creation, update, or deletion as part of a larger workflow. | Turns Heat into a reusable “tool” that agents can invoke programmatically. |
| 4. **Security & Governance Review** | Perform a license audit, scan the code with SAST tools, and verify that the required OpenStack services (Keystone, Nova, Neutron, etc.) are hardened per your policies. | Mitigates the identified risks around licensing and security posture. |
| 5. **Staging Deployment** | Deploy Heat in a staging environment with production‑scale resource quotas, enable logging and monitoring (e.g., Prometheus + Grafana), and run end‑to‑end workflow tests. | Ensures reliability under realistic load and validates observability. |
| 6. **Production Roll‑out** | Promote the vetted templates and agent wrappers to production, establishing CI/CD pipelines that lint, test, and version‑control Heat templates alongside application code. | Provides repeatable, auditable deployments and simplifies future updates. |

**Production Readiness**  
- **Maturity:** Medium – Heat is a core OpenStack component with a long history, but the specific “agent workflow” use case is emerging and not yet covered by extensive production case studies.  
- **Stability:** The codebase is actively maintained (last update 2026‑06‑29) and has a healthy community (≈ 410 ★, 345 forks).  
- **Dependencies:** Requires a functional OpenStack cloud (Keystone, Nova, Neutron, etc.) and careful version alignment; integration signals are sparse, so manual verification is essential.  
- **Risks:** Licensing, security posture, and maintainer activity need final confirmation; ensure regular security scans and monitor upstream changelogs.  

Overall, Heat is well‑suited for prototyping and internal orchestration pipelines, and with the outlined due‑diligence steps it can be hardened for production‑grade, multi‑agent workflows.

### Русский

**openstack/heat** — это открытый проект оркестрации в экосистеме OpenStack, позволяющий превратить разрозненные запросы и инструменты в повторяемые рабочие процессы агентов. Его типичное применение — координация многокомпонентных (мульти‑агентных) сценариев, построение конвейеров с использованием внешних инструментов и стандартизация «памяти» агентов. Готовность к продакшну — средний уровень: проект подходит для прототипов и внутренних процессов, но перед запуском в продакшн требуется ручная проверка интеграции, оценка зависимостей и подтверждение поддержки лицензии и безопасности.

### 中文

**OpenStack Orchestration (Heat) 简介**

OpenStack Orchestration (Heat) 是一个开源项目，帮助用户将孤立的工具和提示转化为可重复的代理工作流。它提供了协调多代理工作流、添加工具使用管道以及标准化代理内存的功能。

**价值**

OpenStack Orchestration (Heat) 的价值在于它可以帮助用户将孤立的工具和提示转化为可重复的代理工作流，从而提高工作效率和标准化工作流程。

**典型接入方式**

典型接入方式包括：

* 将 OpenStack Orchestration (Heat) 与其他 OpenStack 项目集成，例如 Nova、Neutron 等。
* 使用 Heat API 来创建和管理工作流。
* 使用 Heat CLI 来交互操作工作流。

**生产可用性**

OpenStack Orchestration (Heat) 的生产可用性为中等（Medium）。它适合用于原型或内部工作流的开发，需要在生产环境中进行依赖性检查和维护检查后才可使用。

## 🧭 Practical evaluation

**Value:** openstack/heat helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 411 GitHub stars
- 345 forks
- updated 2026-06-29
- primary language: Python
- 1 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 63/100 |
| stars | 56/100 |
| topics | 13/100 |
| outlook | 62/100 |
| quality | 63/100 |
| recency | 80/100 |
| adoption | 58/100 |
| production | 65/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/openstack/heat) · [← Back to Orchestration](./README.md)</sub>
