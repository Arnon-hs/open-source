# taiki-e/auto_enums

[![Stars](https://img.shields.io/github/stars/taiki-e/auto_enums?style=flat-square&color=yellow)](https://github.com/taiki-e/auto_enums/stargazers) [![Forks](https://img.shields.io/github/forks/taiki-e/auto_enums?style=flat-square&color=blue)](https://github.com/taiki-e/auto_enums/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-44%2F100-brightgreen?style=flat-square)](#)

> A library for to allow multiple return types by automatically generated enum.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 382 |
| 🍴 **Forks** | 13 |
| 💻 **Language** | Rust |
| 📈 **Score** | 44/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`no-std` `proc-macro` `rust`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`taiki-e/auto_enums` is a Rust library that generates enums automatically so that functions can return multiple concrete types without hand‑written wrappers. By leveraging procedural macros, it reduces boilerplate and makes heterogeneous return values ergonomic, which is especially handy when prototyping AI‑related pipelines that need to switch between different model outputs.

**Value**  
The crate lets developers compose AI components (e.g., LLM responses, retrieval results, tool calls) while keeping a single, type‑safe return type. This speeds up experimentation, avoids repetitive enum definitions, and integrates cleanly with existing Rust codebases that already use generics and traits.

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | Add the crate to `Cargo.toml` (`auto_enums = "…"`) and enable the `auto_enum` procedural macro. | Minimal dependency; the library is pure Rust with no external binaries. |
| 2️⃣  | Annotate functions that need multiple return types with `#[auto_enum]` (or the macro’s attribute syntax). | The macro expands to a generated enum and implements `From` for each branch automatically. |
| 3️⃣  | Review the generated code (`cargo expand`) to confirm the enum shape matches expectations. | Because integration signals are sparse, a quick compile‑time inspection guarantees correctness before wider rollout. |
| 4️⃣  | Refactor existing hand‑written enums or `Result`‑like wrappers to use the auto‑generated enum. | Reduces boilerplate and keeps the codebase consistent. |
| 5️⃣  | Run the full test suite and benchmark critical paths (especially if the enum is used in hot loops). | Ensures no hidden performance regressions. |
| 6️⃣  | Freeze the version (e.g., `auto_enums = "=0.3.2"`) and add it to internal dependency policies. | Guarantees reproducibility for production builds. |

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last update 2026‑07‑03) and has a modest but healthy community (≈382 ★, 13 forks).  
- **Stability:** The core macro API is stable, but because the library generates code, you should audit the output before committing to a production pipeline.  
- **Risk Mitigation:**  
  1. **Integration uncertainty** – verify that the generated enum aligns with your serialization/deserialization (e.g., `serde`) and error‑handling conventions.  
  2. **Dependency hygiene** – pin the version and monitor upstream releases for breaking changes.  
  3. **Performance** – the generated enums are zero‑cost abstractions, but benchmark if they are used in tight loops.  

Overall, `auto_enums` is well‑suited for prototyping AI features or internal tooling, and with a brief code‑review step it can be hardened for production use in Rust‑centric AI services.

### Русский

**auto_enums** — это Rust‑библиотека, автоматически генерирующая перечисления, позволяющие функциям возвращать несколько разных типов без ручного написания кода, что упрощает прототипирование AI‑фич, RAG‑систем и агентных воркфлоу. Она подходит для внутренних экспериментов и быстрых MVP, однако перед переходом в продакшн требуется проверка зависимости, тестовая интеграция и оценка стоимости настройки, так как путь интеграции из метаданных неочевиден. При надлежащем контроле качества проект считается готовым к среднему уровню производства.

### 中文

**简短介绍**
taiki-e/auto_enums 是一个 Rust 库，允许通过自动生成枚举来支持多个返回类型。它可以帮助开发者快速添加 AI 能力。

**价值**
taiki-e/auto_enums 的主要价值在于，它可以帮助开发者快速添加 AI 能力，而不需要从头开始搭建模型栈。它适合用于原型 AI 特性、构建 RAG 或代理工作流、评估模型工具等场景。

**典型接入方式**
由于 taiki-e/auto_enums 是一个 Rust 库，因此需要手动检查并在项目中进行整合。需要注意的是，整合信号在发现的元数据中很少见，因此需要进行额外的检查和验证。

**生产可用性**
taiki-e/auto_enums 的生产可用性为中等（Medium）。它适合用于原型或内部工作流，需要进行依赖和维护检查后才能在生产环境中使用。

## 🧭 Practical evaluation

**Value:** taiki-e/auto_enums helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 382 GitHub stars
- 13 forks
- updated 2026-07-03
- primary language: Rust
- 3 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 55/100 |
| topics | 38/100 |
| outlook | 48/100 |
| quality | 52/100 |
| recency | 40/100 |
| adoption | 48/100 |
| production | 50/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/taiki-e/auto_enums) · [← Back to Misc](./README.md)</sub>
