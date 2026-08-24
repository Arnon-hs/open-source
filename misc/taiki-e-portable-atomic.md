# taiki-e/portable-atomic

[![Stars](https://img.shields.io/github/stars/taiki-e/portable-atomic?style=flat-square&color=yellow)](https://github.com/taiki-e/portable-atomic/stargazers) [![Forks](https://img.shields.io/github/forks/taiki-e/portable-atomic?style=flat-square&color=blue)](https://github.com/taiki-e/portable-atomic/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-44%2F100-brightgreen?style=flat-square)](#)

> Portable atomic types including support for 128-bit atomics, atomic float, etc.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 238 |
| 🍴 **Forks** | 23 |
| 💻 **Language** | Rust |
| 📈 **Score** | 44/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`atomic` `no-std` `rust`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Portable‑Atomic is a Rust library that provides a consistent, cross‑platform API for atomic operations, including 128‑bit atomics, atomic floating‑point types, and other non‑standard atomics that the Rust standard library lacks on many targets. By abstracting away the platform‑specific intrinsics and fallback implementations, it lets developers write lock‑free code that works on both desktop and embedded environments without having to maintain multiple code paths.

**Value**  
- **Broader atomic support** – Enables true lock‑free data structures and high‑performance concurrency primitives on platforms that only expose 64‑bit atomics in the standard library.  
- **Safety and ergonomics** – Wraps unsafe intrinsics in safe Rust abstractions, reducing the risk of subtle memory‑ordering bugs.  
- **Future‑proofing** – The crate is actively maintained (238 ★, recent updates) and tracks emerging compiler and hardware support, so projects can adopt advanced atomics now and keep them portable as new targets appear.

**Practical Adoption Path**  
1. **Add the dependency**: `cargo add portable-atomic` (or add the crate to `Cargo.toml`).  
2. **Select the needed feature flags** (e.g., `atomic64`, `atomic128`, `float`) to compile only the atomics required for your target platforms, keeping binary size low.  
3. **Replace standard atomics** (`std::sync::atomic::*`) with the equivalents from `portable_atomic::atomic::*`. The API mirrors the std types, so migration is straightforward.  
4. **Run the crate’s test suite** on each target (desktop, ARM, WASM, etc.) to verify that the fallback implementations work as expected.  
5. **Audit the build output** for any `#[cfg]`‑driven conditional compilation warnings; adjust feature flags if needed.

**Production Readiness**  
- **Maturity**: Medium. The library is stable, well‑starred, and receives regular updates, making it suitable for internal services and prototypes.  
- **Risk considerations**: Because the integration path is not fully documented in the metadata, teams should perform a small‑scale validation on each target platform to confirm that the correct atomic implementation (native vs. fallback) is selected and that performance meets expectations.  
- **Maintenance**: Monitor the crate’s changelog for breaking changes (especially when new Rust versions add native 128‑bit atomics) and pin a compatible version in `Cargo.lock` for production builds.  

Overall, Portable‑Atomic offers a practical way to unlock high‑performance lock‑free algorithms across diverse Rust targets, provided that teams allocate a brief validation phase before rolling it out to production.

### Русский

**Portable‑atomic** — это библиотека на Rust, предоставляющая кроссплатформенные атомарные типы, включая 128‑битные атомики и атомарные числа с плавающей точкой, что упрощает написание безопасного конкурентного кода без зависимости от специфичных для платформы реализаций. Типичный сценарий — прототипирование или внутренние сервисы, где требуется высокопроизводительная синхронизация (например, в системах RAG/агентных воркфлоу) и быстрый ввод AI‑фич без собственного низкоуровневого стека. Готовность к production — средний уровень: библиотека стабильно поддерживается (238 звёзд, активные обновления), но требует ручной проверки интеграции и оценки затрат на поддержку перед масштабным развертыванием.

### 中文

**项目简介**  
`taiki-e/portable-atomic` 是一个 Rust 库，提供跨平台的原子类型实现，支持 128 位原子操作、原子浮点数等在标准库中缺失或平台受限的特性。它通过条件编译和内部汇编实现，在不依赖平台特定 API 的情况下，让同一套代码在各种硬件上都能安全使用高级原子操作。

**价值**  
- **跨平台一致性**：在 x86、ARM、WebAssembly 等不同目标上都能使用同一套原子 API，避免因平台差异导致的并发错误。  
- **功能补全**：提供标准库尚未覆盖的 128 位原子和原子浮点数，适合高精度计数、并行数值计算等场景。  
- **零依赖、轻量**：纯 Rust 实现，编译后体积小，易于在性能敏感的项目中引入。

**典型接入方式**  
1. **在 Cargo.toml 中添加依赖**  
   ```toml
   [dependencies]
   portable-atomic = "0.5"
   ```
2. **在代码中使用**  
   ```rust
   use portable_atomic::{AtomicU128, AtomicF64, Ordering};

   let counter = AtomicU128::new(0);
   counter.fetch_add(1, Ordering::SeqCst);

   let atomic_f = AtomicF64::new(0.0);
   atomic_f.store(3.14, Ordering::Relaxed);
   ```
3. **编译目标检查**（可选）  
   对于不支持的目标，库会自动回退到安全的模拟实现或编译错误，开发者只需关注 `cfg` 条件即可。

**生产可用性**  
- **成熟度**：截至 2026‑06‑25，项目拥有 238+ ★、23+ Fork，最近一次提交仍在活跃维护，表明社区对其需求和维护力度较高。  
- **适用范围**：非常适合内部原型、实验性服务以及对并发安全有严格要求的生产系统。  
- **风险与注意事项**  
  - **集成成本**：库的功能主要通过内部汇编实现，某些极端目标（如极旧的嵌入式平台）可能需要手动检查或提供自定义实现。  
  - **依赖审计**：在正式上线前，建议审计其 `Cargo.lock` 中的全部依赖，并进行性能基准测试，以确认在目标平台上的实际开销。  

综上，`portable-atomic` 为需要跨平台原子操作的 Rust 项目提供了可靠且易于上手的解决方案，只要在部署前完成一次兼容性验证，就可以在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** taiki-e/portable-atomic helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 238 GitHub stars
- 23 forks
- updated 2026-06-25
- primary language: Rust
- 3 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 51/100 |
| topics | 38/100 |
| outlook | 48/100 |
| quality | 51/100 |
| recency | 40/100 |
| adoption | 46/100 |
| production | 49/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/taiki-e/portable-atomic) · [← Back to Misc](./README.md)</sub>
