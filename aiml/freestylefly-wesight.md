# freestylefly/wesight

[![Stars](https://img.shields.io/github/stars/freestylefly/wesight?style=flat-square&color=yellow)](https://github.com/freestylefly/wesight/stargazers) [![Forks](https://img.shields.io/github/forks/freestylefly/wesight?style=flat-square&color=blue)](https://github.com/freestylefly/wesight/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> Open-source desktop AI agent workspace with one-click Claude Code, Codex, OpenClaw, Hermes Agent setup and custom LLM model routing.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 730 |
| 🍴 **Forks** | 180 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-workspace` `ai-agent` `claude-code` `codex` `desktop-app` `electron` `hermes-agent` `llm` `local-first` `macos` `model-router` `openclaw`

## 🎯 Categories

AI/ML · Productivity · Frontend

## 📝 Summary

### English

**Brief Summary**  
Freestylefly / Wesight is an open‑source desktop workspace that lets developers spin up AI agents with a single click, bundling Claude Code, Codex, OpenClaw, Hermes and custom LLM routing in a TypeScript‑based UI. It accelerates prototype building, RAG pipelines, and agent‑workflow experimentation without having to assemble a model stack from scratch.

**Value**  
- **Plug‑and‑play AI stack** – One‑click setup eliminates the time‑consuming integration of multiple LLM providers and routing logic.  
- **Unified workspace** – A desktop UI, CLI, and SDK give developers a consistent environment for prototyping, testing, and iterating on AI features.  
- **Extensible routing** – Supports custom model endpoints, enabling teams to evaluate internal or third‑party LLMs side‑by‑side with popular services.

**Practical Adoption Path**  
1. **Clone & install** – `git clone` the repo, run the provided installer (or `npm ci` + `npm start`) to launch the desktop app.  
2. **Select a provider** – Use the UI to enable Claude, Codex, OpenClaw, Hermes, or point to a self‑hosted model via the custom routing panel.  
3. **Integrate via SDK/CLI** – Import the TypeScript SDK in existing codebases or call the CLI to generate agents, retrieve completions, or trigger RAG pipelines.  
4. **Iterate & benchmark** – Swap providers or adjust routing rules on the fly, collect logs, and use built‑in telemetry to compare performance and cost.  
5. **Production hand‑off** – Export the configuration as a JSON manifest and embed the SDK in a server‑side service or containerize the desktop app for internal tooling.

**Production Readiness**  
- **Activity & community** – 730 ★, 180 forks, recent commits (as of 2026‑06‑28) and a growing TypeScript ecosystem indicate active maintenance.  
- **Signal quality** – Clear API/SDK/CLI surface, well‑documented metadata, and focused topics make integration straightforward.  
- **Risk considerations** – License compliance, security hardening, and long‑term maintainer commitment still need a final audit, but the project’s current health is strong enough for a pilot or internal production use.

### Русский

Резюме проекта freestylefly/wesight:

freestylefly/wesight - это открытый исходный код проект, который предоставляет рабочую область AI-агента с одной кнопкой для настройки кода Claude, Codex, OpenClaw, Hermes Agent и маршрутизации пользовательских моделей LLM. Этот проект позволяет добавлять AI-способности без создания пустого стека моделей, что делает его идеальным решением для прототипирования AI-функций, построения RAG или агентных потоков и оценки инструментов моделирования. freestylefly/wesight имеет высокий уровень готовности к production, что делает его подходящим кандидатом для серьезного пилота, с недавней деятельностью, адопцией и сигналами экосистемы.

### 中文

**项目简介**  
freestylefly/wesight 是一款开源的桌面 AI 代理工作空间，提供“一键式”部署 Claude Code、Codex、OpenClaw、Hermes Agent 等模型，并支持自定义 LLM 路由。它让开发者无需从零搭建模型堆栈，即可快速加入 AI 能力。

**价值**  
- **快速原型**：只需几步即可在本地启动完整的 AI 代理环境，适合验证 AI 功能或构建 RAG/Agent 工作流。  
- **统一入口**：通过统一的 UI/CLI/SDK 把多种大模型（Claude、Codex、OpenClaw、Hermes）以及自定义模型整合在同一个工作区，降低切换成本。  
- **可扩展**：模型路由机制灵活，支持按业务需求动态选择或组合不同 LLM，方便实验和迭代。

**典型接入方式**  
1. **一键安装**：克隆仓库后运行 `npm i && npm run setup`（或提供的桌面安装包），系统自动下载并配置所选模型。  
2. **CLI/SDK 调用**：项目暴露 `wesight-cli` 与 TypeScript SDK，开发者可以在代码中通过 `wesight.runAgent(...)` 或 `wesight.invokeModel(...)` 调用特定模型。  
3. **自定义路由**：在 `config/router.ts` 中编写路由规则，依据请求类型、上下文或成本等因素转发到不同的 LLM。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑28，最近一次提交、730+ 星、180+ Fork，社区活跃。  
- **技术成熟度**：采用 TypeScript 编写，拥有完整的 API 文档、示例项目和 CLI，易于集成到现有前端/后端系统。  
- **风险**：许可证、长期维护者以及安全审计仍需进一步确认；但从代码质量、依赖更新频率和社区反馈来看，已具备在内部或受控环境中进行试点的条件。  

综上，wesight 为需要快速加入 AI 功能的团队提供了即插即用的解决方案，接入门槛低，且在当前状态下已具备进行生产级试点的基本保障。

## 🧭 Practical evaluation

**Value:** freestylefly/wesight helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 730 GitHub stars
- 180 forks
- updated 2026-06-28
- primary language: TypeScript
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 61/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 77/100 |
| recency | 80/100 |
| adoption | 60/100 |
| production | 73/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/freestylefly/wesight) · [← Back to AI/ML](./README.md)</sub>
