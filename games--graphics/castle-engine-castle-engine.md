# castle-engine/castle-engine

[![Stars](https://img.shields.io/github/stars/castle-engine/castle-engine?style=flat-square&color=yellow)](https://github.com/castle-engine/castle-engine/stargazers) [![Forks](https://img.shields.io/github/forks/castle-engine/castle-engine?style=flat-square&color=blue)](https://github.com/castle-engine/castle-engine/network) [![Language](https://img.shields.io/badge/lang-Pascal-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Cross-platform (desktop, mobile, console, web) 3D and 2D game engine. Powerful visual editor. Support for glTF, X3D, IFC and more. Fast clean code using modern Pascal. Free and open-source.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.2k |
| 🍴 **Forks** | 157 |
| 💻 **Language** | Pascal |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`2d-game-engine` `3d-game-engine` `castle-game-engine` `delphi` `delphi-game` `delphi-game-engine` `delphi-library` `delphi-source` `firemonkey` `fmx` `fpc` `freepascal`

## 🎯 Categories

Games & Graphics · DevTools

## 📝 Summary

### English

**Brief Summary**  
Castle Engine is a cross‑platform 2D/3D game engine written in modern Pascal, offering a powerful visual editor and native support for formats such as glTF, X3D, and IFC. It is free, open‑source, and actively maintained, making it a solid foundation for building games or interactive visualisations on desktop, mobile, console, and web.

**Value Proposition**  
- **Unified graphics pipeline** – One code base can target a wide range of devices, eliminating the need for separate engines or platform‑specific wrappers.  
- **Rapid prototyping** – The visual editor lets designers assemble scenes, attach scripts, and iterate without recompiling, cutting development cycles.  
- **Extensible data handling** – Built‑in support for industry‑standard 3D formats (glTF, X3D, IFC) simplifies asset pipelines and reduces custom import code.  
- **Modern, clean Pascal code** – The engine’s source is concise and well‑structured, which eases debugging, contributes to long‑term maintainability, and appeals to teams already using Pascal or Delphi.

**Practical Adoption Path**  
1. **Proof‑of‑concept (PoC)** – Clone the repository, follow the README to build the editor on a developer workstation, and import a small glTF model to verify rendering and scripting.  
2. **Integration shim** – Wrap the engine’s core API in a thin module that matches your existing game‑logic interface (e.g., expose `Initialize`, `Update`, `Render` functions).  
3. **Asset pipeline validation** – Test the import of your primary asset formats (e.g., IFC for architectural visualisation) and confirm that metadata and textures survive the conversion.  
4. **Iterative feature rollout** – Start with non‑critical subsystems (menus, UI, simple physics) and gradually replace legacy components, using the visual editor for level design.  
5. **Automated builds** – Add the engine’s build steps to your CI pipeline (it supports Windows, macOS, Linux, Android, iOS, and WebAssembly) to ensure consistent cross‑platform binaries.

**Production Readiness**  
- **Activity & community** – The project shows recent commits (last update 2026‑06‑29), 1,200+ GitHub stars, and 157 forks, indicating an engaged user base.  
- **Maturity** – Core features (rendering, editor, format import) are stable; the codebase follows modern Pascal conventions, which reduces technical debt.  
- **Ecosystem** – The repository includes extensive documentation, sample projects, and a set of topics covering graphics, physics, and tooling, facilitating onboarding.  
- **Risk mitigation** – The primary integration hurdle is the lack of a formal SDK or package manager; teams should allocate time for building the engine from source and for creating a small wrapper layer before full adoption.  

Overall, Castle Engine is a production‑ready OSS candidate for teams that need a versatile, cross‑platform graphics engine and are comfortable working with Pascal or willing to invest in a thin interop layer. A modest PoC followed by incremental integration will let you validate the setup cost while leveraging the engine’s strong visual editing and format support.

### Русский

Castle Engine — кроссплатформенный 2D/3D‑игровой движок с мощным визуальным редактором, поддерживающий форматы glTF, X3D, IFC и другие, написанный на современном Pascal и распространяемый бесплатно под открытой лицензией. Он позволяет командам быстро создавать и переносить игры на настольные ПК, мобильные устройства, консоли и веб, минимизируя необходимость в собственной инфраструктуре рендеринга и управления ресурсами. Благодаря недавней активности, сильным показателям сообщества (1202★, 157 форков, обновление 2026‑06‑29) и чистому коду, проект готов к использованию в production‑проектах после небольшого proof‑of‑concept и проверки README.

### 中文

Castle‑Engine 是一个跨平台的 3D/2D 游戏引擎，提供强大的可视化编辑器并支持 glTF、X3D、IFC 等格式，基于现代 Pascal 编写、免费开源。它的核心价值在于帮助团队以更少的自定义代码实现数据的持

## 🧭 Practical evaluation

**Value:** castle-engine/castle-engine helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1202 GitHub stars
- 157 forks
- updated 2026-06-29
- primary language: Pascal
- 20 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 55/100 |
| stars | 66/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 78/100 |
| recency | 80/100 |
| adoption | 63/100 |
| production | 69/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/castle-engine/castle-engine) · [← Back to Games--graphics](./README.md)</sub>
