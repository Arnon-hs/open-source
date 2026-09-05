# element-hq/element-call

[![Stars](https://img.shields.io/github/stars/element-hq/element-call?style=flat-square&color=yellow)](https://github.com/element-hq/element-call/stargazers) [![Forks](https://img.shields.io/github/forks/element-hq/element-call?style=flat-square&color=blue)](https://github.com/element-hq/element-call/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Group calls powered by Matrix

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 967 |
| 🍴 **Forks** | 200 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`matrix` `matrixrtc` `videoconference` `voip`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
Element Call is an open‑source, Matrix‑based group‑calling solution written in TypeScript. It provides end‑to‑end encrypted audio/video rooms that can be embedded in any Matrix client or used as a standalone web app, making it a natural fit for teams already on the Element ecosystem.

**Value**  
- Leverages Matrix’s federated identity and encryption model, so users can join calls without creating separate accounts or exposing media streams to third‑party services.  
- Tight integration with Element’s UI and chat features enables seamless transition from text discussion to a voice/video meeting, reducing context‑switching for remote teams.  
- The project’s healthy star/fork count and recent updates (as of 2026‑06‑29) indicate active community interest and a growing ecosystem of plugins and integrations.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the provided Docker compose file, and test a call with a few internal users. Verify that the README steps (building, configuring TURN servers, and linking to a Matrix homeserver) work end‑to‑end.  
2. **Pilot Integration** – Embed the Element Call widget into an existing Element client or a custom web portal using the documented iFrame API. Capture feedback on UI/UX, latency, and any required branding tweaks.  
3. **Security & Ops Review** – Conduct a lightweight security audit (dependency scanning, TURN/STUN configuration, media encryption verification) and confirm that the MIT‑style license aligns with corporate policy.  
4. **Scale‑Up** – Deploy a production‑grade instance behind a load balancer, enable monitoring (Prometheus metrics are included), and set up automated CI/CD pipelines for updates.

**Production Readiness**  
- **Maturity:** Medium. The codebase is actively maintained, but it is still positioned as a prototype/early‑stage product rather than a battle‑tested enterprise service.  
- **Dependencies:** Relies on a Matrix homeserver, a TURN/STUN server for NAT traversal, and Node/TypeScript tooling—components that are well understood but require proper ops handling.  
- **Risk Profile:** No major licensing or metadata concerns, but a final security and maintainer audit is recommended before a public‑facing rollout.  

Overall, Element Call is suitable for internal prototypes, sandbox environments, or organizations already committed to the Matrix ecosystem, provided that a small pilot and due‑diligence phase are completed before full production deployment.

### Русский

**element‑hq/element‑call** — это open‑source‑решение для групповых видеозвонков, построенное на протоколе Matrix. Оно подходит для быстрого прототипирования или внутренних коммуникаций, где требуется интеграция видеосвязи без сторонних сервисов; рекомендуется начать с небольшого proof‑of‑concept, проверив README и текущую активность репозитория. Готовность к production — средняя: проект имеет значительное количество звёзд и форков, свежие коммиты (2026‑06‑29) и написан на TypeScript, но перед масштабным внедрением следует уточнить лицензию, безопасность зависимостей и наличие активных мейнтейнеров.

### 中文

**项目价值**  
`element-hq/element-call` 为 Matrix 生态提供了基于浏览器的多人音视频通话解决方案，能够在已有的 Matrix 聊天室或房间中直接发起和加入群组通话。它使用 WebRTC 实现端到端媒体传输，配合 Matrix 的身份认证与房间管理，实现了统一的安全、跨平台的实时通信体验，特别适合希望在自建或私有 Matrix 服务器上快速加入音视频协作的团队和组织。

**典型接入方式**  

| 步骤 | 说明 |
|------|------|
| 1️⃣ 环境准备 | - 确保已有 Matrix homeserver（Synapse、Dendrite 等）并已启用 VoIP（`m.call`）协议。<br>- 前端项目使用 Node.js ≥18、TypeScript。 |
| 2️⃣ 安装依赖 | ```bash\nnpm i @element-call/sdk @matrix-org/matrix-sdk-crypto-nodejs\n``` |
| 3️⃣ 初始化 SDK | ```ts\nimport { ElementCall } from '@element-call/sdk';\nconst call = new ElementCall({\n  homeserverUrl: 'https://matrix.example.com',\n  accessToken: '<user-access-token>',\n  userId: '@alice:example.com',\n});\n``` |
| 4️⃣ 加入/创建房间 | 使用 Matrix 客户端 API 创建或获取目标房间 ID，然后调用 `call.joinRoom(roomId)` 或 `call.createRoom({name: 'Team Call'})`。 |
| 5️⃣ 启动通话 UI | ```ts\nconst container = document.getElementById('call-root');\ncall.mount(container);\n```<br>`mount` 会自动处理本地媒体获取、信令协商以及 UI 渲染。 |
| 6️⃣ 事件监听（可选） | ```ts\ncall.on('participantsChanged', (list) => console.log('当前参与者', list));\ncall.on('error', (err) => console.error(err));\n``` |
| 7️⃣ 部署 | 将前端构建产物（`npm run build`）部署到 CDN 或静态托管服务，后端只需要保持 Matrix homeserver 与信令服务器（默认使用 Element 提供的公共信令）可达。 |

> **小技巧**：如果不想使用公共信令服务器，可自行部署 `element-call-signalling`（同仓库的 `signalling-server` 目录），只需在 `ElementCall` 初始化时通过 `signallingUrl` 参数指定自建地址。

**生产可用性评估**  

| 维度 | 现状 | 建议 |
|------|------|------|
| **成熟度** | 967 ⭐、200 fork、最近一次提交在 2026‑06‑29，活跃度良好。 | 继续关注 release notes，确保使用的版本已通过安全审计。 |
| **依赖稳定性** | 主要依赖 TypeScript、WebRTC、Matrix SDK，均为成熟生态。 | 在生产环境使用前锁定 `package-lock.json`，并在 CI 中跑 `npm audit`。 |
| **安全性** | 采用端到端加密（Matrix Crypto），但信令通道默认是明文。 | 若对隐私要求高，部署自建信令服务器并启用 TLS。 |
| **可扩展性** | 支持自定义 UI、插件化事件，可与现有 Matrix 客户端无缝集成。 | 对大规模并发（>1000 人）需评估信令服务器和 TURN/STUN 基础设施。 |
| **运维成本** | 前端部署简单，后端仅需保持 Matrix homeserver 与 TURN 服务器可用。 | 建议使用容器化（Docker）部署自建信令服务，配合监控（Prometheus）和自动重启（K8s）。 |
| **生产适配度** | **中等**——适合作为内部协作工具或原型验证；在完成安全审计、信令/TURN 高可用部署后可投入正式业务。 | 在正式上线前进行小规模 POC，验证媒体质量、网络穿透和权限控制。 |

**总结**  
`element-hq/element-call` 为基于 Matrix 的组织提供了一套开箱即用的 WebRTC 群组通话能力，接入门槛低、与现有 Matrix 身份体系天然兼容。通过简单的 SDK 初始化和 UI 挂载即可在自有前端项目中嵌入通话功能。只要在生产环境中自行部署信令和 TURN 服务、完成安全审计并做好监控，它完全可以支撑内部协作乃至面向客户的实时沟通场景。

## 🧭 Practical evaluation

**Value:** element-hq/element-call may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 967 GitHub stars
- 200 forks
- updated 2026-06-29
- primary language: TypeScript
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 58/100 |
| stars | 64/100 |
| topics | 50/100 |
| outlook | 67/100 |
| quality | 70/100 |
| recency | 80/100 |
| adoption | 62/100 |
| production | 68/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/element-hq/element-call) · [← Back to Misc](./README.md)</sub>
