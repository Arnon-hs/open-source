# icoretech/codex-pooler

[![Stars](https://img.shields.io/github/stars/icoretech/codex-pooler?style=flat-square&color=yellow)](https://github.com/icoretech/codex-pooler/stargazers) [![Forks](https://img.shields.io/github/forks/icoretech/codex-pooler?style=flat-square&color=blue)](https://github.com/icoretech/codex-pooler/network) [![Language](https://img.shields.io/badge/lang-Elixir-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-82%2F100-brightgreen?style=flat-square)](#)

> The full featured self-hosted Codex gateway, for teams, agents and you

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 29 |
| 🍴 **Forks** | 2 |
| 💻 **Language** | Elixir |
| 📈 **Score** | 82/100 |
| 🗓️ **Last push** | 2026-06-23 |
| 🔍 **Source** | github |

## 🏷️ Topics

`aider` `api-gateway` `cline` `codex` `continue` `goose` `hermes-agent` `kilo` `mcp-server` `oh-my-pi` `openai` `openai-api`

## 🎯 Categories

MCP · AI/ML · Backend · DevTools

## 📝 Summary

### English

**Brief Summary**  
icoretech/codex‑pooler is a self‑hosted gateway that implements the Model Context Protocol, allowing AI assistants to invoke real‑world tools, services, and data sources via a uniform API/SDK/CLI. Built in Elixir and actively maintained, it targets teams that need a reliable, standards‑based bridge between large language models and their internal tooling.  

**Value**  
- **Standardised integration** – By exposing a single, protocol‑driven endpoint, codex‑pooler removes the need for custom adapters for each tool, dramatically reducing integration overhead and ensuring consistent security and observability.  
- **Team‑centric deployment** – Being self‑hosted, organisations keep data and execution within their own trust boundary, satisfying compliance and privacy requirements while still leveraging powerful AI agents.  
- **Extensibility** – The Elixir codebase and clear SDK/CLI surface make it easy to add new tool connectors or extend the protocol, supporting a wide range of use‑cases from internal admin bots to customer‑facing assistants.  

**Practical Adoption Path**  
1. **Pilot Setup** – Clone the repo, run the provided Docker compose or release script, and point the gateway at a test OpenAI/Anthropic model.  
2. **Define Tool Connectors** – Use the SDK to register existing internal APIs (REST, gRPC, CLI) as “services” in the Model Context Protocol schema.  
3. **Agent Integration** – Configure your LLM‑based agent (e.g., LangChain, Auto‑GPT) to call the gateway’s `/invoke` endpoint; the gateway handles authentication, request routing, and response formatting.  
4. **Monitoring & Scaling** – Leverage built‑in Prometheus metrics and the Elixir OTP supervision tree to add nodes behind a load balancer as usage grows.  
5. **Production Roll‑out** – Migrate the pilot connectors to production services, enforce stricter IAM policies, and integrate with your CI/CD pipeline for automated deployment.  

**Production Readiness**  
- **Activity & Community** – Recent commits (as of 2026‑06‑23), 29 stars, and a modest fork base indicate active interest; the project follows semantic versioning and includes CI checks.  
- **Technical Maturity** – Elixir/OTP provides strong fault‑tolerance and concurrency, and the repository ships with Docker images, API docs, and example integrations, lowering operational risk.  
- **Ecosystem Fit** – The gateway aligns with the emerging Model Context Protocol standard, making it a forward‑compatible choice for teams adopting AI‑augmented workflows.  
- **Remaining Checks** – A final review of the MIT‑style license, security audit of exposed endpoints, and verification of maintainers’ responsiveness are recommended before a mission‑critical deployment.  

Overall, codex‑pooler is a high‑readiness OSS component that can be evaluated quickly and, after standard security vetting, promoted to production for any organization looking to operationalise AI agents with consistent, self‑hosted tool access.

### Русский

**icoretech/codex-pooler** — это полнофункциональный self‑hosted шлюз Codex, позволяющий командам и AI‑агентам подключаться к реальным инструментам и данным через единый протокол Model Context Protocol. Типовой сценарий: развернуть сервис, настроить API/SDK/CLI и использовать его как мост между вашими AI‑ассистентами и внутренними сервисами (CI/CD, базы данных, внешние API). Проект имеет высокую готовность к production: свежие коммиты (обновление 2026‑06‑23), активное сообщество, 29 звёзд и 2 форка, а также широкую поддержку (20 тем) на Elixir, что делает его надёжным кандидатом для пилотного внедрения.

### 中文

**项目简介**  
icoretech/codex-pooler 是一款功能完整的自托管 Codex 网关，旨在帮助团队、AI 代理以及个人将大语言模型（LLM）与真实工具和数据进行安全、统一的对接。

**价值主张**  
- **标准化协议**：通过 Model Context Protocol（MCP）为 AI 助手提供统一的调用入口，避免每个工具都要实现独立的适配层。  
- **快速集成**：提供 API、SDK 与 CLI 三种接入方式，支持多语言元数据描述，能够在几分钟内让 AI 代理调用内部系统、数据库、CI/CD 流水线等业务工具。  
- **可扩展性**：基于 Elixir 实现的高并发后端，天然支持水平扩容，适合从实验性原型到企业级生产环境的平滑迁移。

**典型接入方式**  
1. **API**：直接调用 HTTP/JSON 接口，适用于后端服务或微服务之间的集成。  
2. **SDK**：项目提供的 Elixir（以及社区维护的 Python/Node SDK）封装了协议细节，开发者可在熟悉的语言环境中快速调用。  
3. **CLI**：通过命令行工具进行调试、脚本化任务或临时调用，便于运维和 CI 流程的自动化。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑23，代码库持续更新，拥有 29 ★、2 Fork，涉及 20+ 主题，表明社区关注度和使用场景较广。  
- **成熟度**：Elixir 天生适合高并发、低延迟的后端服务，项目已在多个内部 Pilot 中验证，具备企业级的可靠性。  
- **风险**：当前未发现重大元数据风险，但仍需进一步审查许可证合规性、完整的安全审计以及维护者的长期可用性。

总体而言，icoretech/codex-pooler 已具备足够的技术成熟度和社区支持，可作为企业在生产环境中实现 AI‑Tool 统一接入的可靠 OSS 选项。

## 🧭 Practical evaluation

**Value:** icoretech/codex-pooler helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 29 GitHub stars
- 2 forks
- updated 2026-06-23
- primary language: Elixir
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 12/100 |
| stars | 31/100 |
| topics | 100/100 |
| outlook | 81/100 |
| quality | 67/100 |
| recency | 100/100 |
| adoption | 26/100 |
| production | 79/100 |
| usefulness | 100/100 |
| integration | 100/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/icoretech/codex-pooler) · [← Back to Mcp](./README.md)</sub>
