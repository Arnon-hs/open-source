# VirtusLab/cellar

[![Stars](https://img.shields.io/github/stars/VirtusLab/cellar?style=flat-square&color=yellow)](https://github.com/VirtusLab/cellar/stargazers) [![Forks](https://img.shields.io/github/forks/VirtusLab/cellar?style=flat-square&color=blue)](https://github.com/VirtusLab/cellar/network) [![Language](https://img.shields.io/badge/lang-Scala-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> CLI tool for coding agents and developers to query the public API of any Maven JVM dependency — get symbol signatures, list packages, search by name, and inspect dependency trees. Powered by Coursier and tasty-query.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 72 |
| 🍴 **Forks** | 10 |
| 💻 **Language** | Scala |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
Cellar is a Scala‑based CLI that lets AI agents and developers query the public API of any Maven JVM dependency—retrieving symbol signatures, listing packages, searching by name, and visualising dependency trees. It is built on top of Coursier and tasty‑query, making it a lightweight yet powerful bridge between code‑base introspection and LLM‑driven tooling.  

**Value**  
- **AI‑ready code insight** – Provides structured, machine‑readable metadata (signatures, package hierarchies, dependency graphs) that can be fed directly into retrieval‑augmented generation (RAG) pipelines or autonomous coding agents.  
- **Speed up prototyping** – Eliminates the need to roll your own parser or maintain a separate index of JVM libraries; developers can instantly query any artifact on Maven Central.  
- **Extensible backend** – Because it leverages Coursier for resolution and tasty‑query for semantic analysis, it can be extended to support custom repositories or additional Scala/Java language features.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the CLI against a few known dependencies (e.g., `cellar query scala-library`) and verify the output format matches your RAG or agent expectations.  
2. **Integration Wrapper** – Wrap the CLI (or its underlying library) in a thin service (REST/gRPC) that your LLM orchestration layer can call.  
3. **Workflow Embedding** – Incorporate the service into existing AI‑augmented development pipelines (e.g., code‑completion, documentation generation, security scanning) and iterate on prompt design.  
4. **Feedback Loop** – Use the generated signatures to fine‑tune downstream models or to validate agent actions, then monitor latency and cache frequently‑queried artifacts.  

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑07‑08), has ~70 stars and a modest fork count, indicating a small but engaged user base.  
- **Stability**: Core functionality (dependency resolution, symbol extraction) relies on mature libraries (Coursier, tasty‑query), which are battle‑tested in the Scala ecosystem.  
- **Considerations before production**:  
  * Verify the license compatibility with your stack.  
  * Conduct a security audit of the CLI’s handling of external Maven artifacts (e.g., checksum verification, sandboxing).  
  * Assess performance at scale—benchmark resolution time for large dependency trees and decide on caching strategies.  
  * Ensure maintainers are responsive; consider contributing fixes or sponsoring the project if you depend on it long‑term.  

Overall, Cellar is a solid foundation for adding AI‑driven code‑intelligence to JVM‑centric products, especially in prototype or internal tooling contexts, with a clear path to production once the above diligence steps are completed.

### Русский

Резюме проекта VirtusLab/cellar:

ВirtusLab/cellar - это открытый источник инструмент командной строки, позволяющий агентам и разработчикам извлекать данные из публичного API Maven JVM зависимостей. Этот инструмент может помочь добавлять функциональность AI без создания новой базовой модели стека. VirtusLab/cellar готов к использованию в прототипах или внутренних рабочих процессах, но требует проверки зависимостей и поддержки перед выпуском в производство.

### 中文

**VirtusLab/cellar 简介**

VirtusLab/cellar 是一个开源 CLI 工具，用于开发人员和编码代理查询任何 Maven JVM 依赖的公共 API。它支持获取符号签名、列出包、根据名称搜索以及检查依赖树。该工具由 Coursier 和 tasty-query 驱动。

**价值**

VirtusLab/cellar 帮助开发人员在不从零开始建立模型堆栈的情况下添加 AI 能力。它有助于开发者快速实现 AI 功能、构建 RAG 或代理工作流、评估模型工具。

**典型接入方式**

典型接入方式是通过阅读 README 文件并进行小规模的原型验证。需要注意的是，需要检查依赖项和维护情况才能确保生产环境的稳定性。

**生产可用性**

VirtusLab/cellar 的生产可用性为中等（Medium）。它适用于原型开发或内部工作流，需要在生产环境中进行依赖项和维护检查后才能使用。

## 🧭 Practical evaluation

**Value:** VirtusLab/cellar helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 72 GitHub stars
- 10 forks
- updated 2026-07-08
- primary language: Scala

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 26/100 |
| stars | 40/100 |
| topics | 0/100 |
| outlook | 67/100 |
| quality | 51/100 |
| recency | 80/100 |
| adoption | 36/100 |
| production | 63/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-08 · [View on GitHub](https://github.com/VirtusLab/cellar) · [← Back to Misc](./README.md)</sub>
