# qiin2333/sunshine-control-panel

[![Stars](https://img.shields.io/github/stars/qiin2333/sunshine-control-panel?style=flat-square&color=yellow)](https://github.com/qiin2333/sunshine-control-panel/stargazers) [![Forks](https://img.shields.io/github/forks/qiin2333/sunshine-control-panel?style=flat-square&color=blue)](https://github.com/qiin2333/sunshine-control-panel/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-48%2F100-brightgreen?style=flat-square)](#)

> 🎮 Sunshine Foundation 大屏桌面管理器 | Tauri + Vue 3，游戏库管理、米塔AI助手、内存监控、Steam封面搜索、启动助手

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 424 |
| 🍴 **Forks** | 11 |
| 💻 **Language** | Rust |
| 📈 **Score** | 48/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-assistant` `desktop-app` `game-library` `game-streaming` `rust` `steam` `sunshine` `tauri` `vite` `vue3` `windows`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`qiin2333/sunshine-control-panel` is an open‑source desktop manager built with Tauri and Vue 3 for the Sunshine Foundation ecosystem. It bundles a game‑library UI, a Mitra AI assistant, memory monitoring, Steam‑cover search, and a launch helper, giving users a single pane‑of‑glass control surface for gaming and AI‑enhanced workflows. The project is written primarily in Rust, has attracted over 400 stars, and is actively maintained as of July 2026.

**Value**  
- **AI‑enabled UI** – The built‑in Mitra assistant demonstrates how to embed generative‑AI features (e.g., chat, recommendations) directly into a native desktop app without having to assemble a separate model stack.  
- **All‑in‑one gaming console** – Game catalog management, Steam metadata fetching, and real‑time memory monitoring are handled out‑of‑the‑box, saving developers the effort of stitching together disparate APIs.  
- **Cross‑platform native experience** – Leveraging Tauri gives a lightweight, secure binary that runs on Windows, macOS, and Linux while keeping the UI in modern Vue 3.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run `cargo tauri dev` (or the provided Dockerfile) to verify the baseline UI and AI assistant work on your target OS.  
2. **Feature Gating** – Replace the default Mitra endpoint with your own LLM or RAG service by editing the `src-tauri` Rust config and the Vue service layer.  
3. **Integration** – Export the relevant UI components (e.g., `GameList.vue`, `MemoryMonitor.vue`) into your own Tauri/Vue project, or use the existing binary as a side‑car service that your main application can invoke via IPC.  
4. **Testing & CI** – Add the repo’s GitHub Actions workflow to your CI pipeline to catch breaking changes in the Rust/Tauri toolchain early.

**Production Readiness**  
- **Maturity**: Medium. The codebase is actively maintained, has a reasonable star count, and includes core functionality, but documentation around custom AI integration and deployment pipelines is limited.  
- **Dependencies**: Primarily Rust/Tauri and Vue 3; both are stable, but you’ll need to lock versions and monitor upstream security advisories.  
- **Scalability**: Suitable for internal tools, prototypes, or a dedicated gaming workstation. For large‑scale SaaS or multi‑tenant environments, you’ll likely need to containerize the backend AI service and add authentication/authorization layers.  
- **Risk Mitigation**: Conduct a small PoC to validate the setup cost, confirm that the AI assistant can be swapped for your own model, and audit the native binaries for compliance before rolling out to production.

### Русский

**Sunshine Control Panel** — это открытый десктоп‑менеджер для больших экранов на базе Tauri + Vue 3, который объединяет библиотеку игр, AI‑ассистента (Mita), мониторинг памяти, поиск обложек Steam и помощник запуска. Его типичный сценарий — быстрое прототипирование AI‑функций (например, RAG‑агентов) в игровом окружении и интеграция в существующие пайплайны управления контентом; для начала достаточно собрать небольшое POC и проверить README. Готовность к продакшну — средняя: проект уже стабилен и активно поддерживается (Rust, 424★), но требует проверки зависимостей и настройки окружения перед масштабным внедрением.

### 中文

**项目简介（2‑3 句）**  
`qiin2333/sunshine-control-panel` 是基于 Tauri 与 Vue 3 的大屏桌面管理器，面向 Sunshine Foundation 生态，提供游戏库管理、米塔 AI 助手、内存监控、Steam 封面搜索以及一键启动等功能。  

**价值**  
- **AI 能力即插即用**：内置米塔 AI 助手，可在不自行搭建模型堆栈的情况下为桌面管理器增添自然语言交互与智能推荐。  
- **统一的游戏与系统视图**：通过 Tauri 的原生窗口和 Vue 3 的响应式 UI，集中管理本地游戏库、实时监控系统资源，提升玩家与管理员的使用体验。  
- **快速原型与 RAG/Agent 工作流**：项目结构清晰，便于在现有 UI 上快速集成检索增强生成（RAG）或智能代理，实现自定义的游戏推荐、自动化启动脚本等业务场景。  

**典型接入方式**  
1. **克隆仓库并安装依赖**  
   ```bash
   git clone https://github.com/qiin2333/sunshine-control-panel.git
   cd sunshine-control-panel
   npm install   # 前端依赖
   cargo build   # Rust/Tauri 编译
   ```  
2. **配置 AI 助手**  
   - 在 `src-tauri/.env`（或 `.env.local`）中填写米塔 AI 的 API Key 与 Endpoint。  
   - 如需自定义 Prompt，可编辑 `src/ai/prompt.ts`。  
3. **集成到现有系统**  
   - 通过 Tauri 的插件机制，将项目编译为独立的桌面可执行文件，或在已有 Tauri 项目中作为子模块引入。  
   - 前端组件（如 `GameLibrary.vue`、`MemoryMonitor.vue`）可以直接在其他 Vue 3 项目中复用，只需在 `vite.config.ts` 中添加路径别名。  
4. **验证**  
   - 运行 `npm run dev`（开发模式）或 `npm run build && npm run tauri dev`（生产模式）确认 UI 与 AI 对话功能正常。  

**生产可用性**  
- **成熟度**：已有 424 颗星、11 个 fork，最近一次提交在 2026‑07‑13，活跃度尚可。代码基于 Rust + Tauri，具备原生性能和安全性。  
- **适用场景**：非常适合作为内部工具或面向玩家的桌面管理原型；若要在大规模生产环境使用，需要进行以下检查：  
  1. **依赖审计**：确认所有 Rust crates 与 NPM 包的许可证与安全漏洞。  
  2. **CI/CD 流程**：为 Tauri 打包（Windows、macOS、Linux）配置自动化构建与签名。  
  3. **AI 成本评估**：米塔 AI 按调用计费，需预估对话频率并设置限流/缓存。  
- **风险**：项目文档主要集中在 README，缺少完整的插件化指南；因此在首次集成时可能需要花费一定时间梳理构建脚本与环境变量。建议先完成一个“小功能”验证（例如仅使用 Steam 封面搜索），确认构建链路后再扩展 AI 功能。  

总体而言，`sunshine-control-panel` 在功能完整度与 AI 集成便利性上表现突出，适合作为原型或内部业务的起点；在完成依赖安全审查和构建流程固化后，可逐步提升到生产级别使用。

## 🧭 Practical evaluation

**Value:** qiin2333/sunshine-control-panel helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 424 GitHub stars
- 11 forks
- updated 2026-07-13
- primary language: Rust
- 11 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 27/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 54/100 |
| quality | 62/100 |
| recency | 40/100 |
| adoption | 48/100 |
| production | 53/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/qiin2333/sunshine-control-panel) · [← Back to AI/ML](./README.md)</sub>
