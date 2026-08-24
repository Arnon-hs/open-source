# mourner/delaunator-rs

[![Stars](https://img.shields.io/github/stars/mourner/delaunator-rs?style=flat-square&color=yellow)](https://github.com/mourner/delaunator-rs/stargazers) [![Forks](https://img.shields.io/github/forks/mourner/delaunator-rs?style=flat-square&color=blue)](https://github.com/mourner/delaunator-rs/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-46%2F100-brightgreen?style=flat-square)](#)

> Fast 2D Delaunay triangulation in Rust. A port of Delaunator.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 244 |
| 🍴 **Forks** | 31 |
| 💻 **Language** | Rust |
| 📈 **Score** | 46/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`algorithms` `delaunay-triangulation` `geometry` `rust` `spatial`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
Mourner’s *delaunator‑rs* is a high‑performance Rust implementation of the 2‑D Delaunay triangulation algorithm, directly ported from the popular JavaScript library Delaunator. With 244 GitHub stars and recent activity (last commit 2026‑05‑12), it offers a well‑tested, zero‑dependency crate that can generate triangulations in O(n log n) time.  

**Value**  
The crate gives Rust projects a fast, deterministic way to compute Delaunay triangulations without pulling in heavyweight geometry libraries, making it ideal for graphics, GIS, mesh generation, or any workflow that needs rapid planar subdivision. Its API mirrors the original Delaunator, so developers familiar with that library can adopt it with minimal learning curve.  

**Practical adoption path**  

1. **Proof‑of‑concept** – Add `delaunator-rs` as a dev‑dependency and run the examples from the README on a small data set to verify correctness and performance.  
2. **Integration** – Wrap the triangulation call in a thin abstraction layer (e.g., a `Triangulator` trait) so the rest of the codebase remains decoupled from the concrete crate.  
3. **Testing & validation** – Include property‑based tests (e.g., using `proptest`) to ensure the triangulation respects the Delaunay condition for your input domain.  
4. **Security & licensing review** – Confirm the MIT license is compatible with your product and run a dependency scanner (e.g., `cargo audit`) to check for known vulnerabilities.  

**Production readiness**  
The library is **medium‑ready**: its recent maintenance, modest dependency footprint, and solid benchmark reputation make it suitable for prototypes and internal services, but you should perform the above integration checks and monitor upstream activity before deploying to a critical production environment. Once the wrapper and test suite are in place, *delaunator‑rs* can be promoted to production with confidence.

### Русский

**Краткое резюме:**  
`mourner/delaunator-rs` — быстрый Rust‑порт библиотеки Delaunator для 2‑D Делоне‑триангуляции, который может ускорить геометрические расчёты в проектах, требующих построения триангуляций (например, визуализация, игровые карты, GIS‑приложения). Для внедрения рекомендуется сначала реализовать небольшой proof‑of‑concept, проверив совместимость README‑примеров с вашим workflow, а затем оценить зависимости и частоту обновлений перед переходом в продакшн. Текущий уровень готовности — средний: библиотека достаточно зрелая для прототипов и внутренних сервисов, но требует дополнительной проверки лицензии, безопасности и активности мейнтейнеров перед масштабным использованием.

### 中文

**项目简介**  
`mourner/delaunator-rs` 是用 Rust 实现的 2D Delaunay 三角剖分库，直接移植自著名的 JavaScript 项目 Delaunator。它提供了极快的 O(n log n) 三角剖分算法，适合在几何计算、网格生成、可视化和游戏开发等场景中使用。

**价值点**  
- **性能**：基于 Rust 的零成本抽象和安全内存管理，运行速度媲美 C/C++ 实现，远快于纯脚本语言的方案。  
- **易用**：API 简洁，只需把点集合传入 `Delaunator::new(points)` 即可得到三角形索引数组，几行代码即可完成三角剖分。  
- **生态兼容**：与 `geo`, `nalgebra`, `wgpu` 等 Rust 几何/图形生态库配合良好，适合作为内部工具或服务的几何核心模块。  

**典型接入方式**  
1. **依赖添加**：在 `Cargo.toml` 中加入  
   ```toml
   delaunator = "0.1"
   ```  
2. **数据准备**：准备 `Vec<[f64; 2]>` 或实现 `delaunator::Point` trait 的点集合。  
3. **调用 API**：  
   ```rust
   use delaunator::{triangulate, Point};

   let points: Vec<[f64; 2]> = vec![[0.0, 0.0], [1.0, 0.0], [0.5, 1.0]];
   let delaunay = triangulate(&points);
   // `delaunay.triangles` 包含每三个索引一组的三角形
   ```  
4. **后处理**：根据业务需求，将三角形索引映射回实际坐标，或直接喂给渲染/物理引擎。

**生产可用性评估**  
- **成熟度**：已有 244 ⭐、31 fork，最近一次提交在 2026‑05‑12，活跃度尚可。代码体量小、依赖少，审计成本低。  
- **适用场景**：原型、内部工具、数据预处理以及对性能有要求的服务（如实时网格生成、路径规划）。  
- **风险**：需要自行确认许可证（MIT）与项目安全性，检查是否有未修复的 CVE，且项目维护者数量有限，建议在关键业务中做好备份实现或自行维护 fork。  
- **上线建议**：先在测试环境做一个小规模的 PoC，验证输入规模、错误处理和与现有 Rust 生态的兼容性；确认后再将其封装为内部库或微服务，配合 CI 自动化测试即可投入生产。

## 🧭 Practical evaluation

**Value:** mourner/delaunator-rs may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 244 GitHub stars
- 31 forks
- updated 2026-05-12
- primary language: Rust
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 38/100 |
| stars | 51/100 |
| topics | 63/100 |
| outlook | 43/100 |
| quality | 51/100 |
| recency | 20/100 |
| adoption | 47/100 |
| production | 47/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/mourner/delaunator-rs) · [← Back to Misc](./README.md)</sub>
