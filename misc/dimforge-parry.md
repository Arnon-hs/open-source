# dimforge/parry

[![Stars](https://img.shields.io/github/stars/dimforge/parry?style=flat-square&color=yellow)](https://github.com/dimforge/parry/stargazers) [![Forks](https://img.shields.io/github/forks/dimforge/parry?style=flat-square&color=blue)](https://github.com/dimforge/parry/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-44%2F100-brightgreen?style=flat-square)](#)

> 2D and 3D collision-detection library for Rust.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 819 |
| 🍴 **Forks** | 144 |
| 💻 **Language** | Rust |
| 📈 **Score** | 44/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`collision-detection` `gamedev` `rust-lang`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
Parry is a Rust library that provides fast, robust 2‑D and 3‑D collision‑detection primitives (bounding‑volume hierarchies, ray casting, shape queries, etc.). With over 800 ⭐ on GitHub and recent activity, it can serve as the geometric core for games, simulations, or any Rust project that needs precise contact handling.  

**Value**  
Parry offers a well‑tested, mathematically‑sound collision pipeline without pulling in heavyweight game‑engine dependencies, making it ideal for custom physics pipelines, procedural generation tools, or scientific visualizations that run on Rust’s zero‑cost abstractions. Its generic API works across dimensions, so the same codebase can handle both 2‑D and 3‑D scenarios, reducing duplication and maintenance overhead.  

**Practical Adoption Path**  

1. **Evaluate Fit** – Clone the repo and run the example programs (`cargo run --example …`) to confirm that the supported shape types and query APIs match your use‑case.  
2. **Prototype Integration** – Add `parry2d = "0.x"` or `parry3d = "0.x"` to your `Cargo.toml`, wrap your domain objects in Parry’s `Collider`/`Shape` structs, and replace any ad‑hoc intersection checks with Parry’s query functions (e.g., `intersection_test`, `cast_ray`).  
3. **Performance Check** – Benchmark the collision queries on realistic data sets (the repository includes a `benches` folder) to ensure latency meets your requirements.  
4. **Tooling & CI** – Enable `cargo clippy` and `cargo test` in your CI pipeline; Parry’s own test suite can be run as a sanity check (`cargo test --all`).  
5. **Maintenance Guardrails** – Pin the library to a specific minor version, monitor the upstream repository for breaking changes, and consider forking if you need long‑term stability beyond the community release cadence.  

**Production Readiness**  
Parry sits at a “medium” readiness level: it is mature enough for prototypes, internal tools, and even production services that can tolerate a modest integration effort. The codebase is actively maintained (last commit 2026‑05‑12) and has a healthy community signal (≈ 800 stars, 144 forks). However, because the library is low‑level and its integration patterns are not documented in a step‑by‑step guide, teams should allocate time for a manual inspection of the API surface, dependency graph, and build compatibility with their existing Rust toolchain before committing to a production release. Once those checks are done, Parry can be safely used as the collision‑detection backbone of Rust‑based applications.

### Русский

**dimforge/parry** — это кроссплатформенная библиотека на Rust для 2‑D и 3‑D обнаружения столкновений, активно поддерживаемая (819★, 144 форка, последнее обновление 2026‑05‑12). Она подходит для быстрого прототипирования и внутренних систем, где требуется точный физический контроль над пересечениями (игровые движки, симуляции, CAD‑приложения), однако путь интеграции не очевиден из метаданных, поэтому перед внедрением стоит проверить совместимость и оценить затраты на настройку. При достаточной проверке зависимостей и обслуживании библиотека считается готовой к production‑использованию со средним уровнем риска.

### 中文

**项目简介**  
dimforge / parry 是用 Rust 编写的 2D/3D 碰撞检测库，提供高精度的形状相交、射线投射、接触点生成等核心算法，适合游戏、仿真和实时物理系统。

**价值**  
- **性能与安全**：基于 Rust 的零成本抽象和所有权系统，运行时几乎没有 GC 开销，且在编译期即可捕获大多数内存安全问题。  
- **完整的几何支持**：内置球体、立方体、胶囊、凸多边形/多面体、网格等常用形状，支持层次包围体（BVH）加速大规模碰撞查询。  
- **灵活的 API**：既可以直接使用高层函数进行“一键”碰撞检测，也可以自行构建 `Collider`、`BroadPhase`、`NarrowPhase` 组合，实现自定义的碰撞过滤和事件回调。

**典型接入方式**  
1. **依赖声明**：在 `Cargo.toml` 中加入  
   ```toml
   [dependencies]
   parry = "0.13"
   ```  
2. **创建形状并进行查询**：  
   ```rust
   use parry3d::shape::{Cuboid, Shape};
   use parry3d::query::intersection_test;

   let a = Cuboid::new(Vector::new(1.0, 1.0, 1.0));
   let b = Cuboid::new(Vector::new(0.5, 0.5, 0.5));

   // 位姿使用 Isometry（位置+旋转）
   let pos_a = Isometry::identity();
   let pos_b = Isometry::translation(0.8, 0.0, 0.0);

   let collides = intersection_test(&pos_a, &a, &pos_b, &b);
   println!("是否相交: {}", collides);
   ```  
3. **大规模碰撞**：如果需要对成千上万的对象进行快速粗筛，可使用 `BoundingVolumeHierarchy`（BVH）或 `SpatialHash`，配合 `BroadPhase` / `NarrowPhase` 的组合模式。官方示例和 `parry2d`/`parry3d` 的文档提供了完整的工作流示例。  

**生产可用性**  
- **成熟度**：已有 800+ ⭐、140+ forks，最近一次提交在 2026‑05‑12，活跃度良好，表明社区仍在维护。  
- **适用场景**：非常适合内部原型、工具链或对性能要求高的游戏/仿真模块；在对安全性有严格要求的 Rust 项目中尤为匹配。  
- **风险与准备**：库本身提供的 API 完整，但集成路径（如与物理引擎、渲染系统的协同）在元数据中描述有限，建议在引入前：  
  1. **评估依赖树**：确认与现有项目的 Rust 版本兼容，检查是否有冲突的 `nalgebra`/`glam` 版本。  
  2. **编写小型验证用例**：验证形状创建、BVH 更新、并发查询等关键路径是否满足性能预期。  
  3. **监控维护状态**：关注仓库的 Issue 与 PR 活动，确保出现关键 bug 时能得到及时响应。  

综上，parry 在性能、安全性和功能完整性方面具备中等到高的生产就绪度，适合作为内部或面向特定业务的碰撞检测核心，只需在正式上线前完成一次集成验证即可。

## 🧭 Practical evaluation

**Value:** dimforge/parry may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 819 GitHub stars
- 144 forks
- updated 2026-05-12
- primary language: Rust
- 3 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 54/100 |
| stars | 62/100 |
| topics | 38/100 |
| outlook | 44/100 |
| quality | 53/100 |
| recency | 20/100 |
| adoption | 60/100 |
| production | 45/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/dimforge/parry) · [← Back to Misc](./README.md)</sub>
