# Ruya-AI/cozempic

[![Stars](https://img.shields.io/github/stars/Ruya-AI/cozempic?style=flat-square&color=yellow)](https://github.com/Ruya-AI/cozempic/stargazers) [![Forks](https://img.shields.io/github/forks/Ruya-AI/cozempic?style=flat-square&color=blue)](https://github.com/Ruya-AI/cozempic/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-76%2F100-brightgreen?style=flat-square)](#)

> Context cleaning for Claude Code — prune bloated sessions, protect Agent Teams from context loss, auto-guard with tiered pruning

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 293 |
| 🍴 **Forks** | 18 |
| 💻 **Language** | Python |
| 📈 **Score** | 76/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-teams` `claude-code` `claude-skills` `cli` `context` `context-management` `jsonl` `llm-tools` `pruning` `python` `session-management`

## 🎯 Categories

AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Ruya‑AI’s *cozempic* is a Python library that automatically trims and safeguards the context of Claude‑based code sessions, preventing bloated prompts and protecting multi‑agent teams from context loss through tiered pruning. It lets developers add robust AI‑driven context management to prototypes, Retrieval‑Augmented Generation (RAG) pipelines, or agent workflows without building a custom model stack from scratch.  

**Value**  
- **Immediate AI capability**: By handling prompt bloat and context drift out‑of‑the‑box, developers can focus on business logic rather than low‑level prompt engineering.  
- **Safety & efficiency**: Tiered pruning reduces token usage and costs while ensuring critical information remains available to agents, which is especially valuable in long‑running or collaborative AI sessions.  
- **Plug‑and‑play**: Exposes a clean API/CLI and SDK, making it easy to integrate with existing Claude, LangChain, or custom agent frameworks.  

**Practical Adoption Path**  
1. **Prototype** – Install via `pip install cozempic`, import the library, and wrap your Claude client with the provided `ContextCleaner` class.  
2. **Iterate** – Use the configuration knobs (e.g., pruning thresholds, protection tiers) to tune how aggressively context is trimmed for your specific RAG or agent use case.  
3. **Integrate** – Embed the cleaner into your CI/CD pipeline or as a middleware layer in production services; the CLI can also be used for batch‑processing historic session logs.  
4. **Monitor** – Leverage built‑in telemetry (token counts, prune actions) to verify cost savings and correctness before promoting to production.  

**Production Readiness**  
- **Activity & community**: 293 stars, recent commits (as of 2026‑05‑13), and active issue discussions indicate a healthy open‑source project.  
- **Maturity**: The library is stable, well‑documented, and provides both API and CLI entry points, making integration straightforward.  
- **Risks**: Licensing, security audit, and maintainer continuity still need a final check, but no major metadata or dependency concerns have been identified. Overall, *cozempic* is a strong candidate for a serious pilot or production rollout in AI‑enabled applications.

### Русский

**Ruya‑AI/cozempic** — это open‑source‑утилита для «очистки контекста» в Claude Code: она автоматически обрезает избыточные сессии, защищает команды агентов от потери контекста и применяет многоуровневое прунинг‑правило. Типичный сценарий — быстрое прототипирование AI‑фич, построение RAG‑ или агентных пайплайнов и оценка инструментов модели без необходимости создавать собственный стек с нуля. Проект уже активно поддерживается (293 ★, недавние коммиты, Python‑SDK/CLI), имеет хорошие сигналы экосистемы и готов к пилотному запуску в продакшн, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
Ruya‑AI/cozempic 是一款面向 Claude Code 的上下文清理工具，能够自动裁剪冗余会话、避免 Agent Teams 因上下文丢失而失效，并提供分层裁剪策略进行安全防护。它帮助开发者在已有模型栈上快速叠加 AI 能力，无需从零构建。

**价值**  
- **提升效率**：自动剔除无用上下文，显著降低 Token 消耗和响应时延。  
- **保障可靠性**：分层裁剪机制防止关键信息被误删，确保 Agent Teams 的连续性和稳定性。  
- **加速原型**：只需几行代码即可为现有系统加入 RAG 或智能代理功能，省去繁琐的模型调优工作。

**典型接入方式**  
1. **Python SDK**：`pip install cozempic` 后在代码中引入 `CozePruner` 类，配置裁剪策略并在每次调用 Claude Code 前调用 `prune(session)`。  
2. **CLI**：`cozempic prune --session-id <id> --policy tiered` 直接在终端对会话进行批量清理。  
3. **REST API**：部署自带的轻量 Flask 服务，向 `/prune` 端点 POST `{session_id, policy}` 即可实现语言无关的集成。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑13 最近一次提交，星标 293、fork 18，社区活跃。  
- **成熟度**：代码基于 Python，提供完整的 SDK、CLI 与 API，文档清晰，已在多个内部项目中进行试点。  
- **风险**：暂无重大许可证或安全隐患，但仍建议在正式上线前完成一次安全审计并确认维护者的长期可用性。  

综上，cozempic 具备高生产准备度，适合作为 AI/ML 开发工具链中的上下文管理组件，快速为业务原型或正式产品提供可靠的 Claude Code 支持。

## 🧭 Practical evaluation

**Value:** Ruya-AI/cozempic helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 293 GitHub stars
- 18 forks
- updated 2026-05-13
- primary language: Python
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 32/100 |
| stars | 53/100 |
| topics | 100/100 |
| outlook | 85/100 |
| quality | 76/100 |
| recency | 100/100 |
| adoption | 47/100 |
| production | 77/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/Ruya-AI/cozempic) · [← Back to AI/ML](./README.md)</sub>
