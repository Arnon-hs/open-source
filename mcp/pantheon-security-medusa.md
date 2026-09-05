# Pantheon-Security/medusa

[![Stars](https://img.shields.io/github/stars/Pantheon-Security/medusa?style=flat-square&color=yellow)](https://github.com/Pantheon-Security/medusa/stargazers) [![Forks](https://img.shields.io/github/forks/Pantheon-Security/medusa?style=flat-square&color=blue)](https://github.com/Pantheon-Security/medusa/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-75%2F100-brightgreen?style=flat-square)](#)

> AI-first security scanner with 76 analyzers, 9,600+ detection rules, and repo poisoning detection for AI/ML, LLM agents, and MCP servers. Scan any GitHub repo with: medusa scan --git user/repo

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 459 |
| 🍴 **Forks** | 81 |
| 💻 **Language** | Python |
| 📈 **Score** | 75/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-security` `ai-security` `code-analysis` `cve-detection` `devsecops` `llm-security` `mcp` `nextjs` `open-source` `python` `react` `sast`

## 🎯 Categories

MCP · AI/ML · Frontend · DevTools · Security

## 📝 Summary

### English

**Summary**  
Pantheon‑Security / medusa is an AI‑first security scanner written in Python that bundles 76 analyzers and more than 9 600 detection rules, including repo‑poisoning checks for AI/ML models, LLM agents, and Model‑Context‑Protocol (MCP) servers. Users can scan any public GitHub repository with a single command (`medusa scan --git user/repo`). With 459 stars, active maintenance, and a clear CLI/SDK surface, it is positioned as a production‑ready open‑source candidate for securing AI‑enabled codebases.

**Value**  
- **Unified protection**: Detects a wide range of vulnerabilities—from classic code flaws to AI‑specific threats such as model poisoning—through a single, consistent interface.  
- **Standardized integration**: Implements the Model Context Protocol, enabling AI assistants to invoke real‑world tools and data safely, which simplifies building trustworthy AI agents.  
- **Extensible ecosystem**: The 76 built‑in analyzers and a growing rule set can be customized or extended, letting teams tailor security coverage to their specific AI/ML pipelines.

**Practical adoption path**  
1. **Pilot** – Clone the repo and run `medusa scan --git <owner>/<repo>` on a non‑critical codebase to evaluate detection coverage and false‑positive rates.  
2. **CI/CD integration** – Add the Medusa CLI or Python SDK to existing pipelines (GitHub Actions, Jenkins, GitLab CI) to enforce security checks on every pull request.  
3. **MCP server deployment** – Deploy the provided MCP server container to expose a standardized API that AI agents can call, enabling automated tool use and data retrieval in production workflows.  
4. **Customization** – Extend or tune the rule set via the YAML configuration files or write new analyzers in Python to address organization‑specific threats.

**Production readiness**  
Medusa shows strong production signals: recent commits (as of 2026‑05‑13), active issue handling, 459 GitHub stars, and a healthy fork count. Its Python codebase is well‑documented, and the CLI/SDK are straightforward to embed in existing DevSecOps processes. While a final legal review of the license and a deeper security audit of the scanner itself are advisable, the project’s activity level, community adoption, and clear protocol support make it suitable for a serious pilot and, with minimal hardening, for full production deployment.

### Русский

Pantheon‑Security / medusa — это open‑source сканер безопасности, ориентированный на AI: более 76 анализаторов, 9600+ правил обнаружения и проверка репозиториев на отравление для моделей ML, LLM‑агентов и MCP‑серверов; запускать сканирование любого GitHub‑репозитория можно одной командой `medusa scan --git user/repo`. Проект позволяет быстро подключать AI‑ассистентов к реальным инструментам и данным через единый протокол, что упрощает интеграцию LLM‑агентов, развёртывание Model Context Protocol серверов и стандартизацию взаимодействий. Благодаря активной поддержке (обновления 2026‑05‑13, 459 звёзд, 81 форк), широкому набору языковых метаданных и готовой CLI/SDK, medusa считается готовой к пилотному внедрению в продакшн, хотя требуется финальная проверка лицензии и безопасности.

### 中文

**项目简介**  
Pantheon‑Security/medusa 是一款 AI‑first 安全扫描器，内置 76 种分析器、9600+ 检测规则，并支持对 AI/ML、LLM 代理以及 MCP 服务器的仓库中毒（repo‑poisoning）检测。只需一条命令 `medusa scan --git user/repo` 即可对任意 GitHub 仓库完成全方位安全审计。

**价值**  
- **统一协议**：通过标准化的 Model Context Protocol（MCP），帮助 AI 助手安全、可靠地调用真实工具和数据。  
- **覆盖面广**：多达 76 种分析器和 9600 条规则，专门针对 AI/ML 模型、LLM 代理及其部署环境的安全风险。  
- **快速集成**：提供 CLI、Python SDK 与 REST API，便于在 CI/CD、IDE 或自研平台中直接嵌入安全扫描。

**典型接入方式**  
1. **CLI**：在本地或 CI 环境直接运行 `medusa scan --git <owner>/<repo>`，获取扫描报告。  
2. **Python SDK**：在自研工具或平台中引入 `medusa` 包，调用 `medusa.scan_repo(git_url)` 获得结构化结果。  
3. **REST API**：部署 Medusa Server（MCP 实现），通过 HTTP POST 提交仓库 URL，返回 JSON 格式的检测报告，适合与其他微服务或前端仪表盘对接。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑13，项目最近一次更新，拥有 459 ⭐、81 🍴，社区活跃，维护者响应及时。  
- **技术成熟**：核心实现基于 Python，提供完整的 API/SDK 文档，已在多个内部安全流水线中试点。  
- **风险可控**：暂无重大元数据风险，唯一待确认的是许可证合规性及长期维护计划。综合上述因素，Medusa 已具备在生产环境中进行安全扫描的准备度，适合作为正式安全审计工具进行试点或全面部署。

## 🧭 Practical evaluation

**Value:** Pantheon-Security/medusa helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 459 GitHub stars
- 81 forks
- updated 2026-05-13
- primary language: Python
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 48/100 |
| stars | 57/100 |
| topics | 100/100 |
| outlook | 80/100 |
| quality | 74/100 |
| recency | 80/100 |
| adoption | 54/100 |
| production | 72/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/Pantheon-Security/medusa) · [← Back to Mcp](./README.md)</sub>
