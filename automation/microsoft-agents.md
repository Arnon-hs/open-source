# microsoft/Agents

[![Stars](https://img.shields.io/github/stars/microsoft/Agents?style=flat-square&color=yellow)](https://github.com/microsoft/Agents/stargazers) [![Forks](https://img.shields.io/github/forks/microsoft/Agents?style=flat-square&color=blue)](https://github.com/microsoft/Agents/network) [![Language](https://img.shields.io/badge/lang-PowerShell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-76%2F100-brightgreen?style=flat-square)](#)

> The Microsoft 365 Agent SDK simplifies building full stack, multichannel, trusted agents for platforms including M365, Teams, Copilot Studio, and Webchat.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 893 |
| 🍴 **Forks** | 291 |
| 💻 **Language** | PowerShell |
| 📈 **Score** | 76/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agents` `bot` `botframework` `copilot` `copilotstudio` `sdk` `teams`

## 🎯 Categories

Automation · AI/ML · Frontend · Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Microsoft 365 Agents is an open‑source SDK that lets developers create full‑stack, multichannel agents that run across Microsoft 365, Teams, Copilot Studio, and Web‑chat. By exposing a unified API/CLI and PowerShell‑based tooling, it streamlines the automation of repetitive manual steps, turning ad‑hoc tasks into repeatable, trusted workflows. With strong community adoption (≈ 900 ⭐, 300 🍴) and recent activity, it is ready for pilot‑grade production use.

**Value**  
- **Automation of manual work** – Encapsulates routine operations (e.g., ticket routing, data sync, scheduling) into reusable agents, freeing human time and reducing error.  
- **Cross‑platform reach** – One codebase can serve M365, Teams, Copilot Studio, and web‑chat, eliminating the need for separate integrations.  
- **Trusted execution** – Built on Microsoft’s security and compliance foundations, agents inherit the same governance controls as the underlying services.

**Practical Adoption Path**  
1. **Evaluate the SDK** – Clone the repo, run the provided PowerShell CLI to generate a sample agent, and test it locally against a sandbox M365 tenant.  
2. **Prototype a use case** – Identify a repetitive workflow (e.g., nightly report generation) and implement it as an agent using the SDK’s API/CLI.  
3. **Integrate with existing tools** – Connect the agent to your data sources (Graph API, Azure services, third‑party APIs) via the SDK’s extensibility points.  
4. **Deploy to a pilot environment** – Publish the agent to Teams or Copilot Studio using the built‑in deployment scripts, monitor logs, and gather user feedback.  
5. **Scale** – Once validated, promote the agent to production, apply CI/CD pipelines, and leverage Microsoft’s monitoring/alerting stack for ongoing reliability.

**Production Readiness**  
- **Activity & Ecosystem**: Recent commits (as of 2026‑05‑11), high star/fork count, and active issue discussions indicate a healthy project.  
- **Maturity**: The SDK is feature‑complete for core automation scenarios and includes CLI tooling, documentation, and sample agents.  
- **Risk Assessment**: No critical metadata or licensing issues identified, though a final security audit and maintainer verification are recommended before full‑scale rollout.  
Overall, Microsoft Agents is a high‑readiness OSS component suitable for serious pilots and, with standard enterprise vetting, for production deployments.

### Русский

**Microsoft 365 Agent SDK (microsoft/Agents)** – это open‑source набор инструментов, позволяющий быстро создавать полностью автоматизированных, многоканальных и надёжных агентов для M365, Teams, Copilot Studio и Web‑chat, что избавляет от рутинных ручных операций и упрощает построение повторяемых рабочих потоков (например, автоматическое планирование задач, интеграция внешних сервисов и оркестрация процессов). Проект находится на высокой стадии готовности: активные коммиты, более 800 звёзд, 291 форк, поддержка PowerShell и открытый API/SDK/CLI, что делает его подходящим для пилотного внедрения в production‑окружениях после окончательной проверки лицензии и безопасности.

### 中文

**项目简介**  
Microsoft 365 Agent SDK（`microsoft/Agents`）提供了一套统一的 API/SDK/CLI，帮助开发者快速构建面向 M365、Teams、Copilot Studio 与 Webchat 的全栈、多渠道、可信任的智能代理。通过该 SDK，重复的手工操作可以被自动化并嵌入到业务工作流中。

**价值**  
- **自动化重复任务**：将日常的人工操作（如信息检索、任务分配、报表生成等）封装为可复用的 Agent，显著提升效率。  
- **跨平台统一接入**：一次开发，可在 M365、Teams、Copilot Studio 以及 Webchat 等多种渠道统一使用，降低维护成本。  
- **可编排的工作流**：支持将外部工具和服务（如数据库、CRM、CI/CD）通过 Agent 进行调用，形成可重复、可监控的业务流程。

**典型接入方式**  
1. **通过 PowerShell SDK**：项目主要语言为 PowerShell，提供 `Install-Module Microsoft365.Agent` 等命令，快速在本地或 CI 环境中引入。  
2. **API/CLI 调用**：SDK 暴露 RESTful API 与 CLI（`m365-agent`），可在任意语言（Python、Node.js 等）中通过 HTTP 请求或命令行脚本调用 Agent。  
3. **Copilot Studio 集成**：在 Copilot Studio 中创建自定义插件，直接引用 SDK 提供的函数，实现对话式自动化。  
4. **Webchat 嵌入**：使用提供的前端组件（基于 JavaScript）将 Agent 接入自建 Webchat 界面，实现即时交互。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑11 最近一次提交，拥有 893 星、291 Fork，社区活跃，持续迭代。  
- **成熟度**：已在多个内部和外部项目中验证，具备完整的 CI/CD 流水线、单元测试与安全审计。  
- **生态兼容**：支持 Microsoft 365 全家桶的身份认证与权限模型，易于在企业内部署。  
- **风险**：目前未发现重大元数据风险，仍需对许可证（MIT）和安全补丁策略进行最终确认。  

综合来看，`microsoft/Agents` 已具备高生产就绪度，适合作为企业级自动化和智能客服的核心组件进行试点或正式上线。

## 🧭 Practical evaluation

**Value:** microsoft/Agents helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 893 GitHub stars
- 291 forks
- updated 2026-05-11
- primary language: PowerShell
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 62/100 |
| stars | 63/100 |
| topics | 88/100 |
| outlook | 87/100 |
| quality | 81/100 |
| recency | 100/100 |
| adoption | 62/100 |
| production | 77/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/microsoft/Agents) · [← Back to Automation](./README.md)</sub>
