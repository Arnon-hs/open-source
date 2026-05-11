# software-mansion/react-native-reanimated

[![Stars](https://img.shields.io/github/stars/software-mansion/react-native-reanimated?style=flat-square&color=yellow)](https://github.com/software-mansion/react-native-reanimated/stargazers) [![Forks](https://img.shields.io/github/forks/software-mansion/react-native-reanimated?style=flat-square&color=blue)](https://github.com/software-mansion/react-native-reanimated/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> React Native's Animated library reimplemented

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 10.8k |
| 🍴 **Forks** | 1.5k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`animation` `gesture` `javascript` `react-native`

## 🎯 Categories

Frontend · Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
software‑mansion/react‑native‑reanimated is a high‑performance rewrite of React Native’s built‑in Animated library, offering a declarative, JavaScript‑free animation engine that runs on the UI thread. With over 10 k stars, active maintenance and broad community adoption, it lets teams ship polished, fluid interfaces while writing far less custom UI code.  

**Value**  
- **Speed & smoothness:** By moving animation calculations off the JavaScript bridge, UI interactions stay buttery‑smooth even on low‑end devices.  
- **Productivity:** A rich, declarative API and a growing set of pre‑built hooks let developers compose complex gestures and transitions with minimal boilerplate.  
- **Ecosystem fit:** It integrates seamlessly with existing React Native projects and works alongside other popular libraries (e.g., React Navigation, Gesture Handler).  

**Practical Adoption Path**  
1. **Proof‑of‑concept:** Clone the repo, run the “Hello World” example, and verify animation performance on your target devices.  
2. **Read the README & docs:** Follow the installation guide (npm/yarn + pod install) and try the basic `useSharedValue` / `useAnimatedStyle` patterns in a sandbox screen.  
3. **Incremental migration:** Replace a few existing Animated components with Reanimated equivalents in a low‑risk feature module, monitoring bundle size and runtime metrics.  
4. **Full rollout:** Once the pilot proves stable, refactor the remaining animations, add type‑safe wrappers if needed, and lock the version in your monorepo.  

**Production Readiness**  
- **Activity & community:** Recent commits (as of 2026‑05‑11), >10 k stars, 1.4 k forks, and active issue triage signal a mature, well‑maintained project.  
- **Stability:** The library follows semantic versioning, provides TypeScript typings out of the box, and is used in many high‑profile React Native apps (e.g., Expo, Shopify).  
- **Risks:** No immediate licensing or security red flags, but a final review of the MIT license, vulnerability scanning of transitive dependencies, and confirmation of an active maintainer team are recommended before a production‑grade rollout.  

Overall, React‑Native‑Reanimated is a strong OSS candidate for teams looking to accelerate UI delivery with reliable, high‑performance animations.

### Русский

`software‑mansion/react-native-reanimated` – это переосмысленная реализация библиотеки Animated для React Native, позволяющая создавать анимированные пользовательские интерфейсы с минимумом кастомного кода и ускорять выпуск продукта. Рекомендуется начать с небольшого proof‑of‑concept, проверив README и базовую интеграцию, а затем масштабировать на остальные экраны, поскольку проект уже имеет высокую степень готовности к продакшн (активные коммиты, 10 k+ звёзд, широкое принятие в сообществе). Осталось лишь подтвердить лицензионные и security‑аспекты, но в целом он подходит для серьёзного пилотного внедрения в мобильных фронтенд‑проектах.

### 中文

**项目简介**  
software‑mansion/react‑native‑reanimated 是对 React Native 官方 Animated 库的全新实现，提供更高的性能和更丰富的动画 API，帮助开发者以更少的自定义 UI 工作快速交付用户界面。

**价值**  
- **提升开发效率**：声明式 API 与强大的钩子（hooks）让动画逻辑更简洁，复用组件更容易。  
- **性能优势**：底层使用原生 UI 线程执行动画，避免 JS 线程阻塞，确保流畅的交互体验。  
- **生态兼容**：与 React Native 生态中的导航、手势库（如 react‑navigation、react‑native‑gesture‑handler）无缝协作。

**典型接入方式**  
1. **安装**：`yarn add react-native-reanimated`（或 `npm i react-native-reanimated`），随后按照官方文档在 iOS/Android 项目中执行 `pod install` 或 Gradle 同步。  
2. **配置 Babel**：在项目根目录的 `babel.config.js` 中加入 `plugins: ['react-native-reanimated/plugin']`。  
3. **小范围验证**：在一个独立的屏幕或组件中实现一个简单的动画（如淡入淡出），确认编译、运行和动画效果正常。  
4. **逐步迁移**：在已有的 Animated 代码中逐步替换为 Reanimated API，利用 `useSharedValue`、`useAnimatedStyle` 等 Hook 进行状态驱动的动画。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑11，拥有 10 822 星、1 467 Fork，最近一次提交在当日，表明项目仍在积极维护。  
- **成熟生态**：已被多个大型商业应用采用，社区提供丰富的示例和插件。  
- **风险评估**：暂无重大许可证或安全隐患，但建议在正式上线前完成许可证合规审查和安全依赖扫描。  

综上，react‑native‑reanimated 在功能、性能和社区支持上均已达到了可在生产环境大规模使用的水平，适合作为移动前端动画的首选实现。

## 🧭 Practical evaluation

**Value:** software-mansion/react-native-reanimated helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 10822 GitHub stars
- 1467 forks
- updated 2026-05-11
- primary language: TypeScript
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 79/100 |
| stars | 86/100 |
| topics | 50/100 |
| outlook | 79/100 |
| quality | 85/100 |
| recency | 100/100 |
| adoption | 84/100 |
| production | 78/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/software-mansion/react-native-reanimated) · [← Back to Frontend](./README.md)</sub>
