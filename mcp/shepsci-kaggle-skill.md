# shepsci/kaggle-skill

[![Stars](https://img.shields.io/github/stars/shepsci/kaggle-skill?style=flat-square&color=yellow)](https://github.com/shepsci/kaggle-skill/stargazers) [![Forks](https://img.shields.io/github/forks/shepsci/kaggle-skill?style=flat-square&color=blue)](https://github.com/shepsci/kaggle-skill/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-79%2F100-brightgreen?style=flat-square)](#)

> Complete Kaggle integration plugin/skill for AI coding agents — competition reports, dataset/model downloads, notebook execution, and badge collection. Works with Claude Code, Gemini CLI, Cursor, Codex, OpenClaw, and 35+ agents via skills.sh.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 70 |
| 🍴 **Forks** | 3 |
| 💻 **Language** | Python |
| 📈 **Score** | 79/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-skill` `ai-coding-agent` `claude-code` `claude-code-plugin` `claude-code-skill` `codex` `competitions` `cursor` `data-science` `gemini-cli` `hackathon` `kaggle`

## 🎯 Categories

MCP · AI/ML · Backend · DevTools · Data

## 📝 Summary

### English

Here's a brief summary of the open-source project:

**Project Summary:** shepsci/kaggle-skill is an open-source plugin that enables seamless integration of AI coding agents with Kaggle, a leading platform for machine learning competitions and data science. This plugin allows AI agents to access competition reports, datasets, models, and notebooks, making it easier for developers to utilize AI assistants in their workflow. By standardizing integrations through the Model Context Protocol (MCP), the project facilitates the connection of AI agents to real tools and data.

**Value Proposition:** The project's value lies in its ability to connect AI assistants to real tools and data, making it easier for developers to leverage AI in their workflow. This is achieved through a standard protocol, making it simple for developers to integrate AI agents with various tools and platforms.

**Practical Adoption Path:** To adopt this project, developers can start by integrating their AI agents with the Kaggle skill using the skills.sh protocol. The project's documentation and GitHub repository provide detailed information on how to evaluate and integrate the plugin with various AI agents.

**Production Readiness:** The project has a high production readiness score, indicating that it is suitable for serious piloting. The recent activity, adoption, and ecosystem signals are strong, and the primary language is

### Русский

**shepsci/kaggle-skill** — это полностью готовый плагин/skill для AI‑агентов, позволяющий им работать с Kaggle: получать отчёты о соревнованиях, скачивать наборы данных и модели, запускать ноутбуки и собирать бейджи. Он интегрируется через единый протокол с Claude Code, Gemini CLI, Cursor, Codex, OpenClaw и более чем 35 другими агентами (skills.sh), что упрощает подключение ассистентов к реальным инструментам и данным. Проект имеет высокий уровень готовности к production: активные коммиты (обновлён 2026‑07‑03), 70 звёзд, поддержка Python, широкая экосистема и положительные сигналы качества, требующие лишь финального аудита лицензий и безопасности.

### 中文

**项目简介**  
shepsci/kaggle‑skill 是一套完整的 Kaggle 集成插件/skill，能够让 AI 编码助手直接生成竞赛报告、下载数据集/模型、执行 Notebook 并收集徽章。它兼容 Claude Code、Gemini CLI、Cursor、Codex、OpenClaw 等主流模型，以及通过 skills.sh 接入的 35+ 代理。

**价值**  
- **标准化协议**：通过统一的 Model Context Protocol，把 AI 助手与真实的工具和数据桥接起来，降低了每个项目自行实现 Kaggle 接口的成本。  
- **即插即用**：只需在 AI 代理或工作流中加载该 skill，即可获得完整的 Kaggle 功能，提升研发效率和实验可重复性。  
- **生态兼容**：支持多种主流 LLM 与开发平台，帮助企业快速在现有 AI 助手体系中加入数据科学能力。

**典型接入方式**  
1. **CLI/SDK 调用**：在 Python 环境中 `pip install kaggle-skill`，使用提供的 SDK 方法（如 `download_dataset()、run_notebook()`）直接在代码中调用。  
2. **Skill 注册**：在使用 `skills.sh` 的 AI 代理配置文件中声明 `shepsci/kaggle-skill`，代理启动后即可通过自然语言指令触发对应功能。  
3. **MCP 服务**：将项目部署为 Model Context Protocol（MCP）服务器，其他内部工具或自研代理通过 HTTP/gRPC 调用统一的 API。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑07‑03，GitHub 70+ stars、20+ 话题，代码质量和文档较为完善。  
- **生态采纳**：已被 Claude Code、Gemini CLI、Cursor 等主流 AI 编码平台集成，说明兼容性和稳定性得到验证。  
- **风险**：目前未发现重大元数据或安全问题，但仍需对许可证（MIT/Apache 等）和维护者的长期可用性进行最终确认。  
- **总体评估**：在 OSS 候选中属于高准备度，适合作为正式生产环境的 Pilot 项目使用。

## 🧭 Practical evaluation

**Value:** shepsci/kaggle-skill helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 70 GitHub stars
- 3 forks
- updated 2026-07-03
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 15/100 |
| stars | 39/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 65/100 |
| recency | 80/100 |
| adoption | 33/100 |
| production | 73/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/shepsci/kaggle-skill) · [← Back to Mcp](./README.md)</sub>
