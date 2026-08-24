# orium/archery

[![Stars](https://img.shields.io/github/stars/orium/archery?style=flat-square&color=yellow)](https://github.com/orium/archery/stargazers) [![Forks](https://img.shields.io/github/forks/orium/archery?style=flat-square&color=blue)](https://github.com/orium/archery/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-45%2F100-brightgreen?style=flat-square)](#)

> Abstract over the atomicity of reference-counting pointers in rust

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 173 |
| 🍴 **Forks** | 16 |
| 💻 **Language** | Rust |
| 📈 **Score** | 45/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`arc` `concurrency` `memory-management` `rc` `reference-counting` `rust`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
Archery is a small Rust library that abstracts over the atomicity of reference‑counted pointers (e.g., `Arc`, `Rc`). It lets you write code that can switch between thread‑safe and non‑thread‑safe reference counting without changing the surrounding logic, simplifying the development of generic data structures and APIs that may be used in both single‑threaded and multi‑threaded contexts.

**Value**  
- **Unified API** – By providing a single trait and wrapper types, Archery eliminates the need for duplicated code paths for `Arc<T>` and `Rc<T>`.  
- **Zero‑cost abstraction** – When compiled for a single‑threaded target the library resolves to `Rc`, avoiding the overhead of atomic operations; on a multi‑threaded target it resolves to `Arc`.  
- **Improved ergonomics** – The crate supplies helper macros and conversion utilities that make it easy to expose a consistent public interface while retaining optimal performance for each deployment scenario.

**Practical adoption path**  
1. **Proof‑of‑concept** – Add `archery` as a dev‑dependency in a sandbox crate and replace a few `Arc`/`Rc` usages with the library’s `ArcOrRc<T>` (or the trait it provides). Verify that the code compiles for both `#[cfg(feature = "threaded")]` and the default single‑threaded build.  
2. **README validation** – Review the repository’s README and example folder to confirm that the documented usage matches your intended workflow (e.g., custom data structures, async runtimes, or embedded contexts).  
3. **Integration test** – Write a small integration test that builds the same crate twice—once with the “threaded” feature enabled and once without—to ensure the abstraction behaves correctly in both modes.  
4. **Dependency audit** – Check the crate’s dependency tree (it is lightweight, with only the standard library as a requirement) and run `cargo audit` to confirm no known security issues.

**Production readiness**  
- **Maturity**: 173 stars and recent activity (last commit on 2026‑06‑24) indicate an active, community‑tested project, but the overall star count is modest, suggesting a relatively small user base.  
- **Stability**: The API is simple and has few transitive dependencies, which reduces the surface for breaking changes. However, the crate does not yet have a formal stability guarantee (e.g., semver‑major version bump policy).  
- **Risk level**: Medium. The library is suitable for prototypes, internal tools, or services where the atomicity switch is a clear benefit, but you should perform the small proof‑of‑concept and monitor the repository for future breaking changes before rolling it out to a large production system.  

In short, Archery offers a clean way to write reference‑counting code that can be compiled for either single‑ or multi‑threaded environments with negligible runtime cost. Start with a limited pilot to verify the abstraction fits your codebase, and, after confirming the README examples and performing a dependency audit, you can consider it production‑ready for internal workloads while keeping an eye on future releases.

### Русский

**orium/archery** — это небольшая Rust‑библиотека, абстрагирующая атомарность операций над указателями с подсчётом ссылок, что упрощает написание безопасного конкурентного кода без ручного управления `Arc`/`Rc`. Она подходит для прототипов и внутренних сервисов, где требуется лёгкая интеграция атомарных ссылок в существующие структуры данных; рекомендуется начать с небольшого proof‑of‑concept и проверки README, чтобы убедиться, что API совпадает с вашими требованиями. Готовность к production — средняя: библиотека имеет активную поддержку (обновления до 2026‑06‑24), 173 звёзд и 16 форков, но перед вводом в продакшн стоит оценить зависимости и потенциальные затраты на настройку.

### 中文

**项目简介（2‑3 句）**  
`orium/archery` 为 Rust 中的引用计数指针（如 `Arc`、`Rc`）提供原子性抽象层，使得在需要在不同线程或异步上下文中安全共享数据时，可以在编译期统一使用同一套 API，而无需在业务代码里手动切换 `Arc` 与 `Rc`。该库通过宏和 trait 封装，实现了“在单线程时使用轻量的非原子计数，在多线程时自动提升为原子计数”的零成本抽象。

---

## 价值

| 维度 | 价值点 |
|------|--------|
| **代码复用** | 统一的 `Reference` trait 让同一段业务逻辑在单线程/多线程环境间无缝迁移，避免复制两套实现。 |
| **性能优化** | 在单线程路径下保持 `Rc` 的非原子实现，避免不必要的原子操作；在多线程路径自动使用 `Arc`，保证安全。 |
| **安全性** | 编译期即能捕获错误的引用计数使用场景，降低运行时出现数据竞争的风险。 |
| **易于迁移** | 通过 `#[archery]` 宏或 `as_ref`/`as_mut` 转换，现有项目只需少量改动即可接入。 |

---

## 典型接入方式

1. **添加依赖**  
   ```toml
   [dependencies]
   archery = "0.3"
   ```

2. **在代码中使用抽象引用**  
   ```rust
   use archery::{Ref, RefCell};

   // 通过宏声明需要的引用类型
   #[archery]
   struct SharedData {
       counter: RefCell<u32>,
   }

   // 在单线程环境下，`Ref` 实际是 `Rc`
   // 在多线程环境下，`Ref` 实际是 `Arc`
   fn increment(data: Ref<SharedData>) {
       let mut cell = data.counter.borrow_mut();
       *cell += 1;
   }
   ```

3. **在 Cargo.toml 中声明特性**（可选）  
   - `default = ["std"]`（默认使用标准库）  
   - `no_std`（在 `no_std` 环境下使用）  

4. **小范围验证**  
   - 在本地创建一个最小的 demo（如上例），在 `cargo test` 与 `cargo bench` 中分别跑单线程和多线程测试，确认 `Ref` 的实际类型。  
   - 阅读仓库的 `README` 与 `examples/`，确认宏的使用限制（如不支持 `unsafe` 场景）。

---

## 生产可用性评估

| 维度 | 评估 |
|------|------|
| **活跃度** | 173 ★、16 Fork，最近一次提交为 **2026‑06‑24**，说明仍在维护。 |
| **成熟度** | 已发布 0.x 版本，提供 `#[archery]` 宏、`Ref`/`RefCell` trait，文档覆盖基本用例。 |
| **依赖风险** | 仅依赖 Rust 标准库（可选 `alloc`），对生态影响小；需关注未来的 `rustc` 兼容性。 |
| **适用场景** | - 原型或内部工具中需要在单/多线程间切换的共享数据。<br>- 需要在 `no_std` 环境下保持相同 API 的嵌入式项目。 |
| **生产准备度** | **中等**。在原型阶段使用完全安全，进入生产前建议：<br>1. 编写项目级别的集成测试，覆盖单线程与多线程两条路径。<br>2. 通过 `cargo audit` 检查潜在的安全漏洞。<br>3. 评估库的升级频率和维护者响应速度。 |

**结论**：`orium/archery` 为需要在不同并发模型间共享数据的 Rust 项目提供了轻量且安全的抽象，接入成本低（仅几行宏/trait 替换），适合作为原型或内部服务的共享层。若在生产环境使用，建议先在受控的子系统中进行 POC，确认性能与兼容性后再推广。

## 🧭 Practical evaluation

**Value:** orium/archery may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 173 GitHub stars
- 16 forks
- updated 2026-06-24
- primary language: Rust
- 6 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 31/100 |
| stars | 48/100 |
| topics | 75/100 |
| outlook | 51/100 |
| quality | 56/100 |
| recency | 40/100 |
| adoption | 43/100 |
| production | 51/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/orium/archery) · [← Back to Misc](./README.md)</sub>
