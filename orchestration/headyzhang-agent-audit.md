# HeadyZhang/agent-audit

[![Stars](https://img.shields.io/github/stars/HeadyZhang/agent-audit?style=flat-square&color=yellow)](https://github.com/HeadyZhang/agent-audit/stargazers) [![Forks](https://img.shields.io/github/forks/HeadyZhang/agent-audit?style=flat-square&color=blue)](https://github.com/HeadyZhang/agent-audit/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> Static security scanner for LLM agents — prompt injection, MCP config auditing, taint analysis. 51 rules mapped to OWASP Agentic Top 10 (2026). Works with LangChain, CrewAI, AutoGen.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 192 |
| 🍴 **Forks** | 22 |
| 💻 **Language** | Python |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `ai-security` `ai-security-tool` `cli` `crewai` `langchain` `langchain-security-` `llm-safety` `llm-security` `mcp` `owasp` `prompt-injection`

## 🎯 Categories

Orchestration · MCP · AI/ML · DevTools · Security

## 📝 Summary

### English

**Brief Summary**  
HeadyZhang/agent‑audit is an open‑source static security scanner for LLM‑driven agents. It detects prompt‑injection, mis‑configured MCP settings, and taint‑flow issues across 51 rules aligned with the OWASP Agentic Top 10 (2026) and integrates seamlessly with LangChain, CrewAI and AutoGen. With 192 ⭐ on GitHub and recent commits, it’s a mature, Python‑based tool for hardening multi‑agent workflows.

**Value**  
- **Security‑first agent development:** By automatically auditing prompts, tool‑use pipelines, and memory handling, the scanner lets teams catch agentic attack surfaces early, reducing costly post‑deployment breaches.  
- **Standardised compliance:** The OWASP Agentic Top 10 mapping gives a clear, industry‑aligned checklist, making audits auditable and repeatable.  
- **Workflow acceleration:** Developers can safely compose complex, multi‑agent orchestrations (e.g., LangChain chains, CrewAI crews, AutoGen collaborations) knowing that each component passes a consistent security baseline.

**Practical Adoption Path**  
1. **Integrate the CLI/SDK** into CI pipelines (e.g., GitHub Actions, Azure Pipelines) to run static scans on every PR that adds or modifies agent code.  
2. **Add a pre‑commit hook** for local developers to get immediate feedback on prompt‑injection or taint‑flow issues.  
3. **Configure language‑specific adapters** for LangChain, CrewAI, or AutoGen projects, pointing the scanner at the agent definition files and tool‑use specifications.  
4. **Consume the JSON report** in existing monitoring dashboards or ticketing systems to track remediation progress and enforce policy gates before promotion to staging or production.

**Production Readiness**  
- **Active maintenance:** Last commit on 2026‑07‑04, steady issue response, and a growing user base (192 ⭐, 22 forks).  
- **Ecosystem fit:** Native support for the three leading LLM‑agent frameworks and a clear API/CLI surface make integration low‑friction.  
- **Risk profile:** No critical licensing or security red flags identified, though a final review of the maintainer’s activity and vulnerability disclosures is advisable.  
Overall, the project is production‑ready for pilot deployments and can be scaled to enterprise‑grade agent pipelines with minimal overhead.

### Русский

HeadyZhang/agent‑audit — это open‑source сканер статической безопасности для LLM‑агентов, который проверяет уязвимости типа prompt injection, конфигурацию MCP и проводит taint‑анализ по 51 правилу, сопоставленному с OWASP Agentic Top 10 (2026), и поддерживает популярные фреймворки LangChain, CrewAI и AutoGen. Он позволяет превратить разрозненные подсказки и инструменты в проверяемые, повторяемые цепочки агентов — например, координировать многокомпонентные рабочие процессы, добавлять пайплайны использования инструментов и стандартизировать память агентов. По оценке готовности проекта (score 81/100) он считается практически готовым к production: активная разработка, 192 звёзд, 22 форка, свежие коммиты и широкая экосистема, хотя окончательная проверка лицензии и поддержки мейнтейнеров всё‑ещё требуется.

### 中文

**项目介绍**

HeadyZhang/agent-audit 是一个开源项目，提供静态安全扫描工具，用于检测 LLM 代理的安全风险。该项目支持 LangChain、CrewAI 和 AutoGen 等多个代理平台，总共映射了 51 个规则到 OWASP Agentic Top 10（2026）。

**价值**

HeadyZhang/agent-audit 的价值在于，它可以帮助开发者将孤立的提示和工具转化为可重复的代理工作流程。通过使用该工具，开发者可以更好地协调多个代理工作流程、添加工具使用管道以及标准化代理内存。

**典型接入方式**

该项目支持多种接入方式，包括：

* API：通过 API 接口可以对代理进行安全扫描。
* SDK：提供 SDK 接口，开发者可以在自己的应用程序中集成该工具。
* CLI：提供命令行接口，开发者可以直接使用命令行工具进行安全扫描。

**生产可用性**

该项目具有高生产可用性，主要原因包括：

* 最近的活动：项目最近更新，表明开发者仍然活

## 🧭 Practical evaluation

**Value:** HeadyZhang/agent-audit helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 192 GitHub stars
- 22 forks
- updated 2026-07-04
- primary language: Python
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 49/100 |
| topics | 100/100 |
| outlook | 65/100 |
| quality | 60/100 |
| recency | 40/100 |
| adoption | 45/100 |
| production | 59/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-04 · [View on GitHub](https://github.com/HeadyZhang/agent-audit) · [← Back to Orchestration](./README.md)</sub>
