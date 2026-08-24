# seungmanchoi/react-native-fsd-agent-template

[![Stars](https://img.shields.io/github/stars/seungmanchoi/react-native-fsd-agent-template?style=flat-square&color=yellow)](https://github.com/seungmanchoi/react-native-fsd-agent-template/stargazers) [![Forks](https://img.shields.io/github/forks/seungmanchoi/react-native-fsd-agent-template?style=flat-square&color=blue)](https://github.com/seungmanchoi/react-native-fsd-agent-template/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> React Native + Expo template with Feature-Sliced Design (FSD) architecture and AI Agent Harness for Claude Code

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 40 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-team` `ai-agent` `ai-driven-development` `claude-code` `claude-code-harness` `context-engineering` `expo` `feature-sliced-design` `fsd` `harness` `harness-engineering` `nativewind`

## 🎯 Categories

Templates · AI/ML · Frontend · Mobile · Design

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The **seungmanchoi/react-native-fsd-agent-template** is an open‑source starter kit that combines React Native + Expo with a Feature‑Sliced Design (FSD) architecture and a ready‑to‑use AI‑Agent harness for Claude Code. It lets developers prototype AI‑enhanced mobile features—such as Retrieval‑Augmented Generation (RAG) or autonomous agents—without building the underlying model stack from scratch. With a clean TypeScript codebase, sensible folder conventions, and exposed hooks for API/SDK/CLI integration, it serves as a rapid‑bootstrapping platform for AI‑first mobile products.

---

### Value Proposition
- **Speed to market:** All the plumbing for FSD‑structured state management, navigation, and Claude‑based agent interaction is pre‑wired, so teams can focus on domain logic instead of boiler‑plate.
- **Consistent architecture:** FSD enforces clear separation of concerns (features, slices, shared UI), which scales well as the app grows and makes onboarding new developers easier.
- **AI‑first extensibility:** The “Agent Harness” abstracts Claude’s prompt‑execution, session handling, and RAG pipelines, enabling quick experiments with different prompts, tools, or data sources.
- **Cross‑platform reach:** Built on Expo, the template runs on iOS, Android, and the web with a single codebase, expanding the potential user base without extra effort.

### Practical Adoption Path
1. **Clone & install** – `npx expo-cli init my-app --template seungmanchoi/react-native-fsd-agent-template` (or manual clone). Run `yarn install` to fetch dependencies.  
2. **Configure AI credentials** – Add your Claude API key to `.env` (or the Expo secrets manager) as instructed in the README.  
3. **Explore feature modules** – The repo ships with sample feature folders (`/src/entities/chat`, `/src/features/rag`) that demonstrate how to call the agent harness and update UI via FSD slices.  
4. **Replace sample logic** – Swap the demo prompts and data sources with your own business use‑cases (e.g., product recommendation, document search).  
5. **Iterate & test** – Use Expo’s live‑reload on a simulator or device; run unit tests (`yarn test`) and optionally add end‑to‑end tests with Detox.  
6. **Production hardening** – Pin dependency versions, add linting/security scans, and configure CI/CD pipelines (Expo EAS) before publishing to the App Store/Play Store.

### Production Readiness
- **Maturity:** Medium. The template is functional for prototypes and internal tools, but it still requires a thorough dependency audit, security review, and possibly custom error‑handling before public release.  
- **Community signals:** 40 GitHub stars, 8 forks, recent update (2026‑07‑05), and TypeScript as the primary language indicate active maintenance, though the maintainer pool is small.  
- **Risks to address:** Verify the license compatibility with your product, run a security scan on third‑party packages, and ensure you have a plan for long‑term maintenance (e.g., lock versions, monitor Expo SDK upgrades).  

Overall, the template offers a solid foundation for quickly building AI‑enhanced React Native apps, provided you perform the usual production hardening steps.

### Русский

Резюме:

Проект seungmanchoi/react-native-fsd-agent-template представляет собой готовый шаблон для создания приложений на основе React Native и Expo с применением архитектуры Feature-Sliced Design (FSD) и интеграции с AI-агентом Claude Code. Этот шаблон позволяет разработчикам быстро добавить функциональность AI без необходимости начинать с нуля, что делает его идеальным решением для прототипирования и внутренних рабочих процессов. Проект находится на среднем уровне готовности к production, что обусловлено необходимостью проверки зависимостей и поддержки перед выпуском.

### 中文

**项目简介**  
`seungmanchoi/react-native-fsd-agent-template` 是一个基于 React Native + Expo 的项目模板，采用 Feature‑Sliced Design（FSD）架构，并内置了 Claude Code AI Agent 的调用封装，帮助开发者在移动端快速加入 AI 能力。

**价值**  
- **即插即用的 AI 能力**：无需从零搭建模型堆栈，模板已经配置好 Claude Code 的 API/SDK，省去繁琐的集成工作。  
- **结构清晰、可扩展**：使用 FSD 组织代码，业务、UI、公共层分离，便于后期功能迭代和团队协作。  
- **原型与评估友好**：适合快速原型、RAG（检索增强生成）或 Agent 工作流的实验与模型工具评估。

**典型接入方式**  
1. **克隆模板**：`npx degit seungmanchoi/react-native-fsd-agent-template my-app`  
2. **安装依赖**：`yarn install`（或 `npm i`）  
3. **配置 Claude Code**：在 `.env` 中填写 `CLAUDE_API_KEY`，或在 `src/shared/api/claude.ts` 中替换对应的 SDK 初始化代码。  
4. **运行调试**：`expo start`，在 iOS/Android 模拟器或真机上直接预览已集成的 AI 功能。  
5. **业务扩展**：按照 FSD 约定在 `src/entities/*`、`src/features/*`、`src/pages/*` 中添加新模块，调用封装好的 `aiAgent` 服务即可。

**生产可用性**  
- **成熟度**：模板已在 GitHub 获得 40+ stars、8 forks，最近一次更新为 2026‑07‑05，代码基于 TypeScript，结构清晰。  
- **适用场景**：非常适合作为内部原型、概念验证或限流的 AI 功能入口；若要直接上线，需要自行完成以下检查：  
  - **依赖安全**：审计第三方库的安全漏洞和许可证兼容性。  
  - **错误与异常处理**：在生产环境中加入更完善的超时、重试及日志上报。  
  - **性能与体积**：根据目标设备进行 Expo 打包体积优化（如使用 EAS Build、按需加载）。  
- **结论**：在经过依赖审查和异常处理的补充后，模板可用于生产环境；若对安全合规要求极高，建议在内部 CI/CD 中做进一步的代码审计和监控。

## 🧭 Practical evaluation

**Value:** seungmanchoi/react-native-fsd-agent-template helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 40 GitHub stars
- 8 forks
- updated 2026-07-05
- primary language: TypeScript
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 34/100 |
| topics | 100/100 |
| outlook | 57/100 |
| quality | 54/100 |
| recency | 40/100 |
| adoption | 31/100 |
| production | 55/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/seungmanchoi/react-native-fsd-agent-template) · [← Back to Templates](./README.md)</sub>
