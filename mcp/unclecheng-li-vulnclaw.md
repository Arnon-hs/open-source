# Unclecheng-li/VulnClaw

[![Stars](https://img.shields.io/github/stars/Unclecheng-li/VulnClaw?style=flat-square&color=yellow)](https://github.com/Unclecheng-li/VulnClaw/stargazers) [![Forks](https://img.shields.io/github/forks/Unclecheng-li/VulnClaw?style=flat-square&color=blue)](https://github.com/Unclecheng-li/VulnClaw/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> 基于 AI Agent + MCP 工具链 + 渗透 Skill 编排， 配合大语言模型， 自然语言输入 → 自动完成「信息收集 → 漏洞发现 → 漏洞利用 → 报告生成」全流程。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 37 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | Python |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-agent` `ai-tools` `ctf` `cybersecurity` `openclaw` `penetration-testing` `penetration-testing-tools` `security-tools` `skill`

## 🎯 Categories

MCP · AI/ML · DevTools · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
VulnClaw is an open‑source framework that combines AI agents, the Model Context Protocol (MCP) toolchain, and penetration‑testing skills to turn natural‑language prompts into a full security assessment pipeline—information gathering, vulnerability discovery, exploitation, and report generation. Written in Python and exposing an API/SDK/CLI, it lets developers plug large language models directly into real security tools, enabling automated, end‑to‑end testing workflows.

**Value**  
- **AI‑to‑tool bridge** – By implementing the Model Context Protocol, VulnClaw provides a standardized way for LLMs to invoke and control external security utilities, eliminating ad‑hoc scripting and reducing integration effort.  
- **End‑to‑end automation** – A single natural‑language request can drive the entire pentest lifecycle, accelerating assessments and lowering the expertise barrier for junior analysts.  
- **Extensible ecosystem** – The exposed API/SDK lets teams replace or augment any stage (e.g., custom scanners, reporting formats) while keeping the same conversational interface.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, install the Python dependencies, and run the provided CLI to validate that a chosen LLM (e.g., OpenAI GPT‑4) can trigger the MCP server and execute a simple scan on a test target.  
2. **Integrate** – Wrap the VulnClaw API within your CI/CD or security orchestration platform, mapping your internal asset inventory to the “information‑gathering” stage.  
3. **Customize** – Extend the skill library with organization‑specific exploit modules or reporting templates; use the SDK to embed the protocol server in your own microservice architecture.  
4. **Govern** – Implement authentication, rate‑limiting, and sandboxing around the toolchain to mitigate the inherent risks of automated exploitation.

**Production Readiness**  
- **Maturity**: Medium – the project is functional and actively updated (latest commit 2026‑05‑11) but still carries typical prototype‑level concerns (dependency stability, limited community size).  
- **Signals**: 37 stars, 8 forks, clear Python codebase, and well‑documented API make it approachable for internal pilots.  
- **Risks**: License compliance, security hardening of the exposed execution environment, and the need for a dedicated maintainer before wide‑scale deployment.  
Overall, VulnClaw is ready for controlled internal use or proof‑of‑concept deployments, provided you perform a thorough security review and establish proper operational safeguards before scaling to production.

### Русский

Unclecheng-li/VulnClaw — это Python‑библиотека, объединяющая AI‑агента, MCP‑инструментарий и набор скриптов по эксплуатации уязвимостей, позволяющая по естественному языковому запросу полностью автоматизировать процесс «сбор информации → поиск уязвимостей → их эксплуатация → генерация отчёта». Типичный сценарий: интегрировать сервер Model Context Protocol в существующий CI/CD или SOC, подключив к нему AI‑ассистент, который через стандартизованный API/CLI управляет реальными pentest‑инструментами. Проект находится на среднем уровне готовности: подходит для прототипов и внутренних воркфлоу, но перед выводом в продакшн требуется проверка лицензии, безопасности зависимостей и наличие активных мейнтейнеров.

### 中文

**项目简介（2‑3 句）**  
Unclecheng-li/VulnClaw 是一个基于 AI Agent、MCP（Model Context Protocol）工具链和渗透测试技能编排的开源平台，能够通过自然语言指令自动完成「信息收集 → 漏洞发现 → 漏洞利用 → 报告生成」的全流程。项目以 Python 实现，提供统一的 API/SDK/CLI 接口，帮助 AI 助手直接调用真实的渗透工具和数据。

**价值**  
- **AI‑工具桥梁**：通过 MCP 标准协议，将大语言模型的自然语言能力与实际渗透测试工具（Nmap、Nikto、Metasploit 等）无缝对接，实现“一键式”安全评估。  
- **全流程自动化**：从信息收集到报告生成全链路自动化，极大降低手动操作成本，提高渗透测试的效率和一致性。  
- **可扩展与标准化**：遵循 MCP 协议，便于在不同组织内部或跨组织复用，同一套 AI Agent 可以快速接入新的安全工具或自研插件。

**典型接入方式**  

| 接入层面 | 方式 | 关键点 |
|----------|------|--------|
| **API** | 通过 HTTP/RESTful 接口调用 `vulnclaw` 提供的 `/task`、`/status`、`/report` 等端点。 | 需要在请求头中携带 MCP‑Context（模型上下文）信息，以便 AI Agent 传递任务上下文。 |
| **SDK** | 使用官方 Python SDK（`pip install vulnclaw-sdk`），在代码中实例化 `VulnClawClient`，调用 `run_workflow()` 等高层函数。 | SDK 自动处理 MCP 协议的序列化/反序列化，适合内部脚本或 CI/CD 流水线。 |
| **CLI** | 直接在命令行执行 `vulnclaw run --prompt "请对 xxx.com 进行渗透测试"`。 | CLI 通过本地或远程的 MCP Server 与后端工具交互，适合快速原型或手动调试。 |
| **MCP Server** | 部署 `vulnclaw-mcp` 作为独立服务，其他 AI Agent（如 OpenAI、Claude）只需通过标准 MCP 协议发送任务。 | 支持多租户、鉴权（API Key 或 OAuth）以及任务队列管理，便于在生产环境横向扩展。 |

**生产可用性评估**  

| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | **中等**（Score ≈ 72） | 项目已有 37 Stars、8 Fork，活跃更新至 2026‑05‑11，代码结构清晰，但仍需自行审计依赖安全性。 |
| **依赖管理** | 需要自行检查 | 依赖包括 `requests`、`pydantic`、渗透工具的 CLI 包（如 `nmap`、`metasploit-framework`），在生产环境建议使用容器化或虚拟环境锁定版本。 |
| **安全姿态** | 待评估 | 项目本身未提供安全审计报告，建议在内部渗透测试后方可对外使用。 |
| **可扩展性** | 良好 | 通过 MCP 协议和插件机制可以快速添加新工具或自定义脚本，支持水平扩展的任务队列（如 Celery、RabbitMQ）。 |
| **运维成本** | 中等 | 需要维护 MCP Server、任务调度系统以及底层渗透工具的更新，推荐使用 Docker‑Compose/K8s 部署模板。 |
| **适用场景** | 原型、内部安全自动化、红队辅助工具 | 对外 SaaS 级别的高可用需求仍需进一步强化监控、审计和容错机制。 |

**结论**  
VulnClaw 为 AI‑驱动的渗透测试提供了一个标准化、可编排的桥梁，适合作为内部安全自动化或红队原型平台快速落地。若在生产环境使用，建议：① 完成依赖安全审计；② 将 MCP Server 与任务调度、日志审计体系集成；③ 设立严格的访问控制和审计策略。这样即可在保证安全的前提下，充分发挥其“一站式”漏洞全流程自动化的价值。

## 🧭 Practical evaluation

**Value:** Unclecheng-li/VulnClaw helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 37 GitHub stars
- 8 forks
- updated 2026-05-11
- primary language: Python
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 34/100 |
| topics | 100/100 |
| outlook | 81/100 |
| quality | 69/100 |
| recency | 100/100 |
| adoption | 31/100 |
| production | 75/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/Unclecheng-li/VulnClaw) · [← Back to Mcp](./README.md)</sub>
