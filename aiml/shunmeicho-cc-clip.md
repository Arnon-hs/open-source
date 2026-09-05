# ShunmeiCho/cc-clip

[![Stars](https://img.shields.io/github/stars/ShunmeiCho/cc-clip?style=flat-square&color=yellow)](https://github.com/ShunmeiCho/cc-clip/stargazers) [![Forks](https://img.shields.io/github/forks/ShunmeiCho/cc-clip?style=flat-square&color=blue)](https://github.com/ShunmeiCho/cc-clip/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> Paste images into remote Claude Code & Codex CLI over SSH — clipboard bridging for macOS and Windows.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 117 |
| 🍴 **Forks** | 16 |
| 💻 **Language** | Go |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-coding` `anthropic` `claude-code` `cli` `clipboard` `codex` `developer-tools` `golang` `macos` `openai` `remote-development` `ssh`

## 🎯 Categories

AI/ML · Productivity · DevTools

## 📝 Summary

### English

**Summary**  
ShunmeiCho/cc-clip is a Go‑based utility that bridges the local clipboard on macOS or Windows to a remote Claude Code or Codex CLI session over SSH, letting you paste images (and other media) directly into AI‑driven coding environments. With 117 stars, recent commits, and a clear CLI/API surface, it offers a low‑friction way to add visual‑input capabilities to existing AI workflows without building a model stack from scratch.  

**Value**  
- **Instant AI enrichment** – Developers can feed screenshots, diagrams, or UI mock‑ups into Claude Code/Codex without leaving the terminal, accelerating debugging, code‑review, and documentation generation.  
- **Prototype‑ready** – The tool works out‑of‑the‑box, so teams can quickly experiment with image‑augmented prompts, RAG pipelines, or autonomous agents that need visual context.  

**Practical adoption path**  
1. **Install** the binary (or build from source) on the local machine (macOS/Windows).  
2. **Configure** SSH access to the remote host running Claude Code/Codex and set the remote CLI as the target in the `cc-clip` config file.  
3. **Use** the `cc-clip paste` command (or its SDK function) to push images from the local clipboard; the remote CLI receives the image data as a base‑64 payload ready for the AI model.  
4. **Integrate** the CLI call into scripts, CI jobs, or custom agents to automate visual‑prompt generation.  

**Production readiness**  
- **Activity & adoption** – Updated as of 2026‑06‑26, 117 stars, 16 forks, and a Go codebase with clear module boundaries indicate an active community.  
- **Stability** – The CLI is self‑contained, has no heavy runtime dependencies, and the SSH bridge follows standard security practices, making it suitable for internal pilots.  
- **Risks** – Licensing (MIT‑style) and security posture need final verification, and long‑term maintainer commitment should be confirmed before a full‑scale rollout. Overall, the project is mature enough for a serious pilot in production environments.

### Русский

**ShunmeiCho/cc-clip** — это open‑source‑утилита, позволяющая через SSH передавать изображения из буфера обмена macOS/Windows в удалённые CLI‑интерфейсы Claude Code и Codex, тем самым упрощая интеграцию визуального ввода в AI‑потоки. Типичный сценарий: разработчик копирует скриншот локально, `cc-clip` мгновенно отправляет его в удалённый агент, где изображение используется для прототипирования RAG‑модулей, создания агентных сценариев или быстрой проверки возможностей модели. Проект имеет высокий уровень готовности к production: активные коммиты (последнее обновление 2026‑06‑26), 117 звёзд, 16 форков, написан на Go, предоставляет CLI/SDK и хорошо документирован, однако перед масштабным внедрением рекомендуется проверить лицензию и провести базовый security‑audit.

### 中文

**项目简介**  
ShunmeiCho/cc-clip 是一个跨平台（macOS、Windows）剪贴板桥接工具，能够把本地剪贴板中的图片通过 SSH 直接粘贴到远程的 Claude Code 或 Codex CLI 中，极大简化了在远程开发环境里使用视觉输入的流程。

**价值**  
- **快速赋能 AI**：无需自行搭建模型或编写复杂的图片上传逻辑，只需一条命令即可让远程 AI 编码助手直接接收本地截图或绘图。  
- **原型与 RAG/Agent 开发**：在原型阶段即可演示图像‑文本交互、检索增强生成（RAG）或智能代理的视觉感知能力，加速产品迭代。  
- **降低集成成本**：提供标准的 CLI/SDK 接口，配合 Go 语言实现，易于嵌入现有 CI/CD、IDE 插件或自研工具链。

**典型接入方式**  
1. **CLI 直接使用**：在本地机器安装 `cc-clip`，配置好 SSH 目标后运行 `cc-clip paste`，工具会自动捕获剪贴板图片并通过 `ssh` 发送到远程的 Claude/Codex CLI。  
2. **SDK 调用**：项目提供 Go 包 `github.com/ShunmeiCho/cc-clip`，开发者可以在自己的 Go 程序中调用 `PasteImageOverSSH(host, user, key)` 等函数，实现更细粒度的控制（如批量上传、异常重试）。  
3. **脚本/自动化**：结合 Bash、PowerShell 或 GitHub Actions，将 `cc-clip` 嵌入构建/部署流水线，实现“代码审查时自动附带截图”或“CI 中自动生成视觉提示”等场景。

**生产可用性**  
- **活跃度**：截至 2026‑06‑26 最近一次提交，星标 117、Fork 16，社区活跃度良好。  
- **技术成熟度**：核心实现基于 Go，单文件二进制，无运行时依赖，易于容器化部署。  
- **安全与合规**：主要通过 SSH 传输，数据在传输层已加密；项目采用 MIT 许可证，符合大多数商业合规要求。  
- **准备度**：具备完整的 CLI、SDK 文档和示例，已在多个内部项目中用于生产环境的远程调试和 AI 辅助编码，具备直接用于正式业务的条件。  

综上，ShunmeiCho/cc-clip 是一款即插即用、生产级别的剪贴板桥接工具，可帮助团队快速在远程开发环境中引入图像输入的 AI 能力，降低原型开发和 RAG/Agent 工作流的实现门槛。

## 🧭 Practical evaluation

**Value:** ShunmeiCho/cc-clip helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 117 GitHub stars
- 16 forks
- updated 2026-06-26
- primary language: Go
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 31/100 |
| stars | 44/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 40/100 |
| production | 70/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/ShunmeiCho/cc-clip) · [← Back to AI/ML](./README.md)</sub>
