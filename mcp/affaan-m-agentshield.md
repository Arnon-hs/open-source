# affaan-m/agentshield

[![Stars](https://img.shields.io/github/stars/affaan-m/agentshield?style=flat-square&color=yellow)](https://github.com/affaan-m/agentshield/stargazers) [![Forks](https://img.shields.io/github/forks/affaan-m/agentshield?style=flat-square&color=blue)](https://github.com/affaan-m/agentshield/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-87%2F100-brightgreen?style=flat-square)](#)

> AI agent security scanner. Detect vulnerabilities in agent configurations, MCP servers, and tool permissions. Available as CLI, GitHub Action, ECC plugin, and GitHub App integration. 🛡️

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 616 |
| 🍴 **Forks** | 131 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 87/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `anthropic` `claude-code` `hackathon` `mcp` `opus` `security`

## 🎯 Categories

MCP · AI/ML · Backend · DevTools · Security

## 📝 Summary

### English

**Brief Summary**  
Agentshield (affaan‑m/agentshield) is an open‑source security scanner that audits AI agent configurations, Model Context Protocol (MCP) servers, and tool permissions for vulnerabilities. It can be run locally via a CLI, integrated into CI/CD pipelines as a GitHub Action, used as an ECC plugin, or deployed as a GitHub App, making it easy to embed security checks throughout the development lifecycle.  

**Value**  
Agentshield gives developers a standardized way to verify that AI assistants are safely connected to external tools and data sources, reducing the risk of privilege‑escalation, data leakage, or mis‑configured MCP endpoints. By surfacing configuration flaws early, it helps teams ship trustworthy AI‑augmented products without having to build custom security tooling from scratch.  

**Practical Adoption Path**  
1. **Local testing** – Install the TypeScript‑based CLI (`npm i -g agentshield`) and scan your agent repo or MCP server during development.  
2. **CI/CD integration** – Add the official GitHub Action to your workflow to automatically run scans on every push or PR, blocking merges on critical findings.  
3. **Enterprise tooling** – Deploy the ECC plugin or GitHub App to centralize scanning across multiple repositories and enforce organization‑wide policies.  
4. **Feedback loop** – Use the generated reports to remediate permission issues, update MCP schemas, and harden tool integrations before release.  

**Production Readiness**  
Agentshield scores 87/100 and shows strong production signals: 616 stars, 131 forks, active commits (last update 2026‑05‑11), a mature TypeScript codebase, and multiple integration options. The project’s recent activity, community adoption, and clear documentation make it suitable for pilot deployments in production environments, though a final review of licensing and ongoing maintainer commitment is advisable before full enterprise rollout.

### Русский

**Agentshield** — это open‑source сканер безопасности AI‑агентов, который проверяет конфигурации агентов, серверы MCP и права доступа к инструментам, предлагая интеграцию через CLI, GitHub Action, ECC‑плагин и GitHub App. Он идеально подходит для компаний, желающих безопасно подключать AI‑ассистентов к реальным сервисам и данным по стандартному Model Context Protocol, а также для быстрой поставки MCP‑серверов и унификации интеграций. Проект имеет высокий уровень готовности к продакшну: активные коммиты, 616 звёзд, широкое принятие в экосистеме и поддержка нескольких способов внедрения, что делает его надёжным кандидатом для серьёзных пилотных запусков.

### 中文

**项目简介**  
affaan-m/agentshield 是一款 AI Agent 安全扫描器，能够自动检测 Agent 配置、MCP（Model Context Protocol）服务器以及工具权限中的潜在漏洞。它提供 CLI、GitHub Action、ECC 插件以及 GitHub App 四种接入方式，帮助团队在连接 AI 助手与真实工具和数据时保持安全合规。🛡️  

**价值**  
- **统一安全标准**：通过标准化的安全检查，确保 AI Agent 与外部工具的交互不泄露敏感信息或被滥用。  
- **多场景覆盖**：既适用于本地开发（CLI），也能在 CI/CD 流水线（GitHub Action）和企业级平台（ECC、GitHub App）中自动化运行。  
- **提升可信度**：在模型上下文协议（MCP）服务器和工具权限层面发现风险，降低因配置错误导致的攻击面。  

**典型接入方式**  
1. **CLI**：在本地或 CI 环境直接运行 `agentshield scan`，快速获取安全报告。  
2. **GitHub Action**：在工作流中添加 `affaan-m/agentshield@vX` 步骤，实现每次代码推送或 PR 自动扫描。  
3. **ECC 插件**：在企业云控制台中安装插件，统一管理组织内所有 Agent 的安全状态。  
4. **GitHub App**：授权后，App 会在仓库事件触发时自动执行扫描，并在 Pull Request 中留下审计评论。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑11，项目拥有 616 ★、131 🍴，最近一次提交仅在数天前，表明维护持续活跃。  
- **技术成熟**：使用 TypeScript 编写，提供完整的 API/SDK 与 CLI，文档清晰，易于集成。  
- **生态兼容**：已在多个公开仓库和企业内部进行试点，兼容主流 CI/CD 平台和云服务。  
- **风险可控**：暂无重大许可证或安全隐患，仍需对维护者和安全审计流程进行最终确认。  

综合来看，agentshield 已具备 **高生产就绪度**，适合作为 AI Agent 与工具链安全防护的首选开源组件。

## 🧭 Practical evaluation

**Value:** affaan-m/agentshield helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 616 GitHub stars
- 131 forks
- updated 2026-05-11
- primary language: TypeScript
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 53/100 |
| stars | 59/100 |
| topics | 88/100 |
| outlook | 88/100 |
| quality | 79/100 |
| recency | 100/100 |
| adoption | 58/100 |
| production | 83/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/affaan-m/agentshield) · [← Back to Mcp](./README.md)</sub>
