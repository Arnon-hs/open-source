# michaelwilhelmsen/humla

[![Stars](https://img.shields.io/github/stars/michaelwilhelmsen/humla?style=flat-square&color=yellow)](https://github.com/michaelwilhelmsen/humla/stargazers) [![Forks](https://img.shields.io/github/forks/michaelwilhelmsen/humla?style=flat-square&color=blue)](https://github.com/michaelwilhelmsen/humla/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-40%2F100-brightgreen?style=flat-square)](#)

> Personal macOS meeting transcription — OpenAI / Speechmatics / on-device Whisper, per-note summary presets, Tauri 2 + Rust + Swift

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 106 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | Rust |
| 📈 **Score** | 40/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Video Editing · Templates

## 📝 Summary

### English

Here's a brief summary of the open-source project:

**Project Name: Humla**

Humla is an open-source, personal macOS meeting transcription tool that utilizes AI capabilities from OpenAI, Speechmatics, and on-device Whisper. It offers per-note summary presets and is built with Tauri 2, Rust, and Swift. This project helps developers add AI capabilities to their applications without starting from scratch.

**Value:**

The value proposition of Humla lies in its ability to quickly add AI capabilities to applications, making it an ideal choice for prototyping AI features, building RAG (Reusable Assets and Gears) or agent workflows, and evaluating model tooling. By leveraging existing AI models, developers can focus on integrating and customizing the tool rather than building a model stack from the ground up.

**Adoption Path:**

To adopt Humla, developers will need to manually inspect the project and its dependencies before committing to its use. This is due to sparse integration signals in the discovered metadata. Before production, it is essential to perform dependency and maintenance checks to ensure a smooth integration process. The project's GitHub activity, with 106 stars and 5 forks, indicates a relatively active community, which can provide support and guidance during the adoption process.

**Production Readiness:**

### Русский

Резюме open-source проекта michaelwilhelmsen/humla:

Проект michaelwilhelmsen/humla представляет собой персонализированную macOS систему транскрипции встреч, которая использует технологии OpenAI, Speechmatics и Whisper. Он позволяет добавлять функциональность AI без создания новой модели. Проект удобен для прототипирования AI-приложений и оценки инструментов моделирования. 

Проект готов к внедрению в прототипах и внутренних рабочих процессах, но требует тщательного осмотра и проверки перед использованием в производстве.

### 中文

**项目简介**  
Humla（michaelwilhelmsen/humla）是一款基于 Tauri 2、Rust 与 Swift 的 macOS 本地会议转录工具，支持 OpenAI、Speechmatics 与离线 Whisper 多模型，提供按笔记自动生成摘要的预设。  

**价值**  
- **快速落地 AI 能力**：无需自行搭建模型堆栈，即可在 macOS 上实现高质量语音转文字和摘要，适合原型开发和内部工作流。  
- **多模型灵活选择**：可根据精度、成本或隐私需求在云端（OpenAI、Speechmatics）和本地（Whisper）之间切换。  
- **跨语言扩展**：基于 Rust 的核心逻辑易于在其他平台或后端服务中复用，配合 Tauri 可快速包装成桌面或 Web 应用。  

**典型接入方式**  
1. **本地部署**：克隆仓库 → `cargo build --release`（Rust）+ Xcode 编译 Swift UI → 生成的 `.app` 直接运行。  
2. **模型配置**：在 `config.toml` 中填写 OpenAI API Key、Speechmatics Token 或本地 Whisper 模型路径，选择默认的“会议摘要”预设。  
3. **业务集成**：通过 Tauri 提供的 JavaScript API（`invoke('transcribe', {filePath})`）在现有 Electron/React 前端中调用转录与摘要功能，或直接使用 Rust 库 `humla_core` 在后端服务中实现 RAG/Agent 工作流。  

**生产可用性**  
- **成熟度**：GitHub 106 星、5 个 fork，最近一次提交于 2026‑07‑09，代码以 Rust 为主，维护活跃度一般。  
- **适用场景**：非常适合原型验证、内部工具或低流量的生产环境；对高并发、严格 SLA 的大规模部署仍需额外的可靠性与监控包装。  
- **风险与注意事项**：项目文档和元数据的集成指引较少，实际接入前需手动验证模型调用、权限配置以及依赖（Rust、Swift、Tauri）兼容性；建议在受控环境中进行一次完整的端到端测试后再决定是否投入生产。  

总体而言，Humla 为希望在 macOS 上快速加入语音转录与自动摘要功能的团队提供了“即插即用”的解决方案，但在大规模或高可靠性需求下仍需进行额外的评估与加固。

## 🧭 Practical evaluation

**Value:** michaelwilhelmsen/humla helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 106 GitHub stars
- 5 forks
- updated 2026-07-09
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 43/100 |
| topics | 0/100 |
| outlook | 42/100 |
| quality | 41/100 |
| recency | 40/100 |
| adoption | 37/100 |
| production | 46/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-09 · [View on GitHub](https://github.com/michaelwilhelmsen/humla) · [← Back to Video-editing](./README.md)</sub>
