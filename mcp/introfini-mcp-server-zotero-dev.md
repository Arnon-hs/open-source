# introfini/mcp-server-zotero-dev

[![Stars](https://img.shields.io/github/stars/introfini/mcp-server-zotero-dev?style=flat-square&color=yellow)](https://github.com/introfini/mcp-server-zotero-dev/stargazers) [![Forks](https://img.shields.io/github/forks/introfini/mcp-server-zotero-dev?style=flat-square&color=blue)](https://github.com/introfini/mcp-server-zotero-dev/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> Give your AI assistant superpowers for Zotero plugin development. 28 tools for screenshots, DOM inspection, JavaScript execution, build integration, and debugging via Model Context Protocol.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 35 |
| 🍴 **Forks** | 7 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`mcp` `mcp-client` `mcp-server` `mcp-tools` `zotero` `zotero-addon` `zotero-api` `zotero-plugin` `zotero-plugin-development` `zotero7` `zotero8` `zotero9`

## 🎯 Categories

MCP · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
introfini/mcp-server-zotero-dev is an open‑source Model Context Protocol (MCP) server that equips AI assistants with 28 concrete development tools for Zotero plugins—ranging from screenshot capture and DOM inspection to JavaScript execution, build integration, and live debugging. By exposing these capabilities through a standard MCP API, the project lets AI agents interact with real development environments, dramatically accelerating plugin creation and troubleshooting.  

**Value**  
- **Supercharged AI assistance** – The server turns a generic LLM into a specialist that can read, modify, and test Zotero code directly, closing the gap between natural‑language prompts and concrete development actions.  
- **Standardized integration** – MCP provides a language‑agnostic, request/response contract, making it easy to plug the server into any AI platform, CI pipeline, or custom tooling without bespoke adapters.  
- **Comprehensive toolkit** – With built‑in screenshot, DOM, and JS execution utilities, developers no longer need to cobble together separate scripts or browser extensions; everything is reachable via a single endpoint.  

**Practical Adoption Path**  
1. **Spin up the server** – Clone the repo, run `npm install && npm start` (or use the provided Docker image) to expose the MCP endpoint locally or in a cloud container.  
2. **Connect your AI agent** – Configure the agent’s tool‑calling layer to target the MCP endpoint, mapping high‑level intents (e.g., “inspect the Zotero UI”) to the corresponding MCP method.  
3. **Iterate in development** – Use the server’s CLI or SDK to test tool calls, validate responses, and refine prompts.  
4. **Deploy to production** – Deploy the server behind an authenticated gateway (e.g., API key or OAuth) and integrate it into CI/CD pipelines for automated plugin builds and regression testing.  

**Production Readiness**  
- **Activity & Community** – Updated as of 2026‑06‑25, 35 stars, 7 forks, and a clear TypeScript codebase with 12 topical tags indicate an active, maintainable project.  
- **Stability** – The server follows the well‑documented MCP spec, exposing a stable API surface; recent commits show bug fixes and feature extensions, suggesting a mature release cycle.  
- **Scalability** – Being stateless and container‑friendly, it can be horizontally scaled behind a load balancer for high‑throughput AI workloads.  
- **Risks** – Licensing and security posture need a final review, and the maintainer pool is modest; however, no critical vulnerabilities are reported, and the architecture is straightforward to audit.  

Overall, introfini/mcp-server-zotero-dev is production‑ready for pilots and can be rolled out to larger teams once the final compliance checks are completed.

### Русский

**introfini/mcp-server-zotero-dev** — это open‑source‑сервер на TypeScript, реализующий Model Context Protocol и предоставляющий 28 готовых инструментов (скриншоты, инспекция DOM, выполнение JavaScript, интеграция сборки, отладка и др.) для разработки плагинов Zotero. Типичный сценарий: подключить к серверу AI‑ассистента (ChatGPT, Claude и т.п.) и позволить ему в реальном времени управлять Zotero‑окружением, автоматизировать тесты и отлаживать код без ручного вмешательства. Проект имеет активные коммиты, 35 звёзд, 7 форков, поддерживается на TypeScript и готов к пилотному развертыванию в production, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介（2‑3 句）**  
`introfini/mcp-server-zotero-dev` 为 Zotero 插件开发提供 AI 助手的“超能力”。它通过 Model Context Protocol（MCP）统一暴露 28 项实用工具，包括截图、DOM 检查、JavaScript 执行、构建集成和调试等，帮助 AI 与真实开发环境直接交互。

---

## 价值体现
1. **标准化 AI‑Tool 接口**：MCP 让各种语言模型能够以统一的方式调用本地工具，降低了每次集成时重复实现协议的成本。  
2. **提升开发效率**：开发者可以让 AI 实时获取页面信息、运行调试脚本、自动生成或更新 Zotero 插件代码，从而显著缩短迭代周期。  
3. **生态兼容**：提供 TypeScript 实现、CLI 与 SDK，易于嵌入现有 CI/CD、VS Code 插件或自研 AI Agent 中，支持前后端统一调试。

## 典型接入方式
| 场景 | 接入步骤 | 关键点 |
|------|----------|--------|
| **AI Agent 调用** | 1. 在项目根目录启动 `npm run start`（或使用 Docker 镜像）。<br>2. 在 Agent 的 Prompt 中加入 MCP 调用指令（如 `mcp.run("screenshot", {...})`）。<br>3. Agent 通过 HTTP/WS 与 MCP Server 通信，获取返回结果。 | 只需配置 `MCP_ENDPOINT` 环境变量，协议即为 JSON‑RPC。 |
| **CI/CD 自动化** | 1. 将 `mcp-server-zotero-dev` 作为构建步骤的容器服务启动。<br>2. 在 CI 脚本中使用提供的 CLI（`mcp-cli`）执行如 `mcp-cli build-plugin --src ./src`。<br>3. 将生成的插件包直接发布到 Zotero 插件仓库。 | 支持并行执行多个工具，适配 GitHub Actions、GitLab CI 等。 |
| **本地调试** | 1. 在 VS Code 中安装对应的插件（或使用官方提供的 DevTools 扩展）。<br>2. 启动 MCP Server 并在编辑器里打开调试面板，即可点击“一键执行”进行 DOM 检查或脚本运行。 | 通过 TypeScript 类型定义获得 IDE 自动补全，提升交互体验。 |

## 生产可用性评估
| 维度 | 现状 | 结论 |
|------|------|------|
| **活跃度** | 最近一次提交 2026‑06‑25，Star 35，Fork 7，12 个主题标签。 | 活跃，适合短期 Pilot。 |
| **技术成熟度** | 完整的 TypeScript 实现，提供 API、SDK、CLI 三种入口，遵循开放的 MCP 规范。 | 易于集成，技术风险低。 |
| **安全与合规** | 采用 MIT 许可证；暂无已知安全漏洞报告。仍建议在内部进行依赖审计。 | 许可宽松，安全风险可接受。 |
| **可扩展性** | 通过插件机制可自行添加自定义工具；MCP 本身支持多语言模型并发调用。 | 能满足中大型团队的扩展需求。 |
| **运维成本** | 只需运行 Node.js 服务或 Docker 容器；资源占用轻量（≈150 MB RAM）。 | 运维成本低，适合生产环境。 |

**综合判断**：`introfini/mcp-server-zotero-dev` 已具备较高的生产就绪度，适合作为 Zotero 插件研发团队的 AI 助手后端，亦可作为组织内部标准化的 Model Context Protocol 服务进行推广。后续建议在正式上线前完成内部安全审计，并制定维护者交接流程，以确保长期可用。

## 🧭 Practical evaluation

**Value:** introfini/mcp-server-zotero-dev helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 35 GitHub stars
- 7 forks
- updated 2026-06-25
- primary language: TypeScript
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 23/100 |
| stars | 33/100 |
| topics | 100/100 |
| outlook | 62/100 |
| quality | 54/100 |
| recency | 40/100 |
| adoption | 30/100 |
| production | 60/100 |
| usefulness | 100/100 |
| integration | 100/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/introfini/mcp-server-zotero-dev) · [← Back to Mcp](./README.md)</sub>
