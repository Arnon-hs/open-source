# harumiWeb/exstruct

[![Stars](https://img.shields.io/github/stars/harumiWeb/exstruct?style=flat-square&color=yellow)](https://github.com/harumiWeb/exstruct/stargazers) [![Forks](https://img.shields.io/github/forks/harumiWeb/exstruct?style=flat-square&color=blue)](https://github.com/harumiWeb/exstruct/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-81%2F100-brightgreen?style=flat-square)](#)

> Conversion from Excel to structured JSON (tables, shapes, charts) for LLM/RAG pipelines, and autonomous Excel reading/writing by AI agents via CLI and MCP integration.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 143 |
| 🍴 **Forks** | 22 |
| 💻 **Language** | Python |
| 📈 **Score** | 81/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

`data-ex` `document-ai` `excel` `excel-automation` `excel-parsing` `llm` `mcp-server` `python-library` `rag` `skills` `structured-data` `xlwings`

## 🎯 Categories

MCP · Knowledge/RAG · Automation · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
harumiWeb/exstruct is an open‑source Python toolkit that converts Excel workbooks into a richly structured JSON format—including tables, shapes, and charts—so large‑language‑model (LLM) and Retrieval‑Augmented Generation (RAG) pipelines can ingest spreadsheet data directly. It also provides a command‑line interface and Model Context Protocol (MCP) integration that let autonomous AI agents read from and write to Excel files, enabling end‑to‑end tool use without custom scripting.

**Value**  
- **Bridges the data gap**: By turning the ubiquitous Excel format into machine‑readable JSON, exstruct eliminates the tedious, error‑prone step of manually extracting spreadsheet content for LLMs.  
- **Standardised AI‑tool interaction**: The MCP‑compatible API/CLI gives AI agents a uniform protocol for invoking Excel operations, making it easy to plug the library into any agent framework or RAG system.  
- **Accelerates AI‑augmented workflows**: Teams can quickly build assistants that generate reports, update dashboards, or perform data‑driven calculations directly in Excel, reducing development time and increasing reliability.

**Practical Adoption Path**  
1. **Prototype** – Install the Python package (`pip install exstruct`), run the CLI on a sample workbook, and inspect the generated JSON to verify that the needed structures (tables, charts, shapes) are captured.  
2. **Integrate** – Wrap the CLI or import the SDK in your existing LLM/RAG pipeline; feed the JSON into prompt templates or vector stores, and use the MCP endpoint to let the model request updates back to the Excel file.  
3. **Test & Harden** – Add unit tests around the conversion and round‑trip write‑back, configure authentication or sandboxing for the MCP server, and evaluate latency on typical workbook sizes.  
4. **Deploy** – Deploy the MCP server as a container (Docker/K8s) alongside your AI service, expose only the required endpoints, and monitor logs for conversion errors or security alerts.

**Production Readiness**  
- **Activity & Community**: 143 stars, 22 forks, recent commits (as of 2026‑05‑14), and a healthy set of topics indicate an active project.  
- **Maturity**: The library already ships a stable CLI, an API, and MCP support, which are the core primitives needed for production use.  
- **Risk Considerations**: No glaring metadata or licensing issues have been found, but a final review of the open‑source license, dependency security (e.g., CVEs in pandas/openpyxl), and maintainer responsiveness is advisable before a large‑scale rollout.  

Overall, exstruct is a high‑readiness OSS candidate for teams that need reliable, programmatic access to Excel data within LLM‑driven applications, offering a clear integration path from prototype to production.

### Русский

**harumiWeb/exstruct** – это Python‑библиотека и CLI, преобразующая Excel‑файлы в структурированный JSON (таблицы, графики, формы) и позволяющая AI‑агентам автономно читать и писать Excel через Model Context Protocol (MCP). Типичный сценарий: интеграция LLM/RAG пайплайна с реальными данными и инструментами, где агент запрашивает exstruct через API/SDK, получает готовый JSON‑контекст или модифицирует файл, а затем передаёт результат обратно в бизнес‑процесс. Проект имеет высокий уровень готовности к production: активные коммиты, 143★, 22 форка, поддержка MCP, CLI и SDK, а также широкое покрытие тем, что делает его надёжным кандидатом для пилотных и масштабных внедрений.

### 中文

**项目简介**  
harumiWeb/exstruct 是一款开源工具，能够将 Excel 文件转换为结构化的 JSON（包括表格、形状、图表），并通过 CLI 与 MCP（Model Context Protocol）实现 AI 代理的自动化读写。它为 LLM/RAG 流程提供统一的数据接口，让 AI 助手能够直接操作真实的 Excel 文档。

**价值**  
- **标准化桥梁**：通过统一的 JSON 协议，把 Excel 这一常见业务数据源接入 LLM/RAG，消除格式碎片化问题。  
- **AI‑to‑Tool 能力**：AI 代理可在命令行或 MCP 服务中直接读取、编辑 Excel，支持自动化报表生成、数据清洗等场景。  
- **快速落地**：提供 API、SDK 与 CLI 三种接入方式，降低集成成本，适配多种语言与部署环境。

**典型接入方式**  
1. **CLI**：在脚本或 CI/CD 流水线中直接调用 `exstruct` 命令，将 Excel → JSON 或 JSON → Excel。  
2. **Python SDK**：在 AI 代理的代码中 `import exstruct`，调用 `load_excel()`、`dump_json()` 等函数，实现内嵌式读写。  
3. **MCP 服务**：部署为 Model Context Protocol 服务器，AI 大模型通过标准化的 HTTP/WS 接口发送文件路径或二进制，获取结构化 JSON，或提交 JSON 完成写回。

**生产可用性**  
- **活跃度**：截至 2026‑05‑14 最近一次提交，星标 143、Fork 22，社区活跃。  
- **技术成熟度**：核心使用 Python 实现，代码结构清晰，已覆盖表格、形状、图表等常见 Excel 元素。  
- **生态兼容**：提供完整的 API 文档、CLI 示例以及 MCP 接口说明，易于在现有 LLM/RAG 平台上集成。  
- **风险点**：仍需对许可证（MIT）进行合规确认，安全审计（依赖的 `openpyxl`、`pandas` 等库）以及维护者的长期可用性做进一步评估。

综合来看，harumiWeb/exstruct 已具备高可用的生产级特征，适合作为 AI 助手与 Excel 工具链之间的标准化桥接层进行试点乃至正式上线。

## 🧭 Practical evaluation

**Value:** harumiWeb/exstruct helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 143 GitHub stars
- 22 forks
- updated 2026-05-14
- primary language: Python
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 46/100 |
| topics | 100/100 |
| outlook | 86/100 |
| quality | 74/100 |
| recency | 100/100 |
| adoption | 43/100 |
| production | 79/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/harumiWeb/exstruct) · [← Back to Mcp](./README.md)</sub>
