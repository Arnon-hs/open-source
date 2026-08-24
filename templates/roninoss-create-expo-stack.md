# roninoss/create-expo-stack

[![Stars](https://img.shields.io/github/stars/roninoss/create-expo-stack?style=flat-square&color=yellow)](https://github.com/roninoss/create-expo-stack/stargazers) [![Forks](https://img.shields.io/github/forks/roninoss/create-expo-stack?style=flat-square&color=blue)](https://github.com/roninoss/create-expo-stack/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-75%2F100-brightgreen?style=flat-square)](#)

> CLI tool to initialize a React Native application with Expo. Provides options to include Typescript, file-based routing via Expo Router, configuration based routing via pure React Navigation, styling via Nativewind, Restyle, Unistyles, StyleSheets, or Tamagui, and/or backend as a service such as Firebase and Supabase.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.6k |
| 🍴 **Forks** | 115 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 75/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`boilerplate` `cli` `expo` `expo-cli` `expo-router` `expo-template` `firebase` `nativewind` `react-native` `react-native-template` `supabase` `tailwindcss`

## 🎯 Categories

Templates · Frontend · DevTools · Mobile

## 📝 Summary

### English

**Brief Summary**  
`roninoss/create-expo-stack` is a CLI that scaffolds a full‑featured React Native app with Expo, letting you pick TypeScript, routing (Expo Router or React Navigation), styling (Nativewind, Restyle, Unistyles, StyleSheets, Tamagui), and optional BaaS back‑ends like Firebase or Supabase. It streamlines the setup of modern mobile stacks—including AI‑ready components—so you can start building prototypes or production apps without wiring everything from scratch.  

**Value**  
- **Speed × Flexibility** – One command generates a ready‑to‑code project with the exact combination of language, navigation, UI library, and backend you need, cutting weeks of boiler‑plate work.  
- **AI‑first readiness** – By bundling a clean TypeScript base and easy hooks for services (e.g., Firebase Functions, Supabase Edge), the stack is primed for adding LLM‑driven features, RAG pipelines, or autonomous agents.  
- **Ecosystem alignment** – Uses officially supported Expo tooling and popular styling libraries, ensuring compatibility with the broader React Native community and third‑party plugins.  

**Practical Adoption Path**  
1. **Install** the CLI (`npm i -g roninoss/create-expo-stack`).  
2. **Run** `create-expo-stack my-app` and answer the interactive prompts to select TypeScript, routing, UI, and backend options.  
3. **Commit** the generated repository; it already contains scripts for linting, testing, and OTA updates via Expo.  
4. **Extend** – add AI SDKs (e.g., OpenAI, LangChain) or custom serverless functions; the generated project’s folder structure follows best‑practice conventions, making integration straightforward.  
5. **Deploy** – use Expo’s build services or eject to native code when you need deeper platform control.  

**Production Readiness**  
- **Activity & Adoption** – 2.5 k GitHub stars, 115 forks, last updated on 2026‑06‑23, and a healthy issue/PR flow indicate an actively maintained project.  
- **Maturity** – The CLI produces a production‑grade Expo app with TypeScript, OTA updates, and optional BaaS integration; all major components (Expo Router, React Navigation, Nativewind, Tamagui, Firebase, Supabase) are themselves production‑tested.  
- **Risk Profile** – No glaring licensing or security red flags; however, a final review of the project’s license (MIT‑style) and any third‑party SDK versions is advisable before a large‑scale rollout.  

Overall, `roninoss/create-expo-stack` offers a high‑trust, low‑friction way to spin up AI‑enabled mobile applications, making it a solid candidate for pilots and, with the usual due‑diligence, for full production deployments.

### Русский

**roninoss/create-expo-stack** — это CLI‑утилита, позволяющая за несколько команд создать полностью готовый к работе React‑Native проект на базе Expo с выбранными опциями: TypeScript, маршрутизация (Expo Router или React Navigation), стилизация (Nativewind, Restyle, Unistyles, StyleSheets, Tamagui) и интеграция бэкенда как сервиса (Firebase, Supabase). Типичный сценарий — разработчик быстро прототипирует AI‑фичи, RAG‑ или агентные воркфлоу, выбирая нужный стек без необходимости «собирать» его вручную; после генерации проект уже готов к дальнейшей кастомизации и масштабированию. По состоянию на июнь 2026 проект считается почти готовым к production: активные коммиты, более 2500 звёзд на GitHub, широкая экосистема зависимостей и поддержка TypeScript, однако окончательная проверка лицензии, безопасности и активности мейнтейнеров всё‑ещё требуется.

### 中文

**价值**  
`roninoss/create-expo-stack` 是一款面向 React Native/Expo 开发者的脚手架 CLI，能够在几秒钟内生成完整的移动端项目骨架，并可按需开启 Typescript、Expo Router（文件化路由）或纯 React Navigation（配置式路由），以及 Nativewind、Restyle、Unistyles、StyleSheets、Tamagui 等多种 UI 方案，还可以一键接入 Firebase、Supabase 等后端即服务。这样，开发者无需从零搭建基础设施，就能直接在已有的技术栈上快速加入 AI 功能原型（RAG、Agent 工作流等），大幅缩短实验和迭代周期。

**典型接入方式**  
1. **全局安装**：`npm i -g roninoss/create-expo-stack`（或 `pnpm add -g`）。  
2. **创建项目**：在终端运行 `create-expo-stack my-app`，随后通过交互式提示选择 Typescript、路由方案、样式库和后端服务。  
3. **定制化**：生成的项目是标准的 Expo 项目，所有依赖均写在 `package.json` 中，后续可自行 `npm install`、`expo start` 进行本地调试，或直接推送到 CI/CD 流程中。  
4. **AI 集成**：项目模板已经预置了常用的 AI SDK（如 OpenAI、LangChain）示例代码，只需在 `src/api` 或 `src/agents` 目录下编写业务逻辑，即可实现 RAG、工具调用等功能。

**生产可用性**  
- **活跃度**：截至 2026‑06‑23，仓库最近一次提交在当日，拥有 2 562 ★、115 fork，说明社区活跃且维护及时。  
- **技术成熟度**：基于官方 Expo、React Navigation、Nativewind 等成熟生态，使用的全部依赖均为长期维护的开源项目。  
- **安全与合规**：项目采用 MIT 许可证，无明显版权或安全漏洞报告；仍建议在生产环境做一次依赖审计（`npm audit`）并锁定版本。  
- **可扩展性**：生成的代码结构清晰，支持自定义脚本、插件以及 CI/CD（GitHub Actions、Expo EAS），可以平滑迁移到大规模团队协作。  

综合来看，`roninoss/create-expo-stack` 已具备 **高** 生产就绪度，适合作为 AI‑enhanced 移动端原型或正式项目的起点，只需在正式上线前进行常规的安全审计和性能压测即可。

## 🧭 Practical evaluation

**Value:** roninoss/create-expo-stack helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2562 GitHub stars
- 115 forks
- updated 2026-06-23
- primary language: TypeScript
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 52/100 |
| stars | 73/100 |
| topics | 100/100 |
| outlook | 69/100 |
| quality | 70/100 |
| recency | 40/100 |
| adoption | 67/100 |
| production | 63/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/roninoss/create-expo-stack) · [← Back to Templates](./README.md)</sub>
