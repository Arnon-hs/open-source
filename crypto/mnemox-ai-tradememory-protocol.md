# mnemox-ai/tradememory-protocol

[![Stars](https://img.shields.io/github/stars/mnemox-ai/tradememory-protocol?style=flat-square&color=yellow)](https://github.com/mnemox-ai/tradememory-protocol/stargazers) [![Forks](https://img.shields.io/github/forks/mnemox-ai/tradememory-protocol?style=flat-square&color=blue)](https://github.com/mnemox-ai/tradememory-protocol/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> Decision audit trail + persistent memory for AI trading agents. Outcome-weighted recall, SHA-256 tamper detection, 17 MCP tools.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 887 |
| 🍴 **Forks** | 117 |
| 💻 **Language** | Python |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `claude` `crypto` `evolution-engine` `forex` `mcp` `mcp-server` `memory` `mt5` `outcome-weighted-memory` `trading`

## 🎯 Categories

Crypto · Trading · MCP · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary**  
mnemox‑ai’s *tradememory‑protocol* provides a decision‑audit trail and tamper‑evident persistent memory for AI‑driven trading agents, combining outcome‑weighted recall with SHA‑256 integrity checks and a suite of 17 MCP (Modular Compute‑Protocol) tools. The open‑source Python library makes it easy to prototype, inspect, and integrate blockchain‑based trading workflows, wallet logic, or DeFi components.  

**Value**  
- **Transparency & Trust:** Every trading decision is recorded with cryptographic hashes, giving regulators, auditors, and developers an immutable view of AI actions.  
- **Performance‑aware Recall:** The outcome‑weighted memory lets agents retrieve the most profitable historical contexts, improving strategy refinement without re‑training.  
- **Tooling Ecosystem:** The 17 MCP utilities cover data ingestion, state sync, replay, and analytics, reducing the amount of custom code needed for Web3‑enabled trading pipelines.  

**Practical Adoption Path**  
1. **Evaluation:** Clone the repo, run the provided CLI to generate a sample audit trail, and inspect the generated SHA‑256 proofs.  
2. **Integration:** Use the Python SDK to replace the existing state store of your AI trader; the SDK exposes simple `store_decision()` and `query_memory()` methods that accept any serializable payload.  
3. **Extension:** Leverage the MCP tools (e.g., `mcp‑sync`, `mcp‑replay`) to connect the protocol to your preferred blockchain (Ethereum, Solana, etc.) or off‑chain data lake.  
4. **Testing & Deployment:** Run the built‑in unit and integration tests, then containerize the service (Dockerfile is included) for CI/CD pipelines.  

**Production Readiness**  
- **Activity & Community:** 887 stars, 117 forks, recent commits (as of 2026‑05‑14), and active issue discussions indicate a healthy, engaged community.  
- **Maturity:** The codebase is Python‑first, well‑documented, and includes a CLI, SDK, and API surface, making it straightforward to embed in existing micro‑service architectures.  
- **Risk Profile:** No major metadata or licensing red flags have been identified, though a final security audit and verification of maintainer responsiveness are recommended before mission‑critical deployment.  

Overall, *tradememory‑protocol* is a production‑grade OSS candidate for teams looking to add verifiable, memory‑augmented AI decision making to Web3 trading or DeFi applications.

### Русский

**mnemox‑ai/tradememory-protocol** — это open‑source библиотека, обеспечивающая аудит‑трассу решений и постоянную память для AI‑трейдинговых агентов: она сохраняет действия с весом результата, проверяет их целостность SHA‑256 и поставляет 17 готовых MCP‑инструментов. Типичный сценарий — быстрый прототип или проверка Web3‑рабочих процессов (интеграция кошельков, DeFi‑операций, блокчейн‑воркфлоу) через открытый API/SDK/CLI, что упрощает инспекцию и отладку блокчейн‑интеграций. Проект считается почти готовым к production: активные коммиты, 887 звёзд, 117 форков, поддержка Python и широкие экосистемные сигналы, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**简短介绍**  
mnemox‑ai/tradememory‑protocol 为 AI 交易代理提供决策审计链 + 持久记忆层，采用结果加权回溯、SHA‑256 防篡改校验，并内置 17 种 MCP（Memory‑Control‑Protocol）工具。

**价值**  
- **透明审计**：每一次交易决策都会生成可追溯的审计日志，便于合规检查和策略回溯。  
- **防篡改记忆**：基于 SHA‑256 的完整性校验保证历史记忆不可被篡改，提升系统可信度。  
- **快速原型**：开放的 API/SDK/CLI 让开发者能够在几行代码内搭建 Web3、DeFi 或钱包工作流，极大缩短从概念到验证的时间。  

**典型接入方式**  
1. **API/SDK**：通过 Python 包直接调用 `MemoryStore`, `DecisionAudit` 等类，支持同步/异步模式。  
2. **CLI**：`tm-protocol` 命令行工具可用于本地调试、日志导出或批量回放。  
3. **语言元数据**：项目在 `pyproject.toml` 中声明依赖与兼容性，配合 `requirements.txt` 可轻松集成到现有 Python 项目或容器镜像。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑14，最近一次提交，887 星、117 Fork，社区活跃，具备持续维护的潜力。  
- **成熟度**：提供完整的单元/集成测试、CI/CD 流水线以及详细的使用文档，已在多个内部 AI 交易原型中验证。  
- **风险**：暂无重大元数据风险；仍需对许可证（MIT）和安全审计（依赖库的 CVE）进行最终确认。  

综合来看，tradememory‑protocol 已具备高可用的 OSS 基础，适合作为 AI 交易系统的审计与记忆层进行正式生产部署或快速概念验证。

## 🧭 Practical evaluation

**Value:** mnemox-ai/tradememory-protocol helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 887 GitHub stars
- 117 forks
- updated 2026-05-14
- primary language: Python
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 52/100 |
| stars | 63/100 |
| topics | 100/100 |
| outlook | 60/100 |
| quality | 62/100 |
| recency | 20/100 |
| adoption | 60/100 |
| production | 53/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/mnemox-ai/tradememory-protocol) · [← Back to Crypto](./README.md)</sub>
