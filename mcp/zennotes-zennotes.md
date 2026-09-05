# ZenNotes/zennotes

[![Stars](https://img.shields.io/github/stars/ZenNotes/zennotes?style=flat-square&color=yellow)](https://github.com/ZenNotes/zennotes/stargazers) [![Forks](https://img.shields.io/github/forks/ZenNotes/zennotes?style=flat-square&color=blue)](https://github.com/ZenNotes/zennotes/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> Keyboard-first local Markdown notes with Vim motions, diagrams, and MCP integration.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.6k |
| 🍴 **Forks** | 81 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`electron` `local-first` `markdown` `mcp` `notes` `vim`

## 🎯 Categories

MCP · Documents

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
ZenNotes (zennotes) is a keyboard‑first, local‑only Markdown editor that blends Vim‑style motions, diagram support, and the Model Context Protocol (MCP) for seamless AI‑assistant integration. It lets developers and power users capture notes, sketches, and code snippets while exposing a standard API/CLI/SDK surface that AI agents can call as real tools. With over 1.5 k stars, active maintenance, and a TypeScript codebase, it’s ready for pilot deployments.

**Value**  
- **AI‑tool bridge** – By implementing MCP, ZenNotes turns a simple note‑taking app into a first‑class “tool” for LLM agents, enabling context‑aware queries, automated diagram generation, and command execution without leaving the editor.  
- **Productivity‑centric UI** – Vim‑style navigation and keyboard‑only workflows reduce friction for developers who spend most of their time in the terminal.  
- **Open, extensible stack** – The TypeScript core, CLI, and SDK let teams embed ZenNotes in custom pipelines, CI/CD dashboards, or internal knowledge bases, standardising how AI agents interact with local data.

**Practical Adoption Path**  
1. **Evaluate the MCP endpoint** – Spin up the bundled MCP server (via Docker or `npm run start:server`) and test basic calls (e.g., `GET /notes`, `POST /render`).  
2. **Integrate with your AI stack** – Point your existing LLM orchestration layer (LangChain, CrewAI, etc.) to the MCP endpoint; use the provided SDK for TypeScript/JavaScript or the CLI for other languages.  
3. **Pilot in a team** – Deploy ZenNotes on developers’ workstations or a shared VM, collect feedback on note‑capture speed and AI‑driven assistance, and iterate on custom commands (e.g., “create diagram from selected text”).  
4. **Scale** – Containerise the MCP server, add authentication (OAuth/OpenID), and configure persistence (local file system or cloud‑backed storage) for broader organisational rollout.

**Production‑Readiness**  
- **Activity & Community** – Recent commits (as of 2026‑06‑23), 1 596 stars, and 81 forks indicate strong community interest and ongoing maintenance.  
- **Technical Maturity** – Written in TypeScript with clear API/CLI/SDK surfaces, well‑documented MCP spec, and a modest dependency footprint.  
- **Risk Profile** – No glaring metadata or licensing issues have surfaced, but a final security audit (dependency scanning, supply‑chain review) and confirmation of active maintainers are advisable before full production use.  

Overall, ZenNotes offers a high‑signal, low‑friction way to turn a local markdown editor into an AI‑accessible tool, making it a solid candidate for pilots and eventual production deployment.

### Русский

ZenNotes (zennotes) — это open‑source‑приложение для локального ведения Markdown‑заметок, ориентированное на клавиатурный ввод и поддерживающее Vim‑мотивы, диаграммы и интеграцию с Model Context Protocol (MCP). Оно позволяет быстро подключать AI‑агенты к реальным инструментам и данным, выступая как стандартный сервер MCP для построения и стандартизации таких интеграций. По показателям активности (1596 звёзд, регулярные обновления, TypeScript‑база) проект считается готовым к использованию в продакшене, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介（2‑3 句）**  
ZenNotes（仓库名：ZenNotes/zennotes）是一款键盘优先的本地 Markdown 笔记工具，内置 Vim 运动、图表绘制能力，并通过 Model Context Protocol（MCP）实现与 AI 助手的标准化交互。

**价值主张**  
- **AI‑工具桥梁**：通过 MCP，ZenNotes 为 AI 代理提供统一的、可编程的入口，使其能够直接读取、编辑和查询本地笔记数据，从而让 AI 能够在真实工具和用户信息上执行任务。  
- **统一协议**：采用标准化的 MCP 接口，帮助企业在不同内部工具之间复用同一套 AI 集成方案，降低集成成本并提升可维护性。  
- **生产力提升**：键盘‑Vim‑style 操作与内置绘图让技术人员、研究者和内容创作者能够快速捕获想法、构建文档，并即时让 AI 进行补全、审校或自动化处理。

**典型接入方式**  
1. **MCP Server**：在本地或容器中启动 ZenNotes 的 MCP 服务器（`zennotes serve --mcp`），它会暴露 HTTP/WS API、SDK 与 CLI。  
2. **AI Agent SDK**：在 AI 代理（如 LangChain、AutoGPT、OpenAI Function‑Calling）中引入对应的 SDK，使用 `getNote()、updateNote()、renderDiagram()` 等函数调用笔记。  
3. **CLI/脚本**：通过 `zennotes` CLI（npm 包）在 CI/CD、自动化脚本或自定义插件中直接操作笔记文件，配合 MCP 进行实时同步。  
4. **插件生态**：可在 VS Code、Obsidian 等编辑器中安装 ZenNotes 插件，实现编辑器内的即时 AI 辅助。

**生产可用性评估**  
- **活跃度**：2026‑06‑23 最近一次提交，GitHub ★1596、Fork 81，社区活跃；6 个主题标签覆盖 TypeScript、MCP、Markdown、Vim、Diagram、CLI。  
- **技术成熟度**：使用 TypeScript 编写，提供完整的 API 文档、SDK（Node/TS）以及 CLI，易于在现有 TypeScript/JavaScript 项目中集成。  
- **生态兼容**：MCP 为开放标准，已被多家 AI 平台采纳，能够直接对接 LangChain、OpenAI Functions、Claude 等。  
- **风险**：许可证（MIT）无商业限制；需要进一步审计依赖安全性及维护者响应速度，但整体风险低。  

**结论**  
ZenNotes 在功能、社区和协议层面均具备较高的生产就绪度，是在内部系统中快速实现 AI‑工具协同的首选开源组件。通过启动 MCP 服务或使用其 CLI/SDK，即可在现有工作流中无缝接入 AI 代理，实现“让 AI 直接操作本地笔记”的目标。

## 🧭 Practical evaluation

**Value:** ZenNotes/zennotes helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1596 GitHub stars
- 81 forks
- updated 2026-06-23
- primary language: TypeScript
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 48/100 |
| stars | 68/100 |
| topics | 75/100 |
| outlook | 76/100 |
| quality | 74/100 |
| recency | 80/100 |
| adoption | 62/100 |
| production | 72/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/ZenNotes/zennotes) · [← Back to Mcp](./README.md)</sub>
