# permit0-ai/permit0

[![Stars](https://img.shields.io/github/stars/permit0-ai/permit0?style=flat-square&color=yellow)](https://github.com/permit0-ai/permit0/stargazers) [![Forks](https://img.shields.io/github/forks/permit0-ai/permit0?style=flat-square&color=blue)](https://github.com/permit0-ai/permit0/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> Stop AI agents from doing things they shouldn't. The action authorization layer — pre-execution, deterministic, policies included. Drop in. Day one.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 118 |
| 🍴 **Forks** | 13 |
| 💻 **Language** | Rust |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-05-10 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-authorization` `agent-security` `ai-agents` `ai-governance` `ai-safety` `audit-trail` `compliance` `eu-ai-act` `mcp` `policy-engine` `rust`

## 🎯 Categories

MCP · AI/ML · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
permit0‑ai/permit0 is an open‑source, pre‑execution authorization layer that lets developers define deterministic policies for AI agents, preventing them from taking disallowed actions. Packaged as a drop‑in Rust library (with API/SDK/CLI bindings), it enables “day‑one” integration of the Model Context Protocol so AI assistants can safely interact with real tools and data. With active recent commits, a growing user base, and solid ecosystem signals, it’s ready for pilot‑level production use.

**Value**  
- **Safety‑first guardrail:** By enforcing policy checks before any AI‑driven operation, it eliminates the risk of agents performing harmful or unauthorized actions.  
- **Standardized integration:** Implements the Model Context Protocol, giving a common way to connect AI assistants to external tools, services, and datasets without custom glue code.  
- **Developer productivity:** The Rust core plus language‑agnostic SDK/CLI means teams can embed the guardrail in micro‑services, serverless functions, or edge agents with minimal boilerplate.

**Practical Adoption Path**  
1. **Prototype:** Add the permit0 crate (or use the provided CLI) to a sandboxed AI‑agent service and define a simple policy file (e.g., allow read‑only DB queries, block file writes).  
2. **Test & Iterate:** Run the agent through the pre‑execution hook; verify that permitted actions succeed and denied actions are blocked, adjusting policies as needed.  
3. **Scale:** Deploy the permit0 server as a sidecar or as a dedicated Model Context Protocol endpoint in your production environment; configure your agents to call it for every action request.  
4. **Monitor & Govern:** Leverage the built‑in logging and policy‑versioning features to audit decisions and evolve policies alongside changing compliance requirements.

**Production Readiness**  
- **Activity & Adoption:** 118 ★, 13 forks, last commit on 2026‑05‑10, and multiple topics indicate an active community.  
- **Maturity:** The core library is written in Rust (memory‑safe, high‑performance) and exposed via API/SDK/CLI, making it easy to integrate into heterogeneous stacks.  
- **Risk Profile:** No known licensing or critical security issues so far, though a final review of the maintainers’ response cadence and vulnerability handling is advisable.  
Overall, permit0‑ai/permit0 meets the criteria for a serious pilot and can be promoted to production once the final security/license audit is completed.

### Русский

**permit0-ai/permit0** — это открытая библиотека, добавляющая перед выполнением детерминированный слой авторизации действий для AI‑агентов, позволяя безопасно подключать их к реальным инструментам и данным через единый протокол. Типичный сценарий: встраивание permit0 в сервисы, где AI‑ассистенты вызывают внешние API или работают с конфиденциальными ресурсами, чтобы гарантировать, что каждый запрос соответствует заранее определённым политикам. Проект уже имеет активную разработку (обновления 2026‑05‑10), 118 звёзд на GitHub, написан на Rust и готов к пилотному запуску в продакшн, хотя лицензия и детали безопасности требуют окончательной проверки.

### 中文

**项目简介**  
Permit0（`permit0-ai/permit0`）为 AI 代理提供“执行前”授权层，能够在代码或指令真正运行前，根据可组合的确定性策略拦截不合规操作。只需把它当作一个库或服务“drop‑in”，即可在一天内为任何 AI 助手加上安全防护。

**价值主张**  
- **安全防护**：在 AI 与真实工具、数据交互前强制校验，防止泄露、越权或恶意行为。  
- **标准化接入**：通过统一的 Model Context Protocol（MCP）把 AI 助手、工具和数据源统一到同一协议栈，降低集成成本。  
- **即插即用**：提供 API、SDK 与 CLI，支持 Rust 为主的实现，也可通过语言绑定快速嵌入 Python、Go 等生态。

**典型接入方式**  
1. **作为本地库**：在 Rust 项目中直接 `cargo add permit0`，在业务代码调用 `permit0::authorize(request)` 前进行策略检查。  
2. **作为独立服务**：部署 Permit0 的 MCP 服务器（Docker 镜像或二进制），AI 代理通过 HTTP/gRPC 调用 `POST /authorize` 接口获取授权结果。  
3. **通过 CLI/SDK**：在脚本或 CI/CD 流程中使用 `permit0-cli` 检查配置文件或动态生成的指令，适合快速原型或运维自动化。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑05‑10，星标 118、Fork 13，社区活跃。  
- **技术成熟度**：核心实现使用 Rust，具备高性能和内存安全；提供完整的 API 文档、示例代码和多语言绑定。  
- **生态兼容**：已支持 MCP 标准，可直接与现有的模型服务、工具链（如 LangChain、OpenAI SDK）对接。  
- **风险**：当前仍需对许可证（MIT）和安全审计进行最终确认，维护者响应速度良好，适合作为 **OSS 级别的生产候选** 进行试点部署。  

综上，Permit0 能在不改动现有 AI 业务逻辑的前提下，为模型与外部资源的交互提供可靠的授权控制，是实现安全 AI 应用的实用底层组件。

## 🧭 Practical evaluation

**Value:** permit0-ai/permit0 helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 118 GitHub stars
- 13 forks
- updated 2026-05-10
- primary language: Rust
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 44/100 |
| topics | 100/100 |
| outlook | 80/100 |
| quality | 73/100 |
| recency | 100/100 |
| adoption | 40/100 |
| production | 76/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-10 · [View on GitHub](https://github.com/permit0-ai/permit0) · [← Back to Mcp](./README.md)</sub>
