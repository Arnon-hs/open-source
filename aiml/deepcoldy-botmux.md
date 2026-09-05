# deepcoldy/botmux

[![Stars](https://img.shields.io/github/stars/deepcoldy/botmux?style=flat-square&color=yellow)](https://github.com/deepcoldy/botmux/stargazers) [![Forks](https://img.shields.io/github/forks/deepcoldy/botmux?style=flat-square&color=blue)](https://github.com/deepcoldy/botmux/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Bridge Feishu/Lark to AI coding CLIs — Claude Code, Codex, Gemini, OpenCode… every DM, group or topic spawns its own live-streaming CLI session

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 435 |
| 🍴 **Forks** | 85 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`claude` `claude-code` `codex` `feishu` `gemini` `lark` `opencode`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
deepcoldy/botmux is an open‑source bridge that connects Feishu/Lark messaging platforms to AI‑powered coding command‑line interfaces such as Claude Code, Codex, Gemini, and OpenCode. Each direct message, group chat, or topic automatically spawns a live‑streaming CLI session, turning conversational requests into executable code without manual hand‑offs. The tool streamlines repetitive development tasks by turning chat interactions into repeatable, automated workflows.

**Value**  
- **Automation of manual coding steps** – developers can invoke AI coding assistants directly from their preferred chat client, eliminating context switches and copy‑paste errors.  
- **Live, per‑conversation CLI sessions** – every DM, group, or topic gets its own isolated session, preserving state and enabling incremental development.  
- **Unified workflow orchestration** – botmux can be chained with other tools (CI/CD, issue trackers, scheduling services) to create end‑to‑end pipelines that start from a simple chat command.

**Practical Adoption Path**  
1. **Pilot Setup** – Deploy the TypeScript package in a container or serverless function, configure the Feishu/Lark webhook credentials, and add the required AI‑service API keys.  
2. **Define Command Mappings** – Use the provided SDK/CLI to map chat commands (e.g., `/code generate …`) to the desired AI coding backend.  
3. **Integrate with Existing CI/CD** – Hook the live‑streaming sessions into your build pipeline (e.g., trigger a GitHub Action when a session finishes).  
4. **Scale Gradually** – Start with a single team or project channel, collect usage metrics, then roll out to additional groups or topics as confidence grows.

**Production Readiness**  
- **Strong community signals**: 435 ★, 85 forks, recent commits (as of 2026‑06‑23), and active issue/PR activity indicate healthy maintenance.  
- **Technical maturity**: Built in TypeScript, exposing clear API/CLI interfaces and metadata, making integration straightforward for most modern stacks.  
- **Ecosystem fit**: Supports major AI coding models and popular Chinese enterprise chat platforms, covering a niche yet growing market.  
- **Risks to address before full production**: Final review of the software license, a security audit of the exposed APIs, and confirmation of long‑term maintainers. Once these checks are completed, botmux is well‑positioned for a serious pilot or production deployment.

### Русский

deepcoldy/botmux — это open‑source‑мост, позволяющий в реальном времени подключать Feishu/Lark к AI‑кодирующим CLI (Claude Code, Codex, Gemini, OpenCode и др.), автоматически создавая отдельную сессионную трансляцию для каждого личного сообщения, группы или темы. Он упрощает автоматизацию рутинных задач, объединяя инструменты в повторяемые потоки и позволяя планировать операции без ручного вмешательства. Проект имеет высокий уровень готовности к production: активные коммиты, 435 звёзд, 85 форков, поддержка TypeScript и широкие интеграционные сигналы, что делает его надёжным кандидатом для пилотного внедрения.

### 中文

**项目简介**  
deepcoldy/botmux 是一款 TypeScript 编写的开源工具，能够把飞书 / Lark 消息桥接到多种 AI 编码 CLI（Claude Code、Codex、Gemini、OpenCode 等），实现每个私聊、群聊或话题自动开启独立的实时流式 CLI 会话。

**价值**  
- **消除重复手工**：把代码生成、审查、调试等操作交给 AI，省去在 IDE 或终端里手动复制粘贴的繁琐步骤。  
- **统一入口**：团队成员只需在飞书/Lark 中发送指令，即可触发对应的 AI 编码模型，保持工作流一致且可追溯。  
- **可编排**：支持将多个工具链（如代码检查、单元测试、部署脚本）串联成可重复执行的自动化流程，适用于日常运维或 CI/CD 场景。

**典型接入方式**  
1. **部署 Bot 服务器**：使用 Docker 或直接 `npm install && npm start` 启动 botmux 服务。  
2. **配置平台凭证**：在飞书/Lark 开发者后台创建机器人，获取 `app_id`、`app_secret`，在 botmux 的配置文件（`.env`）中填入。  
3. **绑定 AI 模型**：在配置中声明要使用的模型 API（Claude、OpenAI、Gemini 等），提供对应的密钥。  
4. **自定义指令**：通过 `botmux.yml` 定义关键词或正则匹配的指令，映射到具体的 CLI 命令或脚本。  
5. **邀请机器人**：将机器人加入需要的聊天或话题，即可开始使用。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑23，项目最近一次提交，拥有 435 ★、85 Fork，且持续接受 PR。  
- **技术成熟**：核心使用 TypeScript，提供完整的 API/SDK 与 CLI 接口，易于二次集成。  
- **生态兼容**：支持多家主流 AI 编码模型，且可通过插件方式扩展其他工具。  
- **风险点**：需进一步审查许可证（MIT/Apache 等）和安全依赖；建议在正式环境前进行安全扫描并确认维护者响应速度。  

综合来看，botmux 已具备进入生产环境的技术与社区基础，只要完成许可证与安全审计，即可在企业内部作为 AI 编码助手的桥接层投入使用。

## 🧭 Practical evaluation

**Value:** deepcoldy/botmux helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 435 GitHub stars
- 85 forks
- updated 2026-06-23
- primary language: TypeScript
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 48/100 |
| stars | 56/100 |
| topics | 88/100 |
| outlook | 72/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 54/100 |
| production | 71/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/deepcoldy/botmux) · [← Back to AI/ML](./README.md)</sub>
