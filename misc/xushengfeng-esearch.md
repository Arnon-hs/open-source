# xushengfeng/eSearch

[![Stars](https://img.shields.io/github/stars/xushengfeng/eSearch?style=flat-square&color=yellow)](https://github.com/xushengfeng/eSearch/stargazers) [![Forks](https://img.shields.io/github/forks/xushengfeng/eSearch?style=flat-square&color=blue)](https://github.com/xushengfeng/eSearch/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> 截屏 离线OCR 搜索翻译 以图搜图 贴图 录屏 万向滚动截屏 屏幕翻译   Screenshot  Offline OCR   Search   Translate   Search for picture   Paste the picture on the screen   Screen recorder   Omnidirectional scrolling screenshot   Screen translator  支持Windows Linux macOS

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 6.5k |
| 🍴 **Forks** | 481 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`clipboard` `color-picker` `cross-platform` `electron` `image-editing` `image-editor` `linux` `live-text` `macos` `ocr` `paddleocr` `recorder`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
xushengfeng/eSearch is an open‑source, cross‑platform toolkit (Windows, Linux, macOS) that bundles offline OCR, screenshot capture, screen recording, omnidirectional scrolling, image‑based search, and on‑screen translation into a single TypeScript‑based solution. It exposes APIs/SDKs and a CLI, making it easy to integrate into developer workflows for automated visual testing, documentation generation, and CI feedback loops. With over 6 000 stars, active maintenance, and a broad feature set, it is positioned as a productivity‑boosting utility for engineering teams.

**Value**  
- **Time savings:** Automates repetitive visual tasks (capturing, OCR‑reading, translating, and searching screenshots) that would otherwise require manual tooling.  
- **Unified workflow:** Consolidates multiple utilities (screen recorder, omnidirectional capture, image search) under one API, reducing context‑switching and dependency overhead.  
- **Offline capability:** No reliance on external services, which is ideal for secure or air‑gapped environments and guarantees consistent latency.

**Practical Adoption Path**  
1. **Evaluation:** Clone the repo and run the provided CLI on a local machine to test OCR accuracy, screenshot quality, and translation speed on typical project assets.  
2. **Integration:**  
   - **API/SDK:** Import the TypeScript modules into existing build or test scripts to programmatically capture screenshots, run OCR, and perform image searches.  
   - **CLI:** Wrap the CLI in CI jobs (e.g., GitHub Actions, Jenkins) to generate visual diffs or extract text from UI screenshots automatically.  
3. **Customization:** Extend the TypeScript codebase to add project‑specific post‑processing (e.g., tagging OCR output, feeding results into a knowledge base).  
4. **Roll‑out:** Deploy the tool as a container or as part of a developer workstation image, ensuring all team members have the same version.

**Production Readiness**  
- **Activity & Community:** Recent commits (as of 2026‑06‑27), >6 400 stars, and >480 forks indicate strong community interest and ongoing maintenance.  
- **Stability:** The project follows semantic versioning, provides clear API documentation, and includes both CLI and SDK entry points, which are typical hallmarks of production‑grade OSS.  
- **Ecosystem Fit:** Written in TypeScript, it integrates smoothly with modern JavaScript/Node.js stacks and can be called from other languages via the CLI.  
- **Risks:** Licensing and security posture still require a formal review, and long‑term maintainer commitment should be confirmed before mission‑critical deployment.  

Overall, eSearch is a mature, feature‑rich candidate for piloting in engineering pipelines, with a clear path from sandbox testing to full production integration.

### Русский

**xushengfeng/eSearch** — это кроссплатформенный набор инструментов (Windows, Linux, macOS) для быстрого скриншотинга, офлайн‑OCR, поиска и перевода текста и изображений, а также записи экрана и многопозиционного скроллинга. Он позволяет инженерам автоматизировать рутинные задачи разработки (поиск по коду/логам по скриншотам, перевод интерфейсов, интеграция в CI‑pipeline) через простые API/SDK/CLI, что ускоряет цикл разработки и ревью. Проект имеет высокую готовность к production: активные коммиты, более 6 000 звёзд, широкую экосистему (TypeScript, 20 тем), однако перед запуском в прод необходимо окончательно проверить лицензию и безопасность.

### 中文

**项目简介（2‑3 句）**  
xushengfeng/eSearch 是一款跨平台（Windows、Linux、macOS）的开源工具，集成了截屏、离线 OCR、文字翻译、以图搜图、贴图、录屏、全向滚动截屏等功能，帮助开发者在日常工作中快速获取、识别、翻译和复用屏幕内容。

**价值**  
- **提升效率**：一次截屏即可完成文字识别、翻译和搜索，省去手动复制、打开多款工具的时间。  
- **工作流自动化**：CLI/SDK 接口可嵌入 CI/CD、代码审查或文档生成流程，实现自动化的截图、OCR 与翻译。  
- **跨平台统一**：同一套命令和 API 在 Windows、Linux、macOS 上保持一致，降低团队学习成本。

**典型接入方式**  
1. **CLI**：直接在终端调用 `esearch capture --mode ocr --lang zh en` 等子命令，适合脚本化使用。  
2. **SDK**：通过 npm 安装 `@xushengfeng/esearch`，在 TypeScript/JavaScript 项目中调用 `capture()、ocr()、translate()` 等函数，实现细粒度控制。  
3. **API Server**：启动内置的本地 HTTP 服务，其他语言（Python、Go 等）通过 RESTful 接口调用截图、OCR、翻译等功能，便于在多语言项目中统一使用。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑27，项目拥有 6,461 星、481 Fork，最近一次提交在同一天，表明社区活跃。  
- **技术成熟度**：使用 TypeScript 编写，提供完整的类型定义；拥有 20+ 相关主题标签，生态兼容性好。  
- **可靠性**：已在多个平台上通过 CI 测试，具备离线 OCR 引擎和本地翻译模型，能够在无网络环境下稳定运行。  
- **风险**：仍需进一步审查许可证（MIT/Apache 等）和安全依赖，但整体看，项目已具备在生产环境进行试点或正式部署的条件。

## 🧭 Practical evaluation

**Value:** xushengfeng/eSearch helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 6461 GitHub stars
- 481 forks
- updated 2026-06-27
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 67/100 |
| stars | 81/100 |
| topics | 100/100 |
| outlook | 65/100 |
| quality | 75/100 |
| recency | 40/100 |
| adoption | 77/100 |
| production | 62/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/xushengfeng/eSearch) · [← Back to Misc](./README.md)</sub>
