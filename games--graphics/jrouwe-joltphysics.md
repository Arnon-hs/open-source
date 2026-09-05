# jrouwe/JoltPhysics

[![Stars](https://img.shields.io/github/stars/jrouwe/JoltPhysics?style=flat-square&color=yellow)](https://github.com/jrouwe/JoltPhysics/stargazers) [![Forks](https://img.shields.io/github/forks/jrouwe/JoltPhysics?style=flat-square&color=blue)](https://github.com/jrouwe/JoltPhysics/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> A multi core friendly rigid body physics and collision detection library. Written in C++. Suitable for games and VR applications. Used by Horizon Forbidden West and Death Stranding 2.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 10.8k |
| 🍴 **Forks** | 899 |
| 💻 **Language** | C++ |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`c-plus-plus` `cpp` `game-development` `game-engine` `physics` `physics-engine` `physics-simulation` `simulation` `vr`

## 🎯 Categories

Games & Graphics

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
JoltPhysics is a high‑performance, multi‑core‑friendly rigid‑body physics and collision‑detection library written in modern C++. It powers demanding titles such as *Horizon Forbidden West* and *Death Stranding 2*, making it a proven choice for games and VR applications that need real‑time physical simulation. With over 10 k stars, frequent updates, and strong community activity, it is ready for serious production use.  

**Value**  
JoltPhysics off‑loads the heavy lifting of physics simulation to a battle‑tested engine, letting developers focus on building gameplay and user‑facing features rather than writing custom collision code. Its deterministic, multi‑threaded design scales across CPU cores, delivering smooth, realistic motion in both console and VR environments while reducing the need for bespoke physics solutions.  

**Practical Adoption Path**  

1. **Proof‑of‑Concept** – Clone the repo, follow the README to build the library, and run the supplied demo to verify that the build pipeline works on your target platform.  
2. **Integration Scaffold** – Wrap Jolt’s API in a thin abstraction layer that matches your existing game‑engine or VR framework (e.g., Unity, Unreal, or a custom engine). Start with a single subsystem (e.g., character controller) to evaluate API ergonomics and performance.  
3. **Incremental Migration** – Replace legacy physics components piece‑by‑piece, using Jolt’s extensive test suite as reference for correctness. Leverage the provided example scenes and serialization utilities to accelerate asset conversion.  
4. **Performance Tuning** – Profile multi‑threaded stepping, adjust the thread pool size, and tune collision layers to meet your frame‑budget requirements.  

**Production Readiness**  
JoltPhysics scores high on production readiness: it has recent commits (last updated 2026‑07‑12), a large and active community (10 813 stars, 899 forks), and proven deployment in AAA titles. The codebase is C++‑native, well‑documented, and includes unit tests and example projects, indicating a mature release cycle. While the integration steps are not fully detailed in the metadata, the library’s clear build instructions and modular design make a small pilot feasible, after which a full rollout can be planned with confidence.

### Русский

**jrouwe/JoltPhysics** — это высокопроизводительная библиотека для расчёта жёсткой тел и детекции коллизий, написанная на C++ и оптимизированная под многопоточность; её уже используют в крупных проектах, таких как *Horizon Forbidden West* и *Death Stranding 2*. Для фронтенда она позволяет ускорить создание пользовательских интерфейсов, предоставляя готовые компоненты физики и коллизий, которые можно быстро интегрировать в игровые и VR‑приложения, начиная с небольшого proof‑of‑concept и проверки README. Проект обладает высокой готовностью к продакшн‑использованию: активная разработка, более 10 000 звёзд на GitHub, значительное количество форков и недавние обновления, однако перед масштабным внедрением стоит уточнить детали интеграции и оценить затраты на настройку.

### 中文

**项目简介（2‑3 句）**  
jrouwe/JoltPhysics 是一款面向多核的刚体物理与碰撞检测库，使用 C++ 编写，已在《Horizon Forbidden West》和《Death Stranding 2》等大型游戏中实战。它专为游戏和 VR 场景提供高性能、可扩展的物理模拟。

**价值**  
- **提升前端交互体验**：通过内置的物理行为（刚体、约束、碰撞）让 UI 元素具备真实的运动和反馈，减少手工实现动画和交互逻辑的工作量。  
- **加速 UI 开发**：可直接复用库提供的刚体与碰撞组件，快速构建交互式界面（如可拖拽的卡片、弹性按钮、VR 手势等），缩短产品 UI 上线周期。  
- **降低维护成本**：库已在商业大作中验证，社区活跃，bug 修复和功能迭代速度快，使用后可减少自研物理代码的技术债务。

**典型接入方式**  
1. **阅读 README 与示例**：先克隆仓库，运行 `examples/` 中的最小示例，确认编译环境（CMake + 支持的编译器）。  
2. **在项目中引入子模块**：将 JoltPhysics 作为 Git submodule 添加到代码库，或通过 CMake `FetchContent` 拉取。  
3. **创建物理系统实例**：在前端渲染层（如 Unity、Unreal、或者自研 WebGL 引擎）中初始化 `Jolt::PhysicsSystem`，并将 UI 元素对应的渲染对象绑定到 Jolt 的刚体。  
4. **实现更新循环**：在每帧渲染前调用 `physicsSystem->Step(deltaTime)`，随后把刚体的位置信息同步回 UI 元素的变换矩阵。  
5. **小范围验证**：先在一个独立的 UI 组件（如可拖拽的弹窗）做 PoC，确认碰撞、约束行为符合预期，再逐步推广到整个前端系统。

**生产可用性**  
- **活跃度**：截至 2026‑07‑12，项目仍在维护，最近一次提交在当日；GitHub 计有 10 813 星、899 Fork，社区讨论活跃。  
- **成熟度**：已在两款 AAA 级游戏中投入生产，证明其在高负载、多核环境下的稳定性与性能。  
- **风险**：文档侧重底层 API，前端接入路径不够明确；需要在评估阶段投入一定时间进行环境搭建和 PoC 验证。  
- **结论**：在技术准备充分的前提下，JoltPhysics 完全具备作为生产级 OSS 组件在游戏/VR 前端项目中使用的条件，推荐先做小规模概念验证，确认集成成本后再全面推广。

## 🧭 Practical evaluation

**Value:** jrouwe/JoltPhysics helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 10813 GitHub stars
- 899 forks
- updated 2026-07-12
- primary language: C++
- 9 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 74/100 |
| stars | 86/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 87/100 |
| recency | 80/100 |
| adoption | 82/100 |
| production | 72/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/jrouwe/JoltPhysics) · [← Back to Games--graphics](./README.md)</sub>
