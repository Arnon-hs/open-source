# holon-run/uxc

[![Stars](https://img.shields.io/github/stars/holon-run/uxc?style=flat-square&color=yellow)](https://github.com/holon-run/uxc/stargazers) [![Forks](https://img.shields.io/github/forks/holon-run/uxc?style=flat-square&color=blue)](https://github.com/holon-run/uxc/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> A unified CLI for discovering and invoking tools across OpenAPI, MCP, GraphQL, gRPC, and JSON-RPC

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 108 |
| 🍴 **Forks** | 7 |
| 💻 **Language** | Rust |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-tools` `ai-agents` `api` `cli` `developer-tools` `graphql` `grpc` `json-rpc` `mcp` `model-context-protocol` `openapi` `schema-driven`

## 🎯 Categories

MCP · AI/ML · Backend · DevTools

## 📝 Summary

### English

**Brief Summary**  
holon‑run/uxc is a Rust‑based unified CLI that lets developers discover and invoke services defined in OpenAPI, MCP, GraphQL, gRPC, and JSON‑RPC through a single, standard protocol. By exposing implementation signals such as API/SDK/CLI metadata, language tags, and topic focus, it streamlines the wiring of AI assistants to real‑world tools and data sources.  

**Value**  
- **One‑stop gateway**: Eliminates the need to juggle multiple client generators or custom adapters; a single command can query any supported spec type.  
- **AI‑ready interface**: The Model Context Protocol (MCP) integration enables large language models to call external tools safely and predictably, turning abstract prompts into concrete actions.  
- **Consistent metadata**: Built‑in exposure of language, SDK, and topic information makes downstream discovery, documentation, and governance far easier.  

**Practical Adoption Path**  
1. **Prototype** – Install the CLI (`cargo install uxc` or pre‑built binary) and point it at an existing OpenAPI/GraphQL/gRPC spec to validate that tool discovery works.  
2. **Integrate** – Wrap the CLI or its Rust library in a thin service layer (e.g., a lightweight HTTP proxy) that your AI assistant can call via MCP.  
3. **Standardize** – Replace ad‑hoc SDK calls across your codebase with `uxc` invocations, gradually deprecating bespoke client code.  
4. **Scale** – Deploy the proxy as a Model Context Protocol server in your production environment, leveraging the CLI’s built‑in health checks and logging.  

**Production Readiness**  
- **Activity & Adoption**: Recent commits (as of 2026‑05‑14), 108 GitHub stars, and active forks indicate a healthy community.  
- **Maturity**: The project covers a wide range of protocols, provides clear CLI semantics, and is written in Rust, offering performance and safety guarantees.  
- **Risk Considerations**: Licensing and security posture still need a final audit, and you should verify that maintainers are responsive to vulnerability reports. With those checks completed, holon‑run/uxc is a strong candidate for a serious pilot or production deployment.

### Русский

**holon-run/uxc** — это единый CLI, позволяющий автоматически обнаруживать и вызывать инструменты, описанные в OpenAPI, MCP, GraphQL, gRPC и JSON‑RPC, что упрощает подключение AI‑ассистентов к реальным сервисам и данным через единый протокол. Типичный сценарий — интеграция AI‑агента с набором внешних сервисов (например, микросервисов, ML‑моделей или сторонних API) либо развёртывание собственного Model Context Protocol‑сервера, используя готовый Rust‑клиент и метаданные о языке и тематиках. Проект находится на высокой стадии готовности к production: активные коммиты, 108 звёзд, поддержка нескольких языков, недавнее обновление (14 мая 2026) и сильные сигналы экосистемы делают его надёжным кандидатом для пилотных внедрений, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
holon‑run/uxc 是一个统一的命令行工具，能够在 OpenAPI、MCP、GraphQL、gRPC 和 JSON‑RPC 等多种协议之间发现并调用后端工具。它通过标准化的协议把 AI 助手与真实工具和数据桥接起来，实现「AI + 工具」的无缝协作。

**价值**  
- **统一入口**：一次安装即可跨多种 API 风格查询、执行功能，省去维护多个 SDK/CLI 的成本。  
- **AI‑友好**：提供标准的 Model Context Protocol（MCP）实现，使 AI 代理能够像调用本地函数一样调用外部服务。  
- **加速集成**：通过统一的元数据（语言、主题、实现方式等）快速生成集成代码或自动化脚本，提升开发效率。

**典型接入方式**  
1. **CLI 直接调用**：在终端执行 `uxc discover <service>`、`uxc invoke <method> …` 即可完成服务发现和调用。  
2. **SDK 嵌入**：在 Rust、Python、Node.js 等语言的项目中引入 `uxc` 提供的库，使用其 API 动态加载并执行远程方法。  
3. **MCP 服务部署**：将 `uxc` 作为 Model Context Protocol 服务器运行，供内部 AI 助手通过统一协议查询和执行工具。  
4. **CI/CD 自动化**：在构建流水线中加入 `uxc` 检查 API 兼容性或自动生成调用脚本，实现 DevOps 与 AI 的闭环。

**生产可用性**  
- **活跃度高**：最近一次提交在 2026‑05‑14，星标 108、Fork 7，社区讨论活跃，代码基于 Rust，具备良好的性能与安全特性。  
- **成熟度**：项目已实现完整的发现、调用、错误处理等核心功能，且提供多语言元数据，适合作为正式环境的工具层。  
- **风险点**：仍需进一步审查许可证兼容性、依赖安全（尤其是外部协议的认证/授权）以及维护者的长期可用性。总体来看，holon‑run/uxc 已具备在生产环境中进行试点或正式上线的条件。

## 🧭 Practical evaluation

**Value:** holon-run/uxc helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 108 GitHub stars
- 7 forks
- updated 2026-05-14
- primary language: Rust
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 23/100 |
| stars | 43/100 |
| topics | 100/100 |
| outlook | 56/100 |
| quality | 52/100 |
| recency | 20/100 |
| adoption | 38/100 |
| production | 52/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/holon-run/uxc) · [← Back to Mcp](./README.md)</sub>
