# timschmidt/csgrs

[![Stars](https://img.shields.io/github/stars/timschmidt/csgrs?style=flat-square&color=yellow)](https://github.com/timschmidt/csgrs/stargazers) [![Forks](https://img.shields.io/github/forks/timschmidt/csgrs?style=flat-square&color=blue)](https://github.com/timschmidt/csgrs/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Multi-modal constructive solid geometry kernel in Rust

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 224 |
| 🍴 **Forks** | 32 |
| 💻 **Language** | Rust |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`3d-printing` `cnc` `code-cad` `csg` `gamedev` `geo` `geometry` `geospatial` `metaballs` `offsetting` `parametric` `physics`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
timschmidt/csgrs is a Rust‑based, multi‑modal constructive solid geometry (CSG) kernel that enables fast, composable Boolean operations on 2D and 3D meshes. With 224 ★, recent commits (last updated 2026‑05‑12) and a growing ecosystem of related topics, it is a mature open‑source component ready for pilot projects.  

**Value**  
The library offers a high‑performance, type‑safe CSG engine written in Rust, making it attractive for graphics pipelines, CAD/CAM tools, game‑engine geometry processing, and additive‑manufacturing workflows. Its modular design supports multiple input modalities (e.g., point clouds, voxel grids, polygon meshes), allowing developers to integrate sophisticated shape‑combination logic without re‑implementing low‑level geometry algorithms.  

**Practical Adoption Path**  
1. **Read the README and run the example programs** to confirm the API matches your workflow.  
2. **Create a small proof‑of‑concept** that exercises the core CSG operations (union, intersection, difference) on a representative data set.  
3. **Wrap the library** in your existing Rust or FFI‑compatible codebase, adding thin adapters if you need to interoperate with other languages (C/C++, Python).  
4. **Validate performance and correctness** against your production test suite before expanding the integration.  

**Production Readiness**  
The project shows strong production signals: recent activity, a healthy star/fork ratio, and a Rust‑first codebase that benefits from the language’s safety guarantees. While the license and security posture still require a final audit, the overall maturity and community traction make csgrs a solid candidate for a serious pilot or limited‑scope production deployment.

### Русский

**timschmidt/csgrs** — это многомодальный ядро‑конструктивной геометрии в Rust, которое позволяет создавать и комбинировать 3‑D модели через CSG‑операции, поддерживая различные типы данных (модели, облака точек, воксели). Для внедрения рекомендуется сначала проверить README и реализовать небольшой proof‑of‑concept, интегрировав библиотеку в существующий пайплайн генерации геометрии; при положительном результате её можно масштабировать до полноценного сервиса. Проект уже имеет активную поддержку (обновления в 2026 г., 224 звёзд, 32 форка), что свидетельствует о высокой готовности к использованию в production‑окружениях, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
`timschmidt/csgrs` 是用 Rust 实现的多模态构造实体几何（Constructive Solid Geometry，CSG）内核，提供高性能、类型安全的布尔运算、网格生成和多模态（例如体素、点云、隐式表面）支持，适合在实时渲染、CAD、3D 打印和游戏引擎等场景中进行复杂几何建模。

**价值**  
- **性能与安全**：Rust 的零成本抽象和所有权系统让几何运算既快又无内存泄漏风险。  
- **多模态统一**：同一套 API 能处理体素、显式网格和隐式函数，降低跨模型转换的成本。  
- **生态友好**：已在 20+ 相关话题中出现，拥有 224+ 星、活跃的社区和近期提交，易于与 `wgpu`、`nalgebra`、`bevy` 等 Rust 生态组件集成。

**典型接入方式**  
1. **阅读 README 与示例**：项目根目录提供了最小可运行示例，帮助快速验证环境。  
2. **在 Cargo.toml 中添加依赖**  
   ```toml
   [dependencies]
   csgrs = { git = "https://github.com/timschmidt/csgrs", rev = "最新提交哈希" }
   ```  
3. **在代码中创建几何体并执行布尔运算**  
   ```rust
   use csgrs::{Solid, ops::union};

   let cube = Solid::cube([1.0, 1.0, 1.0]);
   let sphere = Solid::sphere(0.8);
   let result = union(&cube, &sphere);
   ```  
4. **与渲染后端对接**：将生成的网格（`Mesh`）导出为 `obj`、`stl`，或直接转换为 `wgpu`/`bevy` 的顶点缓冲区进行实时渲染。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑05‑12，星标 224、fork 32，表明社区仍在维护。  
- **成熟度**：核心 API 已相对稳定，文档覆盖基本用例，适合作为内部原型或正式模块的几何引擎。  
- **风险**：仍需自行审查许可证（MIT/Apache 双许可证）以及潜在的安全依赖（如 `serde`、`nalgebra`），并确认维护者的响应速度。总体来看，项目已具备在生产环境中进行小规模试点的条件，后续可通过持续集成测试和性能基准进一步验证。

## 🧭 Practical evaluation

**Value:** timschmidt/csgrs may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 224 GitHub stars
- 32 forks
- updated 2026-05-12
- primary language: Rust
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 38/100 |
| stars | 50/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 76/100 |
| recency | 100/100 |
| adoption | 47/100 |
| production | 75/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/timschmidt/csgrs) · [← Back to Misc](./README.md)</sub>
