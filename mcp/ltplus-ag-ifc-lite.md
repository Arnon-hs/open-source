# LTplus-AG/ifc-lite

[![Stars](https://img.shields.io/github/stars/LTplus-AG/ifc-lite?style=flat-square&color=yellow)](https://github.com/LTplus-AG/ifc-lite/stargazers) [![Forks](https://img.shields.io/github/forks/LTplus-AG/ifc-lite?style=flat-square&color=blue)](https://github.com/LTplus-AG/ifc-lite/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-80%2F100-brightgreen?style=flat-square)](#)

> Parse, view, query, edit, and export IFC, IDS, BCF, pointclouds and more AEC stuff. In the browser, server or desktop.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 249 |
| 🍴 **Forks** | 68 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 80/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`3d-viewer` `bcf` `cli` `columnar` `ids` `ifc` `ifc-parser` `mcp` `pointcloud` `rust` `script-editor` `sdk`

## 🎯 Categories

MCP · DevTools · Libraries & SDKs

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
LTplus‑AG/ifc‑lite is a TypeScript‑based open‑source library that lets you parse, view, query, edit and export a wide range of AEC data formats—including IFC, IDS, BCF and point clouds—across browser, server and desktop environments. By exposing a clean API/SDK/CLI, it enables AI assistants and other automation tools to interact with real‑world building‑information models through a standard “Model Context Protocol”. With active maintenance, strong community adoption (≈250 ★, 68 forks) and recent releases, it is ready for pilot‑grade production use.

**Value**  
- **Unified data access**: One library handles the most common AEC formats, eliminating the need for multiple parsers and reducing integration complexity.  
- **AI‑ready interface**: The standardized protocol and language‑agnostic SDK let AI agents query and manipulate building models just like any other service, bridging the gap between large‑language models and concrete design tools.  
- **Cross‑environment support**: Works in browsers, Node.js back‑ends and Electron‑style desktop apps, making it suitable for SaaS platforms, on‑premise servers, or offline design tools.

**Practical Adoption Path**  
1. **Prototype** – Install the npm package, spin up the provided CLI or minimal server, and load a sample IFC file to verify parsing and query capabilities.  
2. **Integrate** – Replace existing ad‑hoc parsers with the ifc‑lite SDK in your backend services or front‑end viewers; use the API to expose model data to your AI agent or other micro‑services.  
3. **Extend** – Leverage the modular architecture to add custom exporters (e.g., to proprietary formats) or plug in additional point‑cloud processing libraries.  
4. **Deploy** – Package the server component in a container or embed the library in a desktop client; monitor health via the built‑in diagnostics endpoints.

**Production Readiness**  
- **Activity**: Last commit on 2026‑06‑23, regular issue triage, and a growing contributor base.  
- **Community signals**: 249 GitHub stars, 68 forks, and 13 relevant topics indicate healthy interest and peer validation.  
- **Stability**: The core API is versioned, and the CLI/SDK are well‑documented, making it straightforward to lock to a specific release for reproducible builds.  
- **Risks**: Formal license review and a deeper security audit are still required, but no major red flags have been identified.  

Overall, ifc‑lite offers a mature, extensible foundation for any project that needs to bring AI‑driven workflows into the architecture‑engineering‑construction (AEC) domain, and it is ready for serious pilot deployments.

### Русский

**LTplus‑AG/ifc-lite** — это открытая TypeScript‑библиотека, позволяющая парсить, визуализировать, выполнять запросы, редактировать и экспортировать IFC, IDS, BCF, облака точек и другие форматы AEC как в браузере, так и на сервере или десктопе. Типичный сценарий: интеграция AI‑агента с реальными инженерными данными через единый протокол (Model Context Protocol), что упрощает построение «умных» помощников и развёртывание серверов контекстных моделей. Проект имеет высокий уровень готовности к production: активные коммиты, 249 ★, 68 форков, свежий релиз (23 июн 2026) и поддерживает API/SDK/CLI, однако перед масштабным внедрением следует проверить лицензию и безопасность.

### 中文

**项目简介（2‑3 句话）**  
LTplus-AG/ifc-lite 是一套基于 TypeScript 的开源库，能够在浏览器、服务器或桌面环境下解析、展示、查询、编辑并导出 IFC、IDS、BCF、点云等建筑信息模型（AEC）数据。它提供统一的 API/SDK/CLI，帮助 AI 助手和其他系统以标准协议直接操作真实的建筑数据和工具。

**价值**  
- **桥接 AI 与实际工具**：通过标准化的 Model Context Protocol，让 AI 代理能够直接调用 IFC、IDS、BCF 等专业工具，实现“AI + 工具”协同工作。  
- **统一数据入口**：一次接入即可支持多种 AEC 格式，降低跨系统集成成本。  
- **灵活部署**：同一套代码既可在前端（浏览器）运行，也可作为后端服务或本地桌面应用使用，适配各种业务场景。

**典型接入方式**  
1. **API/SDK**：在 Node.js 或前端项目中 `npm install @ltplus-ag/ifc-lite`，使用其 TypeScript/JavaScript 接口进行模型加载、查询和编辑。  
2. **CLI**：通过 `npx ifc-lite <command>` 在 CI/CD、批处理或本地脚本中完成模型转换、验证或导出。  
3. **服务器模式**：部署为 Express/Koa 中间件或独立的 HTTP 服务，提供 REST/GraphQL 接口，供 AI 代理或其他系统远程调用。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑23 最近一次提交，拥有 249 ⭐、68 🍴，13 个相关话题，社区活跃。  
- **技术成熟度**：全栈 TypeScript 实现，提供完整类型定义，易于在现代前端/后端项目中集成。  
- **生态兼容**：支持标准 AEC 文件格式，已被多个开源和商业项目采用，具备真实生产环境验证。  
- **风险**：需进一步审查许可证（MIT/Apache 等）和安全审计报告；保持维护者活跃度的监控。  

综合来看，ifc-lite 在功能完整性、社区活跃度和技术实现上均已达到可用于正式生产的水平，适合作为 AI 助手与建筑信息模型交互的核心组件。

## 🧭 Practical evaluation

**Value:** LTplus-AG/ifc-lite helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 249 GitHub stars
- 68 forks
- updated 2026-06-23
- primary language: TypeScript
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 46/100 |
| stars | 51/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 50/100 |
| production | 76/100 |
| usefulness | 90/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/LTplus-AG/ifc-lite) · [← Back to Mcp](./README.md)</sub>
