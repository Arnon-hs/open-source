# apisec-inc/mcp-audit

[![Stars](https://img.shields.io/github/stars/apisec-inc/mcp-audit?style=flat-square&color=yellow)](https://github.com/apisec-inc/mcp-audit/stargazers) [![Forks](https://img.shields.io/github/forks/apisec-inc/mcp-audit?style=flat-square&color=blue)](https://github.com/apisec-inc/mcp-audit/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-79%2F100-brightgreen?style=flat-square)](#)

> See what your AI agents can access. Scan MCP configs for exposed secrets, shadow APIs, and AI models. Generate AI-BOMs for compliance.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 149 |
| 🍴 **Forks** | 37 |
| 💻 **Language** | Python |
| 📈 **Score** | 79/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-security` `ai` `ai-bom` `ai-security` `api-inventory` `appsec` `claude` `cursor` `cyclonedx` `devsecops` `llm` `mcp`

## 🎯 Categories

MCP · AI/ML · Backend · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*apisec‑inc/mcp‑audit* is an open‑source Python tool that scans Managed Cloud Platform (MCP) configurations for exposed secrets, shadow APIs, and AI models, then produces AI‑Bill‑of‑Materials (AI‑BOMs) to support compliance and security reviews. It enables teams to quickly see what data and services their AI agents can reach, helping to harden deployments and meet regulatory requirements. The project is actively maintained, with recent commits, strong community signals, and a clear focus on integrating AI assistants with real‑world tools via the Model Context Protocol.

---

### Value Proposition
- **Visibility & Risk Reduction** – Automatically discovers hidden credentials, undocumented endpoints, and model artifacts that could be abused, giving security teams a single source of truth for AI‑related attack surface analysis.  
- **Compliance Automation** – Generates AI‑BOMs that map each model, dataset, and API to regulatory frameworks (e.g., GDPR, SOC 2), simplifying audit preparation.  
- **Standardized Integration** – By adhering to the Model Context Protocol, it provides a common language for connecting AI agents to backend services, reducing custom‑code overhead and fostering ecosystem interoperability.

### Practical Adoption Path
1. **Pilot Scan** – Clone the repo, configure the MCP credentials, and run `mcp-audit scan` against a non‑production environment to produce an initial report.  
2. **Integrate into CI/CD** – Add the scan as a step in your pipeline (e.g., GitHub Actions or Jenkins) to catch newly introduced secrets or shadow APIs before they reach production.  
3. **Deploy as a Service** – Wrap the CLI/SDK in a lightweight Flask/FastAPI wrapper to expose a REST endpoint that other teams can call to request on‑demand AI‑BOMs.  
4. **Policy Enforcement** – Feed the generated BOMs into existing security policy engines (e.g., OPA, Prisma Cloud) to automatically block non‑compliant deployments.  

### Production Readiness
- **Activity & Community** – 149 ★, 37 forks, last updated on 2026‑05‑12; the repository shows regular commits and issue responses, indicating an active maintainer base.  
- **Maturity** – The codebase is written in Python, a language familiar to most AI/ML teams, and includes clear API/CLI interfaces, making integration straightforward.  
- **Ecosystem Fit** – It already supports the Model Context Protocol, aligning with emerging standards for AI‑tool orchestration, and can be paired with existing security tooling.  
- **Risks** – No major metadata concerns, but a final review of the license (likely Apache‑2.0/ MIT) and a deeper security audit of the scanner itself are advisable before mission‑critical deployment.

Overall, *apisec‑inc/mcp‑audit* is production‑ready for a serious pilot, offering immediate security insight and a clean path to embedding AI‑aware compliance checks into existing DevSecOps workflows.

### Русский

**apisec‑inc/mcp‑audit** — это открытый Python‑инструмент, который сканирует конфигурации MCP, выявляя открытые секреты, «теневые» API и модели ИИ, а также генерирует AI‑BOM для аудита соответствия. Он идеально подходит для быстрого подключения AI‑агентов к реальным сервисам и данным через стандартный Model Context Protocol, позволяя компаниям стандартизировать интеграцию и безопасно развертывать серверы MCP. По показателям активности (149 ★, 37 forks, обновления до 2026‑05‑12) и поддержке экосистемы проект считается готовым к использованию в продакшене после финального обзора лицензии и безопасности.

### 中文

**项目简介（2‑3 句话）**  
apisec‑inc/mcp‑audit 是一款开源安全审计工具，专门扫描 MCP（Model Context Protocol）配置，帮助你快速发现暴露的密钥、影子 API 与 AI 模型，并生成合规所需的 AI‑BOM（物料清单）。它通过统一的协议，让 AI 助手能够安全、可控地接入真实的工具和数据。

**价值**  
- **安全可视化**：一键定位配置中的敏感信息泄露和未授权的 API 调用，降低攻击面。  
- **合规支撑**：自动生成 AI‑BOM，帮助组织满足数据治理、隐私和模型使用的合规要求。  
- **标准化集成**：提供统一的 MCP 接口，使得不同 AI 代理、工具链和后端服务能够在同一协议下互操作，提升开发效率。

**典型接入方式**  
1. **作为 CLI/SDK 使用**：在 CI/CD 流水线或本地开发环境中直接调用 `mcp-audit` 命令或 Python SDK，对 MCP 配置文件或运行时环境进行扫描。  
2. **部署为服务**：将其包装成 REST 或 gRPC 服务，供其他系统（如模型管理平台、API 网关）通过 HTTP/gRPC 调用审计接口，实现实时安全检测。  
3. **集成到 Model Context Protocol 服务器**：在构建 MCP 服务器时引入 `mcp-audit`，在模型注册或调用前自动执行安全审计并返回审计报告。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑12 最近一次提交，项目拥有 149 ⭐、37 🍴，且主要语言为 Python，社区活跃。  
- **成熟度**：具备完整的实现信号（API/SDK/CLI）、语言元数据和细分主题，易于评估与集成。  
- **准备度**：在 OSS 候选中评分 79/100，已显示出高水平的生产就绪度，适合作为正式项目的安全审计组件进行试点。  
- **风险**：目前未发现重大元数据风险，但仍建议在正式使用前完成许可证合规、完整的安全审计以及维护者响应能力的二次确认。

## 🧭 Practical evaluation

**Value:** apisec-inc/mcp-audit helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 149 GitHub stars
- 37 forks
- updated 2026-05-12
- primary language: Python
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 39/100 |
| stars | 46/100 |
| topics | 100/100 |
| outlook | 84/100 |
| quality | 75/100 |
| recency | 100/100 |
| adoption | 44/100 |
| production | 79/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/apisec-inc/mcp-audit) · [← Back to Mcp](./README.md)</sub>
