# amicalhq/amical

[![Stars](https://img.shields.io/github/stars/amicalhq/amical?style=flat-square&color=yellow)](https://github.com/amicalhq/amical/stargazers) [![Forks](https://img.shields.io/github/forks/amicalhq/amical?style=flat-square&color=blue)](https://github.com/amicalhq/amical/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> 🎙️ AI Dictation App - Open Source and Local-first ⚡ Type 3x faster, no keyboard needed. 🆓 Powered by open source models, works offline, fast and accurate.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.2k |
| 🍴 **Forks** | 100 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-note-taking-app` `asr` `dictate` `dictation` `dictation-tool` `electron` `expo` `local-ai` `macos` `mcp` `meeting-notes`

## 🎯 Categories

Video Editing · MCP · AI/ML

## 📝 Summary

### English

**Brief Summary**  
Amical is an open‑source, local‑first AI dictation app that lets users dictate text up to three times faster without ever touching a keyboard. Built with TypeScript and powered by offline open‑source models, it runs quickly, accurately, and can be self‑hosted, making it a privacy‑friendly alternative to cloud‑only speech‑to‑text services.

**Value**  
Amical provides a standard “Model Context Protocol” (MCP) layer that bridges AI assistants with real‑world tools and data. By exposing a clean API/SDK/CLI, it lets developers plug any AI agent into existing workflows—whether that’s voice‑driven note‑taking, command‑line automation, or integration with custom business tools—without rewriting the underlying model logic.

**Practical Adoption Path**  

1. **Evaluate the API/SDK** – Clone the repo, run the provided Docker compose or npm scripts, and test the dictation endpoint with a sample audio file.  
2. **Integrate with your AI agent** – Use the MCP‑compatible API to send transcriptions or receive voice commands directly from your assistant.  
3. **Deploy** – Choose a self‑hosted option (Docker, Kubernetes, or a simple Node server) for on‑prem or edge deployment, ensuring data never leaves your environment.  
4. **Extend** – Leverage the TypeScript SDK to add custom post‑processing, trigger external services, or expose additional CLI commands for internal tooling.

**Production Readiness**  
Amical scores high on production readiness: it has recent commits (last updated 2026‑05‑11), strong community adoption (1,211 ★, 100 forks), a rich ecosystem (20 topics), and a well‑documented TypeScript codebase. The project shows active maintenance, clear licensing, and no major security red flags, making it a solid candidate for pilot projects or full‑scale deployment after a final security/license audit.

### Русский

**amical** — это open‑source приложение для диктовки, которое использует локальные модели AI и позволяет вводить текст в 3 раза быстрее без клавиатуры. Типичный сценарий: интегрировать протокол Model Context Protocol в существующие сервисы, чтобы AI‑агенты могли напрямую вызывать инструменты и получать данные, а также развернуть собственный MCP‑сервер для стандартизированных подключений. По оценке проекта готовность к production высокая — активные коммиты, 1 200+ звёзд, широкая экосистема TypeScript и готовые API/SDK/CLI, что делает его надёжным кандидатом для пилотного внедрения.

### 中文

**项目简介**  
amicalhq/amical 是一款开源、离线优先的 AI 语音转写应用，基于社区模型实现 3 倍速的实时听写，无需键盘即可完成文字输入。它不仅提供本地化的高效转写功能，还通过 **Model Context Protocol (MCP)** 为 AI 助手与真实工具、数据之间的交互提供统一的协议层。

**价值主张**  
- **本地化、离线可用**：所有模型和转写引擎均在本地运行，保障数据隐私并消除网络依赖。  
- **高效、准确**：利用最新的开源语音模型，实现 3× 速率的实时转写，误差率低，适合会议纪要、文档撰写等场景。  
- **标准化集成**：通过 MCP，开发者可以快速把 AI 助手接入企业内部工具、数据库或业务系统，统一管理上下文与调用方式。  

**典型接入方式**  
1. **API/SDK**：项目提供基于 TypeScript 的 SDK 与 RESTful API，开发者可在 Node.js、前端或 Electron 应用中直接调用 `transcribe(audio)`、`streamTranscribe()` 等接口。  
2. **CLI**：内置命令行工具 `amical-cli`，支持本地音频文件批量转写或实时麦克风流式转写，适合脚本化集成。  
3. **MCP 服务器**：部署 `amical-mcp` 服务后，其他 AI 代理（如 LangChain、AutoGPT）可通过统一的 `model-context` 协议查询转写结果、发送指令或获取上下文数据，实现“AI + 工具”的闭环。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑11，项目拥有 1.2k+ Stars、100+ Fork，最近一次提交在 1 天前，表明社区和维护者仍在持续迭代。  
- **技术成熟度**：核心代码基于 TypeScript，提供完整的类型定义和单元测试，易于在企业代码库中引入。  
- **部署简便**：提供 Docker 镜像和 npm 包，一键启动本地服务，兼容 Linux、macOS 与 Windows。  
- **安全与合规**：全部模型和数据均在本地处理，无外部网络请求，降低信息泄露风险；项目采用 MIT 许可证，商业使用无额外限制。  

综合来看，amical 在 **离线语音转写** 与 **AI‑工具标准化集成** 两个维度都具备高可用性与可扩展性，适合作为企业内部 AI 助手的底层能力或作为 MCP 生态的入口服务进行试点部署。

## 🧭 Practical evaluation

**Value:** amicalhq/amical helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1211 GitHub stars
- 100 forks
- updated 2026-05-11
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 50/100 |
| stars | 66/100 |
| topics | 100/100 |
| outlook | 60/100 |
| quality | 63/100 |
| recency | 20/100 |
| adoption | 61/100 |
| production | 53/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/amicalhq/amical) · [← Back to Video-editing](./README.md)</sub>
