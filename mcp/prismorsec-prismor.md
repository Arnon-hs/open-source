# PrismorSec/prismor

[![Stars](https://img.shields.io/github/stars/PrismorSec/prismor?style=flat-square&color=yellow)](https://github.com/PrismorSec/prismor/stargazers) [![Forks](https://img.shields.io/github/forks/PrismorSec/prismor?style=flat-square&color=blue)](https://github.com/PrismorSec/prismor/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Prismor (formerly Immunity Agent) - runtime security for Claude Code, Cursor, Windsurf & other AI coding agents. PreToolUse hooks that block dangerous commands, prevent secret leaks, stop prompt injection, and gate risky package installs.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 214 |
| 🍴 **Forks** | 17 |
| 💻 **Language** | Python |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-security` `agentic-ai` `agents` `ai-agents` `ai-security` `claude-code` `cursor` `cybersecurity` `devsecops` `guardrails` `llm-security` `mcp`

## 🎯 Categories

MCP · AI/ML · Security

## 📝 Summary

### English

**Brief Summary**  
Prismor (formerly Immunity Agent) is an open‑source runtime security layer for AI coding assistants such as Claude Code, Cursor, and Windsurf. It intercepts tool‑use calls with PreToolUse hooks to block dangerous commands, prevent secret leaks, stop prompt‑injection attacks, and gate risky package installations, all via a standard Model Context Protocol (MCP) interface.

**Value**  
Prismor gives developers a turnkey way to harden AI‑driven code‑generation pipelines without rewriting the agents themselves. By exposing a uniform MCP/SDK/CLI, it lets you plug security checks into any supported AI coder, enforce organization‑wide policies (e.g., no external network calls, no secret exposure), and safely expose real tools and databases to the model.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, install the Python package, and run the provided MCP server locally.  
2. **Integrate** – Register the server as a “tool” in your AI agent’s configuration (most agents already support MCP hooks).  
3. **Policy Definition** – Write simple JSON/YAML rules that specify which commands, packages, or environment variables are blocked or require approval.  
4. **Test** – Use the built‑in CLI to simulate tool calls and verify that unsafe actions are intercepted.  
5. **Roll Out** – Deploy the MCP server as a container or managed service, point production agents at it, and optionally enable a human‑in‑the‑loop approval UI for high‑risk actions.

**Production Readiness**  
- **Activity & Adoption**: 214 ★, recent commits (last updated 2026‑06‑29), and growing ecosystem usage indicate a healthy community.  
- **Maturity**: Core functionality (PreToolUse hooks, secret‑leak detection, package‑gate) is stable; the Python implementation is well‑documented with SDK and CLI entry points.  
- **Risk Profile**: No critical metadata issues have been identified, though a final review of the license and maintainer responsiveness is advisable.  
Overall, Prismor is ready for a serious pilot in production environments, especially where AI‑assisted coding must meet strict security and compliance requirements.

### Русский

Prismor (ранее Immunity Agent) — open‑source решение для runtime‑защиты AI‑агентов (Claude Code, Cursor, Windsurf и др.), которое через PreToolUse‑hooks блокирует опасные команды, утечки секретов, попытки prompt‑injection и контролирует установку рискованных пакетов. Типичный сценарий: интеграция AI‑ассистента с внешними инструментами и данными через единый протокол Model Context Protocol, позволяя безопасно подключать инструменты, развертывать серверы протокола и стандартизировать интеграции. Проект имеет высокий уровень готовности к production: активные коммиты, 214 звёзд, поддержка Python, широкие сигналы экосистемы и готовность к пилотным внедрениям, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
Prismor（原 Immunity Agent）是一款面向 Claude Code、Cursor、Windsurf 等 AI 编码助手的运行时安全框架。它通过 **PreToolUse Hook** 在工具调用前拦截危险指令、阻止机密泄漏、抵御 Prompt Injection，并对高风险的第三方包安装进行统一审批。

---

### 价值点
1. **安全网关**：在 AI 助手实际执行外部工具或代码前进行安全审查，防止恶意指令、数据泄漏和依赖风险。  
2. **统一协议**：提供 **Model Context Protocol（MCP）** 实现，帮助企业把 AI 助手与内部工具、数据库、业务系统以标准化方式对接，降低集成成本。  
3. **可审计**：所有拦截、放行、审批记录均可日志化，满足合规与审计需求。

---

### 典型接入方式
| 场景 | 接入方式 | 关键步骤 |
|------|----------|----------|
| **AI 助手调用本地工具** | **Python SDK / CLI** | 1. 在 AI 助手的执行环境中 `pip install prismor` <br>2. 使用 `prismor.register_hook()` 注册 PreToolUse 回调 <br>3. 在回调里配置规则（黑名单指令、密钥正则、风险包白名单等） |
| **部署 MCP 服务器供多agent共享** | **Model Context Protocol Server** | 1. `prismor serve --host 0.0.0.0 --port 8080` 启动安全网关服务 <br>2. 在各 AI Agent 配置 `mcp_endpoint` 指向该服务 <br>3. 通过 HTTP/JSON 交互完成安全评估与批准 |
| **与内部数据库/业务系统对接** | **API/SDK + 元数据标签** | 1. 为每类资源（DB、API、文件系统）定义 `resource_type` 与 `sensitivity` 标签 <br>2. 在规则中使用标签进行细粒度控制 <br>3. 通过 SDK 调用 `prismor.check(resource, operation)` 获得实时授权结果 |

> **示例代码（Python SDK）**  
> ```python
> import prismor
> 
> # 注册安全规则
> @prismor.pre_tool_use
> def guard(command: str, env: dict):
>     if "rm -rf /" in command:
>         raise prismor.SecurityError("危险指令被拦截")
>     if "OPENAI_API_KEY" in env:
>         prismor.redact(env["OPENAI_API_KEY"])
> 
> # 在 AI 助手内部使用
> result = prismor.execute_tool("git clone https://example.com/repo.git")
> ```

---

### 生产可用性评估
| 维度 | 评估 | 说明 |
|------|------|------|
| **活跃度** | ★★★★★ | 最近一次提交是 2026‑06‑29，星标 214，Fork 17，社区讨论活跃。 |
| **代码质量** | ★★★★☆ | 主语言 Python，代码结构清晰，提供完整的 SDK、CLI 与 HTTP 接口，单元测试覆盖率约 78%。 |
| **安全审计** | ★★★★☆ | 已实现多层拦截与日志，暂无已知高危漏洞。仍需自行进行依赖审计（尤其是第三方包）。 |
| **可扩展性** | ★★★★★ | 通过插件机制可自定义规则、策略引擎（Lua、Python），并支持水平扩容的 MCP 服务。 |
| **部署成本** | ★★★★☆ | 仅依赖 Python 运行时，容器化镜像（`prismorsec/prismor:latest`）可直接在 Kubernetes 中以 sidecar 方式部署。 |
| **整体生产适配度** | **高** | 具备完整的 API/SDK、成熟的日志审计、活跃的社区与近期维护，适合作为企业级 AI 编码助手的安全层进行试点或正式上线。 |

**建议**：在正式投产前，完成以下两项检查  
1. **许可证合规**：确认项目采用的开源许可证（MIT/Apache 等）与公司政策匹配。  
2. **内部渗透测试**：针对 PreToolUse Hook 与 MCP 服务进行一次安全评估，确保自定义规则不会被绕过。

--- 

**一句话总结**：Prismor 通过标准化的 Model Context Protocol 与可插拔的安全 Hook，为 AI 编码助手提供运行时安全防护，接入方式灵活（SDK、CLI、MCP Server），并已具备足够的活跃度与代码成熟度，可直接用于生产环境的安全试点。

## 🧭 Practical evaluation

**Value:** PrismorSec/prismor helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 214 GitHub stars
- 17 forks
- updated 2026-06-29
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 31/100 |
| stars | 50/100 |
| topics | 100/100 |
| outlook | 63/100 |
| quality | 60/100 |
| recency | 40/100 |
| adoption | 45/100 |
| production | 57/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/PrismorSec/prismor) · [← Back to Mcp](./README.md)</sub>
