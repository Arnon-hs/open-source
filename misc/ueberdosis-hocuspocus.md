# ueberdosis/hocuspocus

[![Stars](https://img.shields.io/github/stars/ueberdosis/hocuspocus?style=flat-square&color=yellow)](https://github.com/ueberdosis/hocuspocus/stargazers) [![Forks](https://img.shields.io/github/forks/ueberdosis/hocuspocus?style=flat-square&color=blue)](https://github.com/ueberdosis/hocuspocus/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> The Yjs CRDT WebSocket backend for conflict-free real-time collaboration in your app.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.3k |
| 🍴 **Forks** | 193 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`collaborative-editing` `crdt` `prosemirror` `real-time` `self-hosted` `slatejs` `tiptap` `yjs`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
Hocuspocus is an open‑source TypeScript WebSocket server that implements Yjs’s CRDT protocol, giving you a ready‑made backend for conflict‑free real‑time collaboration. With strong community adoption (2 257 ★, 193 forks) and recent activity, it lets teams focus on product features instead of rebuilding the synchronization layer.

**Value**  
- **Infrastructure reuse:** Provides a battle‑tested, standards‑based collaboration service that can be shared across multiple apps, reducing duplicate effort and maintenance overhead.  
- **Speed to market:** By plugging in a pre‑built Yjs‑compatible backend, teams can ship collaborative APIs (e.g., shared editors, live dashboards) much faster than building a custom CRDT/WebSocket solution.  
- **Standardization:** Encourages a consistent service pattern for real‑time features across the organization, simplifying onboarding and troubleshooting.

**Practical Adoption Path**  
1. **Proof of concept:** Clone the repo, run the example server, and connect a Yjs client to verify basic sync behavior.  
2. **Readme & API review:** Follow the quick‑start guide, confirm the WebSocket endpoint, authentication hooks, and persistence options meet your requirements.  
3. **Pilot integration:** Wrap the Hocuspocus server in a minimal microservice (e.g., Docker container) within your staging environment; integrate with existing auth/DB layers via the provided hooks.  
4. **Iterate & extend:** Add custom event handlers (e.g., document‑level permissions) and monitor performance with the built‑in metrics.  

**Production Readiness**  
- **High:** The project shows recent commits (as of 2026‑05‑12), active issue handling, and a sizable community, indicating good maintenance.  
- **Ecosystem fit:** Written in TypeScript, it aligns with modern Node.js stacks and integrates cleanly with existing Yjs clients.  
- **Remaining checks:** Conduct a final review of the MIT/Apache license, run a security audit of dependencies, and verify that maintainers are responsive before scaling to full production.

### Русский

**ueberdosis/hocuspocus** — это готовый WebSocket‑бэкенд на основе Yjs CRDT, позволяющий быстро добавить в приложение конфликт‑свободное совместное редактирование без собственного построения инфраструктуры. Его типичный сценарий — небольшая proof‑of‑concept интеграция (по README) для унификации сервисных паттернов и ускорения вывода API‑сервисов в продакшн. Проект обладает высокой готовностью к production: активные коммиты, более 2000 звёзд, широкое принятие в сообществе и стабильный TypeScript‑код, требующий лишь окончательной проверки лицензии и безопасности.

### 中文

**项目简介**  
ueberdosis/hocuspocus 是基于 Yjs 的 CRDT WebSocket 后端，实现了冲突自由的实时协作功能，帮助开发者在自己的应用中快速搭建多人同步编辑服务。

**价值**  
- **复用基础设施**：团队无需从头实现同步协议、状态持久化和冲突解决等通用后台模块，直接使用成熟的 WebSocket + CRDT 服务。  
- **加速交付**：通过统一的 API 与 Yjs 客户端对接，可显著缩短协作功能的研发周期，提升产品迭代速度。  
- **标准化**：提供统一的服务模式和配置约定，便于在多个微服务或 SaaS 项目中保持一致的协作实现。

**典型接入方式**  
1. **阅读 README**：确认 Node.js 环境、TypeScript 支持及所需的 Yjs 客户端版本。  
2. **创建小型 PoC**：在本地或临时容器中运行 `npx hocuspocus-server`，并使用官方示例代码连接 WebSocket。  
3. **集成到业务服务**：在已有的 Express/Koa/Fastify 等后端框架中引入 `@hocuspocus/server`，通过自定义授权、持久化（Redis、PostgreSQL 等）和事件钩子完成业务逻辑的接入。  
4. **部署**：将服务容器化（Docker）并在 Kubernetes 或云托管平台上水平扩展，利用内置的心跳和自动重连机制保证高可用。

**生产可用性**  
- **活跃度**：截至 2026‑05‑12，项目最近一次提交，拥有 2 257 颗星、193 个 Fork，且持续接受 PR 与 Issue。  
- **技术成熟度**：核心使用 TypeScript 编写，提供完整的类型定义；配套的文档和示例较为完善。  
- **生态兼容**：与 Yjs 生态（如 y-websocket、y-webrtc）保持一致，可直接在前端使用同一 CRDT 模型。  
- **风险**：需进一步审查许可证（MIT）与安全审计报告，确认维护者的响应时效。总体而言，项目已具备在正式业务环境中进行试点或生产级部署的条件。

## 🧭 Practical evaluation

**Value:** ueberdosis/hocuspocus helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2257 GitHub stars
- 193 forks
- updated 2026-05-12
- primary language: TypeScript
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 57/100 |
| stars | 71/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 80/100 |
| recency | 80/100 |
| adoption | 67/100 |
| production | 72/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/ueberdosis/hocuspocus) · [← Back to Misc](./README.md)</sub>
