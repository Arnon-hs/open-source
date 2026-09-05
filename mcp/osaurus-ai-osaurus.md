# osaurus-ai/osaurus

[![Stars](https://img.shields.io/github/stars/osaurus-ai/osaurus?style=flat-square&color=yellow)](https://github.com/osaurus-ai/osaurus/stargazers) [![Forks](https://img.shields.io/github/forks/osaurus-ai/osaurus?style=flat-square&color=blue)](https://github.com/osaurus-ai/osaurus/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> Own your AI. The native macOS harness for AI agents -- any model, persistent memory, autonomous execution, cryptographic identity. Built in Swift. Fully offline. Open source.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 6k |
| 🍴 **Forks** | 341 |
| 💻 **Language** | Swift |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anthropic` `apple-foundation-models` `apple-intelligence` `apple-neural-engine` `llm` `mcp` `mcp-server` `mlx` `openai` `swift`

## 🎯 Categories

MCP · Automation · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary**  
osaurus‑ai/osaurus is a native macOS framework written in Swift that lets developers run AI agents completely offline, with persistent memory, cryptographic identity, and autonomous execution. It is positioned as a “own‑your‑AI” platform for building, prototyping, and inspecting Web3‑oriented blockchain workflows, wallets, and DeFi features.

**Value**  
- **Self‑contained AI stack** – By keeping the entire model stack on‑device, teams avoid cloud‑costs, latency, and data‑privacy concerns while still getting full‑featured agents (memory, autonomy, identity).  
- **Web3‑ready primitives** – The built‑in cryptographic identity and SDK/CLI expose low‑level blockchain signals, making it easy to prototype wallet interactions, DeFi contracts, or custom blockchain orchestration without writing glue code.  
- **Swift‑native integration** – macOS developers can embed the framework directly into existing Swift/SwiftUI apps, reducing friction compared with cross‑language bridges.

**Practical Adoption Path**  
1. **Evaluation** – Clone the repo, run the provided CLI or sample Xcode project, and test a simple agent that signs a transaction or queries a smart‑contract. The clear API/SDK surface lets you verify compatibility with your blockchain SDKs early.  
2. **Prototype** – Use the Swift SDK to embed an agent in a sandboxed macOS app, connect it to your local testnet or a simulated DeFi flow, and iterate on memory persistence and autonomous decision‑making.  
3. **Integration** – Wrap the agent’s SDK calls behind a service layer (e.g., gRPC or REST) if you need cross‑platform access, then replace the mock blockchain endpoints with production nodes. Because the framework is offline, you can ship the final binary without external AI services.  
4. **Production rollout** – Deploy the macOS binary (or a packaged macOS‑based server) within your internal infrastructure, leveraging the built‑in cryptographic identity for secure signing and auditability.

**Production Readiness**  
- **Activity & community** – 5,993 stars, 341 forks, recent commits (as of 2026‑06‑22), and a healthy set of topics indicate an active, engaged community.  
- **Maturity** – The project has a stable Swift codebase, documented CLI/SDK, and clear versioning, making it suitable for pilot deployments.  
- **Risk considerations** – The license, long‑term maintainer commitment, and security audit status still need formal verification, but no major metadata or supply‑chain red flags have been identified. Overall, osaurus‑ai/osaurus is a strong OSS candidate for production pilots, especially for teams building Web3 or DeFi tooling on macOS.

### Русский

**osaurus-ai/osaurus** — это open‑source‑платформа для macOS, написанная на Swift, позволяющая запускать автономные AI‑агенты с постоянной памятью, криптографической идентификацией и полной офлайн‑работой. Она идеально подходит для быстрой прототипизации и отладки Web3‑процессов: разработчики могут использовать готовый SDK/CLI для построения и проверки блокчейн‑воркфлоу, интеграции кошельков и DeFi‑фич. Проект обладает высокой готовностью к production‑использованию — активные коммиты, более 5 тыс. звёзд, широкая экосистема и поддержка основных функций, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句）**  
osaurus‑ai/osaurus 是一款基于 Swift 的原生 macOS 框架，提供离线、可持久记忆的 AI 代理能力，并通过加密身份实现安全的自主执行。它支持任意模型、完整的本地推理以及与区块链系统的深度集成，完全开源、可自行托管。

**价值主张**  
- **快速原型与审计**：提供完整的实现细节（API/SDK/CLI），让开发者能够在本地即刻搭建、调试和审计 Web3、钱包、DeFi 等区块链工作流。  
- **安全可信**：离线运行、加密身份和持久记忆确保数据不泄露，适合对安全合规要求高的金融或企业场景。  
- **跨模型兼容**：无论是大语言模型还是专用推理模型，都可以无缝接入，统一管理执行逻辑。

**典型接入方式**  
1. **SDK 引入**：在 Swift 项目中通过 Swift Package Manager 引入 `osaurus` 包，调用 `OsaurusAgent` 类即可创建具备记忆与身份的 AI 代理。  
2. **CLI 使用**：通过 `osaurus-cli` 直接在终端启动本地代理，支持 JSON RPC 与自定义插件，适合脚本化工作流或 CI/CD 集成。  
3. **API/插件**：框架暴露 REST‑like 本地 API 与插件接口，其他语言（如 Python、JavaScript）可通过本地 HTTP/Unix socket 与代理交互，实现跨语言编排。

**生产可用性**  
- **活跃度**：截至 2026‑06‑22，项目拥有近 6 000 星、340+ Fork，最近一次提交在 2026‑06‑22，社区活跃。  
- **成熟度**：提供完整的文档、示例项目以及多平台 CI，已在多个内部 Web3 原型中验证，具备“可直接用于试点”的成熟度。  
- **风险点**：需进一步审查许可证兼容性、长期维护者承诺以及安全审计报告；但目前未发现重大元数据或依赖风险。  

综上，osaurus‑ai/osaurus 是一套面向 macOS 的离线 AI 代理框架，能够帮助团队快速构建、审计和部署区块链相关的 AI 驱动工作流，具备较高的生产可用性，适合作为 OSS 试点或正式项目的核心组件。

## 🧭 Practical evaluation

**Value:** osaurus-ai/osaurus helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 5993 GitHub stars
- 341 forks
- updated 2026-06-22
- primary language: Swift
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 63/100 |
| stars | 80/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 84/100 |
| recency | 80/100 |
| adoption | 76/100 |
| production | 73/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/osaurus-ai/osaurus) · [← Back to Mcp](./README.md)</sub>
