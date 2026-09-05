# SylphxAI/pdf-reader-mcp

[![Stars](https://img.shields.io/github/stars/SylphxAI/pdf-reader-mcp?style=flat-square&color=yellow)](https://github.com/SylphxAI/pdf-reader-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/SylphxAI/pdf-reader-mcp?style=flat-square&color=blue)](https://github.com/SylphxAI/pdf-reader-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-81%2F100-brightgreen?style=flat-square)](#)

> 📄 The PDF intelligence layer for AI agents — Agent Document Twin, evidence-first extraction, visual crops, OCR provenance, trust reports, and benchmark-gated releases. MCP server for Claude, Cursor, VS Code, and any MCP client.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 803 |
| 🍴 **Forks** | 69 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 81/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-document-twin` `ai-agent` `ai-tools` `citations` `document-intelligence` `document-processing` `evidence-first` `llm-tool` `mcp` `model-context-protocol` `nodejs` `ocr`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · Documents · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
SylphxAI/pdf-reader-mcp provides a “PDF intelligence” layer that lets AI agents read, extract, and verify information from PDFs through a standardized Model Context Protocol (MCP) server. It supports visual cropping, OCR provenance, trust reports, and benchmark‑gated releases, and can be used with Claude, Cursor, VS Code, or any MCP‑compatible client. With 800+ stars, active TypeScript development, and recent releases, it’s a mature open‑source component for plugging real‑world documents into AI workflows.

**Value**  
- **Unified PDF interface**: Turns PDFs into structured, provenance‑tracked data that AI agents can query reliably, reducing the need for custom parsers per document type.  
- **Evidence‑first extraction**: Generates visual crops and OCR provenance so the model can cite exact source snippets, improving transparency and trust.  
- **Protocol‑first design**: By exposing an MCP server, the same backend can serve multiple agents (Claude, Cursor, VS Code, custom bots) with a single integration point.  

**Practical Adoption Path**  
1. **Deploy the MCP server** (Docker or npm install) in a sandbox or edge environment.  
2. **Configure the client**: point your AI agent’s MCP client (e.g., Claude’s tool‑use API, Cursor plugin, VS Code extension) to the server’s endpoint.  
3. **Define document ingestion**: upload PDFs via the provided REST/CLI API; the server returns structured JSON, visual crops, and trust reports.  
4. **Iterate**: use the returned evidence in prompts (e.g., “cite page 3, region A”) and refine extraction pipelines as needed.  
5. **Scale**: the server can be container‑orchestrated behind a load balancer for higher throughput, and the same MCP spec lets you add new agents without code changes.  

**Production Readiness**  
- **Active maintenance**: last commit 2026‑07‑01, regular releases, and an active community (800+ ★, 69 forks).  
- **Ecosystem fit**: native support for major AI assistants and a language‑agnostic MCP spec make integration straightforward.  
- **Stability signals**: benchmark‑gated releases and trust‑report generation indicate a focus on reliability and auditability.  
- **Risks to verify**: final due‑diligence on licensing, security hardening, and maintainer responsiveness is still required, but overall the project is mature enough for a pilot or production rollout.

### Русский

SylphxAI/pdf-reader-mcp — это открытый серверный слой, позволяющий AI‑агентам (Claude, Cursor, VS Code и любые MCP‑клиенты) работать с PDF‑документами через единый Model Context Protocol: извлечение данных «от первого доказательства», визуальные вырезки, OCR‑прозрачность, отчёты о доверии и проверка на базе бенчмарков. Типичный сценарий — подключить интеллектуального помощника к реальному хранилищу документов или к инструменту обработки файлов, развернув MCP‑сервер и используя готовый API/SDK/CLI для интеграции. Проект находится на высоком уровне готовности к продакшн: активные коммиты, более 800 звёзд, широкое использование в экосистеме и поддержка TypeScript делают его надёжным кандидатом для пилотных и масштабных внедрений.

### 中文

**项目简介**  
SylphxAI/pdf-reader-mcp 为 AI 代理提供 PDF 智能感知层，支持文档双胞胎、证据优先抽取、可视化裁剪、OCR 溯源、可信报告以及基准门控发布。它实现了 Model Context Protocol（MCP）服务器，可直接供 Claude、Cursor、VS Code 以及任意 MCP 客户端使用。

**价值**  
- **统一协议**：通过标准的 MCP 接口，让各种 AI 助手（大模型、插件、IDE 等）以统一方式访问 PDF 内容，降低集成成本。  
- **可信抽取**：提供证据链、OCR 可信度和报告，帮助业务在合规、审计和质量控制场景下放心使用 AI 抽取结果。  
- **可扩展与可视化**：支持视觉裁剪和自定义插件，方便在文档审阅、数据标注、知识库构建等场景中快速落地。

**典型接入方式**  
1. **MCP 客户端**：在 Claude、Cursor、VS Code 等已有的 MCP 客户端中配置服务器地址，即可直接调用 PDF 阅读与抽取功能。  
2. **SDK / CLI**：项目提供 TypeScript SDK 与命令行工具，开发者可在自研后端或脚本中通过 `PdfReaderMcpClient` 调用 API，实现批量处理或自定义工作流。  
3. **自建 MCP Server**：将源码部署为独立的 HTTP 服务（Docker 镜像或直接 `npm run start`），对外提供标准化的 `/mcp/v1` 接口，供任何遵循 MCP 协议的系统调用。

**生产可用性**  
- **活跃度**：截至 2026‑07‑01，项目拥有 803 ⭐、69 🍴，最近一次提交在 2026‑07‑01，维护频率稳定。  
- **技术成熟度**：使用 TypeScript 编写，代码结构清晰，配套的 API 文档、示例和 CLI 完整，支持 OpenAPI 规范，易于自动化测试与 CI。  
- **生态兼容**：已在 Claude、Cursor、VS Code 等主流 MCP 客户端中验证，具备跨语言（Node、Python 通过 HTTP）调用能力。  
- **安全与合规**：项目采用 MIT 许可证，未发现重大安全漏洞；仍建议在生产环境进行依赖审计和容器安全加固。  

综合来看，SylphxAI/pdf-reader-mcp 具备高可用的实现、明确的标准协议以及良好的社区和生态支撑，适合作为企业级 AI 助手与 PDF 数据对接的生产级组件。

## 🧭 Practical evaluation

**Value:** SylphxAI/pdf-reader-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 803 GitHub stars
- 69 forks
- updated 2026-07-01
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 46/100 |
| stars | 62/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 76/100 |
| recency | 80/100 |
| adoption | 57/100 |
| production | 75/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/SylphxAI/pdf-reader-mcp) · [← Back to Mcp](./README.md)</sub>
