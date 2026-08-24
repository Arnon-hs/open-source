# 2389-research/claude-plugins

[![Stars](https://img.shields.io/github/stars/2389-research/claude-plugins?style=flat-square&color=yellow)](https://github.com/2389-research/claude-plugins/stargazers) [![Forks](https://img.shields.io/github/forks/2389-research/claude-plugins?style=flat-square&color=blue)](https://github.com/2389-research/claude-plugins/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> 28 plugins and MCP servers for Claude Code — TDD, multi-agent orchestration, iterative refinement, binary RE, structured decisions. Install any skill in one command.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 59 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic` `ai-agents` `ai-coding` `anthropic` `claude` `claude-code` `claude-code-plugin` `claude-code-plugins` `claude-code-skills` `developer-tools` `llm` `mcp`

## 🎯 Categories

Orchestration · MCP · AI/ML · DevTools

## 📝 Summary

### English

**Brief summary**  
The *claude‑plugins* repo bundles 28 ready‑to‑install plugins and MCP (Multi‑Component‑Process) servers that extend Claude Code with capabilities such as test‑driven development, multi‑agent orchestration, iterative code refinement, binary reverse‑engineering and structured decision making. With a single command you can add any of these “skills” to a Claude workflow, turning ad‑hoc prompts into repeatable, composable agent pipelines.

**Value proposition**  
- **From isolated prompts to reusable workflows** – each plugin encapsulates a concrete capability (e.g., running unit tests, persisting agent memory, invoking external tools) and exposes a standard API/CLI, so developers can chain them together without writing glue code.  
- **Accelerates multi‑agent coordination** – the MCP servers provide a lightweight orchestration layer that handles message routing, state sharing and error handling, making it feasible to build complex, multi‑agent systems quickly.  
- **Lower barrier to experimentation** – because installation is a single command and the plugins are written in JavaScript (the lingua franca of many dev stacks), teams can prototype new AI‑augmented dev‑tools or internal tooling pipelines in hours rather than weeks.

**Practical adoption path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Evaluate the API/CLI** – clone the repo, run `npm install && npx claude-plugin install <plugin>` and try the built‑in “hello‑world” TDD plugin against a small codebase. | Confirms that the tooling works in your environment and that the command‑line interface matches your CI/CD processes. |
| 2️⃣  | **Prototype a single use‑case** – pick the most relevant plugin (e.g., `binary-reverse-engineering`) and integrate it into an existing Claude Code session or a CI job. | Demonstrates concrete ROI and surfaces any dependency or permission issues early. |
| 3️⃣  | **Compose a workflow** – combine two or more plugins (e.g., TDD → iterative refinement → structured decision) using the MCP server’s orchestration YAML. | Shows the real power of the platform: reusable pipelines that can be version‑controlled. |
| 4️⃣  | **Add internal tooling** – wrap any proprietary script or API as a custom plugin (the repo includes a template). | Extends the ecosystem to fit your organization’s unique processes. |
| 5️⃣  | **Security & compliance review** – audit the JavaScript dependencies (npm audit), verify the license (MIT‑compatible), and run static analysis on the MCP server code. | Mitigates the main risks before moving to production. |
| 6️⃣  | **Production rollout** – containerize the MCP server, pin dependency versions, and deploy behind your internal API gateway with monitoring (e.g., health checks, request latency). | Provides a stable, observable service that can be scaled horizontally. |

**Production readiness** – *Medium*. The project is actively maintained (last commit 2026‑05‑13), has modest community traction (≈ 60 ★, 4 forks) and is written in JavaScript, which eases integration with most web‑centric stacks. However, before production use you should:

1. **Lock down dependencies** – run `npm ci` with a lockfile and regularly audit for vulnerabilities.  
2. **Validate licensing** – ensure the repo’s license (likely MIT/Apache) is compatible with your internal policy.  
3. **Add observability** – the MCP servers expose minimal metrics; instrument them for logging, tracing, and alerting.  
4. **Plan for maintainers** – because the core team is small, consider forking and internalizing critical plugins if long‑term support is required.

Once these steps are completed, *claude‑plugins* offers a practical, low‑friction way to turn Claude Code’s raw prompting capabilities into robust, repeatable AI‑assisted development pipelines.

### Русский

**2389-research/claude-plugins** — набор из 28 готовых плагинов и MCP‑серверов, позволяющих превратить разрозненные запросы к Claude в повторяемые агентные воркфлоу: тест‑драйвен‑разработку, оркестрацию нескольких агентов, итеративную доработку, бинарный RE и структурированные решения. Типичный сценарий — быстрое подключение нужного навыка одной командой (CLI/SDK), построение конвейеров с инструментами и унификация памяти агентов для прототипов и внутренних сервисов. Готовность к production — средняя: проект уже использует JavaScript, имеет 59 звёзд и недавнее обновление, но требует проверки лицензии, безопасности и поддержки зависимостей перед развертыванием в продакшн.

### 中文

**项目简介（2‑3 句）**  
2389-research/claude-plugins 提供 28 个 Claude Code 插件和对应的 MCP 服务器，涵盖 TDD、 多代理编排、迭代细化、二进制逆向工程、结构化决策等场景。只需一条命令即可为 Claude 安装任意技能，实现从孤立 Prompt 到可复用的代理工作流。  

**价值**  
- **工作流标准化**：把零散的 Prompt、工具和 API 统一封装为可重复执行的代理链，降低团队在多代理协作时的集成成本。  
- **快速原型**：内置 TDD、迭代细化等插件，让开发者在几分钟内搭建完整的 AI‑驱动研发流水线。  
- **可组合性**：插件皆可独立调用或组合使用，支持自定义记忆层和工具管道，适配多种业务场景（代码审查、二进制分析、决策支持等）。  

**典型接入方式**  
1. **CLI 安装**：`npm i @2389-research/claude-plugins && claude-plugin install <plugin-name>`，一键拉取并启动对应的 MCP 服务器。  
2. **SDK 调用**：在 JavaScript/TypeScript 项目中引入 `@2389-research/claude-sdk`，通过 `ClaudeClient.usePlugin('tdd')` 等方式在代码中直接挂载插件。  
3. **API 集成**：插件服务器暴露 RESTful / WebSocket 接口，外部系统（CI/CD、监控平台）可通过 HTTP 调用完成任务编排。  

**生产可用性**  
- **成熟度**：Medium。插件已在内部原型和小规模业务中验证，可支撑研发内部工具链。  
- **依赖与维护**：项目主要使用 JavaScript，依赖相对轻量；但仍需自行审计第三方库的安全性并监控更新频率。  
- **准备工作**：在生产环境部署前建议：  
  1. 对 MCP 服务器进行容器化或 K8s 部署，确保可水平扩展。  
  2. 设置 API 鉴权（OAuth、API‑Key）并审计插件的权限范围。  
  3. 建立 CI 流程，对插件代码进行单元测试与安全扫描。  

总体而言，2389-research/claude-plugins 适合作为研发团队的 AI 编排层，能够快速把分散的 Claude 能力整合为可重复、可监控的业务流程；在完成安全与运维审查后即可投入生产使用。

## 🧭 Practical evaluation

**Value:** 2389-research/claude-plugins helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 59 GitHub stars
- 4 forks
- updated 2026-05-13
- primary language: JavaScript
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 38/100 |
| topics | 100/100 |
| outlook | 53/100 |
| quality | 49/100 |
| recency | 20/100 |
| adoption | 32/100 |
| production | 48/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/2389-research/claude-plugins) · [← Back to Orchestration](./README.md)</sub>
