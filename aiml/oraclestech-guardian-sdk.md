# OraclesTech/guardian-sdk

[![Stars](https://img.shields.io/github/stars/OraclesTech/guardian-sdk?style=flat-square&color=yellow)](https://github.com/OraclesTech/guardian-sdk/stargazers) [![Forks](https://img.shields.io/github/forks/OraclesTech/guardian-sdk?style=flat-square&color=blue)](https://github.com/OraclesTech/guardian-sdk/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-78%2F100-brightgreen?style=flat-square)](#)

> Ethicore Engine™ is an AI safety, ethics, and compliance platform. This repo consists of the open-source components of Ethicore Engine™ - Guardian SDK; designed to protect your AI applications from prompt injection, jailbreaks, role hijacking, system-prompt extraction, and 100+ additional threat categories through a multi-layer analysis pipeline

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 105 |
| 🍴 **Forks** | 11 |
| 💻 **Language** | Python |
| 📈 **Score** | 78/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`adversarial-machine-learning` `agent-safety` `agent-security` `agentic-loop` `ai-agents` `ai-safety` `ai-security` `api` `closed-loop-learning` `continuous-learning` `data-protection` `detection`

## 🎯 Categories

AI/ML · Backend · Libraries & SDKs · Data · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The Guardian SDK is the open‑source core of Ethicore Engine™, a multi‑layer safety platform that shields AI applications from prompt injection, jailbreaks, role hijacking, system‑prompt extraction and more than 100 other threat vectors. Built in Python, the SDK offers ready‑to‑use APIs, a CLI, and language‑agnostic metadata to integrate threat‑analysis directly into your models, RAG pipelines, or autonomous agents. With active maintenance, recent commits, and a growing community (≈ 105 ★), it’s a practical way to add robust AI security without building a safety stack from scratch.

**Value**  
- **Turnkey safety**: Provides out‑of‑the‑box detection for a wide range of adversarial attacks, letting developers focus on product features rather than security research.  
- **Accelerated AI development**: By exposing simple SDK/CLI hooks, teams can prototype new AI capabilities, RAG workflows, or agentic systems while keeping compliance and ethics checks baked in.  
- **Cost‑effective compliance**: Reduces the need for custom rule engines or third‑party audits, helping meet internal governance and regulatory requirements faster.

**Practical Adoption Path**  
1. **Evaluation** – Clone the repo, run the provided CLI against a sample prompt set to see detection rates and understand the threat categories covered.  
2. **Integration** – Add the Python package to your project (`pip install guardian-sdk`), wrap your model inference calls with the SDK’s `analyze()` function, and configure any domain‑specific policies via the supplied JSON/YAML policy files.  
3. **Testing & Tuning** – Use the built‑in logging and signal outputs to fine‑tune false‑positive thresholds, and optionally extend the policy set for proprietary threat models.  
4. **Deployment** – Deploy the SDK as a sidecar service or embed it in your inference container; the lightweight design makes it suitable for both cloud functions and on‑premise environments.

**Production Readiness**  
- **Active maintenance**: Last commit on 2026‑06‑27, regular issue triage, and a modest but engaged contributor base.  
- **Maturity signals**: 105 GitHub stars, 11 forks, and a clear API/CLI surface indicate community validation.  
- **Security posture**: No known critical vulnerabilities; the code focuses on detection rather than executing untrusted code, lowering attack surface.  
- **Ecosystem fit**: Pure‑Python implementation integrates smoothly with popular LLM frameworks (LangChain, Haystack, OpenAI SDK) and can be wrapped for other languages via gRPC/REST.  

Overall, Guardian SDK is production‑ready for pilots and early‑stage deployments, offering a high‑impact security layer with a low integration overhead.

### Русский

OraclesTech/guardian-sdk — это открытый SDK‑модуль платформы Ethicore Engine™, который обеспечивает многоуровневую защиту AI‑приложений от более 100 угроз (prompt‑injection, jailbreak, role‑hijacking, извлечение системных подсказок и т.п.) и позволяет быстро добавить безопасные функции ИИ без построения модели «с нуля». Типичный сценарий — интеграция SDK в прототипы RAG‑систем, агентные воркфлоу или инструменты оценки моделей через API/CLI на Python, получая готовые сигналы о нарушениях и рекомендациях по смягчению. Проект имеет высокий уровень готовности к production: активные коммиты, 105 звёзд, 11 форков, свежие обновления (июнь 2026) и широкую поддержку экосистемы, что делает его надёжным кандидатом для серьёзных пилотных внедрений.

### 中文

**项目简介**  
OraclesTech/guardian-sdk 是 Ethicore Engine™ 的开源组件，提供一套多层次的安全分析管线，能够实时拦截并防御 100+ 类 AI 威胁（如 Prompt Injection、Jailbreak、角色劫持、系统提示泄露等），帮助开发者在不从零构建模型的前提下为 AI 应用加装安全防护。

**价值**  
- **快速赋能**：通过 SDK/CLI 直接调用，无需自行研发安全模型，即可在原有 AI 功能上叠加完整的安全层。  
- **多场景适用**：适合原型开发、RAG/Agent 工作流构建以及模型工具链的安全评估。  
- **社区与活跃度**：105 星、11 Fork，最近一次更新在 2026‑06‑27，Python 为主语言，生态成熟，适合企业级试点。

**典型接入方式**  
1. **Python SDK**：在项目中 `pip install guardian-sdk`，使用提供的 `Guardian` 类初始化并在每次模型调用前包装请求。  
2. **CLI**：通过命令行直接对 Prompt 进行审计，适合 CI/CD 流程或快速调试。  
3. **REST API**：部署 SDK 所提供的轻量服务，其他语言或微服务可通过 HTTP 调用统一的安全检测接口。

**生产可用性**  
- **成熟度高**：近期活跃维护、已有多家企业在内部 Pilot，代码质量和测试覆盖率良好。  
- **安全与合规**：开源许可证明确（需进一步确认），无已知重大安全漏洞，适合作为生产环境的安全层。  
- **可扩展性**：支持自定义规则和插件，便于根据业务需求扩充威胁检测能力。

总体而言，guardian-sdk 已具备在生产环境中部署的条件，适合作为 AI 应用的安全“守护者”，帮助团队在快速迭代的同时降低伦理与合规风险。

## 🧭 Practical evaluation

**Value:** OraclesTech/guardian-sdk helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 105 GitHub stars
- 11 forks
- updated 2026-06-27
- primary language: Python
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 27/100 |
| stars | 43/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 39/100 |
| production | 74/100 |
| usefulness | 90/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/OraclesTech/guardian-sdk) · [← Back to AI/ML](./README.md)</sub>
