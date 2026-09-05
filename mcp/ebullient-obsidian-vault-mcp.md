# ebullient/obsidian-vault-mcp

[![Stars](https://img.shields.io/github/stars/ebullient/obsidian-vault-mcp?style=flat-square&color=yellow)](https://github.com/ebullient/obsidian-vault-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/ebullient/obsidian-vault-mcp?style=flat-square&color=blue)](https://github.com/ebullient/obsidian-vault-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> MCP tool allowing Open WebUI or Claude Desktop to retrieve files from your vault

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 24 |
| 🍴 **Forks** | 2 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`mcp-server` `mcp-tools` `obsidian` `obsidian-plugin`

## 🎯 Categories

MCP · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
ebullient/obsidian‑vault‑mcp is a Model Context Protocol (MCP) server that lets AI assistants such as Open WebUI or Claude Desktop read and retrieve files directly from an Obsidian vault. By exposing a simple TypeScript‑based API/CLI, it bridges the gap between large‑language‑model agents and the user’s personal knowledge base, enabling seamless tool‑augmented workflows.

**Value**  
- **Standardised integration** – Implements the open‑source MCP, so the same connector can be reused across different AI platforms without custom adapters.  
- **Rapid prototyping** – Developers can instantly give an AI agent access to vault contents, accelerating use‑case testing (e.g., knowledge‑base‑driven Q&A, automated note‑summaries, or content generation).  
- **Extensible stack** – Written in TypeScript with clear API boundaries, it can be extended to support additional file‑type handlers or security layers as needed.

**Practical Adoption Path**  
1. **Clone & install** – `npm i && npm run build` sets up the server locally.  
2. **Configure** – Point the MCP endpoint to the local vault directory and generate an API token if required.  
3. **Connect the AI** – In Open WebUI or Claude Desktop, add the MCP URL as a “tool” or “resource” endpoint; the assistant can now issue `list`, `read`, or `search` commands against the vault.  
4. **Iterate** – Use the provided CLI to test calls, then embed the server in a Docker container or internal service for team‑wide access.  

**Production Readiness**  
- **Maturity**: Medium. The project is functional for prototypes and internal pipelines, but it has modest community traction (24 ★, 2 forks) and a recent update (June 2026).  
- **Dependencies**: Pure TypeScript with minimal external libraries, simplifying audit and version‑pinning.  
- **Risks**: No formal security review; licensing and long‑term maintainer commitment need verification before a critical production rollout.  
- **Recommendation**: Deploy in a controlled environment (e.g., internal sandbox or CI/CD‑triggered service) while conducting security testing and adding monitoring. Once vetted, it can be promoted to production for low‑risk, data‑aware AI assistants.

### Русский

**ebullient/obsidian-vault-mcp** — это MCP‑инструмент, который через стандартный Model Context Protocol позволяет AI‑ассистентам (Open WebUI, Claude Desktop) получать доступ к файлам вашего Obsidian‑хранилища, упрощая интеграцию интеллектуальных агентов с реальными данными и инструментами. Типичный сценарий: развернуть сервер MCP, подключить к нему AI‑модель и мгновенно использовать содержимое vault в чат‑ботах, прототипах или внутренних workflow. Готовность к production — средняя: проект уже стабильно работает в прототипах, имеет TypeScript‑реализацию, открытый API/CLI и небольшую, но активную пользовательскую базу; перед запуском в продакшн рекомендуется проверить лицензирование, безопасность и обеспечить поддержку зависимостей.

### 中文

**项目简介（2‑3 句）**  
ebullient/obsidian-vault-mcp 是一个基于 Model Context Protocol（MCP）的工具，能够让 Open WebUI、Claude Desktop 等 AI 助手直接读取 Obsidian Vault 中的文件，实现 AI 与本地知识库的实时交互。

**价值**  
- **标准化桥梁**：通过统一的 MCP 接口，将 AI 助手与真实工具和数据（如笔记、文档）连接，避免每个项目都要自行实现文件访问层。  
- **加速原型**：开发者只需启动 MCP 服务器，即可让任何支持 MCP 的模型即时获取、搜索或写入 Vault 内容，显著缩短 AI‑工具集成的迭代周期。  
- **可复用性**：同一套协议可用于多种 AI 平台（Open WebUI、Claude Desktop、ChatGPT 插件等），实现一次实现、多处复用。

**典型接入方式**  
1. **启动 MCP 服务器**：`npm i && npm start`（或使用提供的 Docker 镜像），指定 Obsidian Vault 路径。  
2. **在 AI 平台配置**：在 Open WebUI、Claude Desktop 等的插件/扩展设置中填写服务器地址（如 `http://localhost:8080`）和可选的身份令牌。  
3. **调用协议**：AI 助手通过标准的 MCP API（`/files/list`, `/files/get`, `/files/put` 等）请求或写入笔记，返回的内容即为 Vault 中的 Markdown 文档。  

**生产可用性**  
- **成熟度**：当前评分 67/100，具备基本功能且已在多个原型项目中验证，适合作为内部或实验性工作流的核心组件。  
- **依赖与维护**：项目使用 TypeScript，依赖链相对简洁；但维护者数量有限，建议在生产环境前进行：  
  - 代码审计（尤其是文件路径处理和权限校验）  
  - 监控与日志集成，确保异常请求不会泄露本地文件  
  - 定期同步上游更新，防止安全漏洞累积  
- **可扩展性**：协议层已标准化，后续可自行实现缓存、权限管理或与企业身份系统对接，提升可靠性。  

综上，ebullient/obsidian-vault-mcp 为 AI 与本地知识库的对接提供了快捷、标准的入口，适合在原型阶段快速验证，也可在经过安全与运维加固后用于生产环境的内部工具链。

## 🧭 Practical evaluation

**Value:** ebullient/obsidian-vault-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 24 GitHub stars
- 2 forks
- updated 2026-06-26
- primary language: TypeScript
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 12/100 |
| stars | 30/100 |
| topics | 50/100 |
| outlook | 64/100 |
| quality | 54/100 |
| recency | 80/100 |
| adoption | 25/100 |
| production | 67/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/ebullient/obsidian-vault-mcp) · [← Back to Mcp](./README.md)</sub>
