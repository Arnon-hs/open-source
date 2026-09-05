# scratchfoundation/scratch-desktop

[![Stars](https://img.shields.io/github/stars/scratchfoundation/scratch-desktop?style=flat-square&color=yellow)](https://github.com/scratchfoundation/scratch-desktop/stargazers) [![Forks](https://img.shields.io/github/forks/scratchfoundation/scratch-desktop?style=flat-square&color=blue)](https://github.com/scratchfoundation/scratch-desktop/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> Scratch 3.0 as a self-contained desktop application

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 410 |
| 🍴 **Forks** | 258 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`scratchfoundation/scratch-desktop` packages the Scratch 3.0 visual programming environment into a self‑contained desktop application, letting users run and extend Scratch without a browser. While primarily aimed at educators and hobbyists, the project’s JavaScript codebase can be repurposed to prototype AI‑enhanced blocks, RAG pipelines, or agent workflows directly on the desktop.  

**Value**  
- Provides a ready‑made, fully functional UI and runtime for Scratch, saving you the effort of building a custom front‑end from scratch.  
- Because the core is JavaScript, you can insert AI‑powered extensions (e.g., image‑recognition or language‑model blocks) and test them locally before shipping.  
- The open‑source nature and modest star/fork count (≈410 ★ / 258 forks) give you a visible community and a baseline of stability for rapid experimentation.  

**Practical Adoption Path**  
1. **Clone & Install** – `git clone https://github.com/scratchfoundation/scratch-desktop.git` and run `npm install` (Node ≥ 14).  
2. **Run Locally** – `npm start` launches the desktop app; verify the vanilla Scratch UI works on your OS.  
3. **Add AI Extensions** – Create a new JavaScript block in the `src/extensions` folder that calls your AI service (REST, WebSocket, or local model). Register the block in `extensionManager.js`.  
4. **Test & Iterate** – Use the built‑in Scratch editor to drag the new block into scripts, observing model responses in real time.  
5. **Package for Distribution** – Run the provided Electron build script (`npm run build`) to produce platform‑specific binaries for internal rollout or beta testing.  

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last commit 2026‑05‑13) and runs on stable Electron/Node stacks, but documentation around extending the runtime with external AI services is sparse.  
- **Dependencies:** Relies on Electron, Node, and a handful of front‑end libraries; these should be audited for security and version compatibility before production use.  
- **Risk Mitigation:** Because integration signals are limited, perform a small‑scale proof‑of‑concept to validate the effort required to hook your AI model into the Scratch extension API. Once the extension works locally, you can lock down versions and add CI tests to ensure long‑term stability.  

In short, `scratch-desktop` offers a fast way to prototype AI‑augmented Scratch experiences, but you should verify the integration effort and perform dependency checks before committing it to a production pipeline.

### Русский

Scratch Desktop — это самостоятельное настольное приложение Scratch 3.0, упакованное в JavaScript‑пакет, которое позволяет быстро добавить возможности искусственного интеллекта (например, прототипировать RAG‑ или агентные сценарии) без необходимости строить стек моделей с нуля. Типичный путь внедрения — установить приложение, интегрировать нужные AI‑модули и протестировать их в локальном прототипе, после чего оценить затраты на настройку и поддержку перед переходом в продакшн. Готовность к production — средняя: проект подходит для внутренних прототипов и ограниченных рабочих процессов, но требует ручного аудита и проверки зависимостей из‑за неполной метаданных интеграции.

### 中文

**项目简介（2‑3 句）**  
scratchfoundation/scratch‑desktop 将 Scratch 3.0 打包为独立的桌面应用，免去浏览器依赖，开发者可在本地直接运行、扩展和分发 Scratch 项目。

**价值**  
- 为教育、创意编程和原型设计提供即装即用的环境，无需自行搭建 Web 服务器或处理浏览器兼容性。  
- 通过本地运行，能够方便地接入外部 AI 能力（如文本‑到‑代码、图像生成或 RAG/Agent 工作流），在不改动 Scratch 核心代码的前提下快速验证 AI 功能。  

**典型接入方式**  
1. **下载并安装**：从 GitHub Releases 获取对应平台的可执行文件（Windows / macOS / Linux），直接运行。  
2. **插件/扩展**：利用 Scratch 官方的扩展机制（`extensions` 文件夹）加载自定义 JavaScript 插件，插件中可以调用本地或云端的 AI API（例如 OpenAI、Claude、LangChain 等）。  
3. **本地服务桥接**：若需要更复杂的模型交互，可在本机启动一个轻量 HTTP/WS 服务（Node、Python 等），让 Scratch‑Desktop 通过 `fetch`/`WebSocket` 与之通信。  

**生产可用性**  
- **成熟度**：GitHub 410 星、258 Fork，活跃维护（截至 2026‑05‑13），代码基于成熟的 Electron + JavaScript 框架。  
- **适用场景**：非常适合内部原型、教学实验或小规模内部工具；在正式生产环境使用前，需要完成以下检查：  
  - **依赖审计**：确认 Electron 及第三方 npm 包的安全性与许可证兼容。  
  - **升级策略**：制定对 Scratch‑Desktop 版本升级的回滚与兼容性测试流程。  
  - **AI 接口稳健性**：对接的 AI 服务需实现超时、重试和错误日志，以免影响用户体验。  
- **风险**：项目的集成文档较少，集成路径主要靠代码阅读和手动实验；建议在评估阶段进行小范围的 PoC，确认集成成本后再决定是否投入生产。  

总体而言，scratch‑desktop 是一个 **中等** 级别的生产就绪度解决方案，适合作为 AI 功能原型和内部工作流的起点，前提是做好依赖审查和集成验证。

## 🧭 Practical evaluation

**Value:** scratchfoundation/scratch-desktop helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 410 GitHub stars
- 258 forks
- updated 2026-05-13
- primary language: JavaScript

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 60/100 |
| stars | 56/100 |
| topics | 0/100 |
| outlook | 61/100 |
| quality | 61/100 |
| recency | 80/100 |
| adoption | 57/100 |
| production | 62/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/scratchfoundation/scratch-desktop) · [← Back to Misc](./README.md)</sub>
