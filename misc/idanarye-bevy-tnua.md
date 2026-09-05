# idanarye/bevy-tnua

[![Stars](https://img.shields.io/github/stars/idanarye/bevy-tnua?style=flat-square&color=yellow)](https://github.com/idanarye/bevy-tnua/stargazers) [![Forks](https://img.shields.io/github/forks/idanarye/bevy-tnua?style=flat-square&color=blue)](https://github.com/idanarye/bevy-tnua/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> A floating character controller for Bevy

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 463 |
| 🍴 **Forks** | 54 |
| 💻 **Language** | Rust |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bevy-plugin` `character-controller` `locomotion` `rapier2d` `rapier3d` `rust` `xpbd`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Project Summary:**
idanarye/bevy-tnua is an open-source, floating character controller for Bevy, a game engine. This project offers a reusable backend infrastructure, allowing teams to accelerate API service development and standardize service patterns. With its high production readiness, strong adoption, and recent activity, teams can confidently pilot this solution in their projects.

**Value Proposition:**
The primary value of idanarye/bevy-tnua lies in its ability to help teams quickly reuse and standardize backend infrastructure, enabling faster API service development and deployment. This can lead to significant time and resource savings, as well as improved maintainability and scalability of services.

**Practical Adoption Path:**
To adopt idanarye/bevy-tnua, teams can follow these steps:

1. Evaluate the project's implementation signals, such as API/SDK/CLI, language metadata, and focused topics, to ensure it aligns with their needs.
2. Assess the project's production readiness, including its recent activity, adoption, and ecosystem signals.
3. Review the project's quality signals, including its GitHub stars, forks, and primary language (Rust).
4. Perform a final review of the project's license, security posture, and active maintainers to mitigate any potential risks

### Русский

Резюме проекта idanarye/bevy-tnua:

Проект idanarye/bevy-tnua - это открытое ПО, предназначенное для управления контроллером персонажа в геймдеве на основе Bevy. Он позволяет командам повторно использовать инфраструктуру сервисов, вместо того, чтобы снова и снова создавать общие компоненты backend. Проект готов к использованию в production, поскольку имеет сильные сигналы о продакшн-готовности, таких как активность, приём и сигналы экосистемы.

### 中文

**项目简介**  
`idanarye/bevy-tnua` 是为 Bevy 游戏引擎提供的 **浮空角色控制器**，实现了平滑的移动、跳跃、碰撞检测等基础功能，让开发者可以快速在 3D/2D 场景中加入可漂浮的角色行为，而无需从头编写物理和输入逻辑。

**价值**  
- **复用性强**：将通用的角色控制逻辑封装为插件，团队可以在多个 Bevy 项目中直接复用，省去重复实现的时间和调试成本。  
- **加速开发**：提供即插即用的 API/SDK，配合 Bevy 的 ECS 体系，开发者只需关注游戏业务逻辑即可快速交付。  
- **标准化**：统一的控制器实现帮助团队在不同项目间保持一致的运动行为和代码风格，降低维护难度。

**典型接入方式**  
1. **在 Cargo.toml 中添加依赖**  
   ```toml
   [dependencies]
   bevy = "0.13"
   bevy_tnua = { git = "https://github.com/idanarye/bevy-tnua", tag = "v0.5.0" }
   ```  
2. **在 Bevy 应用中注册插件**  
   ```rust
   use bevy::prelude::*;
   use bevy_tnua::TnuaPlugin;

   fn main() {
       App::new()
           .add_plugins(DefaultPlugins)
           .add_plugin(TnuaPlugin)   // <-- 注册浮空角色控制器
           .add_startup_system(setup)
           .run();
   }
   ```  
3. **为角色实体添加组件**（`TnuaControllerBundle`、`TnuaRigidBody` 等），并在系统中读取/写入控制输入即可实现移动、跳跃、漂浮等行为。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑30，项目最近有提交，拥有 463 颗星、54 个 Fork，社区讨论活跃。  
- **生态兼容**：基于 Rust 与 Bevy 主流版本实现，使用 Cargo 管理，易于与现有 Bevy 项目集成。  
- **质量保障**：代码库包含完整的示例和文档，且已在多个开源游戏项目中实战验证。  
- **风险提示**：仍需自行审查许可证（MIT/Apache 双许可证）和潜在的安全依赖；建议在正式生产环境前进行内部安全审计并关注后续维护者的活跃情况。  

综上，`bevy-tnua` 已具备在商业或大型开源游戏项目中直接使用的条件，能够显著提升角色控制相关功能的开发效率并保持实现的一致性。

## 🧭 Practical evaluation

**Value:** idanarye/bevy-tnua helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 463 GitHub stars
- 54 forks
- updated 2026-06-30
- primary language: Rust
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 57/100 |
| topics | 88/100 |
| outlook | 72/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 53/100 |
| production | 71/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/idanarye/bevy-tnua) · [← Back to Misc](./README.md)</sub>
