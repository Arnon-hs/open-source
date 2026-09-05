# dust-engine/dust

[![Stars](https://img.shields.io/github/stars/dust-engine/dust?style=flat-square&color=yellow)](https://github.com/dust-engine/dust/stargazers) [![Forks](https://img.shields.io/github/forks/dust-engine/dust?style=flat-square&color=blue)](https://github.com/dust-engine/dust/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> A research project trying to push the boundaries of voxel geometry and interactivity. Experimental real-time global illumination renderer powered by Rust, Vulkan and Bevy.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 124 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | Rust |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`game-engine` `rust` `voxel` `voxel-engine` `voxels`

## 🎯 Categories

Games & Graphics

## 📝 Summary

### English

**Summary:** dust-engine/dust is an open-source project that pushes the boundaries of voxel geometry and interactivity with a real-time global illumination renderer powered by Rust, Vulkan, and Bevy. Although its value proposition is not immediately clear, it may be useful for specific workflows that match its README and activity. The project has a medium production readiness level, making it suitable for prototypes or internal workflows.

**Value:** The value of dust-engine/dust lies in its experimental real-time global illumination renderer, which can be used to create visually stunning and interactive voxel-based environments. Its use cases are not explicitly defined, but it may be useful for developers who require high-performance voxel rendering capabilities.

**Practical Adoption Path:** To adopt dust-engine/dust, start by evaluating its README and activity to determine if it matches a specific workflow. Next, create a small proof of concept to test the integration and validate the setup cost. This will help identify potential risks and ensure that the project is a good fit for your needs.

**Production Readiness:** dust-engine/dust has a medium production readiness level, indicating that it is suitable for prototypes or internal workflows but may not be ready for large-scale production use. Before committing to production, perform dependency and maintenance checks to ensure that the project is stable and scalable.

### Русский

dust-engine/dust — это экспериментальный движок на Rust, использующий Vulkan и Bevy для реализации в реальном времени глобального освещения в воксельных сценах. Он подходит для прототипов и внутренних инструментов, где требуется исследовать новые подходы к воксельной геометрии и интерактивности; рекомендуется начать с небольшого proof‑of‑concept, проверив README и текущую активность репозитория. Готовность к production средняя: проект стабилен для экспериментов, но перед внедрением в продакшн следует оценить зависимости, поддерживаемость и затраты на интеграцию.

### 中文

**价值**  
Dust‑engine/dust 是一个基于 Rust、Vulkan 与 Bevy 的实验性实时全局光照渲染器，专注于体素几何与交互性的前沿研究。它提供了高效的 GPU‑driven 光照管线和灵活的 ECS 框架，适合想在原型阶段快速验证体素渲染、光照和物理交互概念的研发团队。

**典型接入方式**  

1. **先行评估**  
   - 克隆仓库并阅读 `README.md`，确认所需的 Rust toolchain（stable 1.78+）和 Vulkan SDK 已安装。  
   - 运行 `cargo run --example simple_voxel`（或项目自带的 demo）验证本地能够成功编译并启动窗口。  

2. **小规模 PoC**  
   - 在现有 Bevy 项目中通过 `cargo add dust-engine/dust`（或在 `Cargo.toml` 中添加路径依赖）引入 `dust` crate。  
   - 只引入渲染子系统（`dust::renderer`），保持原有游戏逻辑不变，使用 `App::add_plugin(dust::RendererPlugin)` 将渲染插件挂载到 Bevy 调度器。  
   - 通过 `dust::voxel::MeshBuilder` 构造一个或几个体素网格，验证光照效果和交互响应是否符合预期。  

3. **逐步扩展**  
   - 若 PoC 成功，可进一步集成 `dust::physics`、`dust::material` 等模块，或在自定义系统中调用 `dust::global_illumination::update` 进行实时 GI 更新。  
   - 通过 CI（GitHub Actions）跑一次完整的 `cargo test`，确认依赖链在你的 CI 环境中可复现。  

**生产可用性**  

| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | 中等 | 项目活跃（最近一次提交 2026‑07‑02），但仍属实验性质，API 可能会有不向后兼容的变更。 |
| **依赖管理** | 需要审查 | 依赖 Rust、Vulkan SDK 与 Bevy，需确保目标平台的驱动和库兼容；建议在内部镜像仓库锁定版本。 |
| **文档/示例** | 基础 | README 提供了快速启动示例，缺少完整的 API 文档和生产级指南，需自行补充。 |
| **社区/维护** | 小规模 | 124 星、5 Fork，社区规模有限，遇到问题可能只能依赖作者或自行排查。 |
| **适用场景** | 原型/内部工具 | 对体素渲染、实时 GI 有强需求的原型或内部可视化工具非常适合；直接用于面向客户的生产线需额外做稳定性和安全性评估。 |

**结论**  
Dust‑engine/dust 适合作为 **原型验证** 或 **内部研发工具** 的渲染核心，尤其是需要实验性体素光照的项目。接入时建议先在独立的 PoC 中验证编译与运行环境，然后逐步把渲染插件迁入现有 Bevy 项目。若要在生产环境使用，需要对依赖版本、API 稳定性以及缺失的文档进行额外的内部封装和测试。

## 🧭 Practical evaluation

**Value:** dust-engine/dust may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 124 GitHub stars
- 5 forks
- updated 2026-07-02
- primary language: Rust
- 5 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 45/100 |
| topics | 63/100 |
| outlook | 65/100 |
| quality | 61/100 |
| recency | 80/100 |
| adoption | 38/100 |
| production | 63/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/dust-engine/dust) · [← Back to Games--graphics](./README.md)</sub>
