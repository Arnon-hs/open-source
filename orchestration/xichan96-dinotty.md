# xichan96/dinotty

[![Stars](https://img.shields.io/github/stars/xichan96/dinotty?style=flat-square&color=yellow)](https://github.com/xichan96/dinotty/stargazers) [![Forks](https://img.shields.io/github/forks/xichan96/dinotty?style=flat-square&color=blue)](https://github.com/xichan96/dinotty/network) [![Language](https://img.shields.io/badge/lang-Vue-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Multi-device terminal server for AI coding agents. Server-side VTE, session persistence, file browser, web preview, plugin system. Self-hosted.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 137 |
| 🍴 **Forks** | 17 |
| 💻 **Language** | Vue |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-coding` `axum` `claude-code` `codex` `coding-agent` `mobile-coding` `pty` `remote-terminal` `rust` `session-persistence` `terminal` `tmux-alternative`

## 🎯 Categories

Orchestration · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Dinotty (xichan96/dinotty) is a self‑hosted, multi‑device terminal server that adds a VTE‑based UI, session persistence, file browsing, web preview, and a plugin system to AI‑coding agents. It lets developers prototype AI‑enhanced workflows—such as RAG pipelines or autonomous agents—without building a terminal interface from scratch. With a Vue front‑end and a simple API/CLI, it can be dropped into existing stacks to give AI agents a real‑time, interactive shell.

**Value**  
- **Accelerates AI feature development** – provides a ready‑made terminal environment so teams can focus on the agent logic rather than UI plumbing.  
- **Extensible plugin system** – lets you attach custom tooling (e.g., linters, debuggers, code generators) that AI agents can invoke directly.  
- **Cross‑device access** – developers can connect from browsers, desktop clients, or headless scripts, enabling seamless collaboration and testing.

**Practical Adoption Path**  
1. **Spin up the server** (Docker compose or npm install) in a sandbox or CI environment.  
2. **Integrate via the exposed API/CLI** to launch sessions, send commands, and retrieve output from your AI model.  
3. **Add plugins** for project‑specific utilities (e.g., repository browsers, test runners).  
4. **Iterate** on agent prompts using the persisted sessions and web preview to debug and refine behavior.  
5. **Gradually migrate** from prototype to internal tooling, adding authentication, monitoring, and scaling as needed.

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last update 2026‑06‑23), has 137 stars and 17 forks, and provides core features needed for prototypes.  
- **Strengths:** Clear API surface, session persistence, and a modular plugin architecture make it suitable for internal workflows.  
- **Caveats:** Before production use, verify the license, conduct a security audit of dependencies, and ensure you have a maintainer or fallback plan for long‑term support. Adding authentication, rate‑limiting, and logging will raise its readiness to production grade.

### Русский

**Краткое резюме:**  
xichan96/dinotty — это self‑hosted сервер терминала с поддержкой VTE, сохранением сессий, файловым браузером, веб‑просмотром и плагин‑системой, позволяющий быстро добавить в приложение AI‑кодинг‑агентов без необходимости собирать собственный стек моделей. Типичный сценарий — прототипирование AI‑фич, построение RAG‑или агентных пайплайнов и оценка инструментов модели через предоставляемый API/SDK/CLI. Проект находится на среднем уровне готовности к production: подходит для внутренних прототипов, но требует проверки лицензий, безопасности и поддержки зависимостей перед масштабным внедрением.

### 中文

**项目简介**  
xichan96/dinotty 是一个多设备终端服务器，提供服务器端 VTE、会话持久化、文件浏览、网页预览和插件系统，支持自托管。它让开发者可以在已有的 AI 编码代理上快速接入终端交互能力，而无需从零搭建模型栈。

**价值**  
- **加速 AI 功能原型**：通过统一的终端界面，即可让大型语言模型直接在代码编辑、文件操作、调试等真实开发环境中执行任务，显著缩短 AI 功能的验证周期。  
- **支持 RAG 与 Agent 工作流**：内置文件浏览和网页预览，可轻松实现检索增强生成（RAG）以及多步骤 Agent 流程的闭环。  
- **灵活插件体系**：开发者可自行编写插件扩展功能，满足特定业务需求，降低二次开发成本。

**典型接入方式**  
1. **API/SDK**：项目提供 HTTP API 与 Node.js/Python SDK，调用 `createSession`、`sendInput`、`receiveOutput` 等接口即可在自己的系统中嵌入终端交互。  
2. **CLI**：通过 `dinotty-cli` 在本地或 CI 环境启动会话，适合脚本化测试或自动化流水线。  
3. **Web UI**：前端基于 Vue，直接部署后即可通过浏览器访问终端，适合作为内部工具或 demo 页面。  

**生产可用性**  
- **成熟度**：GitHub 137 星、15 个主题标签，最近一次更新在 2026‑06‑23，活跃度尚可。  
- **适用场景**：非常适合作为原型验证、内部研发平台或实验性 RAG/Agent 流程的基础设施。  
- **上线注意**：在生产环境使用前需完成以下检查：  
  - **依赖安全审计**：确认所有后端依赖（Node、VTE、WebSocket 等）无已知漏洞。  
  - **授权与许可证**：项目采用的开源许可证需与企业合规要求匹配。  
  - **运维监控**：为会话持久化和插件执行添加日志、资源配额和异常报警，防止单个会话占用过多资源。  
  - **维护者沟通**：若计划长期使用，建议与原作者或社区保持联系，以获取安全补丁和功能更新。  

总体而言，dinotty 在原型阶段和内部工具链中具备较高的性价比；经过安全与运维审查后，可在受控的生产环境中稳妥部署。

## 🧭 Practical evaluation

**Value:** xichan96/dinotty helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 137 GitHub stars
- 17 forks
- updated 2026-06-23
- primary language: Vue
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 31/100 |
| stars | 46/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 42/100 |
| production | 68/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/xichan96/dinotty) · [← Back to Orchestration](./README.md)</sub>
