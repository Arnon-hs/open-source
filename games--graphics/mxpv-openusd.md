# mxpv/openusd

[![Stars](https://img.shields.io/github/stars/mxpv/openusd?style=flat-square&color=yellow)](https://github.com/mxpv/openusd/stargazers) [![Forks](https://img.shields.io/github/forks/mxpv/openusd?style=flat-square&color=blue)](https://github.com/mxpv/openusd/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> Native Rust USD library

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 107 |
| 🍴 **Forks** | 15 |
| 💻 **Language** | Rust |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`gamedev` `openusd` `rust` `usd` `usdz`

## 🎯 Categories

Games & Graphics

## 📝 Summary

### English

**Summary**  
mxpv/openusd is a native Rust implementation of Pixar’s Universal Scene Description (USD) format. With over 100 stars and recent activity, it can serve as a lightweight alternative to the C++‑based USD libraries for Rust‑centric pipelines, especially when the project’s README aligns with your workflow.

**Value**  
- **Rust‑first**: Provides idiomatic Rust APIs, eliminating the need for FFI bindings to the official C++ USD core.  
- **Performance‑friendly**: Leverages Rust’s zero‑cost abstractions and memory safety, which can simplify concurrent scene processing.  
- **Open‑source & Extensible**: The codebase is openly available, making it easy to add custom USD extensions or integrate with other Rust crates.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the examples in the README, and verify that it can read/write the USD files used in your pipeline.  
2. **Dependency audit** – Check the crate’s transitive dependencies for licensing, maintenance frequency, and compatibility with your existing Rust toolchain.  
3. **Integration shim** – Wrap the library in a small adaptor layer that translates your internal scene representation to/from USD, then run a targeted test (e.g., a single asset export).  
4. **Iterate** – Expand coverage to more USD features as needed, contributing back any missing functionality.

**Production readiness**  
- **Maturity**: Medium. The library is actively maintained (last update 2026‑06‑25) and has a modest community (107 stars, 15 forks), but it lacks the extensive validation and ecosystem support of the official USD C++ stack.  
- **Risks**: Integration steps are not fully documented; you’ll need to verify that required USD schemas and plugins are supported and assess the effort to keep the crate up‑to‑date.  
- **Recommendation**: Suitable for prototypes, internal tools, or services where a pure‑Rust stack is a priority. Before moving to production, perform a thorough dependency review, add automated tests around your critical USD workflows, and monitor upstream changes for breaking updates.

### Русский

OpenUSD — это нативная библиотека USD, написанная на Rust, которая позволяет работать с сценами и данными Universal Scene Description без привлечения C++‑кода. Она подходит для быстрого прототипирования или внутренних пайплайнов, где уже используется Rust, однако из‑за ограниченной документации и неочевидного процесса интеграции её стоит сначала проверить в небольшом proof‑of‑concept и убедиться в совместимости с текущим workflow. Готовность к production — средняя: библиотека стабильно обновляется и имеет небольшую, но активную пользовательскую базу, однако перед масштабным внедрением требуется оценить затраты на настройку и поддержку зависимости.

### 中文

**项目简介**  
mxpv/openusd 是一个用 Rust 编写的原生 USD（Universal Scene Description）库，旨在为 Rust 生态提供高性能、类型安全的 USD 读取、写入与编辑能力。

**价值**  
- **Rust 原生实现**：避免了 C++‑FFI 的开销与安全隐患，天然兼容 Rust 的所有权与并发模型。  
- **高效且安全**：利用 Rust 的零成本抽象，实现对大规模场景数据的快速解析与序列化，同时在编译期捕获大多数错误。  
- **生态桥梁**：可直接在 Rust‑based 渲染、仿真或游戏引擎中使用 USD，填补了 Rust 与行业标准 USD 之间的空白。

**典型接入方式**  
1. **阅读 README 与示例**：项目已提供 `Cargo.toml` 示例依赖和最小的 “hello_usd” 示例代码。  
2. **在 Cargo 项目中添加依赖**：  
   ```toml
   [dependencies]
   openusd = { git = "https://github.com/mxpv/openusd.git", tag = "v0.x.x" }
   ```  
3. **编写小型 PoC**：使用 `openusd::Stage::new()` 打开或创建 `.usd` 文件，调用 `openusd::Prim`、`openusd::Attribute` 等 API 完成基本的读写操作，验证编译、运行时行为以及与现有数据管线的兼容性。  
4. **逐步迁移**：在 PoC 稳定后，将核心的场景导入/导出逻辑迁移到生产代码中，配合 CI 检查库的更新频率与破坏性变更。

**生产可用性**  
- **成熟度**：已有 107 星、15 Fork，最近一次提交在 2026‑06‑25，活跃度尚可。  
- **适用场景**：非常适合内部原型、研发工具或需要 Rust 全栈的渲染/仿真系统。  
- **风险与注意事项**：  
  - 文档相对简略，集成路径需自行探索；建议先在受控环境中完成功能验证。  
  - 关注 upstream 的发布节奏和依赖的 C++ USD 库版本，以防二进制兼容性问题。  
  - 在进入生产前，进行依赖审计、性能基准以及长期维护计划（例如锁定特定 tag、制定升级策略）。  

综上，openusd 为 Rust 项目提供了直接使用 USD 的能力，适合作为原型或内部工作流的技术选型；在投入生产前，需要通过小规模 PoC 验证其功能、性能与维护成本。

## 🧭 Practical evaluation

**Value:** mxpv/openusd may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 107 GitHub stars
- 15 forks
- updated 2026-06-25
- primary language: Rust
- 5 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 30/100 |
| stars | 43/100 |
| topics | 63/100 |
| outlook | 63/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 40/100 |
| production | 63/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/mxpv/openusd) · [← Back to Games--graphics](./README.md)</sub>
