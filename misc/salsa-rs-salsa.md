# salsa-rs/salsa

[![Stars](https://img.shields.io/github/stars/salsa-rs/salsa?style=flat-square&color=yellow)](https://github.com/salsa-rs/salsa/stargazers) [![Forks](https://img.shields.io/github/forks/salsa-rs/salsa?style=flat-square&color=blue)](https://github.com/salsa-rs/salsa/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> A generic framework for on-demand, incrementalized computation. Inspired by adapton, glimmer, and rustc's query system.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.9k |
| 🍴 **Forks** | 214 |
| 💻 **Language** | Rust |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
`salsa-rs/salsa` is a Rust library that provides a generic, on‑demand incremental computation framework, inspired by the ideas behind Adapton, Glimmer, and the Rust compiler’s query system. It lets you declare “queries” whose results are cached and automatically recomputed only when their inputs change, making large, inter‑dependent pipelines fast and deterministic.  

**Value**  
- **Speed & determinism** – By recomputing only the parts of a graph that are affected by a change, Salsa can shrink rebuild times from minutes to seconds for data‑intensive tools (e.g., language servers, build systems, static analysis).  
- **Zero‑cost abstraction** – The API is pure Rust, with no runtime garbage collection; caching is handled through lifetimes and ownership, so you get compile‑time safety with minimal overhead.  
- **Extensible design** – Queries are defined as plain Rust functions, and the framework supplies a macro‑based DSL to declare dependencies, making it easy to retrofit into existing Rust codebases.  

**Practical Adoption Path**  
1. **Prototype** – Add `salsa = "0.x"` to `Cargo.toml` and start by converting a small, pure‑function component into a Salsa “database” (define a `Database` trait and a few queries).  
2. **Benchmark** – Compare incremental rebuild times against the current naïve recomputation to validate the performance win.  
3. **Iterate** – Gradually migrate more modules, using Salsa’s `#[salsa::query_group]` and `#[salsa::tracked]` attributes to express dependencies.  
4. **Tooling** – Integrate with your build pipeline (e.g., Cargo scripts, CI) to persist the on‑disk cache if needed, and add tests that exercise cache invalidation paths.  

**Production Readiness**  
- **Maturity** – With ~2.9 k stars, 214 forks, and recent commits (as of 2026‑06‑26), the project is actively maintained and battle‑tested in several open‑source tools.  
- **Risk level** – Medium. The core library is stable, but integration details (e.g., custom storage back‑ends, multi‑threaded query execution) are not extensively documented, so a small amount of engineering effort is required to fit it into complex workflows.  
- **Recommendation** – Suitable for internal services, prototypes, or as the backbone of a new language server/analysis tool. Before a full production rollout, perform a dependency audit, verify that the incremental model aligns with your data flow, and run a pilot to gauge the setup cost and long‑term maintenance burden.

### Русский

Salsa‑rs / salsa — это универсальный фреймворк на Rust для построения on‑demand и инкрементальных вычислений, позволяющий автоматически кэшировать результаты запросов и пересчитывать только затронутые части при изменении входных данных. Он идеален для прототипов и внутренних систем, где требуется гибкая система запросов (например, компиляторы, анализаторы кода или сложные графы зависимостей), однако перед внедрением следует вручную проверить совместимость и оценить стоимость интеграции, так как готовые «plug‑and‑play» решения в метаданных отсутствуют. Уровень готовности к production — средний: проект активен (обновлён 2026‑06‑26, 2881 звёзд), но требует дополнительного аудита зависимостей и поддержки перед использованием в критически важных сервисах.

### 中文

**项目简介**  
`salsa-rs/salsa` 是一个基于 Rust 的通用增量计算框架，支持按需（on‑demand）和增量化（incrementalized）地执行查询。它的设计受到了 Adapton、Glimmer 以及 Rust 编译器（rustc）查询系统的启发，能够在大量相互依赖的计算中自动缓存并仅在输入变化时重新计算受影响的部分。

**价值**  
- **高效增量更新**：在数据或配置变化时，只重新计算受影响的查询，避免全量重算，显著提升响应速度。  
- **抽象统一的查询模型**：通过声明式的 `query` 宏，开发者可以像写普通函数一样定义依赖关系，框架负责管理缓存和调度。  
- **Rust 生态友好**：全 Rust 实现、零运行时开销、无 GC，天然兼容 Cargo、async/await 等生态工具，适合编译器、IDE、游戏引擎、数据流处理等需要高性能增量计算的场景。

**典型接入方式**  
1. **在 Cargo.toml 中添加依赖**  
   ```toml
   [dependencies]
   salsa = "0.16"
   ```  
2. **定义数据库（Database）和查询**  
   ```rust
   #[salsa::database]
   #[derive(Default)]
   struct MyDatabase {
       storage: salsa::Storage<Self>,
   }

   #[salsa::query_group(MyQueries)]
   trait MyQueries {
       #[salsa::input]
       fn source(&self, id: u32) -> String;

       #[salsa::invoke(my_compute)]
       fn computed(&self, id: u32) -> usize;
   }

   fn my_compute(db: &dyn MyQueries, id: u32) -> usize {
       let src = db.source(id);
       // 这里写实际的计算逻辑
       src.len()
   }
   ```
3. **在业务代码中创建数据库实例并使用**  
   ```rust
   let mut db = MyDatabase::default();
   db.set_source(1, "hello".into());
   let len = db.computed(1); // 首次计算
   let len2 = db.computed(1); // 直接命中缓存
   ```
4. **增量化使用**：当 `source` 输入改变后，只有依赖 `computed` 的查询会被重新调度，其他查询保持缓存。

**生产可用性**  
- **成熟度**：截至 2026‑06‑26，项目拥有约 2.9k ⭐、214 forks，活跃维护，最近一次提交在同日，社区活跃度良好。  
- **适用场景**：非常适合作为内部原型、工具链、IDE 插件或业务系统的增量计算层；在对性能和一致性要求高、且可以接受一定的学习成本时，也可用于生产环境。  
- **风险与注意事项**  
  - 框架的接入点主要是代码层面的 `Database` 与 `query` 定义，缺少即插即用的配置或插件式集成，需要开发者自行设计数据库结构。  
  - 依赖的 Rust 版本和编译器特性需保持同步，升级时需检查兼容性。  
  - 对于极其复杂的依赖图，调试缓存失效可能需要额外的日志或自定义 `debug` 钩子。  

**结论**：`salsa-rs/salsa` 在需要高效增量计算的 Rust 项目中提供了强大的抽象和性能优势。若项目已有 Rust 代码基并能够投入一定的集成工作，它完全可以在生产环境中使用；否则建议先在原型或内部工具中验证其集成成本与收益后再决定是否推广。

## 🧭 Practical evaluation

**Value:** salsa-rs/salsa may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 2881 GitHub stars
- 214 forks
- updated 2026-06-26
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 58/100 |
| stars | 74/100 |
| topics | 0/100 |
| outlook | 67/100 |
| quality | 66/100 |
| recency | 80/100 |
| adoption | 69/100 |
| production | 64/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/salsa-rs/salsa) · [← Back to Misc](./README.md)</sub>
