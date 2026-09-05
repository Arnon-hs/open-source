# geckse/n8n-desk

[![Stars](https://img.shields.io/github/stars/geckse/n8n-desk?style=flat-square&color=yellow)](https://github.com/geckse/n8n-desk/stargazers) [![Forks](https://img.shields.io/github/forks/geckse/n8n-desk?style=flat-square&color=blue)](https://github.com/geckse/n8n-desk/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> Bringing n8n to your Machine — a desktop & mobile companion app for n8n. Chat with agents, build workflows conversationally, work with local files.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 79 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `claude` `cross-platform` `desktop` `electron` `langchain` `local` `n8n`

## 🎯 Categories

Orchestration · Automation · AI/ML · Communication

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
geckse/n8n‑desk is an open‑source desktop and mobile companion for the n8n workflow automation platform. It lets users chat with AI agents, build and run n8n workflows conversationally, and interact with local files, turning ad‑hoc prompts into repeatable, tool‑enabled pipelines. The project aims to make multi‑agent orchestration and memory management easy to prototype and share.

**Value**  
- **Unified interface**: Combines a chat UI with n8n’s visual workflow engine, so non‑technical users can create and test automation without leaving a conversational context.  
- **Tool‑use pipelines**: Agents can invoke local scripts, read/write files, or call external APIs directly from the chat, enabling richer multi‑agent scenarios (e.g., data extraction → transformation → storage).  
- **Repeatable agent workflows**: Prompts and tool interactions are captured as n8n nodes, giving you version‑controlled, reusable automation that can be exported or shared across teams.

**Practical Adoption Path**  
1. **Proof‑of‑Concept**: Clone the repo, run the provided Docker/Node setup, and follow the README to connect the companion app to an existing n8n instance. Build a simple “chat‑to‑workflow” use case (e.g., generate a report from a CSV).  
2. **Evaluation**: Verify that the generated n8n workflows match expectations, test local file access, and assess the UI/UX for your team.  
3. **Pilot**: Integrate with internal tools (e.g., ticketing, CI/CD) and add any needed custom nodes. Document the workflow templates and establish a minimal governance process.  
4. **Scale**: Package the companion as an internal desktop app (or mobile build) and roll out to broader users, adding monitoring and version control for the generated workflows.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last update 2026‑07‑08), has modest community interest (79 ★, 8 forks), and is written in TypeScript, which eases integration with existing n8n setups.  
- **Strengths**: Good for prototypes, internal tooling, and teams that already rely on n8n. The codebase is small enough to audit quickly.  
- **Caveats**: Before production use, perform a security review (especially around local file access), confirm the licensing terms, and verify that the maintainers can address bugs or pull‑requests. Dependency hygiene and automated tests are limited, so add your own CI checks and consider forking if long‑term support is required.  

Overall, n8n‑desk offers a compelling way to bridge conversational AI with workflow automation, making it a viable candidate for internal pilots and, with proper hardening, for production‑grade agent‑driven pipelines.

### Русский

Резюме:

geckse/n8n-desk - это open-source проект, который позволяет работать с n8n на компьютере или мобильном устройстве. Это приложение позволяет общаться с агентами, создавать потоки данных беседами и работать с локальными файлами. geckse/n8n-desk помогает превратить изолированные команды и инструменты в повторяемые потоки данных агентов, что делает его идеальным решением для координации мульти-агентных потоков данных, добавления инструментальных линий и стандартизации агентной памяти. Проект готов к внедрению в прототипах или внутренних потоках данных, но требует проверки зависимостей и поддержки перед выпуском в производство.

### 中文

**简短介绍**

geckse/n8n-desk 是一个开源项目，旨在为 n8n 提供桌面和移动应用程序的补充。它使您可以与代理交互、使用会话式工作流程构建工作流程以及与本地文件进行工作。

**价值**

geckse/n8n-desk 的价值在于，它可以帮助您将孤立的命令和工具转换成可重复执行的代理工作流程。通过使用它，您可以更好地协调多个代理的工作流程、添加工具使用的管道以及标准化代理的记忆。

**典型接入方式**

鉴于 geckse/n8n-desk 的设计，接入方式可能如下：

1. 首先评估项目的可行性，查看 README 和开始一个小的原型验证。
2. 确认项目的依赖关系和维护需求。
3. 确保与 n8n 的集成符合您的需求。

**生产可用性**

geckse/n8n-desk 的生产可用性被评估为中等（Medium）。它适合用于原型或内部工作流程，但在

## 🧭 Practical evaluation

**Value:** geckse/n8n-desk helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 79 GitHub stars
- 8 forks
- updated 2026-07-08
- primary language: TypeScript
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 41/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 66/100 |
| recency | 80/100 |
| adoption | 36/100 |
| production | 67/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-07-08 · [View on GitHub](https://github.com/geckse/n8n-desk) · [← Back to Orchestration](./README.md)</sub>
