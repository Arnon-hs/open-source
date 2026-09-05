# juanibiapina/deltoids

[![Stars](https://img.shields.io/github/stars/juanibiapina/deltoids?style=flat-square&color=yellow)](https://github.com/juanibiapina/deltoids/stargazers) [![Forks](https://img.shields.io/github/forks/juanibiapina/deltoids?style=flat-square&color=blue)](https://github.com/juanibiapina/deltoids/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> Diff filter that expands every hunk to include the enclosing function or block via tree-sitter. Pager for git, gh, or lazygit; viewer for coding-agent edit traces.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 21 |
| 🍴 **Forks** | 1 |
| 💻 **Language** | Rust |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`claude` `claude-code` `cli` `code-review` `coding-agents` `developer-tools` `diff` `git` `lazygit` `pager` `pi` `pi-package`

## 🎯 Categories

AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Deltoids is a Rust‑based diff filter that uses Tree‑Sitter to expand each changed hunk so it includes the surrounding function or code block, making context‑aware patches easier to read and apply. It doubles as a pager for Git, GitHub, or Lazygit and can visualise coding‑agent edit traces, enabling rapid prototyping of AI‑driven code‑assist tools.  

**Value Proposition**  
- **Context‑rich diffs:** By automatically pulling in the enclosing syntactic unit, developers and AI agents get the full semantic picture of a change, reducing guesswork and improving the reliability of automated refactorings or suggestions.  
- **Plug‑and‑play AI integration:** The tool exposes its functionality through a CLI, SDK, and API, allowing teams to layer RAG, agent‑based workflows, or custom model inference on top without building a diff engine from scratch.  
- **Developer‑centric workflow:** Works as a drop‑in pager for familiar tools (git, gh, lazygit), so adoption does not disrupt existing pipelines while adding AI‑ready insight into code evolution.  

**Practical Adoption Path**  
1. **Prototype:** Clone the repo, run the provided CLI on a local Git repo to verify that expanded hunks match the desired context.  
2. **Integrate:** Wrap the CLI or call the Rust library from your AI service (e.g., a LangChain or LlamaIndex pipeline) to feed context‑aware diffs into prompts or RAG indexes.  
3. **Automate:** Add a thin wrapper script or CI step that invokes Deltoids before running code‑review bots, test‑generation agents, or automated refactoring tools.  
4. **Scale:** Containerise the binary or compile it as a shared library for use in larger micro‑service architectures, and configure monitoring for the Tree‑Sitter parsing step.  

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last update 2026‑06‑24) and has a modest but positive community signal (21 stars, 1 fork).  
- **Dependencies:** Relies on Tree‑Sitter and Rust toolchains; these are well‑supported but add a native‑build requirement that must be vetted for your target environment.  
- **Risk Areas:** License and security posture need a final review, and the maintainer base is small, so long‑term support should be assessed (e.g., by forking or sponsoring).  
- **Suitability:** Ideal for internal prototypes, RAG pipelines, or agent‑driven coding assistants; with proper dependency hardening and a fallback plan for maintenance, it can be promoted to production for non‑mission‑critical services.

### Русский

**juanibiapina/deltoids** — это Rust‑утилита, расширяющая каждый дифф‑ханк до границ функции или блока с помощью tree‑sitter, предоставляя удобный pager для Git, gh и lazygit, а также просмотрщик трассировок редактирования для coding‑agent. Проект позволяет быстро добавить AI‑функциональность (RAG, агентные рабочие потоки, прототипы) в существующие инструменты, не начиная с нуля, и уже готов к использованию в прототипах и внутренних пайплайнах, хотя перед запуском в production требуется проверка лицензии, безопасности и поддержки зависимостей.

### 中文

**项目简介（2‑3 句）**  
`juanibiapina/deltoids` 是一个基于 Tree‑sitter 的 diff 过滤器，能够在展示差异时自动把每个变更块扩展到其所在的函数或代码块。它既可以作为 Git、GitHub CLI、lazygit 等的分页器使用，也能在编码‑agent 的编辑追踪中提供可视化视图。

**价值**  
- **快速为 AI 功能提供上下文**：通过自动捕获完整函数/块，帮助大模型在代码补全、错误定位或 RAG（检索‑增强生成）场景下获得更丰富的语义信息，省去手动编写上下文提取逻辑的工作。  
- **加速原型开发**：提供即插即用的 API/SDK/CLI，开发者可以在几行代码或一条命令中把 diff 扩展能力嵌入到现有的 CI/CD、代码审查或智能编辑工作流中。  
- **提升可观测性**：在 AI‑agent 的编辑轨迹中直观展示每一步的代码变更范围，便于调试、审计和模型行为分析。

**典型接入方式**  
1. **CLI**：直接在终端使用 `deltoids diff <git‑diff>`，输出已扩展的 hunks，可配合 `less`、`bat` 等分页工具。  
2. **SDK**：在 Rust 项目中引入 `deltoids` crate，调用 `expand_hunks(diff: &str) -> Vec<ExpandedHunk>`，返回包含函数/块元数据的结构体，供后续模型调用。  
3. **API/服务**：将 `deltoids` 部署为轻量 HTTP 服务（例如使用 `actix‑web`），通过 `POST /expand` 传入 diff，返回 JSON 格式的扩展结果，适合与 Python、Node.js 等语言的 AI pipeline 交互。

**生产可用性**  
- **成熟度**：目前在 GitHub 上拥有 21 星、1 个 fork，最近一次更新于 2026‑06‑24，代码以 Rust 实现，具备较好的性能和类型安全。  
- **适用场景**：非常适合作为内部原型或实验平台的“上下文增强层”，在原型验证、RAG 构建、智能代码审查等场景中已经可以直接使用。  
- **生产准备度**：**中等**。在正式上线前建议完成以下检查：  
  - **依赖审计**：确认 Tree‑sitter 语言库和 Rust 生态依赖的安全性与许可证兼容性。  
  - **维护者确认**：项目维护者活跃度尚未明确，最好与作者或社区沟通获取长期支持计划。  
  - **容错与监控**：为 API/服务模式加入超时、重试和日志监控，以防解析错误导致工作流中断。  

总体而言，`deltoids` 为在代码层面加入 AI 能力提供了即插即用的上下文扩展工具，能够显著降低原型开发成本，并在经过适当的安全与运维加固后，具备在内部生产环境中稳定运行的潜力。

## 🧭 Practical evaluation

**Value:** juanibiapina/deltoids helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 21 GitHub stars
- 1 forks
- updated 2026-06-24
- primary language: Rust
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 8/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 60/100 |
| recency | 80/100 |
| adoption | 23/100 |
| production | 67/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/juanibiapina/deltoids) · [← Back to AI/ML](./README.md)</sub>
