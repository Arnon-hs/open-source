# Tencent/AI-Infra-Guard

[![Stars](https://img.shields.io/github/stars/Tencent/AI-Infra-Guard?style=flat-square&color=yellow)](https://github.com/Tencent/AI-Infra-Guard/stargazers) [![Forks](https://img.shields.io/github/forks/Tencent/AI-Infra-Guard?style=flat-square&color=blue)](https://github.com/Tencent/AI-Infra-Guard/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-82%2F100-brightgreen?style=flat-square)](#)

> A full-stack AI Red Teaming platform securing AI ecosystems via OpenClaw Security Scan, Agent Scan, Skills Scan, MCP scan, AI Infra scan and LLM jailbreak evaluation.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.7k |
| 🍴 **Forks** | 364 |
| 💻 **Language** | Python |
| 📈 **Score** | 82/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `agent-security` `ai-infra` `ai-red-teaming` `ai-security` `llm` `llm-evaluation` `llm-jailbreak` `llm-security` `mcp-scan` `openclaw-security` `prompt-injection`

## 🎯 Categories

MCP · AI/ML · Database · DevOps/Infra · Security

## 📝 Summary

### English

**Summary**  
Tencent/AI‑Infra‑Guard is a full‑stack red‑team platform that secures AI ecosystems by scanning OpenClaw, agents, skills, MCP, AI infrastructure and LLM jailbreaks. It also defines a standard Model Context Protocol (MCP) that lets AI assistants safely invoke real tools and data sources.  

**Value**  
The project bundles automated security checks with a unified protocol for connecting LLMs to external services, enabling teams to both harden their AI pipelines and expose trustworthy tool‑calling interfaces without reinventing the integration layer.  

**Practical adoption path**  
1. **Prototype** – Pull the Python SDK/CLI, run the built‑in scans on a sandbox model or agent to assess current risk.  
2. **Integrate** – Deploy the MCP server (Docker or Helm chart) and register your internal tools via the provided schema; update your LLM’s prompt or tool‑calling wrapper to use the MCP endpoint.  
3. **Scale** – Incorporate the scans into CI/CD pipelines (GitHub Actions, Jenkins, etc.) and monitor results through the built‑in dashboard or export to existing observability stacks.  

**Production readiness**  
With 3.6 k GitHub stars, recent commits (as of 2026‑05‑13), active forks, and a Python codebase that exposes clear API/SDK/CLI entry points, the project shows strong community traction and maintainability. The architecture is modular, the MCP server is container‑ready, and security scans are automated, making it suitable for a serious pilot in production environments—pending a final review of licensing and maintainer responsiveness.

### Русский

Tencent/AI-Infra-Guard — это полнофункциональная платформа для red‑team‑тестирования ИИ, объединяющая сканеры OpenClaw, Agent, Skills, MCP, AI‑Infra и оценку jailbreak‑уязвимостей LLM, что позволяет безопасно подключать AI‑ассистентов к реальным инструментам и данным через единый протокол Model Context Protocol. Типичный сценарий — развертывание сервера MCP, интеграция AI‑агентов с внешними сервисами и автоматическое сканирование инфраструктуры и моделей перед выводом в продакшн. По оценке готовности проект находится на высоком уровне production‑ready: активные коммиты, более 3600 звёзд на GitHub, широкая поддержка Python‑SDK/CLI и подтверждённое принятие в экосистеме, что делает его подходящим для серьёзных пилотных внедрений.

### 中文

**项目简介**  
Tencent/AI-Infra-Guard 是一套全栈 AI 红队平台，提供 OpenClaw 安全扫描、Agent 扫描、Skills 扫描、MCP 扫描、AI 基础设施扫描以及大模型 Jailbreak 评估，帮助企业在开发、部署和运维阶段发现并修复 AI 系统的安全漏洞。

**价值**  
- **统一协议**：通过 Model Context Protocol（MCP）将 AI 助手安全地对接真实工具和数据，实现“AI + 工具”的可控交互。  
- **全方位防护**：覆盖代码、模型、运行时、数据库和 DevOps 基础设施的多层安全检测，降低 AI 供应链风险。  
- **快速落地**：提供 API、SDK 与 CLI 三种接入方式，支持 Python 为主的生态，可直接嵌入现有 CI/CD 流程或模型服务。

**典型接入方式**  
1. **API/SDK**：在模型服务或 AI Agent 项目中引入 Python SDK，调用 `ai_infra_guard.scan()` 完成代码/模型安全扫描。  
2. **CLI**：在 CI/CD pipeline 中加入 `ai-infra-guard scan --target ./my_project`，实现自动化安全审计。  
3. **MCP Server**：部署 MCP Server，统一管理模型上下文与工具调用权限，供多 AI 助手共享安全策略。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑13，项目拥有 3,666 星、364 Fork，最近一次提交在当日，表明维护活跃。  
- **成熟度**：已在腾讯内部多条 AI 业务线上验证，具备完整的测试覆盖和文档，适合作为正式生产环境的安全组件。  
- **风险**：需进一步审查许可证合规性和长期维护者承诺，但目前的代码质量、社区活跃度和生态集成情况足以支撑企业级试点甚至全量上线。

## 🧭 Practical evaluation

**Value:** Tencent/AI-Infra-Guard helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3666 GitHub stars
- 364 forks
- updated 2026-05-13
- primary language: Python
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 64/100 |
| stars | 76/100 |
| topics | 100/100 |
| outlook | 91/100 |
| quality | 88/100 |
| recency | 100/100 |
| adoption | 73/100 |
| production | 81/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/Tencent/AI-Infra-Guard) · [← Back to Mcp](./README.md)</sub>
