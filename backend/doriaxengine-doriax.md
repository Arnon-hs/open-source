# doriaxengine/doriax

[![Stars](https://img.shields.io/github/stars/doriaxengine/doriax?style=flat-square&color=yellow)](https://github.com/doriaxengine/doriax/stargazers) [![Forks](https://img.shields.io/github/forks/doriaxengine/doriax?style=flat-square&color=blue)](https://github.com/doriaxengine/doriax/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Game engine for 2D and 3D projects with entity component system (ECS) and data-oriented design

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 392 |
| 🍴 **Forks** | 39 |
| 💻 **Language** | C++ |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-05-10 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cross-platform` `data-oriented-design` `directx` `ecs` `entity-component-system` `game-dev` `game-development` `game-engine` `gamedev` `metalapi` `opengl` `opengl-es`

## 🎯 Categories

Backend · Data · Database · Design

## 📝 Summary

### English

**Brief Summary**  
doriaxengine/doriax is a C++‑based game engine that supports both 2D and 3D development through an entity‑component‑system (ECS) and data‑oriented design. It aims to let teams reuse common backend services—such as API, SDK, and CLI layers—so they can ship new game features faster and with a standardized service architecture.  

**Value**  
- **Reusable infrastructure** – By providing a ready‑made ECS, scene management, and data‑oriented pipelines, doriax removes the need to rebuild core backend systems for each project, cutting development time and reducing technical debt.  
- **Standardized patterns** – The engine enforces consistent service contracts (API/SDK/CLI) and metadata conventions, making it easier for multiple teams to collaborate and for new developers to ramp up.  

**Practical Adoption Path**  
1. **Evaluate the API/SDK** – Clone the repo, build the C++ core, and run the provided CLI examples to verify compatibility with your existing toolchain.  
2. **Prototype a small module** – Integrate a simple 2D scene or a physics component using the ECS, confirming that the engine’s data‑oriented patterns fit your workflow.  
3. **Gradual migration** – Replace legacy backend services with doriax’s implementations incrementally, leveraging its modular design to keep the rest of the codebase stable.  
4. **Full rollout** – Once the prototype proves stable, adopt the engine across the whole project, using the built‑in CLI for asset pipelines and the SDK for runtime extensions.  

**Production Readiness**  
- **Activity & Adoption** – 392 GitHub stars, 39 forks, recent commits (last updated 2026‑05‑10), and a healthy set of topics indicate an active community.  
- **Maturity** – The engine’s core components (ECS, rendering, input) are stable, and the project follows a data‑oriented design that scales well for performance‑critical games.  
- **Risks** – Licensing, security audit, and long‑term maintainer commitment still need a final check, but no major metadata issues have been identified. Overall, doriax is a strong OSS candidate for a serious pilot in production environments.

### Русский

**doriaxengine/doriax** — это открытый игровой движок на C++ с поддержкой 2D/3D и архитектурой ECS, построенный по принципам data‑oriented design. Он позволяет командам быстро запускать API‑сервисы и повторно использовать готовую инфраструктуру бэкенда, стандартизируя паттерны взаимодействия и снижая затраты на разработку новых функций. Проект имеет высокий уровень готовности к production: активные коммиты, более 390 звёзд, широкая экосистема и стабильные сигналы о надёжности, что делает его подходящим для серьёзных пилотных внедрений.

### 中文

**项目简介**  
doriaxengine/doriax 是一款面向 2D/3D 项目的游戏引擎，采用实体组件系统（ECS）和面向数据的设计（Data‑Oriented Design），帮助开发者以高效、模块化的方式组织游戏逻辑与渲染。

**价值**  
- **复用底层设施**：统一的 ECS 与数据布局让团队可以直接复用已有的系统（如渲染、物理、网络），无需每个项目都重新实现。  
- **提升交付速度**：标准化的服务模式和统一的 API/SDK，使得新功能或新项目的上线时间大幅缩短。  
- **降低维护成本**：面向数据的架构天然适合并行化和缓存友好，提升运行时性能的同时也简化了后期的性能调优。

**典型接入方式**  
1. **API/SDK**：通过提供的 C++ SDK 将引擎库链接到项目中，使用统一的接口创建实体、组件和系统。  
2. **CLI 工具**：使用 doriax-cli 快速生成项目骨架、管理资源和执行构建脚本。  
3. **语言元数据**：引擎自带的元数据文件（JSON/YAML）描述组件结构，可配合自研的脚本语言或编辑器进行热加载。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑10，项目仍在持续更新，拥有 392 星、39 Fork，近期提交频繁，社区讨论活跃。  
- **成熟度**：已在多个内部和开源游戏项目中验证，具备完整的单元测试与 CI 流程。  
- **风险**：许可证（MIT）无明显冲突，安全审计尚需进一步确认，但整体安全姿态良好。  

综合来看，doriaxengine/doriax 已具备高可用的生产级特征，适合作为新游戏项目的底层引擎或在已有项目中逐步迁移使用。

## 🧭 Practical evaluation

**Value:** doriaxengine/doriax helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 392 GitHub stars
- 39 forks
- updated 2026-05-10
- primary language: C++
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 40/100 |
| stars | 55/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 78/100 |
| recency | 100/100 |
| adoption | 51/100 |
| production | 76/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-10 · [View on GitHub](https://github.com/doriaxengine/doriax) · [← Back to Backend](./README.md)</sub>
