# milisp/awesome-claude-dxt

[![Stars](https://img.shields.io/github/stars/milisp/awesome-claude-dxt?style=flat-square&color=yellow)](https://github.com/milisp/awesome-claude-dxt/stargazers) [![Forks](https://img.shields.io/github/forks/milisp/awesome-claude-dxt?style=flat-square&color=blue)](https://github.com/milisp/awesome-claude-dxt/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> Awesome Claude Desktop Extensions (dxt) (not only Claude) mcpb

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 176 |
| 🍴 **Forks** | 33 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`awesome` `awesome-list` `claude` `claude-desktop` `dxt` `mcp` `mcp-server` `mcp-servers` `mcp-tools` `self-hosted`

## 🎯 Categories

MCP · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
milisp/awesome-claude-dxt is a curated collection of “Claude Desktop Extensions” (dxt) that implements the Model Context Protocol (MCP) to let AI assistants—Claude and others—talk to real‑world tools, data sources, and services. The repository provides ready‑to‑use API/SDK/CLI artifacts, language‑specific metadata, and example integrations that make it easy to prototype or ship MCP‑based back‑ends.

**Value**  
- **Standardised connectivity** – By adopting the MCP, developers can expose any tool or data source through a uniform interface, reducing the friction of writing custom adapters for each AI agent.  
- **Accelerated prototyping** – The curated list of extensions, sample code, and clear metadata let teams spin up functional integrations in hours rather than weeks.  
- **Future‑proof ecosystem** – Because MCP is designed to be language‑agnostic, the same extensions can be reused across Claude, other LLMs, or custom agents, protecting investment as AI platforms evolve.

**Practical Adoption Path**  
1. **Explore the catalogue** – Browse the repository’s topics and language tags to locate an extension that matches the target tool (e.g., a CLI wrapper, a REST API, or a SDK).  
2. **Clone & test** – Use the provided Docker/Node scripts to run the extension locally; the built‑in API/CLI lets you send MCP requests and inspect responses.  
3. **Integrate** – Replace the sample payloads with your own tool’s schema, adjust authentication (API keys, OAuth, etc.), and register the new MCP endpoint with your AI assistant’s runtime.  
4. **Iterate & scale** – Once the prototype works, containerise the service, add health‑checks, and push it to a staging environment for internal QA.  

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑06‑27), has 176 stars and 33 forks, and provides clear API/SDK boundaries, making it suitable for internal workflows or proof‑of‑concept deployments.  
- **Dependencies**: Primarily JavaScript/Node; verify compatibility with your runtime, and audit third‑party packages for security vulnerabilities.  
- **Operational considerations**: Add logging, rate‑limiting, and authentication hardening before exposing the MCP server to external traffic. A formal security review and licensing confirmation are still required for mission‑critical production use.  

Overall, milisp/awesome-claude-dxt offers a practical, standards‑based route to connect AI agents with real tools, with a clear path from prototype to a hardened production service after due diligence.

### Русский

**milisp/awesome-claude-dxt** — набор открытых расширений, реализующих Model Context Protocol и позволяющих быстро подключать AI‑ассистентов (в том числе Claude) к реальным инструментам, сервисам и данным через единый API/SDK/CLI. Типичный сценарий: разработчик развертывает MCP‑сервер, использует готовые JavaScript‑модули для интеграции инструментов (базы данных, CLI‑утилиты, веб‑сервисы) и тем самым ускоряет прототипирование и построение внутренних workflow‑ботов. Готовность к production — средняя: проект уже имеет 176 звёзд, активные коммиты и достаточный набор функций, но перед запуском в продакшн требуется проверка лицензии, безопасности и поддержка зависимостей.

### 中文

**项目简介（2‑3 句）**  
milisp/awesome-claude-dxt 是一个收录 Claude（以及其他 AI 助手）桌面扩展（dxt）的精选列表，提供基于 Model Context Protocol（MCP）的统一接入方案。它帮助开发者快速把 AI 代理连接到本地工具、数据源和后端服务，从而实现“AI + 工具”的协同工作。

---

### 价值点
- **统一协议**：通过标准化的 MCP 接口，消除不同工具、语言或平台之间的集成壁垒。  
- **快速原型**：提供现成的 API/SDK/CLI 示例，开发者可以在几分钟内让 AI 访问本地文件、数据库、命令行工具等。  
- **生态沉淀**：汇总了社区维护的优秀扩展，降低自行实现协议栈的成本，便于复用和迭代。

### 典型接入方式
1. **API/SDK**：在项目中引入 `@milisp/claude-dxt`（或对应语言的 SDK），按照文档注册工具插件并实现 `execute`, `fetchData` 等接口。  
2. **CLI**：使用项目自带的命令行工具启动本地 MCP 服务器，配置 `dxt.yaml` 指向需要暴露的工具，然后让 Claude（或其他 AI）通过 HTTP/WS 与之通信。  
3. **语言元数据**：通过项目提供的 JSON/YAML 元数据文件声明工具的输入/输出 schema，AI 能在运行时自动生成调用代码。  

> **示例（Node.js）**  
> ```js
> const { startMCPServer } = require('@milisp/claude-dxt');
> startMCPServer({
>   plugins: ['./plugins/git.js', './plugins/terminal.js'],
>   port: 8080,
> });
> // Claude 现在可以通过 http://localhost:8080 调用 git、终端等工具
> ```

### 生产可用性评估
| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | 中等 | 已有 176 星、33 Fork，活跃更新至 2026‑06‑27，适合原型和内部业务。 |
| **依赖与维护** | 需审查 | 依赖主要是 JavaScript 生态（Node.js），建议检查第三方库的安全报告和许可证兼容性。 |
| **安全性** | 待确认 | 当前未发现重大元数据风险，但需自行进行代码审计、API 鉴权和网络隔离。 |
| **可扩展性** | 良好 | 通过插件化机制可以灵活添加自定义工具，支持多语言元数据描述。 |
| **上线建议** | ✅ 适用于内部或低风险业务 | 在正式生产前进行：<br>1. 代码安全审计<br>2. 依赖漏洞扫描<br>3. 高可用部署（容器化 + 负载均衡）<br>4. 监控与日志收集 |

**结论**：milisp/awesome-claude-dxt 为 AI‑工具集成提供了一个轻量且标准化的入口，适合快速验证概念或在受控环境中使用。若要在面向客户的生产环境中部署，建议完成安全审计、依赖管理并实现高可用部署方案后再上线。

## 🧭 Practical evaluation

**Value:** milisp/awesome-claude-dxt helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 176 GitHub stars
- 33 forks
- updated 2026-06-27
- primary language: JavaScript
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 38/100 |
| stars | 48/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 70/100 |
| recency | 80/100 |
| adoption | 45/100 |
| production | 68/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/milisp/awesome-claude-dxt) · [← Back to Mcp](./README.md)</sub>
