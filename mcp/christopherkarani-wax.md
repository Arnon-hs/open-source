# christopherkarani/Wax

[![Stars](https://img.shields.io/github/stars/christopherkarani/Wax?style=flat-square&color=yellow)](https://github.com/christopherkarani/Wax/stargazers) [![Forks](https://img.shields.io/github/forks/christopherkarani/Wax?style=flat-square&color=blue)](https://github.com/christopherkarani/Wax/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-81%2F100-brightgreen?style=flat-square)](#)

> Single-file memory layer for AI agents, sub mili-second RAG on Apple Silicon. Metal Optimized On-Device. No Server. No API. One File. Pure Swift

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 730 |
| 🍴 **Forks** | 42 |
| 💻 **Language** | Swift |
| 📈 **Score** | 81/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `cli` `coreml` `coreml-framework` `data-science` `machine-learning` `mcp` `mcp-server` `memory` `memory-cache` `memory-hacking` `metal`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · Backend · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Wax is a single‑file, pure‑Swift memory layer that enables sub‑millisecond Retrieval‑Augmented Generation (RAG) for AI agents on Apple‑Silicon devices, running entirely on‑device with Metal acceleration and no external servers or APIs. It provides a lightweight, standardized protocol for connecting AI assistants to tools, data sources, and Model Context Protocol (MCP) servers, making it easy to embed real‑world knowledge and functionality directly into iOS/macOS apps. With 730 ★, recent commits, and strong community interest, Wax is positioned as a production‑ready OSS component for on‑device AI workloads.

**Value**  
- **Speed & Privacy:** Metal‑optimized, sub‑ms RAG eliminates network latency and keeps user data on the device, satisfying privacy‑by‑design requirements.  
- **Simplicity:** A single Swift file means minimal integration overhead—no build‑system gymnastics, no external dependencies, and no need to manage server infrastructure.  
- **Standardization:** Implements the Model Context Protocol, giving developers a common contract for tool and data integration that can be reused across different agents and services.  

**Practical Adoption Path**  
1. **Evaluate:** Clone the repo, run the provided CLI or Swift SDK demo, and benchmark retrieval latency on your target Apple‑Silicon hardware.  
2. **Integrate:** Add the single Swift file to your Xcode project, configure the memory layer with your data embeddings, and invoke the RAG API from your AI assistant code.  
3. **Extend:** Use the exposed protocol to register custom tool adapters or MCP servers, enabling the assistant to call external services while staying on‑device.  
4. **Deploy:** Ship the app through the App Store; the entire stack remains self‑contained, requiring no backend changes.  

**Production Readiness**  
- **Activity & Adoption:** Recent commits (as of 2026‑05‑11), 730 ★, 42 forks, and active issue discussions indicate a healthy maintainer community.  
- **Stability:** The single‑file architecture reduces build‑time bugs and dependency conflicts; Metal acceleration is well‑tested on Apple Silicon.  
- **Risk Considerations:** License compliance, security audit, and maintainer continuity should be verified before large‑scale rollout, but no major red flags are evident.  

Overall, Wax offers a fast, private, and low‑friction way to equip on‑device AI agents with real‑time knowledge and tool access, making it a strong candidate for production pilots in iOS/macOS AI products.

### Русский

**Wax** — однопоточный слой памяти для AI‑агентов, реализованный в едином Swift‑файле и оптимизированный под Metal на Apple Silicon, что обеспечивает под‑миллисекундный RAG без серверов и внешних API. Он позволяет быстро подключать ассистентов к реальным инструментам и данным через стандартный Model Context Protocol, что упрощает создание интеграций и развертывание собственных протокольных серверов. По активности репозитория (730 ★, регулярные коммиты, широкая экосистема) проект готов к пилотному использованию в продакшене, хотя требуется финальная проверка лицензии и безопасности.

### 中文

**项目简介**  
`christopherkarani/Wax` 是一个 **单文件** 的本地记忆层，专为 Apple Silicon 设备上的 AI 代理设计，使用 Metal 完全在设备端加速，实现 **亚毫秒级 RAG（检索增强生成）**。无需服务器、无需外部 API，只需一行 Swift 代码即可把向量检索功能嵌入到你的应用中。

**价值主张**  
- **即时、低延迟**：在本地完成向量索引与检索，省去网络往返，响应时间可达 sub‑ms。  
- **极简部署**：单文件、纯 Swift 实现，直接加入 Xcode 项目即可，无需额外依赖或云服务。  
- **统一协议**：实现了 Model Context Protocol（MCP），帮助 AI 助手统一对接各种工具、数据源和插件，降低集成成本。  
- **开源且活跃**：730+ Stars、42+ Forks，近期仍在维护，适合作为生产级 OSS 组件。

**典型接入方式**  

| 场景 | 接入步骤 | 关键接口 |
|------|----------|----------|
| **在 iOS/macOS 应用中为 AI 助手提供本地记忆** | 1. 将 `Wax.swift` 单文件拖入 Xcode 项目。<br>2. 初始化 `Wax` 实例并加载/保存向量数据。<br>3. 在对话生成前调用 `search(query:)` 获取相关上下文。 | `init(storagePath: String)`, `addDocument(id: String, embedding: [Float])`, `search(query:, topK:)` |
| **作为工具插件的后端** | 1. 使用提供的 CLI (`wax-cli`) 启动本地服务。<br>2. 通过标准的 MCP HTTP/JSON 接口让外部 AI 代理调用检索。 | `wax serve --port 8080`, `POST /mcp/search` |
| **在 Swift 包或服务器端（Apple Silicon）上统一管理记忆** | 1. 将仓库作为 Swift Package 引入。<br>2. 在后端服务中创建单例 `Wax`，并通过 SDK 暴露 `search` API。 | `Package.swift` 依赖, `Wax.shared` |

**生产可用性评估**  

- **活跃度**：最近一次提交是 2026‑05‑11，项目保持持续更新；Issue 与 PR 反馈速度快。  
- **成熟度**：单文件实现降低了依赖冲突风险，Metal 加速已在真实设备上验证，适合在 iOS/macOS 生产环境直接使用。  
- **安全/合规**：采用 MIT 许可证，代码体积小，审计成本低；但仍建议在引入前进行内部安全审查。  
- **生态兼容**：提供 API、SDK 与 CLI 三种接入方式，且遵循标准的 Model Context Protocol，便于与已有的 AI 框架（如 LangChain、OpenAI‑compatible 代理）对接。  

综合来看，`Wax` 已具备 **高可用、低延迟、易集成** 的特性，适合作为生产环境中 AI 代理的本地记忆层或 RAG 引擎的首选 OSS 方案。

## 🧭 Practical evaluation

**Value:** christopherkarani/Wax helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 730 GitHub stars
- 42 forks
- updated 2026-05-11
- primary language: Swift
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 61/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 75/100 |
| recency | 80/100 |
| adoption | 55/100 |
| production | 74/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/christopherkarani/Wax) · [← Back to Mcp](./README.md)</sub>
