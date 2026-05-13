# software-mansion/react-native-gesture-handler

[![Stars](https://img.shields.io/github/stars/software-mansion/react-native-gesture-handler?style=flat-square&color=yellow)](https://github.com/software-mansion/react-native-gesture-handler/stargazers) [![Forks](https://img.shields.io/github/forks/software-mansion/react-native-gesture-handler?style=flat-square&color=blue)](https://github.com/software-mansion/react-native-gesture-handler/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> Declarative API exposing platform native touch and gesture system to React Native.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 6.7k |
| 🍴 **Forks** | 1.1k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`gesture` `javascript` `react-native`

## 🎯 Categories

Frontend · Backend · Database · Mobile

## 📝 Summary

### English

**Summary**  
software‑mansion/react‑native‑gesture‑handler provides a declarative, TypeScript‑based API that exposes the native touch‑and‑gesture subsystems of iOS and Android to React Native apps. With over 6 700 stars and active maintenance, it enables developers to build fluid, gesture‑rich UIs with far less custom native code. A small proof‑of‑concept integration (following the README) is enough to validate its fit before scaling to larger screens.

**Value**  
By abstracting platform‑specific gesture handling into a single, well‑documented library, the project dramatically reduces the amount of bespoke UI work required to implement swipes, pan, pinch, and tap interactions. Teams can reuse the same components across iOS and Android, speeding up UI delivery, improving consistency, and lowering the risk of bugs that stem from hand‑rolled gesture logic.

**Practical adoption path**  

1. **Proof of concept** – Add the package to a sandbox React Native project, follow the quick‑start guide, and implement a simple gesture (e.g., a swipe‑to‑delete list item).  
2. **Component migration** – Replace existing gesture implementations in a low‑risk screen with the library’s `PanGestureHandler`, `TapGestureHandler`, etc., validating behavior on both platforms.  
3. **Full rollout** – Extend the pattern to higher‑traffic screens, optionally wrapping the handlers in reusable UI components for the rest of the codebase.  
4. **CI/QA** – Include the library in automated tests (e.g., Detox) to catch regressions in gesture handling.

**Production readiness**  
The library scores high on production readiness: recent commits (as of 2026‑05‑13), strong community adoption, 6 724 stars, and 1 051 forks indicate a mature ecosystem. Its TypeScript codebase, clear documentation, and widespread use in popular React Native projects suggest stability, though a final check of the license, security audit, and maintainer activity is still advisable before a full‑scale deployment.

### Русский

**software-mansion/react-native-gesture-handler** — это декларативный API, который открывает нативные сенсорные и жестовые возможности платформы для React Native, позволяя быстро создавать интерактивные пользовательские интерфейсы без написания собственного UI‑кода. Типовой сценарий внедрения — запуск небольшого proof‑of‑concept, проверка README и последующее масштабирование в продукт, что облегчает повторное использование компонентов и ускоряет доставку фронтенда. Проект считается готовым к production: активные коммиты, более 6 тыс. звёзд, широкое принятие в экосистеме и высокая стабильность, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**简短介绍**  
software‑mansion/react-native-gesture-handler 是一个声明式 API，直接将 iOS/Android 原生的触摸与手势系统暴露给 React Native，帮助开发者在移动端快速实现流畅、可靠的交互。

**价值**  
- **降低 UI 开发成本**：提供即插即用的手势组件（如 PanGestureHandler、TapGestureHandler），无需自行实现复杂的原生手势逻辑。  
- **提升交互体验**：利用平台原生手势实现更高的响应速度和更低的卡顿，提升用户满意度。  
- **复用性强**：配合 React Native 的组件化思想，可在多个页面或项目中共享同一套手势实现，缩短产品上线时间。

**典型接入方式**  
1. **安装**：`yarn add react-native-gesture-handler`（或 `npm i`），并在 iOS/Android 原生项目中执行 `pod install`（iOS）或确保 Gradle 已同步（Android）。  
2. **初始化**：在入口文件（如 `index.js`）中调用 `import 'react-native-gesture-handler';`，并在根组件外层包裹 `GestureHandlerRootView`。  
3. **使用**：直接在 JSX 中使用提供的手势组件，例如：

   ```tsx
   import { TapGestureHandler } from 'react-native-gesture-handler';

   const MyButton = () => (
     <TapGestureHandler onActivated={() => console.log('tap')}>
       <View style={styles.button}><Text>点我</Text></View>
     </TapGestureHandler>
   );
   ```

4. **验证**：先在一个小的功能模块或 Demo 页面做 PoC，确认手势行为符合预期后再逐步推广到全局。

**生产可用性**  
- **成熟度高**：截至 2026‑05‑13，项目拥有 6.7k+ ⭐、1k+ 🍴，最近一次提交仅在数天前，活跃度和社区支持都非常强。  
- **生态兼容**：已被 React Native 官方推荐，并被多个大型商业项目（如 Expo、Shopify 等）在生产环境使用。  
- **风险可控**：暂无重大许可证或安全漏洞报告，仍需在正式上线前完成最终的许可证合规与安全审计。  

综上，react‑native‑gesture‑handler 具备高生产就绪度，适合作为移动端手势交互的首选库，在项目中通过小范围验证后即可全面推广。

## 🧭 Practical evaluation

**Value:** software-mansion/react-native-gesture-handler helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 6724 GitHub stars
- 1051 forks
- updated 2026-05-13
- primary language: TypeScript
- 3 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 76/100 |
| stars | 81/100 |
| topics | 38/100 |
| outlook | 80/100 |
| quality | 82/100 |
| recency | 100/100 |
| adoption | 80/100 |
| production | 79/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/software-mansion/react-native-gesture-handler) · [← Back to Frontend](./README.md)</sub>
