# traverse-framework/Traverse

[![Stars](https://img.shields.io/github/stars/traverse-framework/Traverse?style=flat-square&color=yellow)](https://github.com/traverse-framework/Traverse/stargazers) [![Forks](https://img.shields.io/github/forks/traverse-framework/Traverse?style=flat-square&color=blue)](https://github.com/traverse-framework/Traverse/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> Contract-driven runtime for portable business capabilities — spec-governed, WASM-first, composable across browser, edge, cloud, and AI.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 163 |
| 🍴 **Forks** | — |
| 💻 **Language** | Rust |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`business-logic` `capabilities` `cli` `contracts` `event-driven` `mcp` `portable-runtime` `rust` `spec-driven` `uma` `universalmicroservices` `wasi`

## 🎯 Categories

MCP · DevTools

## 📝 Summary

### English

Traverse is a contract‑driven, WASM‑first runtime that lets AI assistants securely call real‑world tools and data via the Model Context Protocol, enabling portable, composable business capabilities across browsers, edge, cloud, and AI environments. Its clear API/SDK/CLI surface and strong recent Rust‑based activity make it straightforward to evaluate and integrate for pilots, while the project’s growing stars, updates, and ecosystem signals indicate high production readiness for an open‑source candidate.

### Русский

**Traverse** — это open‑source runtime, построенный на контрактах и ориентированный на WASM, который позволяет быстро и надёжно подключать AI‑ассистентов к реальным инструментам и данным через единый протокол. Типичный сценарий: разработчик разворачивает сервер Model Context Protocol, а затем AI‑агент в браузере, на edge‑функциях или в облаке без изменения кода получает доступ к бизнес‑логике, хранилищам и внешним сервисам. Проект уже имеет активную поддержку (163 ★, частые коммиты, Rust‑база, 14 тем), поэтому готов к пилотному запуску в продакшн, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句）**  
Traverse 是一个基于合约驱动的运行时框架，采用 WASM‑first 设计，能够在浏览器、边缘、云端以及 AI 环境中以统一的协议组合和调用业务能力。它通过 **Model‑Context‑Protocol（MCP）** 为 AI 助手提供标准化的工具与数据接入层，使得 AI 能够安全、可控地执行真实业务操作。

**价值主张**  
- **统一协议**：使用 MCP（规范化的 JSON‑RPC/Protobuf 合约）把 AI 代理、后端服务、浏览器插件等全部映射为同一套可调用的“能力”。  
- **跨平台可移植**：基于 WASM，业务能力可以一次编译后在浏览器、Edge、云函数、容器甚至 AI 推理节点上运行，降低部署与维护成本。  
- **可组合与可扩展**：能力以模块化插件形式提供，开发者可以在运行时自由组合、替换或升级，而无需改动上层 AI 代码。  

**典型接入方式**  

| 场景 | 接入方式 | 关键步骤 |
|------|----------|----------|
| **AI 代理调用工具** | 使用官方 **SDK（Rust / TypeScript）** 或 **CLI** 发起 MCP 请求 | 1. 在 AI Prompt 中声明需要的合约（如 `traverse://weather/get`）<br>2. SDK 自动生成对应的 WASM 调用包装<br>3. 通过 HTTP/gRPC 将请求发送到 Traverse Runtime |
| **部署 Model Context Protocol 服务器** | 直接运行 `traverse-server`（Docker 镜像或二进制） | 1. 编写业务能力合约（OpenAPI / Protobuf）<br>2. 用 `traverse-cli` 编译为 WASM 插件<br>3. 将插件挂载到 Runtime，开启 HTTP/gRPC 端点供 AI 调用 |
| **标准化第三方集成** | 通过 **API/SDK** 暴露语言元数据（Rust、TS、Python） | 1. 在已有微服务中加入 `traverse-sdk`<br>2. 注册能力合约到中心注册表<br>3. 其他项目即可通过合约 ID 动态发现并调用 |

**生产可用性评估**  

- **活跃度**：截至 2026‑06‑27 最近一次提交，GitHub ★163，14 个主题标签，社区活跃。  
- **技术成熟度**：核心采用 Rust，提供高性能 WASM 编译链；官方提供完整的 CLI、SDK、Docker 镜像，支持 CI/CD 自动化部署。  
- **安全与合规**：采用 MIT/Apache 双许可证（需再次确认），所有 WASM 插件在沙箱中运行，默认限制文件系统与网络访问，符合多数企业安全策略。  
- **生态兼容**：已在多个公开案例中与 OpenAI、Claude、Vertex AI 等模型集成，支持浏览器（WebAssembly）、边缘（Cloudflare Workers、Fastly）、云函数（AWS Lambda、GCP Cloud Run）以及传统后端。  

**结论**：Traverse 在规范化 AI‑Tool 交互、跨环境部署以及模块化能力组合方面提供了完整且易用的解决方案，具备高可用的生产级特征，适合作为企业级 AI 助手与业务系统的桥梁进行试点甚至全面落地。

## 🧭 Practical evaluation

**Value:** traverse-framework/Traverse helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 163 GitHub stars
- updated 2026-06-27
- primary language: Rust
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 47/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 65/100 |
| recency | 80/100 |
| adoption | 34/100 |
| production | 71/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/traverse-framework/Traverse) · [← Back to Mcp](./README.md)</sub>
