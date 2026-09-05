# Amanieu/intrusive-rs

[![Stars](https://img.shields.io/github/stars/Amanieu/intrusive-rs?style=flat-square&color=yellow)](https://github.com/Amanieu/intrusive-rs/stargazers) [![Forks](https://img.shields.io/github/forks/Amanieu/intrusive-rs?style=flat-square&color=blue)](https://github.com/Amanieu/intrusive-rs/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> Intrusive collections for Rust

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 530 |
| 🍴 **Forks** | 62 |
| 💻 **Language** | Rust |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
Amanieu/intrusive-rs provides a set of intrusive data structures (lists, trees, etc.) for the Rust language, allowing elements to own their linking nodes and avoid extra heap allocations. With over 500 stars and recent activity, it can be handy for low‑level or performance‑critical Rust code, but the integration details are not fully documented.  

**Value**  
The library lets you embed collection pointers directly inside your structs, which can dramatically reduce allocation overhead and improve cache locality—beneficial for systems programming, game engines, or any workload where tight control over memory layout matters. It also offers a familiar API that mirrors Rust’s safe collections while still exposing the power of intrusive techniques.

**Practical adoption path**  

1. **Evaluate the API** – Clone the repo and run the examples/tests to see how the intrusive list/tree APIs fit your data model.  
2. **Prototype** – Replace a hot‑path collection in a sandbox project with the intrusive version, measuring allocation counts and latency.  
3. **Integration checks** – Verify that the crate’s dependencies (currently just `core`/`alloc`) align with your build environment and that the required `unsafe` blocks are acceptable for your code‑review policies.  
4. **Documentation review** – Because the README is brief, browse the source code and inline comments to understand safety contracts and required invariants.  

**Production readiness**  
The project is at a **medium** readiness level: it is actively maintained (last commit 2026‑07‑02) and has a healthy star/fork count, indicating community interest, but the lack of detailed integration guides and limited usage examples means you should treat it as a **prototype‑grade** dependency. Before shipping to production, perform a thorough audit of the unsafe code, add integration tests for your specific use‑cases, and monitor the repository for future breaking changes or security updates. If those steps are satisfied, intrusive‑rs can be safely used in internal services or performance‑critical components, though a fallback to standard collections should be kept in mind for long‑term stability.

### Русский

Резюме проекта Amanieu/intrusive-rs:

Проект Amanieu/intrusive-rs предлагает коллекции с встраиванием в Rust, которые могут оказаться полезными в конкретном рабочем процессе, если README и активность проекта соответствуют этому процессу. Внедрение коллекций возможно в прототипах или внутренних рабочих процессах, но требует тщательного анализа и проверки перед выпуском в production. Уровень готовности к production оценивается как средний, что предполагает необходимость дополнительных проверок и проверок перед широким внедрением.

### 中文

**Amanieu/intrusive-rs 简介**

Amanieu/intrusive-rs 是一款 Rust 开源项目，提供了侵入式集合（Intrusive collections）功能。这种集合可以在 Rust 应用程序中使用，特别是在需要高性能和低延迟的场景下。

**价值**

Amanieu/intrusive-rs 的价值在于，它可以帮助开发者实现高性能的集合操作，尤其是在内存资源紧张的环境下。这种集合可以减少内存分配和回收的开销，从而提高应用程序的整体性能和效率。

**典型接入方式**

为了接入 Amanieu/intrusive-rs，开发者需要在项目中添加依赖，并手动检查和验证接入过程。具体步骤如下：

1. 在 Cargo.toml 文件中添加 Amanieu/intrusive-rs 的依赖。
2. 导入 Intrusive collections 的模块。
3. 使用 Intrusive collections 的 API 实现集合操作。

**生产可用性**

Amanieu/intrusive-rs 的生产可用性为中等（Medium）。虽然它可以在生产环境中使用，但

## 🧭 Practical evaluation

**Value:** Amanieu/intrusive-rs may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 530 GitHub stars
- 62 forks
- updated 2026-07-02
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 58/100 |
| topics | 0/100 |
| outlook | 60/100 |
| quality | 59/100 |
| recency | 80/100 |
| adoption | 54/100 |
| production | 62/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/Amanieu/intrusive-rs) · [← Back to Misc](./README.md)</sub>
