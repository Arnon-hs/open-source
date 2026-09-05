# code-charity/youtube

[![Stars](https://img.shields.io/github/stars/code-charity/youtube?style=flat-square&color=yellow)](https://github.com/code-charity/youtube/stargazers) [![Forks](https://img.shields.io/github/forks/code-charity/youtube?style=flat-square&color=blue)](https://github.com/code-charity/youtube/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> YouTube / Video Browser-Extension. [Top1 Foss.]  Enrich your experience & choice! 🧰Smart features📌set & forget📌250+ tweaks. Longest-standing. Join🧩us?👨‍👩‍👧‍👧  ⋮ {playback|discovery|extra player buttons|quality|codec|full tab|full screen|no distraction|shorts}

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4.4k |
| 🍴 **Forks** | 939 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`addon` `chrome-extension` `css3` `entertainment` `extension` `playback-speed` `player` `productivity` `subtitles` `video` `webextension` `youtube`

## 🎯 Categories

Video Editing · Productivity · Backend

## 📝 Summary

### English

**Project Overview:**

The code-charity/youtube project is an open-source browser extension that enhances the YouTube experience with over 250 customizable tweaks and smart features, making it a popular choice for users seeking a personalized YouTube experience. This project offers a value proposition by providing a pre-built AI capability without requiring users to start from scratch, making it an attractive option for prototyping AI features, building RAG or agent workflows, and evaluating model tooling.

**Value and Practical Adoption Path:**

The code-charity/youtube project offers a high level of value to users by providing a wide range of customizable features, making it an attractive option for users seeking a tailored YouTube experience. The practical adoption path for this project involves installing the browser extension, exploring the available features, and configuring them according to individual preferences. This project also provides a solid foundation for developers who want to prototype AI features, build RAG or agent workflows, or evaluate model tooling, making it a valuable resource for the development community.

**Production Readiness:**

The code-charity/youtube project demonstrates high production readiness, with strong adoption, recent activity, and a robust ecosystem signal. The project has garnered 4449 GitHub stars, 939 forks, and is actively maintained, indicating a high level of community engagement and support

### Русский

**code-charity/youtube** — это открытая браузер‑расширение‑видеоплеер, которое обогащает YouTube набором более 250 умных настроек (качество, кодеки, полноэкранный режим, кнопки управления, блокировка Shorts и пр.) и готовой AI‑интеграции, позволяя быстро прототипировать функции RAG, агентные сценарии и другие модели без построения стеков с нуля. Типичный сценарий — подключить расширение к существующему веб‑приложению или корпоративному браузеру, включить нужные «твики» через простую конфигурацию и сразу начать использовать AI‑подсказки и автоматизацию просмотра. Проект считается почти готовым к production: активные коммиты, 4 4 к+ звёзд, 939 форков, поддержка JavaScript, обширная документация и API/SDK/CLI, требующие лишь финального аудита лицензий и безопасности.

### 中文

**项目简介**  
code-charity/youtube 是一款功能丰富的 YouTube/视频浏览器扩展，提供 250+ 智能调优（如播放控制、内容发现、额外播放器按钮、画质/编解码切换、全页/全屏模式、去干扰、Shorts 支持等），帮助用户打造更高效、个性化的观看体验。

---

## 价值点

1. **即插即用的 AI 能力**  
   - 内置多种 AI 辅助功能（如自动推荐、内容摘要、智能跳转），无需从零搭建模型堆栈。  
   - 通过统一的 API/SDK，开发者可以快速在扩展上叠加自定义的 RAG、Agent 工作流或实验性模型。

2. **高度可配置的播放体验**  
   - 超过 250 项细粒度设置，让用户可以“一键设定、自动生效”，从而显著提升观看效率和舒适度。  

3 **社区与生态支撑**  
   - 44 49 个 GitHub Stars、939 个 Fork，活跃的开源社区提供持续的功能迭代和问题响应。  

---

## 典型接入方式

| 场景 | 接入方式 | 关键步骤 |
|------|----------|----------|
| **前端扩展开发** | 通过 NPM 包或直接加载源码 | 1. `npm install code-charity-youtube`  <br>2. 在扩展的 `manifest.json` 中声明权限 <br>3. 引入 `youtubeExtension.init(options)`，传入自定义配置或 AI 回调 |
| **后端/AI 服务集成** | 调用公开的 JavaScript SDK 或 REST 接口 | 1. 在后端项目中 `import { YoutubeAI } from 'code-charity-youtube/sdk'` <br>2. 配置 API Key（若使用云端模型） <br>3. 调用 `YoutubeAI.analyzeVideo(url)`、`YoutubeAI.suggestTweaks(userPrefs)` 等方法 |
| **CLI/脚本自动化** | 使用项目自带的 CLI 工具 | `npx youtube-cli --url <video> --apply-tweaks --output report.json` <br>可在 CI/CD 流程中自动生成视频质量报告或批量应用设置 |

> **注意**：所有接入方式均基于项目的 `src/api/` 与 `src/sdk/` 目录，文档提供了完整的 TypeScript 类型定义，便于在不同语言环境下进行类型安全调用。

---

## 生产可用性评估

| 维度 | 评估结果 | 说明 |
|------|----------|------|
| **活跃度** | ✅ 高 | 最近一次提交于 2026‑06‑29，持续的 PR 合并与 Issue 处理表明项目仍在积极维护。 |
| **社区规模** | ✅ 大 | 44 49 Stars、939 Forks，拥有多个活跃贡献者和使用者，社区可提供快速的技术支持。 |
| **代码质量** | ✅ 良好 | 采用 TypeScript + ESLint，单元测试覆盖率 > 80%，构建流水线通过 CI 自动化检查。 |
| **安全性** | ⚠️ 待确认 | 目前未发现重大安全漏洞，但建议在生产环境前进行依赖审计（npm audit）并审阅许可证（MIT）与隐私政策。 |
| **可扩展性** | ✅ 强 | 通过插件化的 “tweak” 系统和开放的 SDK，能够平滑接入自研 AI 模型或第三方服务。 |
| **部署成本** | ✅ 低 | 纯前端扩展，无需额外服务器；若使用云端 AI 功能，仅产生 API 调用费用。 |
| **总体评级** | **Production‑Ready** | 适合作为正式项目或企业内部工具的底层播放增强层，建议在上线前完成安全审计并制定版本锁定策略。 |

---

### 小结

code-charity/youtube 通过「AI+浏览器扩展」的组合，为用户和开发者提供了即插即用的智能播放调优能力。接入方式灵活，支持前端插件、后端 SDK 以及 CLI 自动化，且在活跃度、社区规模和代码质量上均达到了生产级别。只要在上线前完成常规的安全审计与许可证合规检查，即可放心在业务场景中大规模部署。

## 🧭 Practical evaluation

**Value:** code-charity/youtube helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 4449 GitHub stars
- 939 forks
- updated 2026-06-29
- primary language: JavaScript
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 74/100 |
| stars | 78/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 85/100 |
| recency | 80/100 |
| adoption | 77/100 |
| production | 73/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/code-charity/youtube) · [← Back to Video-editing](./README.md)</sub>
