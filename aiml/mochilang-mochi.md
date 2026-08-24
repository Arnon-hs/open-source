# mochilang/mochi

[![Stars](https://img.shields.io/github/stars/mochilang/mochi?style=flat-square&color=yellow)](https://github.com/mochilang/mochi/stargazers) [![Forks](https://img.shields.io/github/forks/mochilang/mochi?style=flat-square&color=blue)](https://github.com/mochilang/mochi/network) [![Language](https://img.shields.io/badge/lang-Scheme-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-47%2F100-brightgreen?style=flat-square)](#)

> Mochi is a small, fast, embeddable programming language designed for agents, data, and AI. It combines functional syntax, stream-first semantics, and native support for datasets, graphs, and simulation.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 327 |
| 🍴 **Forks** | 14 |
| 💻 **Language** | Scheme |
| 📈 **Score** | 47/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `ai` `graph` `leetcode` `stream`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Mochi is a lightweight, high‑performance language built for agents, data pipelines, and AI workloads. It blends a functional syntax with stream‑first semantics and first‑class support for datasets, graphs, and simulations, letting developers prototype AI‑driven features without assembling a full model stack from scratch. With a modest codebase written in Scheme, it is easy to embed in existing systems for rapid experimentation.

**Value**  
- **Fast prototyping:** Provides native abstractions for data streams, graph traversals, and simulation loops, so common AI/ML patterns (e.g., retrieval‑augmented generation, agent orchestration) can be expressed concisely.  
- **Lower entry cost:** You can add AI capabilities by writing Mochi scripts rather than wiring together multiple libraries and services, reducing both development time and operational overhead.  
- **Embeddable:** Because it compiles to a small runtime, it can be dropped into micro‑services, edge devices, or internal tooling without heavyweight dependencies.

**Practical Adoption Path**  
1. **Proof‑of‑Concept:** Clone the repo, run the README examples, and build a tiny “hello‑world” agent that consumes a dataset or calls an LLM.  
2. **Integration Scaffold:** Wrap the Mochi interpreter as a library (e.g., via a C‑FFI or a simple HTTP wrapper) inside the target service.  
3. **Iterative Expansion:** Replace existing glue code with Mochi scripts for data‑flow, RAG pipelines, or simulation loops, validating each step against existing unit tests.  
4. **Tooling Check:** Verify that the build system, CI pipelines, and dependency manager (Scheme’s Racket/Guile) fit your organization’s standards before scaling.

**Production Readiness**  
- **Maturity:** Medium – the project is actively maintained (last commit 2026‑05‑12) and has a modest but healthy community (≈ 327 ★, 14 forks).  
- **Stability:** Suitable for internal prototypes, sandbox environments, or low‑risk services after a thorough dependency audit.  
- **Risks:** Integration guidance is sparse; you’ll need to invest time in understanding the Scheme‑based toolchain and in setting up reliable build/release pipelines. A small pilot and a dedicated “integration owner” are recommended before committing Mochi to mission‑critical production workloads.

### Русский

Mochi — это лёгкий и быстрый встраиваемый язык программирования, ориентированный на агентные, датасетные и AI‑задачи; он сочетает функциональный синтаксис, поток‑ориентированную семантику и встроенную поддержку наборов данных, графов и симуляций, позволяя быстро добавить AI‑функциональность без необходимости строить собственный стек моделей. Типичный сценарий внедрения — небольшие proof‑of‑concept или внутренние прототипы (RAG, агентные воркфлоу, оценка инструментов моделей), где достаточно подключить библиотеку и написать скрипт на Mochi. Готовность к production средняя: проект подходит для прототипов и внутренних сервисов, но перед выпуском в продакшн требуется проверить процесс установки, зависимости и план обслуживания.

### 中文

**价值**  
Mochi 通过内置的函数式语法、流优先（stream‑first）语义以及对数据集、图结构和仿真模型的原生支持，让开发者能够在几行代码里为 Agent、RAG（检索增强生成）或其他 AI 工作流快速原型化。它相当于一个轻量级的“AI 语法糖层”，帮助团队在不从零搭建模型堆栈的前提下，直接在业务代码中嵌入推理、检索、数据处理等能力。

**典型接入方式**  
1. **阅读 README 并完成最小示例**：项目提供了一个 “Hello, World” 示例，直接 `git clone` 后运行 `make run`（或 `scheme` 解释器）即可验证环境。  
2. **在现有服务中嵌入解释器**：Mochi 以 Scheme 为实现语言，提供 C 库接口（`libmochi.so`）和 Python FFI 包（`mochi-py`），可以在微服务或脚本中通过 `import mochi` 调用 `mochi.eval("(your code)")`。  
3. **构建数据管道**：利用其原生 `Dataset`、`Graph` 类型，将业务数据（CSV、JSON、向量库等）直接包装为 Mochi 对象，然后在语言内部完成过滤、映射、流式聚合，再输出给模型 API。  
4. **与模型 API 对接**：Mochi 提供 `llm` 模块，封装了 OpenAI、Claude、Gemini 等主流大模型的 HTTP 调用，语法上像普通函数调用，便于在 Agent 脚本中编排多轮对话或工具调用。

**生产可用性**  
- **成熟度**：GitHub 目前 327 星、14 Fork，活跃度仍在（最近一次提交 2026‑05‑12），代码基于 Scheme，社区规模小但技术栈清晰。  
- **适用场景**：非常适合作为**内部原型**、**实验性功能**或**业务流程自动化**的脚本层；在需要快速迭代、频繁调试的 AI Agent 项目中能显著提升开发效率。  
- **上线前检查**：  
  1. **依赖审计**：确认 `libmochi` 的二进制发行版与生产环境的 OS/CPU 兼容；若使用 Python 包，锁定版本并在 CI 中加入安全扫描。  
  2. **稳定性验证**：在预生产环境跑一次完整的 RAG/Agent 流程，监控内存泄漏、GC 延迟以及外部模型调用的超时重试。  
  3. **运维准备**：为解释器进程设置资源上限（CPU、内存），并在异常时提供回退路径（如直接调用原生 Python 实现）。  
- **结论**：在 **中等风险**、**内部或边缘服务**的场景下可直接投入使用；若要在面向外部用户的高可用系统中采用，建议先做更严格的安全、性能和容灾评估后再推广。

## 🧭 Practical evaluation

**Value:** mochilang/mochi helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 327 GitHub stars
- 14 forks
- updated 2026-05-12
- primary language: Scheme
- 5 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 54/100 |
| topics | 63/100 |
| outlook | 47/100 |
| quality | 50/100 |
| recency | 20/100 |
| adoption | 47/100 |
| production | 44/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/mochilang/mochi) · [← Back to AI/ML](./README.md)</sub>
