# deonmenezes/bountyhunter

[![Stars](https://img.shields.io/github/stars/deonmenezes/bountyhunter?style=flat-square&color=yellow)](https://github.com/deonmenezes/bountyhunter/stargazers) [![Forks](https://img.shields.io/github/forks/deonmenezes/bountyhunter?style=flat-square&color=blue)](https://github.com/deonmenezes/bountyhunter/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> Mantis — autonomous offensive-security platform for Claude Code. DISCOVER → REASON → TEST → LEARN over a 7-phase FSM with parallel specialist agents, 3-round Multi-Step Evidence verification, MCP control plane. Evidence, not alerts.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 79 |
| 🍴 **Forks** | 24 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-harness` `ai-agents` `autonomous-agents` `bug-bounty` `claude-code` `mantis` `mcp` `offensive-security` `security`

## 🎯 Categories

MCP · Automation · AI/ML · DevTools · Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
BountyHunter is an open‑source, autonomous offensive‑security platform built on the Mantis framework that lets Claude‑style AI agents execute the full “Discover → Reason → Test → Learn” workflow through a 7‑phase finite‑state machine with parallel specialist agents and multi‑step evidence verification. It provides a standard Model Context Protocol (MCP) control plane that turns AI assistants into “evidence‑driven” tools rather than simple alert generators, exposing a clean API/SDK/CLI for integration.

**Value**  
- **Bridges AI and real tooling** – By exposing a standard MCP interface, BountyHunter lets LLM agents invoke actual security tools, databases, and custom scripts, turning abstract reasoning into concrete, verifiable actions.  
- **Evidence‑first approach** – The platform records and verifies evidence across three verification rounds, reducing false positives and giving security teams auditable proof of each step.  
- **Modular, parallel execution** – Specialist agents run concurrently in a deterministic 7‑phase FSM, accelerating complex attack‑surface assessments while keeping the workflow transparent.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Docker compose or npm scripts, and experiment with the built‑in CLI to trigger a simple “discover” use‑case (e.g., enumerating subdomains).  
2. **Integrate** – Replace the demo agents with your own tool wrappers (e.g., Nessus, Burp, custom scripts) by implementing the MCP‑defined request/response schema; the existing SDK makes this a low‑effort code addition.  
3. **Deploy** – Containerize the MCP control plane and agent pool, configure TLS and authentication, and expose the API to your internal AI orchestration layer or to a Claude‑based assistant.  
4. **Iterate** – Use the built‑in evidence verification logs to fine‑tune prompts and agent behaviours, then expand the FSM phases to cover full penetration‑testing cycles.

**Production Readiness**  
- **Maturity** – Medium. The project is actively maintained (last commit 2026‑05‑13), has 79 ★ and 24 forks, and is written in JavaScript with clear API/CLI entry points, making it suitable for internal prototypes or limited‑scope deployments.  
- **Considerations before production**  
  * **Dependency hygiene** – Review transitive npm packages for known vulnerabilities and lock versions.  
  * **Security posture** – Perform a supply‑chain audit and ensure the MCP endpoints are hardened (TLS, auth, rate limiting).  
  * **License & maintainer support** – Verify the repository’s license compatibility with your stack and confirm an active maintainer or community fallback.  
- **Outcome** – With the above checks, BountyHunter can be promoted to a production‑grade security automation layer for organizations that want AI‑driven, evidence‑backed offensive testing integrated directly into their tooling ecosystem.

### Русский

**deonmenezes/bountyhunter** — это open‑source платформа Mantis, реализующая автономный цикл «DISCOVER → REASON → TEST → LEARN» через 7‑фазный FSM, параллельных специализированных агентов и 3‑кратную проверку Multi‑Step Evidence. Она позволяет быстро подключать AI‑ассистентов к реальным инструментам и данным по единому Model Context Protocol, что удобно для прототипов и внутренних воркфлоу, где требуется стандартизировать интеграцию сервисов (API/SDK/CLI) и собирать проверяемые доказательства вместо простых оповещений. Готовность к production — средняя: проект имеет активные обновления, 79 ★ и 24 fork, но требует дополнительной проверки лицензии, безопасности и поддержки перед масштабным развертыванием.

### 中文

**项目简介**  
deonmenezes/bountyhunter 是基于 Claude Code 的全自动化进攻式安全平台 **Mantis**，通过 7 步状态机（DISCOVER → REASON → TEST → LEARN）并行调度多专长代理，配合 3 轮多步证据验证和 MCP 控制平面，实现“证据而非告警”的安全检测与学习。

**价值主张**  
- 为 AI 助手提供统一的 **Model Context Protocol (MCP)** 接口，能够安全、可靠地调用真实工具和数据库。  
- 将安全检测、漏洞验证等复杂任务抽象为可编排的工作流，降低 AI 与底层系统的集成门槛。  
- 支持多轮证据链验证，提升自动化攻击/防御结果的可信度，适合安全团队、研发平台以及 AI‑Ops 场景。

**典型接入方式**  
1. **API/SDK**：项目提供 HTTP/REST 接口以及 Node.js SDK，直接在现有服务中调用 `discover`, `reason`, `test`, `learn` 等阶段的 API。  
2. **CLI**：通过 `bountyhunter` 命令行工具，可在 CI/CD、脚本或本地调试环境中快速触发工作流。  
3. **MCP 服务器**：部署自带的 Model Context Protocol 服务器，作为统一的协议网关，让任意语言的 AI 助手（Python、Go、Java 等）通过标准协议与平台交互。  

**生产可用性评估**  
- **成熟度**：GitHub 79 星、24 Fork，最近一次提交在 2026‑05‑13，代码以 JavaScript 为主，社区活跃度中等。  
- **适用场景**：适合作为原型、内部安全自动化或研发工具链的实验平台；在正式生产环境使用前，需要完成依赖审计、版本锁定以及安全审查（如许可证合规、容器安全基线）。  
- **风险**：当前缺乏明确的长期维护者信息和完整的安全审计报告，建议在投入生产前进行内部安全评估并制定升级/回滚策略。  

总体而言，bountyhunter 为将 AI 与真实安全工具桥接提供了一个标准化、可扩展的方案，适合在受控环境中快速验证概念并逐步迁移到生产。

## 🧭 Practical evaluation

**Value:** deonmenezes/bountyhunter helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 79 GitHub stars
- 24 forks
- updated 2026-05-13
- primary language: JavaScript
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 41/100 |
| topics | 100/100 |
| outlook | 80/100 |
| quality | 73/100 |
| recency | 100/100 |
| adoption | 39/100 |
| production | 74/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/deonmenezes/bountyhunter) · [← Back to Mcp](./README.md)</sub>
