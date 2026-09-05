# Keel-Labs/keel

[![Stars](https://img.shields.io/github/stars/Keel-Labs/keel?style=flat-square&color=yellow)](https://github.com/Keel-Labs/keel/stargazers) [![Forks](https://img.shields.io/github/forks/Keel-Labs/keel?style=flat-square&color=blue)](https://github.com/Keel-Labs/keel/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> An AI assistant whose memory belongs to you. Local-first Mac app, plain markdown workspace, bring your own model.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 22 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `claude` `electron` `knowledge-base` `llm` `local-first` `macos` `markdown` `ollama` `openai` `openrouter` `personal-knowledge-management`

## 🎯 Categories

Knowledge/RAG · AI/ML · Documents · Productivity

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Keel is a local‑first macOS app that lets you build a personal AI assistant powered by any LLM you choose, with all memory stored on your own device. It provides a plain‑markdown workspace that can index and retrieve internal knowledge bases, turning documents into searchable context for the assistant. The project is open‑source, written in TypeScript, and aims to give you full control over data privacy while still delivering a usable RAG‑style experience.

**Value**  
- **Data sovereignty** – because the assistant runs locally, your organization’s confidential documents never leave your infrastructure.  
- **Model flexibility** – you can plug in any compatible LLM (e.g., open‑source models, hosted APIs) without being locked into a vendor.  
- **Unified markdown workspace** – knowledge is stored in plain markdown, making it easy to author, version‑control, and integrate with existing documentation pipelines.  
- **Rapid prototyping** – the built‑in indexing and retrieval tools let teams quickly turn static docs into context‑aware answers, accelerating internal knowledge sharing and support workflows.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – clone the repo, run the provided Docker/Node setup, and point Keel at a small, representative markdown knowledge base. Verify that the assistant can retrieve and cite the content correctly.  
2. **Model Selection** – experiment with a lightweight open‑source model (e.g., Llama‑3‑8B) locally; once confidence is built, optionally switch to a higher‑capacity hosted model if needed.  
3. **Integration** – embed the Keel CLI or API into existing CI/CD or documentation pipelines to keep the index up‑to‑date automatically.  
4. **User Testing** – roll the desktop app out to a pilot group of internal users (e.g., support engineers) and collect feedback on relevance, latency, and UI/UX.  
5. **Scale & Harden** – add monitoring, automate index rebuilds, and enforce security policies (e.g., code‑signing the macOS app, sandboxing).  

**Production Readiness**  
- **Maturity** – Medium. The codebase is recent (last updated 2026‑05‑12) and functional for prototypes, but it lacks extensive production‑grade testing, CI pipelines, and formal release engineering.  
- **Dependencies** – Primarily TypeScript and Node; you’ll need to audit third‑party packages for known vulnerabilities before a production rollout.  
- **Maintenance** – With only 22 stars and a handful of forks, the community around Keel is small; you may need to be prepared to contribute fixes or fork the repo for long‑term stability.  
- **Risk** – No immediate licensing or data‑privacy red flags, but a thorough review of the MIT/Apache license (as applicable) and a security audit of the local server component are recommended.  

Overall, Keel offers a compelling, privacy‑first foundation for internal AI assistants, best suited for internal pilots or knowledge‑base augmentation projects, with a clear, incremental path to production once the code and dependency hygiene are validated.

### Русский

Keel — это локальное mac‑приложение‑помощник с открытой моделью, которое превращает ваши markdown‑базы знаний в интерактивную память, позволяя быстро искать и использовать внутреннюю информацию в диалогах. Для внедрения обычно начинают с небольшого proof‑of‑concept: индексируют выбранный набор документов, проверяют работу через README‑пример и оценивают качество поиска, после чего масштабируют на остальные источники. Готовность к production — средняя: проект подходит для прототипов и внутренних процессов, но требует проверки зависимостей, лицензии и безопасности перед использованием в продакшене.

### 中文

**项目简介（2‑3 句）**  
Keel 是一款本地优先的 Mac 应用，提供纯 Markdown 工作区并支持自带模型（BYOM），让 AI 助手的记忆完全归用户所有。它可以把企业内部的文档、知识库等内容快速索引，为助手提供可靠的上下文来源。

**价值**  
- **内部知识可搜索、可复用**：将散落在不同系统的文档统一索引，帮助员工和 AI 助手在对话中即时检索到最新、最准确的信息。  
- **数据安全可控**：所有索引和向量存储都在本地完成，避免敏感信息外泄，符合合规要求。  
- **灵活模型接入**：支持自带模型（OpenAI、Claude、Llama 等），可根据成本、隐私或性能需求自由切换。

**典型接入方式**  
1. **准备 Markdown 工作区**：在本地文件夹中组织业务文档（Markdown、txt、pdf 等），Keel 会自动监控并生成向量索引。  
2. **配置模型**：在设置页面填写模型 API 密钥或指向本地模型的路径，实现 “bring‑your‑own‑model”。  
3. **调用 API**：使用 Keel 提供的本地 HTTP 接口（或 SDK）发送查询/对话请求，返回带有检索上下文的答案。  
4. **小范围 PoC**：先在单个项目或部门建立一个工作区，验证检索质量和响应时延，再逐步扩展到全公司。

**生产可用性**  
- **成熟度**：当前评分 55/100，适合作为原型或内部工作流工具。代码基于 TypeScript，活跃度尚可（最近更新），但仍需自行进行依赖审计和安全评估。  
- **部署要求**：仅需 macOS 环境（或通过 Docker 在其他平台运行），本地存储空间随文档规模线性增长。  
- **运维成本**：无外部服务依赖，主要成本在模型调用（若使用云模型）和本地硬件资源。建议在正式生产前完成：  
  1. 许可证合规检查（MIT/Apache 等）。  
  2. 安全审计（依赖库、网络访问）。  
  3. 监控索引更新和查询延迟。  

综上，Keel 适合作为内部知识检索的快速落地方案，先在小范围 PoC 验证后，可通过完善运维和安全流程逐步提升到生产级别。

## 🧭 Practical evaluation

**Value:** Keel-Labs/keel helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 22 GitHub stars
- 5 forks
- updated 2026-05-12
- primary language: TypeScript
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 63/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 26/100 |
| production | 65/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/Keel-Labs/keel) · [← Back to Knowledgerag](./README.md)</sub>
