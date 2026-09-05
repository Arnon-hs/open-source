# google/filament

[![Stars](https://img.shields.io/github/stars/google/filament?style=flat-square&color=yellow)](https://github.com/google/filament/stargazers) [![Forks](https://img.shields.io/github/forks/google/filament?style=flat-square&color=blue)](https://github.com/google/filament/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> Filament is a real-time physically based rendering engine for Android, iOS, Windows, Linux, macOS, and WebGL2

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 20.1k |
| 🍴 **Forks** | 2.2k |
| 💻 **Language** | C++ |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`3d-graphics` `android` `gltf` `gltf-viewer` `graphics` `metal` `opengl` `opengl-es` `pbr` `real-time` `vulkan` `wasm`

## 🎯 Categories

Games & Graphics · Mobile

## 📝 Summary

### English

**Summary**  
Filament is Google’s open‑source, real‑time physically based rendering engine that runs on Android, iOS, Windows, Linux, macOS and WebGL2. With over 20 k stars, active commits, and a growing ecosystem, it is production‑ready for pilots that need high‑quality graphics across mobile and desktop platforms. A pragmatic entry point is to follow the README, spin up a minimal “hello‑triangle” proof‑of‑concept, and then evaluate the API against your specific rendering workflow.  

**Value**  
Filament delivers a unified, high‑performance graphics pipeline that abstracts platform differences, letting developers write once and ship to mobile, desktop and web. Its physically based shading, post‑processing, and material system provide visual fidelity comparable to commercial engines while remaining lightweight enough for embedded devices.  

**Practical adoption path**  
1. **Read the documentation** – clone the repo, run the “samples” build instructions, and verify the “Hello Triangle” example on your target platform.  
2. **Create a small proof‑of‑concept** that mirrors a core use case (e.g., loading a glTF model, applying a material, rendering to a UI surface).  
3. **Integrate incrementally** – replace existing rendering calls with Filament’s API, starting with isolated modules (e.g., skybox, post‑process).  
4. **Validate performance and compatibility** across the required OS versions and GPU families, using Filament’s profiling tools.  

**Production readiness**  
The project shows strong signals of maturity: frequent commits, recent releases (last update 2026‑05‑14), a large contributor base, and adoption in several Google products. Its C++ core, extensive test suite, and active issue triage make it suitable for a serious pilot. Remaining due‑diligence steps include confirming the Apache‑2.0 license compliance, reviewing any disclosed security advisories, and ensuring that the maintainers are responsive to your support needs. Once these checks are cleared, Filament can be considered production‑ready for high‑performance graphics workloads.

### Русский

Filament — это кроссплатформенный движок реального времени с физически‑корректным рендерингом, который легко встраивается в мобильные (Android, iOS) и десктопные (Windows, Linux, macOS) приложения, а также в WebGL2‑проекты. Для начала рекомендуется реализовать небольшой proof‑of‑concept, следуя инструкциям в README, чтобы убедиться, что API и требования к графическому стеку соответствуют вашему workflow. Проект считается готовым к production‑использованию: активные коммиты, более 20 000 звёзд, широкое принятие в индустрии и стабильный C++‑кодовая база.

### 中文

**项目简介**  
Filament 是 Google 开源的实时物理渲染引擎，支持 Android、iOS、Windows、Linux、macOS 以及 WebGL2，使用 C++ 实现高效的 PBR 渲染管线，适合在移动端和跨平台应用中提供真实感视觉效果。

**价值**  
- **跨平台统一**：一次编写渲染代码即可在移动端、桌面端和浏览器上运行，降低平台适配成本。  
- **高性能 PBR**：基于物理的光照模型和 GPU 优化，实现实时光线追踪级别的视觉质量，适合游戏、AR/VR、可视化等对画面质量有要求的场景。  
- **活跃生态**：超 2 万星、数千叉、定期更新，已有多个 Google 项目（如 SceneViewer、ARCore）以及社区项目在生产环境中使用，验证了其可靠性。

**典型接入方式**  
1. **阅读官方 README 与示例**，确认渲染管线与项目需求匹配。  
2. **通过 CMake/Gradle/Bazel 引入**：在 Android 项目中使用 `filament-android` AAR；在 iOS 使用 CocoaPods；在桌面/Web 使用源码或预编译库。  
3. **实现最小可运行示例**（如加载一个 glTF 模型并渲染），验证渲染、资源加载和平台兼容性。  
4. 在此基础上逐步集成自定义材质、后处理效果或与现有引擎（Unity、Unreal）进行桥接。

**生产可用性**  
- **成熟度高**：最近一次提交（2026‑05‑14）且活跃维护，拥有完整的 CI、单元测试和文档。  
- **社区与内部采用**：Google 多个内部产品已在生产环境使用，社区贡献者活跃，问题响应及时。  
- **风险**：需进一步审查许可证（Apache‑2.0）兼容性、第三方依赖的安全性以及长期维护计划，但整体已具备直接用于正式项目的条件。  

综上，Filament 具备高性能、跨平台和成熟社区等优势，是在移动端及跨平台应用中实现实时 PBR 渲染的可靠 OSS 选型。

## 🧭 Practical evaluation

**Value:** google/filament may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 20060 GitHub stars
- 2178 forks
- updated 2026-05-14
- primary language: C++
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 83/100 |
| stars | 92/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 90/100 |
| recency | 80/100 |
| adoption | 89/100 |
| production | 75/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/google/filament) · [← Back to Games--graphics](./README.md)</sub>
