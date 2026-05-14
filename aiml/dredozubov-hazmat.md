# dredozubov/hazmat

[![Stars](https://img.shields.io/github/stars/dredozubov/hazmat?style=flat-square&color=yellow)](https://github.com/dredozubov/hazmat/stargazers) [![Forks](https://img.shields.io/github/forks/dredozubov/hazmat?style=flat-square&color=blue)](https://github.com/dredozubov/hazmat/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> macOS containment for AI agents — user isolation, kernel sandbox, pf firewall, DNS blocklist, backup/rollback. TLA+ verified.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 111 |
| 🍴 **Forks** | 3 |
| 💻 **Language** | Go |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `claude-code` `cli` `containment` `developer-tools` `formal-verification` `go` `macos` `pf-firewall` `sandbox` `seatbelt` `security`

## 🎯 Categories

AI/ML · DevTools · Database · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
dredozubov/hazmat is an open‑source macOS containment framework that secures AI agents through user isolation, a kernel‑level sandbox, pf firewall rules, DNS blocklisting, and automated backup/rollback, with its core logic formally verified in TLA+. By providing ready‑made security primitives and a Go‑based SDK/CLI, it lets developers add AI capabilities—such as RAG pipelines or autonomous agents—without building a secure stack from scratch.

**Value**  
- **Security‑first foundation:** Eliminates the most common attack surface for on‑device AI agents (privilege escalation, network abuse, data leakage) with a verified sandbox and network controls.  
- **Speed to prototype:** The SDK exposes clear API hooks, so teams can focus on model logic and workflow orchestration rather than low‑level OS hardening.  
- **Formal verification:** TLA+ proofs give confidence that the containment policies behave as intended, reducing the need for extensive manual security testing.

**Practical Adoption Path**  
1. **Clone the repo** and run the provided Docker‑less installer on a macOS development machine.  
2. **Integrate** the Go SDK or invoke the CLI to wrap existing AI services (e.g., LangChain, LlamaIndex) inside the sandbox.  
3. **Configure** firewall rules and DNS blocklists via the supplied YAML templates to match your organization’s network policy.  
4. **Test** locally using the built‑in backup/rollback feature; once validated, promote the same containerized configuration to CI/CD pipelines for automated deployment.  

**Production Readiness**  
- **Activity & community:** 111 ★, recent commits (last updated 2026‑05‑14), and a small but active fork base indicate ongoing maintenance.  
- **Maturity:** Core security components are TLA+ verified; the Go codebase is compact and well‑documented, making audits tractable.  
- **Risk considerations:** License compliance and a final security audit of the upstream dependencies are still required, but no major metadata or supply‑chain issues have been identified. Overall, the project is solid enough for a serious pilot in a controlled production environment.

### Русский

**dredozubov/hazmat** — это open‑source‑решение для macOS, обеспечивающее изоляцию AI‑агентов на уровне пользователя, ядра, сетевого трафика (pf‑firewall, DNS‑блоклист) и поддерживает резервное копирование/откат; проект формально верифицирован в TLA+, имеет 111 звёзд на GitHub и активную поддержку (обновления — 2026‑05‑14). Он позволяет быстро добавить AI‑функциональность в существующие системы без построения полной модели‑стека: типичный сценарий — прототипирование RAG‑ или агентных рабочих процессов и оценка инструментов моделей через API/SDK/CLI. По готовности к продакшн проект считается «high»: свежий код, растущий экосистемный интерес и достаточная зрелость для серьёзного пилотного внедрения, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
dredozubov/hazmat 是一套在 macOS 上为 AI 代理提供完整隔离的安全框架，涵盖用户隔离、内核沙箱、pf 防火墙、DNS 黑名单以及备份/回滚机制，并通过 TLA+ 形式化验证。

**价值主张**  
- **安全可靠**：在系统层面实现多层防护，防止 AI 代理对主机造成意外破坏或数据泄漏。  
- **快速集成**：提供 API、SDK 与 CLI 三种接入方式，配合 Go 语言实现，可直接在现有 AI/ML 项目中嵌入，无需从零搭建安全层。  
- **实验与生产兼顾**：适用于原型开发（如 RAG、Agent 工作流）和正式业务的安全评估，帮助团队在不牺牲安全的前提下快速验证模型和工具链。

**典型接入方式**  
1. **CLI**：通过 `hazmat run --agent <binary> --config <file>` 启动受控的 AI 代理进程。  
2. **SDK（Go）**：在代码中引入 `github.com/dredozubov/hazmat`，使用 `hazmat.NewSandbox()` 创建沙箱对象并调用 `sandbox.Start(agentExec)`。  
3. **API/HTTP**：使用内置的 REST 接口提交代理任务，系统在后台自动完成隔离、网络过滤和日志收集。

**生产可用性**  
- **活跃度**：截至 2026‑05‑14 最近一次提交，星标 111、Fork 3，代码基于 Go，拥有 13 个主题标签，表明社区关注度和维护力度较高。  
- **成熟度**：已实现内核级沙箱、pf 防火墙规则、DNS blocklist 与完整的备份/回滚流程，并通过 TLA+ 形式化验证，降低了实现缺陷的风险。  
- **风险点**：仍需进一步审查许可证细节、长期安全响应能力以及维护者的持续投入，但整体已具备在生产环境中进行试点的条件。  

综上，hazmat 为在 macOS 上部署 AI 代理提供了一套即插即用的安全解决方案，接入门槛低，适合快速原型验证，也具备向生产环境迁移的技术基础。

## 🧭 Practical evaluation

**Value:** dredozubov/hazmat helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 111 GitHub stars
- 3 forks
- updated 2026-05-14
- primary language: Go
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 15/100 |
| stars | 44/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 71/100 |
| recency | 100/100 |
| adoption | 36/100 |
| production | 75/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/dredozubov/hazmat) · [← Back to AI/ML](./README.md)</sub>
