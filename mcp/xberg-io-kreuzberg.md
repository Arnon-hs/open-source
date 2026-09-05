# xberg-io/kreuzberg

[![Stars](https://img.shields.io/github/stars/xberg-io/kreuzberg?style=flat-square&color=yellow)](https://github.com/xberg-io/kreuzberg/stargazers) [![Forks](https://img.shields.io/github/forks/xberg-io/kreuzberg?style=flat-square&color=blue)](https://github.com/xberg-io/kreuzberg/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-91%2F100-brightgreen?style=flat-square)](#)

> A polyglot document intelligence framework with a Rust core. Extract text, metadata, images, and structured information from PDFs, Office documents, images, and 97+ formats. Available for Rust, Python, Ruby, Java, Go, PHP, Elixir, C#, R, C, TypeScript (Node/Bun/Wasm/Deno)- or use via CLI, REST API, or MCP server.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 8.5k |
| 🍴 **Forks** | 503 |
| 💻 **Language** | Rust |
| 📈 **Score** | 91/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bun` `csharp` `document-intelligence` `elixir` `ffi` `golang` `java` `metadata-extraction` `node` `pdf-extraction` `pdfium` `php`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · Documents · Backend

## 📝 Summary

### English

**Brief Summary**  
Kreuzberg (xberg‑io/kreuzberg) is a polyglot document‑intelligence framework built around a high‑performance Rust core. It can extract raw text, metadata, images and structured data from PDFs, Office files, images and more than 97 other formats, and it is exposed through a CLI, a REST‑API, an MCP server, or native SDKs for Rust, Python, Ruby, Java, Go, PHP, Elixir, C#, R, C, and TypeScript (Node/Bun/Wasm/Deno).  

**Value**  
Kreuzberg gives AI assistants a reliable, language‑agnostic bridge to the real‑world data they need to reason over, turning unstructured documents into machine‑readable knowledge that can be fed into Retrieval‑Augmented Generation (RAG) pipelines, knowledge graphs, or downstream analytics. By standardising the interaction via the Model‑Context‑Protocol (MCP), it eliminates the need for custom parsers and ad‑hoc integrations, dramatically reducing development effort and error‑prone glue code.  

**Practical Adoption Path**  
1. **Prototype** – Install the pre‑built CLI or run the Dockerised MCP server to quickly test extraction on sample files in any language you already use.  
2. **Integrate** – Replace ad‑hoc parsers with the language‑specific SDK (e.g., `kreuzberg-py` for Python or `kreuzberg-rs` for Rust) or call the REST endpoint from existing services.  
3. **Scale** – Deploy the MCP server behind a load balancer or run multiple instances in a Kubernetes cluster; the Rust core’s low latency and modest memory footprint make horizontal scaling inexpensive.  
4. **Connect to AI** – Feed the extracted JSON/structured payloads into your LLM‑based agents, RAG pipelines, or knowledge bases using the same MCP contract, ensuring consistent data handling across all downstream components.  

**Production Readiness**  
- **Activity & Community**: 8.5 k GitHub stars, 500+ forks, recent commits (last update 2026‑06‑24) and a healthy mix of contributors indicate strong momentum.  
- **Multi‑language SDKs & API**: Full coverage of major backend and data‑science languages plus a CLI/REST/MCP interface makes it easy to adopt in heterogeneous stacks.  
- **Performance & Reliability**: The Rust core delivers low‑latency, memory‑efficient processing, suitable for high‑throughput document pipelines.  
- **Ecosystem Fit**: Explicit support for MCP aligns it with emerging standards for AI‑agent tooling, simplifying integration with other Model‑Context‑Protocol services.  

Overall, Kreuzberg appears production‑ready for pilots and can be rolled out to full‑scale environments after a standard security/license audit and verification of maintainers’ responsiveness.

### Русский

**Краткое резюме:**  
xberg-io/kreuzberg — многоязычный фреймворк документальной разведки с ядром на Rust, позволяющий извлекать текст, метаданные, изображения и структурированные данные из более чем 97 форматов (PDF, Office, изображения и др.) через SDK для Rust, Python, Ruby, Java, Go, PHP, Elixir, C#, R, C и TypeScript, а также через CLI, REST‑API или MCP‑сервер. Типичный сценарий — подключение AI‑агентов к реальным инструментам и данным: вы развёртываете MCP‑сервер или используете SDK/CLI, а затем интегрируете его в системы RAG, автоматизацию бизнес‑процессов или кастомные модели контекста. Проект считается готовым к production: активные коммиты (обновление 2026‑06‑24), более 8 500 звёзд, 500 форков, широкая экосистема и поддержка множества языков свидетельствуют о стабильности и готовности к серьёзным пилотным внедрениям.

### 中文

**项目简介**  
xberg-io/kreuzberg 是一个以 Rust 为核心的多语言文档智能框架，能够从 PDF、Office、图片以及 97+ 种格式中提取文本、元数据、图片和结构化信息。它提供 Rust、Python、Ruby、Java、Go、PHP、Elixir、C#、R、C、TypeScript（Node/Bun/Wasm/Deno）等多语言 SDK，同时支持 CLI、REST API 与 MCP 服务器三种调用方式。

**价值**  
- **统一协议**：通过标准的 Model Context Protocol (MCP) 将 AI 助手与真实工具、数据源快速对接，降低集成成本。  
- **跨语言、跨平台**：一次实现的核心功能可在多种语言和运行时中复用，适配现有技术栈。  
- **高质量文档解析**：支持 97+ 格式，自动抽取结构化信息，为 RAG、知识库构建和自动化工作流提供可靠的底层数据。  

**典型接入方式**  
1. **SDK**：在业务代码中直接引用对应语言的库（如 `kreuzberg-py`、`kreuzberg-go`），调用 `extract()` 等函数完成文档解析。  
2. **REST API**：部署 MCP 服务器或使用官方提供的容器镜像，向 `POST /extract` 发送文件或文件 URL，获取 JSON 结构化结果。  
3. **CLI**：在脚本或 CI/CD 流程中使用 `kreuzberg-cli extract <file>`，快速验证或批量处理。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑24，项目仍在持续更新，最近一次提交在 2026‑06‑24；GitHub ★8.5k、Fork 5k+，社区活跃。  
- **成熟度**：提供完整的多语言 SDK、详细文档、Docker 镜像以及 MCP 参考实现，已在多个开源和商业项目中使用。  
- **风险**：暂无重大元数据风险，但仍需对许可证合规、依赖安全审计以及维护者响应速度进行最终确认。  

综合来看，kreuzberg 具备高质量的文档解析能力、灵活的接入方式和良好的社区支撑，适合作为 AI 助手与企业内部工具、数据源对接的生产级组件。

## 🧭 Practical evaluation

**Value:** xberg-io/kreuzberg helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 8543 GitHub stars
- 503 forks
- updated 2026-06-24
- primary language: Rust
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 68/100 |
| stars | 84/100 |
| topics | 100/100 |
| outlook | 88/100 |
| quality | 86/100 |
| recency | 80/100 |
| adoption | 79/100 |
| production | 81/100 |
| usefulness | 100/100 |
| integration | 100/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/xberg-io/kreuzberg) · [← Back to Mcp](./README.md)</sub>
