# hashgraph-online/hol-guard

[![Stars](https://img.shields.io/github/stars/hashgraph-online/hol-guard?style=flat-square&color=yellow)](https://github.com/hashgraph-online/hol-guard/stargazers) [![Forks](https://img.shields.io/github/forks/hashgraph-online/hol-guard?style=flat-square&color=blue)](https://github.com/hashgraph-online/hol-guard/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-82%2F100-brightgreen?style=flat-square)](#)

> AI antivirus for developer agents: protect Codex, Claude Code, Cursor, Gemini, OpenCode, plugins, skills, MCP servers, and AI harnesses before tools run.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 370 |
| 🍴 **Forks** | 7 |
| 💻 **Language** | Python |
| 📈 **Score** | 82/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `codex` `codex-plugins` `mcp` `plugin-scanner` `python` `scanner` `security`

## 🎯 Categories

MCP · AI/ML · DevTools · Security

## 📝 Summary

### English

**Summary**  
HOL Guard is an Apache-2.0 open-source security tool for AI coding agents. It uses supported agent and harness integration points to review selected risky actions against local policy. Depending on the available event hooks, it can allow an action, block it, or request approval and keep a local decision record. Coverage varies by agent, adapter, version, and event. HOL Guard does not intercept every tool invocation, file read, or external API call.

**Value**

- **Bounded runtime controls:** apply local policy to supported events such as selected commands, package operations, and MCP configuration or tool interactions when the installed integration exposes them.
- **Review and evidence:** request approval or block covered operations and inspect available local receipts.
- **Clear scope:** consult the current agent/event coverage documentation rather than assuming universal interception or prompt-injection prevention.

**Practical adoption path**

1. Read the maintained [HOL Guard documentation](https://hol.org/guard) and determine which agent, version, and event types are supported.
2. Install HOL Guard using the current official instructions in the [source repository](https://github.com/hashgraph-online/hol-guard).
3. In a safe test workspace, check the Guard status, enabled protection and local policy, then exercise a benign supported action to inspect its decision and receipt.
4. Review the limits for the chosen adapter and plan additional controls for actions outside the supported hook surface.

**MCP server scope**  
The optional local stdio MCP server exposes sanitized Guard status, receipts, inventory, policy validation and approval-backed policy workflows. The documented command is `uvx --from hol-guard hol-guard mcp serve --stdio`. This server is not a universal MCP-to-backend gateway, generic API router, or transparent proxy for every agent tool call.

**Production readiness**  
This automatically maintained catalog provides discovery metadata, not an independent security audit or proof of customer pilots, complete coverage, or production deployments. Confirm current releases, actual event coverage, failure behavior, data-handling requirements and operational fit before production use.

### Русский

**Кратко**  
HOL Guard — открытый инструмент безопасности для ИИ-ассистентов разработчика под лицензией Apache-2.0. Он проверяет определённые действия через доступные интеграции и хуки агента, применяет локальные политики и может разрешать, блокировать или запрашивать подтверждение с записью решения. Охват зависит от агента, версии и типа события: не все вызовы инструментов, чтения файлов или API-запросы перехватываются. Локальный MCP-сервер предоставляет сведения о состоянии Guard, журналы решений и операции с политиками; он не является универсальным шлюзом к сторонним инструментам. Для оценки следует сверить [официальную документацию](https://hol.org/guard) с конкретной конфигурацией и провести безопасные тесты. Данных для утверждения о полной защите, независимом аудите или подтверждённых внедрениях в продакшене здесь нет.

### 中文

**简介**  
HOL Guard 是采用 Apache-2.0 许可证的开源 AI 编码代理安全工具。它通过受支持的代理集成和事件钩子，依据本地策略检查特定高风险操作，并可允许、拦截或请求批准，同时记录本地决策。覆盖范围取决于代理、版本及事件类型；它不能保证拦截所有工具调用、文件读取或 API 请求。其本地 MCP stdio 服务用于查询 Guard 状态、经过处理的记录及策略操作，并非通用第三方工具网关或 API 代理。评估时应先核对[官方文档](https://hol.org/guard)中的适配范围，再在隔离环境中测试具体操作。当前目录记录不能证明完整安全防护、独立审计或实际生产部署。

## 🧭 Practical evaluation

**Value:** Local policy checks, approvals, and inspectable evidence for supported AI coding-agent actions.

**Best use cases**

- review selected risky actions in supported coding-agent workflows;
- inspect local policy decisions and sanitized Guard receipts;
- evaluate specific agent/event combinations before expanding deployment.

**Integration notes:** Use an officially supported adapter and the documented installation flow. The optional Guard MCP server serves Guard's own status, receipts, inventory and policy operations; it does not forward arbitrary backend tool requests.

**Production readiness:** Requires a fresh, agent-specific coverage review, benign integration tests, and an independent operational/security assessment. Catalog popularity and score figures are not evidence of security guarantees or deployed customer pilots.

**Quality signals:** Snapshot star, fork, date and topic counts above are third-party catalog metadata and may lag behind the source repository.

**Risks:** Unsupported event paths and differences among adapters, plus no established universal interception, full prompt-injection prevention, or audited production-readiness guarantee.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 23/100 |
| stars | 55/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 71/100 |
| recency | 80/100 |
| adoption | 46/100 |
| production | 75/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/hashgraph-online/hol-guard) · [← Back to Mcp](./README.md)</sub>
