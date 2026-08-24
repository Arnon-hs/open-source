# iPlug2/iPlug2

[![Stars](https://img.shields.io/github/stars/iPlug2/iPlug2?style=flat-square&color=yellow)](https://github.com/iPlug2/iPlug2/stargazers) [![Forks](https://img.shields.io/github/forks/iPlug2/iPlug2?style=flat-square&color=blue)](https://github.com/iPlug2/iPlug2/network) [![Language](https://img.shields.io/badge/lang-C-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> C++ Audio Plug-in Framework for desktop, mobile, xr and web

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.3k |
| 🍴 **Forks** | 343 |
| 💻 **Language** | C |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`aax` `audio` `audiounit` `audioworklet` `auv3` `clap` `emscripten` `gui` `iplug2` `plugins` `skia` `swiftui`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
iPlug2 is a modern C++ framework for building audio plug‑ins that run on desktop, mobile, XR devices, and the web. It supplies a rich set of ready‑made UI components and cross‑platform abstractions, letting developers ship user‑facing interfaces with far less custom UI code. With strong community adoption (2.3 k ★, 343 forks) and active maintenance, it is a solid candidate for production‑grade projects.

**Value**  
- **Accelerated UI development** – pre‑built widgets, layout helpers, and theme support let audio engineers focus on DSP logic rather than hand‑crafting controls.  
- **Cross‑platform consistency** – a single code base compiles to VST3, AU, AAX, iOS, Android, WebAssembly, and XR runtimes, reducing duplication and QA effort.  
- **Reusable components** – plug‑ins can share custom skins, parameter mapping, and host‑integration code across products, improving maintainability.

**Practical adoption path**  
1. **Prototype**: Clone the repo, run the CMake build scripts, and create a minimal plug‑in using the provided “HelloWorld” example.  
2. **Integrate**: Replace the example UI with your own components, leveraging iPlug2’s `IControl` hierarchy and parameter automation APIs.  
3. **Test across targets**: Use the built‑in host wrappers (VST3, AU, AAX) and the WebAssembly demo to verify behavior on each platform.  
4. **CI/CD**: Add iPlug2 as a submodule or fetch via Conan/vcpkg, then automate builds for all target SDKs in your pipeline.  

**Production readiness**  
- **Activity & ecosystem**: Recent commits (as of 2026‑05‑14), a vibrant fork network, and extensive documentation indicate a healthy project.  
- **Stability**: The framework has been used in multiple commercial audio products, and its abstraction layer isolates platform quirks, making releases predictable.  
- **Risks to resolve**: Final due‑diligence on the permissive license (MIT), a security audit of third‑party dependencies, and confirmation of an active maintainer roster are recommended before a full‑scale rollout.  

Overall, iPlug2 offers a high‑productivity, cross‑platform UI stack that is mature enough for serious pilot deployments, provided the remaining compliance checks are cleared.

### Русский

iPlug2 — это кроссплатформенный C++‑фреймворк для создания аудио‑плагинов с пользовательским интерфейсом на десктопе, мобильных устройствах, XR и в вебе; он предоставляет готовые UI‑компоненты и сигналы реализации, что позволяет существенно сократить время разработки и переиспользовать элементы интерфейса. Типичный сценарий — быстрый вывод продукта на рынок: разработчики подключают iPlug2 к своему аудио‑движку, собирают UI из готовых виджетов и сразу получают готовый к публикации плагин. По уровню готовности проект считается production‑ready: активные коммиты, более 2300 звёзд на GitHub, широкое принятие в сообществе и стабильный набор функций, хотя лицензия и безопасность требуют финального аудита.

### 中文

**项目简介**  
iPlug2 是一个基于 C++ 的跨平台音频插件框架，支持桌面、移动、XR 以及 Web 环境。它提供了一套完整的 UI 抽象层，让开发者能够以最少的自定义工作快速构建用户界面，并在多个平台上保持一致的体验。

**价值点**  
- **加速 UI 开发**：内置丰富的界面组件（旋钮、滑块、波形显示等），可直接复用，显著缩短产品 UI 的交付周期。  
- **跨平台统一**：一次实现的界面代码可在 Windows、macOS、iOS、Android、AR/VR 以及 Web（via WebAssembly）上运行，降低维护成本。  
- **开源且活跃**：拥有 2300+ Stars、300+ Forks，最近一次提交在 2026‑05‑14，社区活跃度高，易于获取社区支持和插件示例。

**典型接入方式**  
1. **源码集成**：将 iPlug2 的源码克隆到项目中，使用 CMake（或自带的 IDE 项目文件）编译生成插件库。  
2. **插件模板**：项目提供多种插件模板（VST3、AU、AAX、RTAS、WebAssembly 等），直接拷贝模板并在 `MyPlugin.cpp` 中实现业务逻辑。  
3. **UI 定制**：通过继承 `IControl` 或使用自带的 `IGraphics` API，快速拖拽式搭建 UI，亦可在需要时嵌入自定义绘制代码。  
4. **构建脚本**：使用提供的 CLI（`make`, `gradle`, `xcodebuild`）一键生成对应平台的二进制包，便于 CI/CD 流水线自动化。

**生产可用性**  
- **成熟度**：项目已稳定多年，拥有完整的插件格式支持和跨平台测试，适合作为正式产品的音频插件核心。  
- **社区与维护**：活跃的贡献者和定期的更新表明项目维护良好，关键功能（如实时音频处理、UI 渲染）已有大量实战案例。  
- **安全与合规**：目前未发现重大许可证或安全漏洞风险，但在正式投产前仍建议进行一次许可证合规审查和安全审计。  

综上所述，iPlug2 具备高生产可用性，能够帮助音频软件团队快速交付一致且专业的用户界面，是构建跨平台音频插件的可靠选择。

## 🧭 Practical evaluation

**Value:** iPlug2/iPlug2 helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2308 GitHub stars
- 343 forks
- updated 2026-05-14
- primary language: C
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 63/100 |
| stars | 72/100 |
| topics | 100/100 |
| outlook | 56/100 |
| quality | 66/100 |
| recency | 20/100 |
| adoption | 69/100 |
| production | 52/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/iPlug2/iPlug2) · [← Back to Misc](./README.md)</sub>
