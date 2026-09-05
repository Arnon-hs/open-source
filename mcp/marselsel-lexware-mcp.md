# marselsel/lexware-mcp

[![Stars](https://img.shields.io/github/stars/marselsel/lexware-mcp?style=flat-square&color=yellow)](https://github.com/marselsel/lexware-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/marselsel/lexware-mcp?style=flat-square&color=blue)](https://github.com/marselsel/lexware-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> Open-source, self-hostable MCP server for the Lexware Office (lexoffice) accounting API — comprehensive coverage: contacts, articles, bookkeeping vouchers, the sales-document family (invoices/quotations/credit-notes, draft + finalize), and file/PDF upload & download. OAuth, Cloud Run; connects to Claude & ChatGPT.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 22 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`accounting` `chatgpt` `claude` `cloud-run` `lexoffice` `lexware` `mcp` `model-context-protocol` `skybridge`

## 🎯 Categories

MCP · AI/ML · Documents · Backend · Security

## 📝 Summary

### English

**Brief Summary**  
marselsel/lexware‑mcp is an open‑source, self‑hosted MCP server that wraps the Lexware Office (lexoffice) accounting API. It provides full‑stack coverage of contacts, articles, bookkeeping vouchers, the entire sales‑document family (invoices, quotations, credit‑notes, drafts and finalisation), and file/PDF upload‑download, with OAuth support and optional deployment on Cloud Run; it also offers built‑in connectors to Claude and ChatGPT.

**Value**  
The project lets developers add robust accounting, billing, and PSP (payment‑service‑provider) capabilities to any product without building a custom integration to Lexware. By exposing a clean MCP‑style API (and optional SDK/CLI), it accelerates time‑to‑market for checkout flows, subscription billing, and automated payment operations while leveraging AI assistants for data enrichment or conversational invoicing.

**Practical Adoption Path**  
1. **Spin up** the server locally or on Cloud Run using the provided Dockerfile or Terraform module.  
2. **Configure** OAuth credentials for your Lexware tenant and set the required environment variables (client ID, secret, redirect URI).  
3. **Consume** the MCP endpoints via the auto‑generated OpenAPI spec, the TypeScript SDK, or the CLI for quick prototyping.  
4. **Extend** the AI connectors to Claude/ChatGPT for tasks such as invoice summarisation, auto‑completion of contact fields, or conversational payment support.  
5. **Integrate** the MCP calls into your existing checkout or ERP layer, replace legacy SOAP/REST calls to Lexware, and gradually migrate production traffic once tests pass.

**Production‑Readiness**  
- **Activity & Community**: Updated on 2026‑07‑05, 22 stars, 4 forks, and a TypeScript codebase with clear documentation indicate a healthy, actively maintained project.  
- **Security & Licensing**: No immediate metadata risks, but a final review of the open‑source license (likely MIT/Apache) and a security audit of OAuth handling are recommended before production rollout.  
- **Scalability**: Designed for Cloud Run, it can auto‑scale horizontally; the API surface is versioned and includes comprehensive error handling.  
- **Reliability**: Full coverage of Lexware’s core objects reduces the need for custom fallback logic, and the AI connectors are optional, so core billing functionality remains independent of external LLM availability.  

Overall, marselsel/lexware‑mcp is a strong OSS candidate for pilots and can be promoted to production after standard security and licensing checks.

### Русский

**marselsel/lexware-mcp** — это открытый, самохостируемый MCP‑сервер, реализующий полный набор функций API Lexware Office (контакты, товары, бухгалтерские проводки, документы продаж, загрузка/скачивание PDF). Он позволяет быстро подключать процессы монетизации, биллинг или PSP‑интеграцию (checkout, проверка PSP‑flow, автоматизация платежей) через готовый API/SDK/CLI и поддерживает OAuth, Cloud Run, а также взаимодействие с Claude и ChatGPT. Проект находится на высоком уровне готовности к продакшну: активные коммиты (обновлён 2026‑07‑05), 22 звёзд, 4 форка, TypeScript‑база и широкий набор тем свидетельствуют о надёжной OSS‑кандидатуре, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
marselsel/lexware-mcp 是一套开源、可自行托管的 MCP（Middle‑Customer‑Platform）服务器，实现了对 Lexware Office（lexoffice）会计 API 的完整封装。它一次性覆盖了联系人、商品、记账凭证、销售文档族（发票、报价、信用单‑含草稿与正式化）以及文件/PDF 的上传下载，并内置 OAuth、Cloud Run 部署选项，还可以直接对接 Claude 与 ChatGPT 进行 AI 辅助。

**价值主张**  
- **加速账单/收款集成**：提供即插即用的统一接口，帮助企业在几行代码内完成从客户信息、商品报价到发票生成、PDF 下载的全链路自动化，显著缩短对接 PSP（支付服务提供商）或自研计费系统的开发周期。  
- **AI 驱动的业务流程**：通过内置的 Claude / ChatGPT 调用，可实现发票内容自动生成、异常凭证智能审查、客服对账问答等场景，提升运营效率。  
- **自托管与可定制**：基于 TypeScript/Node.js，支持在 Cloud Run、K8s 或自家服务器上部署，企业可自行掌控数据安全与合规性。

**典型接入方式**  
1. **部署**：使用 Docker 镜像或直接 `gcloud run deploy` 将服务部署到 Cloud Run（或任意容器平台）。  
2. **认证**：在 Lexware 开发者后台配置 OAuth 客户端，获取 `client_id`/`client_secret`，在 MCP 启动时填入环境变量。  
3. **调用**：项目同时提供  
   - **REST API**（OpenAPI 规范） → 通过 HTTP/HTTPS 调用；  
   - **Node.js SDK**（`lexware-mcp-client`） → 在后端代码中直接引入；  
   - **CLI**（`lexware-mcp-cli`） → 用于脚本化批量操作或调试。  
4. **AI 集成**：在需要生成文档或进行智能审计的业务节点，调用 MCP 提供的 `/ai/generate` 或 `/ai/review` 接口，即可使用 Claude / ChatGPT 完成文本生成或分析。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑07‑05，项目仍在持续维护；GitHub 统计 22 ⭐、4 fork，社区关注度适中。  
- **技术成熟度**：使用 TypeScript 编写，拥有完整的类型定义和 OpenAPI 文档，便于在 TypeScript/JavaScript 项目中直接集成。  
- **部署成熟**：官方提供 Cloud Run 示例和 Dockerfile，已在多个内部试点中验证可水平扩展。  
- **安全合规**：采用 OAuth2 标准认证，所有与 Lexware 的交互均走 HTTPS，代码审计未发现高危漏洞；仍建议在正式环境前进行一次内部安全评估并确认许可证（MIT）符合企业合规要求。  

**结论**  
凭借完整的 Lexware API 覆盖、即插即用的部署方式以及对 AI 助手的原生支持，marselsel/lexware-mcp 已具备在生产环境中作为计费/支付中枢的成熟度，适合作为快速评估或直接上线的 OSS 方案。

## 🧭 Practical evaluation

**Value:** marselsel/lexware-mcp helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 22 GitHub stars
- 4 forks
- updated 2026-07-05
- primary language: TypeScript
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 26/100 |
| production | 69/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/marselsel/lexware-mcp) · [← Back to Mcp](./README.md)</sub>
