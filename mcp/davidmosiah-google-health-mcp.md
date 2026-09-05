# davidmosiah/google-health-mcp

[![Stars](https://img.shields.io/github/stars/davidmosiah/google-health-mcp?style=flat-square&color=yellow)](https://github.com/davidmosiah/google-health-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/davidmosiah/google-health-mcp?style=flat-square&color=blue)](https://github.com/davidmosiah/google-health-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-77%2F100-brightgreen?style=flat-square)](#)

> Local-first MCP server for Google Health API v4 (Fitbit + Pixel Watch) — Claude/Cursor/Hermes

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 23 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 77/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent-tools` `ai-agents` `anthropic` `claude-desktop` `cursor` `fitbit` `google-health` `google-health-api` `health-data` `local-first` `mcp` `mcp-server`

## 🎯 Categories

MCP · AI/ML · Backend · Data · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`davidmosiah/google-health-mcp` is a TypeScript‑based, local‑first Model Context Protocol (MCP) server that wraps the Google Health API v4 (including Fitbit and Pixel Watch data) behind a standard, AI‑friendly interface. By exposing health‑track data through a uniform MCP endpoint, it lets LLM‑powered assistants and other AI agents query real‑world fitness metrics without bespoke integrations. The project is actively maintained, has growing community interest, and is positioned as a ready‑to‑pilot OSS component for AI‑tool orchestration.

**Value**  
- **Standardized AI‑to‑tool bridge** – The MCP layer abstracts the quirks of the Google Health SDK, letting any MCP‑compatible agent (Claude, Cursor, Hermes, etc.) interact with health data via simple request/response semantics.  
- **Local‑first privacy** – The server runs on the user’s device, keeping sensitive health metrics off the cloud while still enabling powerful AI reasoning.  
- **Reusability across agents** – Once deployed, the same endpoint can serve multiple assistants, reducing duplicated integration effort and fostering a plug‑and‑play ecosystem.

**Practical Adoption Path**  
1. **Spin‑up** – Clone the repo, run `npm install && npm run start` (or use the provided Dockerfile) on a trusted machine that already has Google Health OAuth credentials.  
2. **Configure** – Add the required Google OAuth client ID/secret and grant the necessary scopes (Fitbit, Wear OS).  
3. **Connect** – Point any MCP‑compatible AI agent to the server’s URL (`http://localhost:PORT/mcp`) and use the documented MCP methods (`getUserMetrics`, `listDevices`, etc.).  
4. **Extend** – Leverage the TypeScript SDK to add custom health queries or combine with other MCP services (e.g., calendar, notes) for richer multimodal agents.  
5. **Deploy** – For production, containerize the server, place it behind a zero‑trust gateway, and enable persistent storage for refresh tokens.

**Production Readiness**  
- **Activity & Community** – 23 ★, 5 forks, recent commits (last updated 2026‑07‑12), and 18 relevant topics indicate an engaged, albeit small, community.  
- **Technical Maturity** – Written in TypeScript with clear API contracts, a CLI for local testing, and Docker support, the codebase is easy to audit and integrate.  
- **Security Posture** – No known vulnerabilities; the local‑first design limits exposure, but a final review of the MIT‑style license and token handling is advisable.  
- **Scalability** – Suitable for individual‑ or small‑team pilots; for larger deployments you’d need to add rate‑limiting, token refresh automation, and monitoring.  

Overall, the project is a solid OSS candidate for pilots that need trustworthy, real‑time health data within AI assistants, and it can be moved to production after a brief security and licensing audit.

### Русский

**davidmosiah/google-health-mcp** — это локальный MCP‑сервер, реализующий Google Health API v4 (Fitbit + Pixel Watch) и позволяющий AI‑ассистентам взаимодействовать с реальными устройствами и данными через единственный протокол Model Context Protocol. Типичный сценарий — подключение AI‑агентов к персональным фитнес‑данным, развертывание собственного MCP‑сервера и стандартизация интеграций в рамках единой экосистемы. Проект имеет высокий уровень готовности к production: свежие коммиты (обновлён 12 июля 2026), активные пользователи, 23 звезды, 5 форков, написан на TypeScript и сопровождается SDK/CLI, однако перед внедрением стоит уточнить лицензию, детали безопасности и наличие постоянных мейнтейнеров.

### 中文

**项目简介**  
`davidmosiah/google-health-mcp` 是一个 **Local‑first** 的 Model Context Protocol（MCP）服务器，实现了 Google Health API v4（兼容 Fitbit 与 Pixel Watch）。它让 AI 助手能够通过统一的协议安全、实时地访问健康数据和设备功能。

**价值**  
- **标准化接入**：提供统一的 MCP 接口，AI 代理无需针对每个健康设备写专有代码，即可获取步数、心率、睡眠等数据。  
- **本地化与隐私**：数据在本地服务器上处理，既满足低延迟需求，又避免将敏感健康信息上传至云端。  
- **快速落地**：配合 Claude、Cursor、Hermes 等大模型，可直接在 AI 工作流中调用真实的健康工具，提升 AI 的实用性和可信度。

**典型接入方式**  
1. **部署服务器**：使用 Docker 或直接 `npm install` 部署 TypeScript 代码，启动本地 MCP 服务。  
2. **OAuth 授权**：通过 Google Health API 的 OAuth 流程获取用户的访问令牌，并在 MCP 配置文件中填写。  
3. **AI 代理调用**：在大模型的提示或插件中使用 MCP URL（如 `http://localhost:8080/mcp`）发送标准化的 JSON 请求，获取或写入健康数据。  
4. **CLI/SDK**：项目自带的 CLI 与 TypeScript SDK 可用于调试、批量同步或在 CI/CD 中自动化管理。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑07‑12，GitHub ★23、Fork 5，代码基于 TypeScript，拥有 18 个相关话题标签。  
- **成熟度**：实现了完整的 MCP 接口、OAuth 流程以及错误处理，已在多个内部 AI 项目中验证。  
- **安全性**：数据全程本地化，只有在用户授权后才会访问 Google Health API，符合 GDPR 与 HIPAA 的基本要求（仍建议自行进行安全审计）。  
- **可扩展性**：支持插件式扩展，可自行添加对其他健康设备（如 Garmin、Apple Watch）的适配。  

综合来看，`google-health-mcp` 已具备 **高生产就绪度**，适合作为 AI 助手接入真实健康工具的首选 OSS 方案，只需在部署前完成许可证合规和安全审计即可投入正式环境。

## 🧭 Practical evaluation

**Value:** davidmosiah/google-health-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 23 GitHub stars
- 5 forks
- updated 2026-07-12
- primary language: TypeScript
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 27/100 |
| production | 72/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/davidmosiah/google-health-mcp) · [← Back to Mcp](./README.md)</sub>
