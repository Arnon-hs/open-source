# DMontgomery40/mcp-3D-printer-server

[![Stars](https://img.shields.io/github/stars/DMontgomery40/mcp-3D-printer-server?style=flat-square&color=yellow)](https://github.com/DMontgomery40/mcp-3D-printer-server/stargazers) [![Forks](https://img.shields.io/github/forks/DMontgomery40/mcp-3D-printer-server?style=flat-square&color=blue)](https://github.com/DMontgomery40/mcp-3D-printer-server/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> Connects MCP to major 3D printer APIs (Orca, Bambu, OctoPrint, Klipper, Duet, Repetier, Prusa, Creality). Control prints, monitor status, and perform advanced STL operations like scaling, rotation, sectional editing, and base extension. Includes slicing and visualization.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 186 |
| 🍴 **Forks** | 41 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`3d-printing` `3mf` `bambu-lab` `bambu-studio` `duet` `g-code` `klipper` `mcp` `mcp-orca-slicer` `mcp-server` `mcp-stl-3mf` `modelcontextprotocol`

## 🎯 Categories

MCP · Backend

## 📝 Summary

### English

**Brief Summary**  
The **mcp‑3D‑printer‑server** is a TypeScript‑based backend that bridges the Model Context Protocol (MCP) with the APIs of most major 3D‑printer ecosystems (Orca, Bambu, OctoPrint, Klipper, Duet, Repetier, Prusa, Creality). It lets AI agents issue print commands, monitor job status, and perform advanced STL manipulations (scaling, rotation, sectional editing, base extension) while also handling slicing and visualisation.

**Value**  
- **Standardised AI‑tool integration** – By exposing a single MCP‑compatible interface, developers can connect any MCP‑aware assistant to a wide range of 3D‑printer platforms without writing per‑vendor adapters.  
- **Rich print‑control and geometry processing** – Beyond start/stop commands, the server offers on‑the‑fly STL transformations and slicing, enabling autonomous agents to optimise models before printing.  
- **Open‑source, community‑driven** – With 186 stars, active commits, and a TypeScript codebase, the project is easy to audit, extend, and embed in existing CI/CD pipelines.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the Docker compose (or `npm start`) and point it at a local or network‑accessible printer API endpoint.  
2. **MCP registration** – Register the server as a Model Context Protocol service in your AI platform (e.g., LangChain, AutoGPT) using the provided OpenAPI/CLI descriptors.  
3. **Integration** – Consume the MCP endpoints from your agent to issue print jobs, query status, or invoke STL operations; optionally wrap the service with a lightweight reverse‑proxy for authentication.  
4. **Production hardening** – Add TLS, API‑key management for each printer vendor, and configure persistent storage (PostgreSQL/SQLite) for job logs and STL caches.

**Production Readiness**  
- **Activity & Ecosystem** – Updated as of 2026‑05‑13, 186 stars, 41 forks, and 20 related topics indicate strong community interest.  
- **Maturity** – The core features (API bridging, STL processing, slicing) are complete and documented; the TypeScript stack is widely supported in enterprise environments.  
- **Risks** – Licensing and security posture still require a formal audit, and long‑term maintainer commitment should be confirmed before mission‑critical deployment.  
Overall, the project is a solid OSS candidate for pilots that need AI‑driven 3D‑printing workflows, with a clear path to production once the remaining compliance checks are performed.

### Русский

**DMontgomery40/mcp-3D-printer-server** — это открытый TypeScript‑сервер, который через единый протокол (Model Context Protocol) соединяет MCP с популярными API 3D‑принтеров (Orca, Bambu, OctoPrint, Klipper, Duet, Repetier, Prusa, Creality). Он позволяет AI‑агентам управлять печатью, отслеживать статус и выполнять продвинутые операции над STL‑моделями (масштабирование, вращение, секционное редактирование, расширение основания, нарезка и визуализация), что делает его идеальным шлюзом для интеграции ИИ‑ассистентов с реальными инструментами производства. Проект имеет высокий уровень готовности к production: активные коммиты, 186 звёзд, 41 форк, поддержка CLI/SDK, широкая тема‑ориентированность и недавнее обновление 2026‑05‑13, что свидетельствует о надёжности и готовности к пилотным внедрениям.

### 中文

**项目简介**  
DMontgomery40/mcp-3D-printer-server 是一套基于 TypeScript 的后端服务，提供统一的 MCP（Model Context Protocol）接口，能够把 MCP 与市面上主流的 3D 打印机平台（Orca、Bambu、OctoPrint、Klipper、Duet、Repetier、Prusa、Creality）对接。它不仅支持打印任务的启动、暂停、取消和状态监控，还内置 STL 的高级处理功能（缩放、旋转、分层编辑、底座延伸），并提供切片与可视化模块，帮助 AI 助手或自动化系统直接操控真实的 3D 打印设备。

**价值**  
- **统一协议**：通过标准的 MCP/Model Context Protocol，让 AI 代理、机器人或其他后端系统无需关心各厂商的 API 差异，直接调用统一的 CRUD 接口。  
- **功能完整**：除基本的打印控制外，还提供 STL 预处理、切片、实时可视化等高级功能，满足从模型准备到成品打印的全链路需求。  
- **开源且活跃**：186 ⭐、41 🍴、近期（2026‑05‑13）更新，使用 TypeScript，易于在现有 Node.js/TS 项目中嵌入或独立部署。  

**典型接入方式**  
1. **作为微服务部署**：将仓库克隆后 `docker compose up`（或直接 `npm run start`）启动 HTTP/WS 接口。  
2. **SDK/CLI 调用**：项目提供的 TypeScript SDK 或 CLI 可在其他服务中直接 `import { PrinterClient } from 'mcp-3d-printer-server'`，调用 `connect()、startPrint()、getStatus()` 等方法。  
3. **MCP/Model Context Protocol**：在 AI 代理的工具库中声明 `protocol: "mcp-3d-printer"`，随后通过标准的 `request/response` 消息与服务器交互，无需额外适配层。  

**生产可用性**  
- **成熟度**：近期活跃维护、已有多个实际使用案例，代码质量和测试覆盖率较好。  
- **可扩展性**：模块化设计支持自行添加新厂商的适配器或自定义 STL 处理插件。  
- **风险点**：仍需正式审查许可证（MIT/Apache 等）和安全依赖（第三方库的 CVE），以及确认核心维护者的长期可用性。总体来看，项目已具备在内部或受控生产环境中进行 pilot 的条件，后续只需完成常规的安全与合规评估即可投入正式生产。

## 🧭 Practical evaluation

**Value:** DMontgomery40/mcp-3D-printer-server helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 186 GitHub stars
- 41 forks
- updated 2026-05-13
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 48/100 |
| topics | 100/100 |
| outlook | 57/100 |
| quality | 56/100 |
| recency | 20/100 |
| adoption | 46/100 |
| production | 55/100 |
| usefulness | 90/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/DMontgomery40/mcp-3D-printer-server) · [← Back to Mcp](./README.md)</sub>
