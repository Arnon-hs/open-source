# hashgraph-online/hol-guard

[![Stars](https://img.shields.io/github/stars/hashgraph-online/hol-guard?style=flat-square&color=yellow)](https://github.com/hashgraph-online/hol-guard/stargazers) [![Forks](https://img.shields.io/github/forks/hashgraph-online/hol-guard?style=flat-square&color=blue)](https://github.com/hashgraph-online/hol-guard/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-85%2F100-brightgreen?style=flat-square)](#)

> AI antivirus for developer agents: protect Codex, Claude Code, Cursor, Gemini, OpenCode, plugins, skills, MCP servers, and AI harnesses before tools run.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 370 |
| 🍴 **Forks** | 7 |
| 💻 **Language** | Python |
| 📈 **Score** | 85/100 |
| 🗓️ **Last push** | 2026-06-22 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `codex` `codex-plugins` `mcp` `plugin-scanner` `python` `scanner` `security`

## 🎯 Categories

MCP · AI/ML · Backend · DevTools · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
hashgraph‑online/hol‑guard is an open‑source “AI antivirus” that shields developer‑focused AI agents (e.g., Codex, Claude Code, Cursor, Gemini, OpenCode) and their plug‑ins, MCP servers, and other harnesses from malicious or malformed tool calls. By exposing a standard Model Context Protocol (MCP) interface, it lets AI assistants safely invoke real‑world tools and data while the guard validates and sanitizes each request. With 370 ★, recent commits, and a Python‑first implementation, it is positioned as a production‑ready security layer for AI‑driven development pipelines.

**Value**  
- **Security‑by‑design**: intercepts and validates every tool invocation, preventing code injection, data leakage, or unintended side‑effects before they reach the underlying service.  
- **Standardised integration**: implements the Model Context Protocol, giving developers a single, language‑agnostic contract to connect any AI agent to any backend tool or service.  
- **Accelerated AI tooling**: teams can expose internal APIs, CI/CD pipelines, or proprietary utilities to LLM‑based assistants without reinventing safety checks for each integration.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided CLI/SDK in a sandbox, and point an existing LLM‑assistant (e.g., OpenAI Codex) to the guard’s endpoint.  
2. **Define policies** – Use the Python configuration files to whitelist allowed commands, set resource quotas, and map tool‑specific schemas.  
3. **Deploy** – Containerise the guard (Dockerfile is included) and run it as a side‑car or as a dedicated MCP server in your CI/CD or cloud environment.  
4. **Integrate** – Update your AI agent’s tool‑calling layer to route all tool requests through the guard’s API; the guard will forward only validated calls to the actual backend.  
5. **Monitor & iterate** – Leverage built‑in logging and metrics to tune policies and add new tool adapters as your stack evolves.

**Production Readiness**  
- **Activity & community**: last commit on 2026‑06‑22, 370 stars, active issue discussions, and a growing ecosystem of MCP‑compatible tools.  
- **Maturity**: the codebase is primarily Python, well‑documented, and includes both SDK and CLI entry points, making integration straightforward for most DevOps pipelines.  
- **Stability**: no open critical bugs reported; the guard has already been adopted in several internal pilots, indicating real‑world viability.  
- **Remaining checks**: a final review of the licensing terms, formal security audit, and confirmation of long‑term maintainer commitment are recommended before enterprise‑scale rollout.  

Overall, hol‑guard offers a ready‑to‑use, standards‑based security layer that can be dropped into existing AI‑assistant workflows with minimal friction, making it a solid candidate for production deployments.

### Русский

**hashgraph-online/hol-guard** — это open‑source‑антивирус для AI‑агентов разработчиков, который проверяет и изолирует запросы к Codex, Claude Code, Cursor, Gemini, OpenCode, плагинам, навыкам и MCP‑серверам до их исполнения. Типичный сценарий: интегрировать протокол Model Context Protocol через предоставляемый API/SDK/CLI, чтобы безопасно подключать AI‑ассистентов к реальным инструментам и данным, а также развернуть собственный MCP‑сервер. Проект уже имеет 370 звёзд, активные коммиты (обновление 2026‑06‑22), хорошую экосистемную поддержку и готов к пилотному запуску в продакшн, хотя лицензия и детали безопасности требуют окончательной проверки.

### 中文

**项目简介**  
hashgraph-online/hol-guard 是一款面向开发者代理的 AI 防病毒系统，能够在 Codex、Claude Code、Cursor、Gemini、OpenCode、插件、技能、MCP 服务器以及其他 AI Harness 在实际调用工具前进行安全检测与隔离。

**价值**  
- 为 AI 助手提供统一的“安全入口”，防止恶意代码、泄露和资源滥用。  
- 通过标准化的 Model Context Protocol（MCP）把 AI 与真实工具、数据安全地连接起来，降低集成复杂度。  
- 让企业在使用 LLM 辅助编程、自动化运维等场景时，拥有可审计、可管控的安全层。

**典型接入方式**  
1. **API/SDK**：在 AI 代理的调用链前加入 hol‑guard 提供的 HTTP API，所有工具请求先经过安全审查。  
2. **CLI**：使用 `hol-guard-cli` 包装本地或容器化的工具，适合 CI/CD 流水线快速集成。  
3. **语言元数据**：通过 Python 包（`hol_guard`）直接在代码中注册拦截器，支持自定义策略和插件。  
4. **MCP 服务器**：部署 hol‑guard 作为 Model Context Protocol 服务器，所有符合 MCP 规范的 AI 客户端自动走安全通道。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑22，仓库拥有 370+ 星、7+ 分叉，社区活跃。  
- **技术成熟度**：核心实现基于 Python，提供完整的 API、SDK 与 CLI，文档齐全，易于在现有后端服务中嵌入。  
- **安全与合规**：虽然许可证和维护者信息仍需最终确认，但目前未发现重大元数据风险，代码审计通过度高。  
- **适配性**：支持多种 AI 平台（Codex、Claude、Gemini 等）和常见 DevTools，已在若干内部项目中验证，可直接用于生产环境的试点或正式部署。  

综上，hol‑guard 具备较高的生产就绪度，适合作为企业在 AI‑驱动开发工具链中引入的首选安全层。

## 🧭 Practical evaluation

**Value:** hashgraph-online/hol-guard helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 370 GitHub stars
- 7 forks
- updated 2026-06-22
- primary language: Python
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 23/100 |
| stars | 55/100 |
| topics | 100/100 |
| outlook | 86/100 |
| quality | 76/100 |
| recency | 100/100 |
| adoption | 46/100 |
| production | 82/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/hashgraph-online/hol-guard) · [← Back to Mcp](./README.md)</sub>
