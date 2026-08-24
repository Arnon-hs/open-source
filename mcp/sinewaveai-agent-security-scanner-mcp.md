# sinewaveai/agent-security-scanner-mcp

[![Stars](https://img.shields.io/github/stars/sinewaveai/agent-security-scanner-mcp?style=flat-square&color=yellow)](https://github.com/sinewaveai/agent-security-scanner-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/sinewaveai/agent-security-scanner-mcp?style=flat-square&color=blue)](https://github.com/sinewaveai/agent-security-scanner-mcp/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Security scanner MCP server for AI coding agents. Prompt injection firewall, package hallucination detection (4.3M+ packages), 1000+ vulnerability rules with AST & taint analysis, auto-fix.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 100 |
| 🍴 **Forks** | 10 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-security` `ai-security` `auto-fix` `claude-code` `cline` `codex` `cursor` `hallucination-detection` `llm-security` `mcp` `mcp-server` `openai-codex`

## 🎯 Categories

MCP · AI/ML · Backend · Security

## 📝 Summary

### English

**Brief Summary**  
sinewaveai/agent-security-scanner-mcp is an open‑source MCP (Model Context Protocol) server that protects AI coding agents from prompt‑injection attacks and package‑hallucination errors. It ships with a 4.3 M‑package hallucination database, more than 1 000 vulnerability rules powered by AST and taint analysis, and an auto‑fix engine, all exposed via a clean API/SDK/CLI.  

**Value**  
The project gives developers a turnkey security layer that can be dropped into any AI‑assistant workflow, turning raw LLM output into safe, verifiable actions. By standardising on MCP, teams can reuse the same scanner across multiple agents and tools, reducing duplicated security effort and enabling consistent policy enforcement (prompt‑injection firewall, dependency safety, code‑vulnerability checks).  

**Practical Adoption Path**  
1. **Prototype** – Pull the repository, run the provided Docker image or npm start script, and point your agent’s MCP client at the server’s endpoint.  
2. **Integrate** – Replace the agent’s direct tool calls with MCP‑wrapped calls; the scanner will automatically inspect prompts, resolve package names against the 4.3 M‑entry database, and apply the AST/taint rules.  
3. **Customize** – Extend the rule set or add organization‑specific policies via the JSON/YAML rule files or the SDK’s rule‑registration API.  
4. **Deploy** – Containerise the server, configure TLS and authentication, and roll it out behind your internal gateway for production workloads.  

**Production Readiness**  
- **Activity & Adoption**: Recent commits (last update 2026‑05‑12), 100 ★, 10 forks, and active discussion in the MCP community indicate healthy momentum.  
- **Technical Maturity**: Implemented in JavaScript with a well‑documented API, CLI, and SDK; supports auto‑fix and real‑time scanning, making it suitable for high‑throughput pipelines.  
- **Risk Profile**: No critical metadata issues identified; the remaining checks (license compliance, formal security audit, maintainer commitment) are routine due‑diligence steps before a full production rollout.  

Overall, the scanner is a strong OSS candidate for pilots and can be promoted to production once the final compliance review is completed.

### Русский

**sinewaveai/agent-security-scanner-mcp** — открытый MCP‑сервер, который защищает AI‑агентов от подстановки запросов и «галлюцинаций» пакетов (база > 4,3 млн пакетов), автоматически обнаруживает более 1000 уязвимостей с помощью AST‑ и taint‑анализов и предлагает автокоррекции. Типичный сценарий: интеграция сервера в пайплайн разработки, где AI‑ассистент взаимодействует с реальными инструментами и данными через Model Context Protocol, получая мгновенную проверку запросов и зависимостей. Проект считается почти готовым к продакшну — активные коммиты, 100+ звёзд, JavaScript‑SDK/CLI и ясные API, однако перед широким внедрением рекомендуется финальная проверка лицензии и поддержки.

### 中文

**项目简介**  
sinewaveai/agent-security-scanner-mcp 是面向 AI 编码助手的安全扫描 MCP（Model Context Protocol）服务器，提供 Prompt 注入防火墙、4.3M+ 包的幻觉检测、基于 AST 与污点分析的 1000+ 漏洞规则以及自动修复功能。

**价值**  
- 为 AI 助手与真实工具、数据的交互构建安全屏障，防止恶意 Prompt 与依赖包幻觉导致的风险。  
- 丰富的漏洞规则和自动修复让开发者在使用 AI 生成代码时无需额外手动审计，提升交付速度与代码质量。  
- 通过标准化的 MCP 接口，帮助企业快速将安全扫描能力嵌入到现有的 AI 编程工作流或自研工具链中。

**典型接入方式**  
1. **API/SDK**：直接调用提供的 HTTP API 或使用官方 JavaScript SDK，将代码片段或依赖清单发送给 MCP 服务，获取安全报告与修复建议。  
2. **CLI**：在 CI/CD 流程中通过 `agent-security-scanner-mcp` 命令行工具执行扫描，适配 GitHub Actions、GitLab CI 等。  
3. **MCP 服务器**：部署为独立的 MCP 服务节点，供多租户 AI 代理通过标准 Model Context Protocol 进行统一访问，实现“一次部署、全局复用”。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑05‑12，仓库拥有 100+ 星、10+ Fork，代码基于 JavaScript，维护频率高。  
- **生态兼容**：提供完整的 API、SDK 与 CLI，支持常见的 CI/CD 平台和容器化部署，易于与现有 DevTools、后端服务对接。  
- **安全与可靠性**：已实现 Prompt 注入防火墙、AST/污点分析以及大规模包幻觉检测，规则库持续更新，具备自动修复能力，适合作为生产环境的安全防线。  
- **风险**：需进一步确认许可证细节、长期维护者承诺以及对内部安全合规的审计结果，但从当前信号来看，已具备在正式业务中试点甚至全量上线的条件。

## 🧭 Practical evaluation

**Value:** sinewaveai/agent-security-scanner-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 100 GitHub stars
- 10 forks
- updated 2026-05-12
- primary language: JavaScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 26/100 |
| stars | 43/100 |
| topics | 100/100 |
| outlook | 55/100 |
| quality | 52/100 |
| recency | 20/100 |
| adoption | 38/100 |
| production | 49/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/sinewaveai/agent-security-scanner-mcp) · [← Back to Mcp](./README.md)</sub>
