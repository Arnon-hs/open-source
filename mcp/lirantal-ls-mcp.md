# lirantal/ls-mcp

[![Stars](https://img.shields.io/github/stars/lirantal/ls-mcp?style=flat-square&color=yellow)](https://github.com/lirantal/ls-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/lirantal/ls-mcp?style=flat-square&color=blue)](https://github.com/lirantal/ls-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> List MCP Server configurations in your system used by AI applications like Cursor, Claude Desktop, VS Code and others

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 84 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`claude-ai` `claude-desktop` `cursor` `cursor-ai` `mcp` `mcp-server` `model-context-protocol`

## 🎯 Categories

MCP · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary**  
`lirantal/ls-mcp` is a TypeScript library that discovers and lists Model Context Protocol (MCP) server configurations installed on a machine, enabling AI assistants such as Cursor, Claude Desktop, and VS Code extensions to locate the back‑end services they need. By exposing a simple API/CLI, it lets developers programmatically enumerate MCP endpoints and metadata, making it easier to wire AI agents to real tools and data sources.

**Value**  
- **Standardised discovery** – Provides a unified way to locate MCP servers, removing the need for custom scripts or hard‑coded paths when integrating AI assistants.  
- **Tool‑agnostic** – Works with any MCP‑compatible service, so the same discovery logic can be reused across editors, IDEs, and bespoke AI‑driven workflows.  
- **Developer productivity** – The CLI and SDK surface configuration details (host, port, language metadata, supported topics) instantly, accelerating prototyping and debugging of AI‑tool integrations.

**Practical Adoption Path**  
1. **Prototype** – Add the npm package to a proof‑of‑concept project and call `listMcpServers()` (or run `npx ls-mcp`) to verify that local MCP servers are detected.  
2. **Integrate** – Hook the returned configuration into your AI‑agent bootstrap code or VS Code extension, using the provided endpoint URLs to initialise the Model Context Protocol client.  
3. **Extend** – If you run custom MCP servers, add the required configuration files (e.g., `mcp.yaml`) in the standard locations; `ls-mcp` will pick them up automatically.  
4. **Ship** – Bundle the library with your production bundle or expose it as a micro‑service that other components can query for MCP endpoint discovery.

**Production Readiness**  
- **Maturity** – Medium; the project is actively maintained (last update 2026‑06‑25), has 84 ★ and 8 forks, and the codebase is relatively small and TypeScript‑typed, which eases auditing.  
- **Stability** – The core API (list, CLI) is simple and has few external dependencies, making it low‑risk to embed in internal pipelines.  
- **Considerations before production** – Verify the license compatibility with your stack, perform a security review of the configuration files it reads, and ensure you have a fallback if the library cannot locate an MCP server (e.g., default endpoints or graceful degradation).  

Overall, `ls-mcp` is a practical, low‑overhead component for any project that needs to connect AI assistants to MCP back‑ends, suitable for prototypes and internal tools, and ready for production after the usual compliance and security checks.

### Русский

**ls-mcp** — это открытый TypeScript‑инструмент, позволяющий автоматически перечислять конфигурации Model Context Protocol (MCP)‑серверов, используемых AI‑ассистентами (Cursor, Claude Desktop, VS Code и др.). Типичный сценарий — интеграция AI‑агентов с реальными инструментами и данными: разработчики быстро получают список доступных MCP‑эндпоинтов, могут развернуть свои MCP‑серверы и стандартизировать взаимодействие с внешними сервисами. Проект находится на среднем уровне готовности к production: имеет активные обновления, 84 звёзд и базовый API/CLI, но перед масштабным вводом следует проверить лицензию, безопасность зависимостей и наличие поддерживающих мейнтейнеров.

### 中文

**项目简介（2‑3 句）**  
`lirantal/ls-mcp` 是一个用 TypeScript 编写的开源工具，能够在本机上列出所有已注册的 MCP（Model Context Protocol）服务器配置，帮助 AI 助手（如 Cursor、Claude Desktop、VS Code 插件等）快速发现并连接可用的后端服务。

**价值**  
- **统一协议**：通过标准化的 MCP 接口，把 AI 助手与真实的工具、数据源以及自研服务桥接起来，降低集成成本。  
- **即插即用**：只需一行命令即可获取系统中所有 MCP 实例的地址、认证信息和元数据，帮助开发者快速构建 AI‑to‑Tool 场景。  
- **加速原型**：在内部实验或原型项目中，能够快速验证 AI 代理对外部工具的调用路径，提升迭代速度。

**典型接入方式**  
1. **CLI**：`npx ls-mcp`（或全局安装后使用 `ls-mcp`）直接在终端输出当前机器的 MCP 配置列表。  
2. **SDK**：在 TypeScript/JavaScript 项目中 `import { listMcpServers } from 'ls-mcp'`，调用 API 获得结构化的服务器信息，可进一步用于动态创建连接。  
3. **API/HTTP**：项目提供可选的本地 HTTP 端点（`/mcp/servers`），方便非 Node 环境（如 Python、Go）通过 REST 读取配置。  

**生产可用性**  
- **成熟度**：当前在 GitHub 上拥有 84 ★、8 Fork，最近一次提交在 2026‑06‑25，活跃度尚可。  
- **适用场景**：非常适合原型、内部工具链或中小规模服务的 MCP 配置管理；在大规模生产环境使用前，需要评估以下方面：  
  - **依赖安全**：检查其依赖的 NPM 包是否有已知漏洞。  
  - **许可证兼容**：确认项目许可证（MIT）与贵公司合规要求匹配。  
  - **维护者活跃度**：虽然近期有更新，但核心维护者人数有限，建议自行 fork 并制定内部维护策略。  
- **结论**：在做好安全审计和维护计划后，`ls-mcp` 可作为生产环境中 MCP 配置发现的可靠组件，尤其适用于需要统一管理多种 AI 工具接入的企业内部平台。

## 🧭 Practical evaluation

**Value:** lirantal/ls-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 84 GitHub stars
- 8 forks
- updated 2026-06-25
- primary language: TypeScript
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 41/100 |
| topics | 88/100 |
| outlook | 67/100 |
| quality | 64/100 |
| recency | 80/100 |
| adoption | 36/100 |
| production | 68/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/lirantal/ls-mcp) · [← Back to Mcp](./README.md)</sub>
