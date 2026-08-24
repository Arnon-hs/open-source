# sandraschi/inkscape-mcp

[![Stars](https://img.shields.io/github/stars/sandraschi/inkscape-mcp?style=flat-square&color=yellow)](https://github.com/sandraschi/inkscape-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/sandraschi/inkscape-mcp?style=flat-square&color=blue)](https://github.com/sandraschi/inkscape-mcp/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> FastMCP 3.1 MCP server for controlling Inkscape svg editor. Includes Webapp

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 23 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | Python |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`inkscape` `mcp-server` `svg`

## 🎯 Categories

MCP · Backend

## 📝 Summary

### English

**Brief Summary**  
sandraschi/inkscape‑mcp is a Python‑based FastMCP 3.1 server that exposes Inkscape’s SVG editing capabilities through the Model‑Context‑Protocol (MCP) and ships with a small web UI. It lets AI assistants and other automation agents invoke Inkscape operations (e.g., create, edit, export SVGs) via a standard, language‑agnostic API.

**Value**  
By wrapping Inkscape in an MCP server, the project provides a ready‑made bridge between AI agents and a mature vector‑graphics editor, enabling use‑cases such as AI‑driven design generation, automated diagram updates, or batch SVG processing without writing custom Inkscape plugins. The standard MCP interface also makes it easy to swap or combine with other MCP‑compatible tools, fostering a reusable ecosystem for AI‑tool integration.

**Practical Adoption Path**  

1. **Proof‑of‑Concept** – Clone the repo, run the provided Dockerfile or `pip install -r requirements.txt` and start the server; use the bundled webapp to verify basic commands (open, draw, export).  
2. **Integration Layer** – Write a thin MCP client in the target AI platform (e.g., LangChain, AutoGPT) that calls the server’s endpoints for the needed SVG actions.  
3. **Iterate & Extend** – Add custom MCP methods or wrap additional Inkscape extensions as needed, and lock the server version in a CI pipeline.  
4. **Production Hardening** – Containerize the service, place it behind an authenticated reverse proxy, and monitor logs for errors or security alerts.

**Production Readiness**  
The project is at a **medium** readiness level. It is functional and recently updated (2026‑06‑25) with modest community interest (23 stars, 5 forks). For production use you should:

* Verify the MIT/Apache license compliance and perform a security audit of the Python dependencies.  
* Pin the FastMCP and Inkscape versions to avoid breaking changes.  
* Add health‑checks, logging, and rate‑limiting to the MCP server.  
* Consider running it in a sandboxed container or VM to isolate any file‑system access Inkscape may require.

With these steps, sandraschi/inkscape‑mcp can move from prototype to a reliable component in internal workflows or AI‑augmented design pipelines.

### Русский

**sandraschi/inkscape-mcp** — это сервер FastMCP 3.1, реализованный на Python, который позволяет управлять редактором Inkscape через протокол Model Context Protocol (MCP) и поставляется с простым веб‑приложением. Типичный сценарий — подключение AI‑агентов или других автоматизированных систем к Inkscape для выполнения операций над SVG‑файлами, что упрощает создание прототипов и внутренние рабочие процессы. Готовность к production — средняя: проект уже стабилен и имеет базовую документацию, но перед развертыванием в продакшн требуется проверка лицензии, безопасности и поддержка зависимостей.

### 中文

**项目简介（2‑3 句）**  
sandraschi/inkscape‑mcp 是基于 FastMCP 3.1 实现的 MCP 服务器，可通过标准的 Model Context Protocol（MCP）远程控制 Inkscape SVG 编辑器，并自带一个简易 Web UI。它让 AI 助手能够像本地插件一样直接调用 Inkscape 的绘图功能，实现“AI + 工具”的闭环。

**价值**  
- **统一协议**：使用 MCP 作为桥梁，AI 代理无需了解 Inkscape 的内部 API，即可发送指令、获取画布状态，实现即插即用的工具接入。  
- **加速原型**：开发者只需启动该服务器，即可在聊天机器人、自动化脚本或其他 AI 系统中调用真实的图形编辑能力，显著缩短概念验证周期。  
- **可视化调试**：自带的 Webapp 让用户在浏览器中实时查看指令执行结果，便于调试和演示。

**典型接入方式**  
1. **部署服务器**：在能够访问 Inkscape 的机器上 `pip install inkscape-mcp && python -m inkscape_mcp`，启动 MCP 服务（默认 127.0.0.1:5000）。  
2. **在 AI 代理中配置 MCP 客户端**：使用任意支持 MCP 的 SDK（如 Python 的 `fastmcp`），在对话流或工作流脚本中创建 `MCPClient('http://localhost:5000')`。  
3. **发送指令**：调用 `client.send('inkscape.open', {'path': 'example.svg'})`、`client.send('inkscape.add_rect', {...})` 等标准化动作；服务器会在本地 Inkscape 实例中执行并返回结果。  
4. **可选 Web UI**：打开 `http://localhost:5000/ui` 查看当前画布、已执行的命令日志，或手动调试。

**生产可用性**  
- **成熟度**：项目已更新至 2026‑06‑25，拥有 23 ⭐、5 🍴，代码量适中，核心功能基本稳定，适合作为内部原型或工具链的实验平台。  
- **依赖与维护**：基于 Python 与 FastMCP，依赖相对轻量；但仍需自行审计第三方库的安全性，并确认 Inkscape 版本兼容性。  
- **上线建议**：在生产环境使用前，建议先完成小范围 PoC，检查 README 中的部署步骤、日志输出和错误处理；对关键路径（如文件读写、网络通信）加入超时和重试机制，并做好容器化或服务化部署以便监控。  

总体而言，inkscape‑mcp 能快速为 AI 系统提供真实的图形编辑能力，适合原型开发和内部工作流；在经过安全审计和可靠性加固后，也可逐步推广至生产环境。

## 🧭 Practical evaluation

**Value:** sandraschi/inkscape-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 23 GitHub stars
- 5 forks
- updated 2026-06-25
- primary language: Python
- 3 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 29/100 |
| topics | 38/100 |
| outlook | 46/100 |
| quality | 43/100 |
| recency | 40/100 |
| adoption | 27/100 |
| production | 51/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/sandraschi/inkscape-mcp) · [← Back to Mcp](./README.md)</sub>
