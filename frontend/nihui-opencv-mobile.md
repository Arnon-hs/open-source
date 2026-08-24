# nihui/opencv-mobile

[![Stars](https://img.shields.io/github/stars/nihui/opencv-mobile?style=flat-square&color=yellow)](https://github.com/nihui/opencv-mobile/stargazers) [![Forks](https://img.shields.io/github/forks/nihui/opencv-mobile?style=flat-square&color=blue)](https://github.com/nihui/opencv-mobile/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> The minimal opencv for Android, iOS, ARM Linux, Windows, Linux, MacOS, HarmonyOS, WebAssembly, watchOS, tvOS, visionOS

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.3k |
| 🍴 **Forks** | 457 |
| 💻 **Language** | C++ |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-07-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `arm-linux` `harmonyos` `ios` `linux` `macos` `opencv` `tvos` `visionos` `watchos` `webassembly` `windows`

## 🎯 Categories

Frontend · Mobile

## 📝 Summary

### English

**Summary**  
nihui/opencv-mobile is a lightweight, cross‑platform build of OpenCV that runs on Android, iOS, ARM‑Linux, Windows, macOS, HarmonyOS, WebAssembly, watchOS, tvOS and visionOS. With 3.3 k stars and recent commits, it lets teams ship visual‑processing UI components without writing extensive native glue code, accelerating frontend delivery and UI reuse across devices.

**Value**  
- Provides a ready‑made, minimal OpenCV library for a wide range of consumer platforms, eliminating the need to compile and maintain separate native builds.  
- Enables UI teams to embed image‑analysis, computer‑vision, or AR features directly into user‑facing screens, reducing custom UI work and shortening time‑to‑market.  
- The single C++ codebase can be shared across mobile, desktop, embedded, and web‑assembly targets, fostering component reuse and consistent behavior.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, follow the README to build the library for the target platform (e.g., Android NDK or iOS Xcode). Verify a simple sample (e.g., camera capture + edge detection).  
2. **Integration scaffolding** – Wrap the generated binaries in your app’s build system (Gradle, CocoaPods, CMake, etc.) and expose a thin API layer that matches your UI framework (React Native, Flutter, SwiftUI, etc.).  
3. **Component migration** – Replace existing custom vision modules with the opencv‑mobile APIs, reusing the same UI widgets across platforms.  
4. **Pilot rollout** – Deploy the updated module to a subset of users to monitor performance, binary size, and stability before a full rollout.

**Production readiness**  
- **Activity & community**: Last commit on 2026‑07‑12, 3,313 stars, 457 forks, and active issue discussions indicate healthy maintenance.  
- **Platform coverage**: Pre‑built scripts for all major OSes reduce integration effort; the minimal footprint makes it suitable for performance‑sensitive devices.  
- **Risk mitigation**: The integration steps are not fully documented in the metadata, so a small PoC is essential to gauge setup complexity and any hidden dependencies. Once the PoC succeeds, the library’s stability and broad adoption make it a solid candidate for production use.

### Русский

nihui/opencv-mobile — это минимальная сборка OpenCV, поддерживающая Android, iOS, ARM‑Linux, Windows, macOS, HarmonyOS, WebAssembly и другие платформы, что позволяет быстро создавать пользовательские интерфейсы без написания собственного UI‑кода. Для внедрения рекомендуется начать с небольшого proof‑of‑concept, проверив README и собрав пример, после чего можно масштабировать решение в полномасштабный продукт. Проект считается готовым к production: активные коммиты, более 3000 звёзд, широкое принятие в сообществе и поддержка множества платформ.

### 中文

**项目简介（2‑3 句）**  
nihui/opencv-mobile 是一个极简版的 OpenCV 移植库，支持 Android、iOS、HarmonyOS、watchOS、tvOS、visionOS、WebAssembly 以及主流桌面平台（Linux、Windows、macOS、ARM Linux）。它提供跨平台的计算机视觉基础能力，让前端/移动团队在构建用户界面时无需自行实现底层图像处理，从而显著降低 UI 开发工作量。

**价值**  
- **快速交付 UI**：直接调用统一的 OpenCV 接口即可完成图像采集、滤波、特征检测等常见视觉任务，避免在每个平台上重复实现。  
- **组件复用**：同一套代码可在 Android、iOS、HarmonyOS、Web 等多端共享，提升团队的代码复用率和维护效率。  
- **降低前端门槛**：前端开发者只需了解少量 C++/JNI/Swift 接口，即可在现有 UI 框架（Flutter、React Native、原生）中嵌入视觉功能，减少对底层图像处理的依赖。

**典型接入方式**  
1. **阅读 README 并完成环境准备**：项目提供了 Android（Gradle + CMake）、iOS（CocoaPods/Swift Package Manager）以及 WebAssembly 的构建脚本。先在本地跑通示例工程，确认编译链路。  
2. **创建小型 PoC**：在目标平台（如 Android）新建一个最小的 App，使用 `opencv-mobile` 的 `Mat`、`Imgproc` 等 API 完成一次图像灰度化或人脸检测，验证库的加载和运行时行为。  
3. **封装为业务模块**：将 PoC 中的代码抽象为统一的跨平台接口（例如 `VisionEngine.init() / VisionEngine.process(frame)`），并在 UI 层通过平台通道（Flutter 的 MethodChannel、React Native 的 Native Module）调用。  
4. **持续集成**：将库的编译脚本加入 CI（GitHub Actions、GitLab CI），确保每次代码变更后自动构建所有目标平台的二进制。

**生产可用性**  
- **活跃度**：截至 2026‑07‑12，项目最近一次提交，拥有 3313 ⭐、457 🍴，说明社区活跃且维护及时。  
- **平台覆盖**：官方提供完整的跨平台构建脚本，已在 Android、iOS、HarmonyOS、WebAssembly 等多端验证，基本满足主流移动/前端产品需求。  
- **风险点**：元数据中未提供一键式的集成指南，实际接入时需要自行梳理 CMake/Gradle/SwiftPM 的配置；因此建议先在单一平台完成 PoC，评估集成成本后再推广。  
- **结论**：在确认 PoC 能稳定运行且构建链路可自动化后，nihui/opencv-mobile 完全具备在生产环境中使用的条件，适合作为视觉功能的底层库进行长期维护。

## 🧭 Practical evaluation

**Value:** nihui/opencv-mobile helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3313 GitHub stars
- 457 forks
- updated 2026-07-12
- primary language: C++
- 12 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 67/100 |
| stars | 75/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 88/100 |
| recency | 100/100 |
| adoption | 73/100 |
| production | 77/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/nihui/opencv-mobile) · [← Back to Frontend](./README.md)</sub>
