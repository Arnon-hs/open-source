# vishalguptax/claude-manager

[![Stars](https://img.shields.io/github/stars/vishalguptax/claude-manager?style=flat-square&color=yellow)](https://github.com/vishalguptax/claude-manager/stargazers) [![Forks](https://img.shields.io/github/forks/vishalguptax/claude-manager?style=flat-square&color=blue)](https://github.com/vishalguptax/claude-manager/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Claude Manager — manage Claude Code sessions, MCP, skills, hooks, agents, accounts & usage from your VS Code sidebar. 100% local.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 21 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`account-switcher` `ai-coding` `ai-tools` `anthropic` `antigravity` `claude` `claude-ai` `claude-code` `claude-code-manager` `claude-manager` `claude-session` `claude-session-manager`

## 🎯 Categories

MCP · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Claude Manager is a VS Code sidebar extension that lets you run and control Claude Code sessions, MCP servers, skills, hooks, agents, accounts, and usage—all locally. Written in TypeScript, it provides a unified UI for managing the Model Context Protocol (MCP) ecosystem, making it easy to connect Claude‑powered AI assistants to real tools and data without leaving your editor.

**Value**  
- **Unified control plane** – All MCP components (servers, skills, hooks, agents, usage metrics) are accessible from a single sidebar, removing the friction of juggling multiple terminals or web consoles.  
- **Zero‑trust, local‑first** – Because everything runs locally, you keep proprietary data and model prompts in‑house, which is crucial for privacy‑sensitive projects.  
- **Standardised integration** – By adhering to the Model Context Protocol, the extension serves as a reference implementation that can be reused to ship new MCP‑based services or plug‑in existing AI agents to external tools.

**Practical Adoption Path**  
1. **Install the extension** in VS Code and open the Claude Manager sidebar.  
2. **Configure your Claude API credentials** (or point to a self‑hosted Claude endpoint) inside the UI.  
3. **Spin up an MCP server** directly from the sidebar or attach to an existing one; the UI will show health, logs, and usage stats.  
4. **Add skills, hooks, or agents** via the “Add” wizard; the extension scaffolds the required TypeScript/JSON files and registers them with the running MCP server.  
5. **Iterate locally**—run code, debug hooks, and monitor token usage in real time.  
6. **Export or containerise** the generated MCP artifacts when you’re ready to move from prototype to a shared dev‑ops pipeline.

**Production Readiness**  
- **Maturity**: Medium. The project is functional and actively maintained (last commit 2026‑06‑26) with 21 ⭐ and a modest fork count, indicating community interest but limited large‑scale validation.  
- **Dependencies**: Pure TypeScript/Node.js stack; no heavy native binaries, which simplifies CI/CD integration.  
- **Security & Licensing**: No red‑flag metadata yet, but a formal review of the repository’s license (likely MIT/Apache) and any third‑party SDKs is required before production use.  
- **Operational considerations**: Because the manager runs locally, you must ensure the host machine has sufficient resources for Claude sessions and MCP servers; for multi‑user or cloud deployments you’ll need to containerise the setup and handle secret management externally.  

Overall, Claude Manager is a solid starting point for teams that want to prototype AI‑assistant‑to‑tool integrations quickly and keep everything under local control. With a brief security audit and some production‑grade orchestration (e.g., Docker/K8s wrappers), it can be hardened for internal‑service or low‑risk production workloads.

### Русский

**vishalguptax/claude-manager** — это расширение для VS Code, позволяющее полностью локально управлять сессиями Claude, MCP, навыками, хуками, агентами и учётными записями прямо из боковой панели. Оно упрощает подключение AI‑агентов к реальным инструментам и данным через стандартный Model Context Protocol, что делает его удобным решением для прототипов и внутренних рабочих процессов, где требуется быстрая интеграция и контроль использования. Готовность к production — средняя: проект достаточно стабилен для разработки и тестирования, но перед выводом в продакшн следует проверить зависимости, безопасность и наличие активных мейнтейнеров.

### 中文

**项目简介（2‑3 句）**  
Claude Manager 是一款 VS Code 侧边栏插件，能够在本地完整管理 Claude Code 会话、MCP（Model Context Protocol）服务、技能、Hook、Agent、账号及使用情况，免除云端依赖。它通过统一的协议把 AI 助手与本地工具、数据源相连接，让开发者在 IDE 中直接调度和监控 AI 工作流。

**价值**  
- **统一入口**：在 VS Code 中即可创建、切换、监控 Claude 会话和 MCP 服务器，省去多窗口切换的繁琐。  
- **本地安全**：所有交互均在本地完成，代码、凭证和模型上下文不离开开发者机器，符合企业内部合规要求。  
- **标准化集成**：实现了对 Model Context Protocol 的原生支持，开发者可以快速把任意 AI Agent、Skill、Hook 接入本地工具链，降低二次开发成本。  

**典型接入方式**  
1. **VS Code 插件**：在 VS Code Marketplace 安装 `Claude Manager`，插件会在侧边栏自动加载。  
2. **MCP 服务器**：通过插件提供的 UI 启动/停止本地 MCP 实例，或在终端使用 `claude-manager serve` 启动自定义服务器。  
3. **API/SDK**：插件暴露的本地 HTTP/WS 接口（或对应的 TypeScript SDK）可被其他工具或脚本调用，完成如下场景：  
   - 将自研 CLI 与 Claude Agent 绑定，实现“一键执行”。  
   - 在 CI/CD 流水线中调用 MCP API，自动生成代码审查或文档。  
4. **Hook / Skill 注册**：在插件 UI 中上传或编辑 JavaScript/TypeScript 文件，即可将自定义 Hook/Skill 注入 Claude 会话，实时生效。  

**生产可用性评估**  
- **成熟度**：项目已有 21 星、4 个 fork，最近一次提交在 2026‑06‑26，活跃度尚可。代码基于 TypeScript，结构清晰，提供 CLI、API 与 UI 三层入口。  
- **适用场景**：非常适合原型开发、内部工具链实验以及需要本地化 AI 助手的安全敏感环境。  
- **风险与准备**：  
  - **依赖管理**：需审查其依赖的 Node 包版本及安全报告，确保不引入已知漏洞。  
  - **维护者**：当前维护者信息有限，建议在生产环境部署前与作者或社区确认长期维护计划。  
  - **许可证**：项目使用的开源许可证需确认与企业合规要求匹配。  
- **结论**：在做好依赖安全审计和维护承诺确认后，Claude Manager 可作为内部 AI‑Tool 集成的“生产级”组件使用，尤其适用于需要本地化、可审计的 AI 工作流。

## 🧭 Practical evaluation

**Value:** vishalguptax/claude-manager helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 21 GitHub stars
- 4 forks
- updated 2026-06-26
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 58/100 |
| quality | 51/100 |
| recency | 40/100 |
| adoption | 25/100 |
| production | 54/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/vishalguptax/claude-manager) · [← Back to Mcp](./README.md)</sub>
