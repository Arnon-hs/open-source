# software-mansion/react-native-screens

[![Stars](https://img.shields.io/github/stars/software-mansion/react-native-screens?style=flat-square&color=yellow)](https://github.com/software-mansion/react-native-screens/stargazers) [![Forks](https://img.shields.io/github/forks/software-mansion/react-native-screens?style=flat-square&color=blue)](https://github.com/software-mansion/react-native-screens/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> Native navigation primitives for your React Native app.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.7k |
| 🍴 **Forks** | 646 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`react-native` `react-navigation` `typescript`

## 🎯 Categories

Frontend · Mobile

## 📝 Summary

### English

**Summary**  
software‑mansion/react‑native‑screens provides native navigation primitives that let React Native apps render screens with the performance and look‑and‑feel of true platform UI components. With over 3,600 stars, frequent releases, and broad community adoption, it’s a mature, production‑ready library that can cut the amount of custom UI code you need to write.  

**Value**  
By delegating screen transitions, gestures, and memory management to the underlying iOS/Android navigation stacks, the library delivers smoother animations, lower memory usage, and a more native user experience—all without having to build those primitives yourself. This speeds up UI development, reduces bugs, and lets teams reuse a single, well‑tested navigation layer across multiple projects.  

**Practical adoption path**  

1. **Initial assessment** – Review the repository’s README and migration guides; verify that the version you plan to use matches the React Native version of your app.  
2. **Prototype integration** – Add the package (`yarn add react-native-screens`) and enable the native modules (run `pod install` for iOS, rebuild Android). Wrap a few existing screens with `<Screen>`/`<ScreenStack>` to confirm correct rendering and navigation behavior.  
3. **Manual inspection** – Because metadata on integration patterns is sparse, run the app through your UI test suite and manually check edge cases (modal screens, deep linking, orientation changes).  
4. **Gradual rollout** – Replace legacy navigation components screen‑by‑screen, monitoring performance metrics (FPS, memory) and crash reports.  

**Production readiness**  
The project scores 63/100 but is considered “high” for an OSS candidate: it has recent activity (last commit May 2026), a large star/fork base, TypeScript typings, and is already used by many high‑profile React Native apps. While no critical licensing or security red flags appear, a final review of the license (MIT) and any open CVEs is advisable before a full production rollout. Once that check is done, the library is ready for a serious pilot and, with the incremental adoption steps above, can be safely promoted to production.

### Русский

**software-mansion/react-native-screens** — это набор нативных навигационных примитивов для React Native, позволяющий быстро собрать пользовательский интерфейс без написания собственного UI‑кода. Проект уже активно поддерживается (3659 звёзд, 646 форков, последние обновления — 2026‑05‑14), имеет широкое распространение в экосистеме и готов к использованию в продакшене после обычной проверки лицензии и безопасности. При внедрении достаточно выполнить ручную проверку интеграции, после чего можно сразу начать переиспользовать готовые экранные компоненты и ускорять доставку фронтенда.

### 中文

**项目简介（2‑3 句）**  
software‑mansion/react-native-screens 为 React Native 提供原生的页面切换与栈管理能力，让移动端 UI 能够像原生应用一样流畅且占用更少的 JavaScript 资源。它通过在原生层实现导航原语，显著降低了自定义 UI 的工作量，帮助团队更快交付用户可见的界面。

**价值**  
- **提升性能**：页面切换在原生层完成，减少 JS‑bridge 开销，滚动、手势等交互更顺滑。  
- **降低开发成本**：无需自行实现复杂的栈管理或动画，直接复用成熟的原生实现。  
- **加速交付**：配合 React Navigation 等上层库，可快速搭建完整的产品 UI，缩短迭代周期。

**典型接入方式**  
1. **安装**：`yarn add react-native-screens`（或 `npm i react-native-screens`）。  
2. **原生链接**（React Native 0.60+ 自动链接，若使用旧版需手动运行 `pod install`）。  
3. **在入口文件中启用**：  
   ```tsx
   import { enableScreens } from 'react-native-screens';
   enableScreens();   // 可选，但推荐开启以获得最佳性能
   ```  
4. **与导航库配合**：在 React Navigation 中使用 `createNativeStackNavigator` 或在自定义路由实现中直接使用 `<Screen>`、`<ScreenContainer>` 组件。  
5. **验证**：在真实设备或模拟器上跑一次完整的页面切换，确认原生动画生效后即可投入使用。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑14，项目仍在维护，最近一次提交在当日，拥有 3 659 颗星、646 次 fork，社区活跃。  
- **生态兼容**：已被 React Navigation、Expo 等主流生态广泛采用，具备成熟的集成案例。  
- **质量与风险**：代码基于 TypeScript，类型安全；许可证为 MIT，商业使用无障碍。唯一需要在正式投产前进行的检查是安全审计（依赖库的漏洞扫描）以及确认维护者的响应速度。整体来看，项目已具备 **高** 生产就绪度，适合作为正式产品的导航层实现。

## 🧭 Practical evaluation

**Value:** software-mansion/react-native-screens helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3659 GitHub stars
- 646 forks
- updated 2026-05-14
- primary language: TypeScript
- 3 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 70/100 |
| stars | 76/100 |
| topics | 38/100 |
| outlook | 48/100 |
| quality | 59/100 |
| recency | 20/100 |
| adoption | 74/100 |
| production | 50/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/software-mansion/react-native-screens) · [← Back to Frontend](./README.md)</sub>
