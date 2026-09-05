# Noxmore/bevy_trenchbroom

[![Stars](https://img.shields.io/github/stars/Noxmore/bevy_trenchbroom?style=flat-square&color=yellow)](https://github.com/Noxmore/bevy_trenchbroom/stargazers) [![Forks](https://img.shields.io/github/forks/Noxmore/bevy_trenchbroom?style=flat-square&color=blue)](https://github.com/Noxmore/bevy_trenchbroom/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> TrenchBroom integration, .map, and .bsp loading for Bevy

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 143 |
| 🍴 **Forks** | 19 |
| 💻 **Language** | Rust |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`3d` `bevy` `bevy-plugin` `game-development` `gamedev` `mapping-tools` `quake` `rust`

## 🎯 Categories

Games & Graphics

## 📝 Summary

### English

**Brief Summary**  
*bevy_trenchbroom* is a Rust library that adds native support for TrenchBroom‑created *.map* and *.bsp* files to the Bevy game engine. It provides a straightforward API for loading level geometry, entities, and textures directly into a Bevy app, making it easy to prototype or build games that rely on classic BSP‑based level design.

**Value**  
- **Seamless workflow**: Designers can continue using TrenchBroom’s visual editor while developers import the exact same level data into Bevy without writing custom parsers.  
- **Time‑saving**: The crate handles geometry conversion, texture mapping, and entity translation out of the box, reducing boilerplate and the risk of mismatched assets.  
- **Community traction**: With 143 stars and active commits as of June 2026, the project has a modest but engaged user base, indicating that the core functionality is battle‑tested for hobby and prototype projects.

**Practical Adoption Path**  
1. **Add the crate**: Include `bevy_trenchbroom = "0.x"` in your `Cargo.toml`.  
2. **Enable the plugin**: In your Bevy `App`, call `app.add_plugin(bevy_trenchbroom::TrenchBroomPlugin);`.  
3. **Load a map**: Use the provided `load_map("assets/level.map")` (or `.bsp`) function to obtain a `Scene` or entity hierarchy you can insert into your world.  
4. **Integrate with your game logic**: The plugin emits events for loaded entities, allowing you to attach custom components (e.g., AI, physics) based on TrenchBroom entity properties.  
5. **Iterate**: Re‑export the updated `.map` from TrenchBroom and hot‑reload in the running Bevy app for rapid iteration.

**Production‑Readiness Assessment**  
- **Maturity**: Medium. The crate is functional for prototypes and internal tools, but it lacks extensive documentation, automated tests, and a formal release schedule.  
- **Maintenance**: Recent commits (June 2026) show activity, yet the maintainer count is low; you should verify that security patches and dependency updates are being applied.  
- **Risk Mitigation**: Review the MIT/Apache license (as listed in the repo) for compatibility, audit the dependency tree for known CVEs, and consider pinning versions or forking the library if you need long‑term stability.  

Overall, *bevy_trenchbroom* offers a practical bridge between TrenchBroom level design and Bevy development, suitable for early‑stage projects and internal pipelines, provided you perform the usual due‑diligence checks before committing it to a production codebase.

### Русский

**Краткое резюме:**  
`Noxmore/bevy_trenchbroom` — это Rust‑библиотека, добавляющая в движок Bevy поддержку форматов уровней TrenchBroom (.map и .bsp). Она удобна для быстрого прототипирования или внутренних пайплайнов, где требуется импортировать готовые карты из TrenchBroom без написания собственного парсера. Готовность к production — средняя: проект имеет активные коммиты, 143 звёзд и базовую документацию, но перед выпуском в продакшн стоит проверить лицензию, безопасность зависимостей и наличие поддерживающего мейнтейнера.

### 中文

**项目简介（2‑3 句）**  
`Noxmore/bevy_trenchbroom` 为 Bevy 引擎提供了 TrenchBroom 关卡编辑器的原生集成，能够直接加载 `.map` 与 `.bsp` 文件并将其转换为 Bevy 可用的实体与碰撞体。该库封装了关卡解析、网格生成和 BSP 分割等核心逻辑，让开发者可以在 Rust/Bevy 项目中快速使用 TrenchBroom 设计的关卡资源。

**价值点**  
- **降低门槛**：无需自行实现复杂的 `.map/.bsp` 解析，只需几行代码即可把 TrenchBroom 的关卡导入 Bevy 场景。  
- **保持编辑器优势**：TrenchBroom 的可视化编辑、实体属性和纹理管理全部保留，编辑流程与游戏运行时解耦。  
- **Rust/Bevy 生态兼容**：基于纯 Rust 实现，遵循 Bevy 的插件体系，天然支持 ECS、系统调度和资源管理。  

**典型接入方式**  
1. **在 `Cargo.toml` 中添加依赖**  
   ```toml
   [dependencies]
   bevy_trenchbroom = "0.3"
   bevy = "0.13"
   ```  
2. **在 Bevy 应用中注册插件**  
   ```rust
   use bevy::prelude::*;
   use bevy_trenchbroom::TrenchBroomPlugin;

   fn main() {
       App::new()
           .add_plugins(DefaultPlugins)
           .add_plugin(TrenchBroomPlugin)   // 注册 TrenchBroom 插件
           .add_startup_system(load_map.system())
           .run();
   }

   fn load_map(
       mut commands: Commands,
       asset_server: Res<AssetServer>,
       mut loader: ResMut<TrenchBroomMapLoader>,
   ) {
       // 加载 .map 或 .bsp 文件
       let map_handle = asset_server.load("maps/level1.map");
       loader.spawn_map(&mut commands, map_handle);
   }
   ```  
3. **可选的自定义**：通过插件提供的 `TrenchBroomMapLoader`，可以自定义材质、碰撞体或实体标签的映射规则，以适配项目特有的渲染或物理系统。  

**生产可用性评估**  
- **成熟度**：已有 143 ⭐、19 🍴，最近一次提交在 2026‑06‑30，表明项目仍在活跃维护。  
- **适用场景**：非常适合原型开发、内部工具或中小型游戏项目的关卡快速迭代；对于大型商业项目，需要进一步评估其 BSP 处理性能、内存占用以及与自研渲染管线的兼容性。  
- **风险**：目前缺少明确的长期维护者信息和安全审计报告，建议在正式上线前：  
  1. **审查许可证**（默认 MIT/Apache），确保符合公司合规。  
  2. **进行安全扫描**（如 `cargo audit`），确认无已知漏洞。  
  3. **编写回退方案**，如保留自行实现的简易解析或使用外部工具预处理关卡。  

综合来看，`bevy_trenchbroom` 在功能完整性和易用性上已足以支撑原型与内部工作流，经过适当的安全与性能验证后，也可以在生产环境中使用。

## 🧭 Practical evaluation

**Value:** Noxmore/bevy_trenchbroom may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 143 GitHub stars
- 19 forks
- updated 2026-06-30
- primary language: Rust
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 33/100 |
| stars | 46/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 42/100 |
| production | 68/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/Noxmore/bevy_trenchbroom) · [← Back to Games--graphics](./README.md)</sub>
