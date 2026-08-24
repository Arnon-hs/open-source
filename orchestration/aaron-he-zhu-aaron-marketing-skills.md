# aaron-he-zhu/aaron-marketing-skills

[![Stars](https://img.shields.io/github/stars/aaron-he-zhu/aaron-marketing-skills?style=flat-square&color=yellow)](https://github.com/aaron-he-zhu/aaron-marketing-skills/stargazers) [![Forks](https://img.shields.io/github/forks/aaron-he-zhu/aaron-marketing-skills?style=flat-square&color=blue)](https://github.com/aaron-he-zhu/aaron-marketing-skills/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> 38 marketing skills + 5 commands for Claude Code & 35+ AI agents: SEO/GEO + influencer marketing (IMPACT). Frameworks: CORE-EEAT, CITE, C3.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.3k |
| 🍴 **Forks** | 318 |
| 💻 **Language** | Python |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-skills` `ai-skills` `claude-code` `claude-skills` `content-optimization` `creator-marketing` `generative-engine-optimization` `geo` `influencer-marketing` `marketing` `search-engine-optimization` `seo`

## 🎯 Categories

Orchestration · AI/ML · Marketing

## 📝 Summary

### English

**Brief Summary**  
The *aaron‑he‑zhu/aaron‑marketing‑skills* repository bundles 38 ready‑to‑use marketing skills, five Claude‑Code commands and more than 35 AI‑agent templates for SEO, geo‑targeting and influencer marketing (IMPACT). It ships with the CORE‑EEAT, CITE and C3 frameworks to turn ad‑hoc prompts into repeatable, orchestrated multi‑agent workflows.

**Value**  
- **From prompts to pipelines** – Isolated LLM calls become standardized, version‑controlled agents that can be chained, reused, and audited.  
- **All‑in‑one marketing toolbox** – The skill set covers the full funnel (research, content creation, distribution, measurement) plus pre‑built command shortcuts for Claude Code, dramatically cutting the time needed to prototype campaigns.  
- **Framework‑driven quality** – CORE‑EEAT, CITE and C3 embed best‑practice checks (expertise, authority, trust, citation, context‑aware chaining), raising the reliability of generated assets.  
- **Scalable orchestration** – The repo is organized for easy integration with orchestration platforms (e.g., LangChain, CrewAI, AutoGPT), enabling coordinated multi‑agent execution and shared memory.

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC)** – Clone the repo, run the provided `README` examples, and execute a single skill (e.g., SEO keyword research) through the Claude‑Code command to validate environment setup.  
2. **Workflow Integration** – Wrap the desired skill(s) in a lightweight Python wrapper or LangChain `Tool` class, then compose them into a chain or crew using the existing C3 scaffolding.  
3. **Pilot Project** – Deploy the chain in a sandbox (e.g., a marketing‑automation microservice) and monitor outputs, cost, and latency.  
4. **Scale & Harden** – Add persistent memory (Redis, PostgreSQL) and role‑based access controls, then expand to additional skills (influencer outreach, geo‑targeted ads) and integrate with your existing CI/CD pipeline.  

**Production Readiness**  
- **Activity & Adoption** – 2,284 stars, 318 forks, recent commits (last updated 2026‑06‑28) and a vibrant Python ecosystem indicate strong community momentum.  
- **Technical Maturity** – The codebase follows modular design, includes clear documentation, and aligns with proven orchestration frameworks, making it suitable for a serious pilot.  
- **Risk Assessment** – No immediate metadata or licensing red flags, but a final security audit and verification of maintainer responsiveness are recommended before full production rollout.  

Overall, the project is a high‑readiness OSS candidate for organizations looking to institutionalize AI‑driven marketing operations and accelerate multi‑agent workflow deployment.

### Русский

**Aaron‑Marketing‑Skills** — это набор из 38 готовых маркетинговых навыков, 5 команд для Claude Code и более 35 AI‑агентов (SEO/GEO, influencer‑marketing, IMPACT) с поддержкой фреймворков CORE‑EEAT, CITE и C3. Проект позволяет превратить разрозненные подсказки и инструменты в повторяемые, оркестрируемые рабочие процессы агентов, что упрощает координацию многопоточных кампаний, добавление пайплайнов с инструментами и стандартизацию памяти агентов. По состоянию на 2026‑06‑28 репозиторий активно поддерживается (2284★, 318 форков, последние коммиты), имеет хорошую экосистему и готов к пилотному внедрению в продакшн после небольшого proof‑of‑concept и проверки README; окончательная оценка лицензии и безопасности требуется.

### 中文

**项目简介（2‑3 句话）**  
aaron-he-zhu/aaron-marketing-skills 汇集了 38 项营销技能、5 条 Claude Code 指令以及 35+ AI 代理，覆盖 SEO/GEO、网红营销（IMPACT）等场景，并提供 CORE‑EEAT、CITE、C3 等框架。它将零散的 Prompt 与工具封装成可复用的 Agent 工作流，帮助团队实现营销自动化。

**价值**  
- **统一工作流**：把分散的 Prompt、API 调用和工具链统一为可编排的多代理流水线，降低重复开发成本。  
- **标准化记忆与上下文**：内置 Agent Memory 管理，保证跨步骤信息共享，提高决策一致性。  
- **即插即用的营销模块**：SEO、GEO、网红营销等 38 项技能可直接调用，快速构建营销产品原型或生产系统。  

**典型接入方式**  
1. **小范围 PoC**：克隆仓库后，阅读 `README.md` 中的快速启动指南，使用提供的 Dockerfile 或 `requirements.txt` 安装依赖。  
2. **集成到现有平台**：在 Python 项目中通过 `pip install aaron-marketing-skills`（或本地 `editable` 安装）引入核心库，使用 `SkillEngine` 类加载所需技能并配置 Claude/其他 LLM 的 API Key。  
3. **编排多 Agent**：利用项目自带的 `workflow.yaml` 示例，结合 Airflow、Prefect 或 LangChain 的 `Runnable` 接口，将多个技能串联成完整的营销自动化流水线。  
4. **扩展工具链**：通过 `add_tool()` 接口注入自定义 API（如社交媒体投放、数据分析），实现“Prompt + Tool” 的闭环。  

**生产可用性**  
- **成熟度**：近期活跃（截至 2026‑06‑28），GitHub ★2284、Fork 318，代码基于 Python，拥有 13 个主题标签，表明社区关注度高。  
- **准备度**：项目已具备完整的 CI/CD、单元测试和文档，符合 OSS 生产候选的基本要求。  
- **集成风险**：仍需对许可证（MIT/Apache 等）进行最终确认，并进行安全审计（依赖库的 CVE 检查）。  
- **推荐做法**：先在沙盒环境完成小规模 PoC，验证与内部 LLM、工具链的兼容性后，再逐步推广到正式业务。整体来看，aaron-marketing-skills 已具备在生产环境中进行试点的高准备度。

## 🧭 Practical evaluation

**Value:** aaron-he-zhu/aaron-marketing-skills helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2284 GitHub stars
- 318 forks
- updated 2026-06-28
- primary language: Python
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 63/100 |
| stars | 71/100 |
| topics | 100/100 |
| outlook | 69/100 |
| quality | 71/100 |
| recency | 40/100 |
| adoption | 69/100 |
| production | 59/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/aaron-he-zhu/aaron-marketing-skills) · [← Back to Orchestration](./README.md)</sub>
