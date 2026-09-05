# Doist/todoist-mcp

[![Stars](https://img.shields.io/github/stars/Doist/todoist-mcp?style=flat-square&color=yellow)](https://github.com/Doist/todoist-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/Doist/todoist-mcp?style=flat-square&color=blue)](https://github.com/Doist/todoist-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> A set of tools to connect to AI agents, to allow them to use Todoist on a user's behalf. Includes MCP support.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 478 |
| 🍴 **Forks** | 44 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

MCP

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Doist’s **todoist‑mcp** is a TypeScript library that implements the Model Context Protocol (MCP) to let AI agents interact with a user’s Todoist account—creating, updating, and querying tasks on their behalf. By exposing Todoist’s functionality through a standard MCP interface, developers can rapidly prototype AI‑driven productivity assistants or integrate Todoist into larger AI‑centric workflows.  

**Value**  
- **Standardized AI‑to‑tool bridge** – MCP provides a common contract for AI agents, so the same integration code can be reused across different models or platforms.  
- **Accelerates AI assistant development** – Instead of writing bespoke Todoist APIs for each assistant, developers plug the MCP server into their stack and immediately gain full task‑management capabilities.  
- **Open‑source community backing** – With ~480 stars and active recent commits, the project already enjoys a modest community that can help troubleshoot and extend the integration.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the provided Docker/Node example, and verify that a simple prompt can add a task to a test Todoist account.  
2. **Read‑me & MCP contract review** – Ensure the MCP schema matches your internal data model and adjust the mapping layer if needed.  
3. **Secure credential handling** – Store the Todoist API token in a secret manager (e.g., Vault, AWS Secrets Manager) and configure the MCP server to load it at runtime.  
4. **Iterative feature addition** – Start with core CRUD operations, then expand to task comments, labels, or project queries as the AI use case matures.  
5. **Production hardening** – Add logging, rate‑limit handling, and automated tests around the MCP endpoints before rolling out to production.  

**Production Readiness**  
- **Maturity:** Medium. The library is functional and actively maintained (last update 2026‑05‑14) but has not been battle‑tested at large scale.  
- **Suitability:** Ideal for prototypes, internal tools, or early‑stage AI assistants; production deployments should include additional safeguards (dependency audits, security scanning, monitoring).  
- **Risks to address:** Verify the MIT‑style license compatibility, conduct a security review of the MCP server (exposed endpoints, token handling), and confirm that maintainers are responsive for critical bug fixes.  

Overall, **todoist‑mcp** offers a low‑friction way to bring Todoist into AI‑driven workflows, with a clear path from a quick sandbox test to a hardened production service.

### Русский

Doist/todoist-mcp — это набор TypeScript‑утилит, реализующих Model Context Protocol (MCP) и позволяющих AI‑ассистентам напрямую работать с Todoist от имени пользователя. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept сервера MCP, подключение к нему AI‑модели и проверка интеграции через README; при положительных результатах проект можно масштабировать до внутренних или клиентских сервисов. Готовность к production оценивается как средняя: проект стабилен и активно поддерживается (478 звёзд, обновление 2026‑05‑14), но перед выпуском в продакшн требуется проверка лицензии, безопасности и зависимости.

### 中文

**项目简介**  
Doist/todoist‑mcp 是一套基于 Model Context Protocol（MCP）的工具库，帮助 AI 代理在用户授权下直接操作 Todoist（创建、更新、查询任务等），从而让语言模型能够使用真实的生产力数据。  

**价值**  
- **标准化接入**：通过 MCP 统一协议，将 AI 助手与 Todoist 以及其他类似服务以相同的方式对接，降低了多平台集成的复杂度。  
- **加速原型**：开发者只需几行代码即可让 ChatGPT、Claude 等模型完成日程管理、任务分配等实际业务场景，显著缩短产品验证周期。  
- **可复用的服务端**：提供可直接部署的 MCP 服务器，实现“模型即服务”，便于内部或第三方 AI 产品快速获取 Todoist 能力。  

**典型接入方式**  
1. **准备环境**：克隆仓库，使用 `npm install` 安装依赖（TypeScript）。  
2. **配置凭证**：在 `.env` 中填入 Todoist API Token 与 MCP 服务器的密钥/URL。  
3. **启动 MCP 服务器**：`npm run start`（或 `docker compose up`）启动符合 MCP 规范的 HTTP/WS 服务。  
4. **在 AI 模型侧注册**：在模型的工具列表中声明 `todoist` 工具，指向上述服务器的 endpoint。  
5. **调用示例**：模型在对话中发送 `create_task`、`list_tasks` 等标准化 JSON 请求，服务器转化为 Todoist API 调用并返回结果。  

**生产可用性**  
- **成熟度**：当前得分 72/100，拥有 478+ 星、44+ Fork，活跃维护至 2026‑05‑14，适合作为原型或内部工作流的核心组件。  
- **准备度**：依赖主要是 TypeScript 与 Node.js，易于容器化部署；但在正式生产环境前，需要完成：  
  - **安全审计**：确认依赖库无已知漏洞，审查 API Token 的存储与访问控制。  
  - **许可证合规**：检查项目使用的 MIT/Apache 等许可证是否与贵公司政策匹配。  
  - **运维监控**：为 MCP 服务器添加日志、健康检查与限流，防止滥用。  
- **结论**：在完成上述审查后，可作为生产级别的 Todoist 接口服务使用，尤其适合需要让 AI 助手直接操作用户任务的 SaaS 产品或企业内部自动化平台。

## 🧭 Practical evaluation

**Value:** Doist/todoist-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 478 GitHub stars
- 44 forks
- updated 2026-05-14
- primary language: TypeScript

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 57/100 |
| topics | 0/100 |
| outlook | 69/100 |
| quality | 59/100 |
| recency | 80/100 |
| adoption | 53/100 |
| production | 66/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/Doist/todoist-mcp) · [← Back to Mcp](./README.md)</sub>
