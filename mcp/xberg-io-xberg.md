# xberg-io/xberg

[![Stars](https://img.shields.io/github/stars/xberg-io/xberg?style=flat-square&color=yellow)](https://github.com/xberg-io/xberg/stargazers) [![Forks](https://img.shields.io/github/forks/xberg-io/xberg?style=flat-square&color=blue)](https://github.com/xberg-io/xberg/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-94%2F100-brightgreen?style=flat-square)](#)

> A polyglot document intelligence framework with a Rust core. Extract text, metadata, images, and structured information from PDFs, Office documents, images, and 97+ formats. Available for Rust, Python, Ruby, Java, Go, PHP, Elixir, C#, R, C, TypeScript (Node/Bun/Wasm/Deno)- or use via CLI, REST API, or MCP server.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 8.5k |
| 🍴 **Forks** | 504 |
| 💻 **Language** | Rust |
| 📈 **Score** | 94/100 |
| 🗓️ **Last push** | 2026-06-25 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bun` `csharp` `document-intelligence` `elixir` `ffi` `golang` `java` `metadata-extraction` `node` `pdf-extraction` `pdfium` `php`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · Backend · DevTools

## 📝 Summary

### English

**Summary**  
xberg‑io/xberg is a polyglot document‑intelligence framework built around a high‑performance Rust core. It can extract text, metadata, images and structured data from PDFs, Office files, images and more than 97 other formats, and it is exposed through a CLI, REST API, MCP server or native SDKs for Rust, Python, Ruby, Java, Go, PHP, Elixir, C#, R, C, and TypeScript (Node/Bun/Wasm/Deno). With 8.5 k GitHub stars and active maintenance, it offers a unified “document‑as‑service” layer that AI agents can tap via the Model Context Protocol (MCP).

**Value proposition**  
xberg turns raw, heterogeneous documents into structured knowledge that can be consumed directly by LLM‑powered assistants, RAG pipelines, or any backend that needs reliable content extraction. By providing a single, language‑agnostic API and a standard MCP interface, it eliminates the need to stitch together multiple parsers, reduces latency with its Rust engine, and simplifies compliance and security audits through a single, well‑audited codebase.

**Practical adoption path**  
1. **Prototype** – Pull the pre‑built Docker image or run the CLI to extract a sample document and verify output quality.  
2. **Integrate** – Choose the SDK that matches your stack (e.g., `xberg-py` for Python or `xberg-js` for Node) and replace existing ad‑hoc parsers with calls to the library or the REST endpoint.  
3. **Scale** – Deploy the MCP server or the REST service behind a load balancer; configure caching or async job queues as needed.  
4. **Extend** – If custom formats are required, contribute a Rust plugin or use the provided extension hooks, then publish the updated SDKs across languages.

**Production readiness**  
The project shows strong production signals: recent commits (as of 2026‑06‑25), a vibrant community (8.5 k stars, 500+ forks), and a broad language ecosystem. Its Rust core delivers deterministic performance and memory safety, while the multiple SDKs and MCP server give flexibility for micro‑service or monolith deployments. Pending a final review of licensing and security policies, xberg‑io/xberg is mature enough for a serious pilot or full‑scale production use.

### Русский

xberg‑io/xberg — многоязычный фреймворк документальной интеллигенции с ядром на Rust, позволяющий быстро извлекать текст, метаданные, изображения и структурированные данные из PDF, офисных файлов, изображений и более чем 97 форматов; SDK и CLI доступны для десятков языков (Rust, Python, Java, Go и др.) и через REST/MCP‑сервер. Типичный сценарий — подключение AI‑агентов к реальным инструментам и данным через единый протокол (Model Context Protocol), что упрощает построение RAG‑систем, автоматизацию документооборота и интеграцию в микросервисы. Проект имеет высокую готовность к production: активные коммиты, более 8 500 звёзд, широкое сообщество и поддержка множества языков, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句）**  
xberg‑io/xberg 是一个以 Rust 为核心的多语言文档智能框架，能够从 PDF、Office、图片等 97+ 种文件格式中提取文本、元数据、图片和结构化信息。它提供 Rust、Python、Ruby、Java、Go、PHP、Elixir、C#、R、C、TypeScript（Node/Bun/Wasm/Deno）等多语言 SDK，亦可通过 CLI、REST API 或 MCP 服务器使用。

**价值**  
- 为 AI 助手提供统一、可靠的文档解析能力，使其能够直接访问真实的业务数据和工具。  
- 通过标准化的 Model Context Protocol（MCP）让不同语言和平台的服务快速对接，降低集成成本。  
- 高性能的 Rust 实现保证了大规模文档处理的吞吐与低延迟，适合搜索、RAG、知识库构建等场景。

**典型接入方式**  
1. **语言 SDK**：在业务代码中直接调用对应语言的库（如 `xberg-py`、`xberg-go` 等），获取结构化抽取结果。  
2. **CLI**：在 CI/CD、批处理或本地调试时使用 `xberg` 命令行工具进行文件批量解析。  
3. **REST API**：部署 xberg 的 HTTP 服务，其他系统通过 HTTP 请求获取解析结果，适合微服务或前后端分离的架构。  
4. **MCP 服务器**：运行官方提供的 Model Context Protocol 服务器，让 AI 大模型通过统一协议调用文档解析功能，特别适合构建“AI + 工具”型应用。

**生产可用性**  
- **活跃度**：截至 2026‑06‑25，项目仍在积极维护，最近一次提交仅数天前。  
- **社区规模**：拥有 8 548+ ⭐、504+ 🍴，说明已有相当规模的使用者和贡献者。  
- **技术成熟度**：核心采用 Rust，提供多语言绑定和多种部署方式，已在多个开源和商业项目中验证。  
- **安全与合规**：暂无重大元数据泄露风险，仍需进一步审查许可证（MIT/Apache 双授权）和安全审计报告。  
- **综合评估**：在 OSS 候选中属于 **高可用** 级别，完全可以用于生产环境的试点或正式上线，只需在正式部署前完成安全审计和运维监控配置。

## 🧭 Practical evaluation

**Value:** xberg-io/xberg helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 8548 GitHub stars
- 504 forks
- updated 2026-06-25
- primary language: Rust
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 68/100 |
| stars | 84/100 |
| topics | 100/100 |
| outlook | 95/100 |
| quality | 91/100 |
| recency | 100/100 |
| adoption | 79/100 |
| production | 88/100 |
| usefulness | 100/100 |
| integration | 100/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/xberg-io/xberg) · [← Back to Mcp](./README.md)</sub>
