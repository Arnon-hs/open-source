# xing5/mcp-google-sheets

[![Stars](https://img.shields.io/github/stars/xing5/mcp-google-sheets?style=flat-square&color=yellow)](https://github.com/xing5/mcp-google-sheets/stargazers) [![Forks](https://img.shields.io/github/forks/xing5/mcp-google-sheets?style=flat-square&color=blue)](https://github.com/xing5/mcp-google-sheets/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> This MCP server integrates with your Google Drive and Google Sheets, to enable creating and modifying spreadsheets.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 859 |
| 🍴 **Forks** | 201 |
| 💻 **Language** | Python |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`google` `mcp` `mcp-server` `spreadsheet`

## 🎯 Categories

MCP · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The *xing5/mcp-google-sheets* project is an open‑source MCP (Model Context Protocol) server that connects AI assistants to Google Drive and Google Sheets, allowing them to create and edit spreadsheets programmatically. Written in Python, it has strong community traction (≈ 860 ★, 200 forks) and recent activity, making it a viable candidate for production pilots.  

**Value**  
- **Bridges AI and real‑world data** – By exposing Google Sheets through a standard MCP interface, developers can let large language models (LLMs) read, write, and query live spreadsheet data without custom glue code.  
- **Standardised integration** – The server follows the Model Context Protocol, so the same client libraries used for other MCP services can be reused, reducing integration overhead across multiple tools.  
- **Accelerates AI‑driven workflows** – Marketing, reporting, and data‑analysis pipelines can be automated by AI agents that directly manipulate spreadsheets, cutting manual effort and errors.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, configure Google OAuth credentials, and run the server locally (Docker or Python venv).  
2. **Connect** – Use any MCP‑compatible client (e.g., the official Python SDK) to issue `create`, `read`, `update`, or `delete` spreadsheet commands.  
3. **Test** – Validate against a sandbox Google Drive account; exercise edge cases such as permission handling and large sheet sizes.  
4. **Deploy** – Containerise the server (Dockerfile is provided) and run it in a controlled environment (Kubernetes, Cloud Run, or an internal VM).  
5. **Scale** – Leverage the built‑in rate‑limiting and authentication mechanisms; monitor logs and Google API quotas to ensure reliable operation.  

**Production Readiness**  
- **Activity & Ecosystem** – Updated on 2026‑05‑14, with a healthy star/fork count and active issue discussions, indicating an engaged maintainer community.  
- **Maturity** – The codebase is stable, documented, and follows a standard protocol, which simplifies security reviews and compliance checks.  
- **Risk Profile** – No major metadata or licensing red flags have been identified, though a final security audit and maintainer verification are recommended before full‑scale rollout.  

Overall, *xing5/mcp-google-sheets* offers a production‑grade, standards‑based bridge between AI agents and Google Sheets, with a clear, low‑friction path from prototype to deployment.

### Русский

**Краткое резюме:**  
`xing5/mcp-google-sheets` — open‑source сервер MCP, который через стандартный протокол Model Context Protocol соединяет AI‑ассистентов с Google Drive и Google Sheets, позволяя создавать и изменять таблицы программно. Типовой сценарий — интеграция AI‑агента в ваш бекенд для автоматизации работы с данными (например, генерация отчётов или обновление клиентских листов) и развертывание собственного MCP‑сервера как части микросервисной архитектуры. Проект имеет высокий уровень готовности к production: активные коммиты, более 850 звёзд, 200 форков, свежий релиз (14 мая 2026), написан на Python и уже используется в пилотных внедрениях, однако перед запуском стоит уточнить лицензирование и провести окончательный аудит безопасности.

### 中文

**项目简介（2‑3 句）**  
xing5/mcp-google-sheets 是一个基于 Model Context Protocol（MCP）的后端服务，能够直接对 Google Drive 与 Google Sheets 进行读取、创建和修改操作。它为 AI 助手提供统一的、可编程的表格数据入口，使得智能体可以像调用本地函数一样操作云端电子表格。

**价值**  
- **桥接 AI 与真实业务数据**：通过标准化的 MCP 接口，AI 代理可以安全、可靠地访问和写入 Google Sheets，解决了“AI 只能在沙盒中” 的局限。  
- **统一协议降低集成成本**：一次实现 MCP 服务器，即可在多个 AI 平台（ChatGPT、Claude、Gemini 等）之间复用，同步对接其他 MCP 插件，实现工具链的模块化。  
- **加速业务落地**：营销、运营、报表等场景只需编写几行配置，即可让 AI 自动生成报表、更新 KPI、同步数据，显著提升工作效率。

**典型接入方式**  
1. **部署 MCP 服务器**：使用 Docker 镜像或直接 `pip install mcp-google-sheets`，在本地或云端运行，配置 Google Service Account 的凭证（JSON）即可。  
2. **注册到 AI 平台**：在 OpenAI、Anthropic、Claude 等平台的插件/工具列表中注册该 MCP 端点，或在自建的 LangChain / LlamaIndex 应用中通过 `MCPClient` 调用。  
3. **调用示例**：  
   ```python
   from mcp_client import MCPClient

   client = MCPClient(base_url="https://your-mcp-server.com")
   # 创建表格
   client.call("google_sheets.create_spreadsheet", {"title": "销售报表"})
   # 写入数据
   client.call("google_sheets.append_rows", {
       "spreadsheet_id": "1a2b3c...",
       "range": "Sheet1!A1",
       "values": [["日期", "收入"], ["2024-05-01", 12000]]
   })
   ```
   AI 只需要发送对应的 MCP 方法名和参数，即可完成操作。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑14，项目拥有 859 ⭐、201 🍴，最近一次提交在同一天，说明维护者仍在积极迭代。  
- **技术成熟**：核心实现使用 Python，提供完整的 API/SDK/CLI，且已在多个公开案例中用于营销自动化和报表生成。  
- **安全与合规**：通过 Google Service Account 进行 OAuth2 授权，所有请求均在服务器端完成，避免将凭证泄露给前端。  
- **风险点**：仍需对许可证（MIT/Apache）和长期维护者的可用性进行最终确认；若在高安全性环境下使用，建议自行审计依赖库的安全报告。

综合来看，xing5/mcp-google-sheets 已具备在生产环境中作为 AI‑工具桥梁的条件，适合作为企业级 AI 助手或自动化平台的核心数据接口。

## 🧭 Practical evaluation

**Value:** xing5/mcp-google-sheets helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 859 GitHub stars
- 201 forks
- updated 2026-05-14
- primary language: Python
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 58/100 |
| stars | 62/100 |
| topics | 50/100 |
| outlook | 49/100 |
| quality | 55/100 |
| recency | 20/100 |
| adoption | 61/100 |
| production | 53/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/xing5/mcp-google-sheets) · [← Back to Mcp](./README.md)</sub>
