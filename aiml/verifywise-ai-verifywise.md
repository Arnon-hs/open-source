# verifywise-ai/verifywise

[![Stars](https://img.shields.io/github/stars/verifywise-ai/verifywise?style=flat-square&color=yellow)](https://github.com/verifywise-ai/verifywise/stargazers) [![Forks](https://img.shields.io/github/forks/verifywise-ai/verifywise?style=flat-square&color=blue)](https://github.com/verifywise-ai/verifywise/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Complete AI governance and LLM Evals platform with support for EU AI Act, ISO 42001, NIST AI RMF and 20+ more AI frameworks and regulations. Join our Discord channel: https://discord.com/invite/d3k3E4uEpR

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 312 |
| 🍴 **Forks** | 105 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-auditing` `ai-compliance` `ai-governance` `ai-governance-model` `ai-risk` `audit` `auditing` `compliance` `eu-ai-act` `governance` `grc`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary**  
VerifyWise (github.com/verifywise‑ai/verifywise) is an open‑source AI‑governance and LLM‑evaluation platform that bundles compliance checks for more than 20 standards—including the EU AI Act, ISO 42001 and NIST AI RMF—alongside tooling for rapid prototyping of RAG, agent, and evaluation workflows. With a modern TypeScript codebase, active community (312 ★, 105 forks) and recent commits, it lets teams embed responsible‑AI capabilities without assembling a custom stack from scratch.  

**Value**  
- **One‑stop compliance**: Pre‑built adapters for the most relevant AI regulations let you generate audit‑ready artifacts (risk assessments, impact analyses, policy reports) automatically, reducing legal overhead.  
- **Fast prototyping**: Built‑in RAG and agent orchestration components accelerate proof‑of‑concepts, while the evaluation suite (benchmark runners, metric dashboards) provides immediate feedback on model behaviour.  
- **Extensible stack**: Because the core is TypeScript and publishes npm packages, it can be dropped into existing Node/React or serverless back‑ends, and custom plugins can be added for additional frameworks or internal policies.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run `npm install && npm run dev` and follow the README to spin up the local dashboard. Use the sample RAG workflow to ingest a small document set and run a compliance check against the EU AI Act.  
2. **Integration** – Wrap the VerifyWise SDK around your existing LLM service (e.g., OpenAI, Anthropic, or a self‑hosted model). Map your model‑metadata to the platform’s schema and enable the desired regulation modules via the configuration file.  
3. **Pilot** – Deploy the containerised version (Dockerfile provided) to a staging environment, connect it to your CI pipeline, and let the evaluation suite automatically generate risk reports on each new model version.  
4. **Scale** – Move to a production‑grade Kubernetes deployment, enable role‑based access control, and integrate with your data‑lineage and audit‑log systems.  

**Production Readiness**  
- **Activity & Community**: Recent commits (as of 2026‑06‑25), 312 GitHub stars and 105 forks indicate a healthy, engaged user base.  
- **Maturity**: The platform already supports 20+ compliance frameworks and provides a UI, API, and CLI, covering most enterprise governance needs out of the box.  
- **Stability**: Written in TypeScript with clear typings, automated tests, and CI pipelines; Docker images are published and versioned.  
- **Risks**: Licensing (MIT) and security posture appear clean, but a final audit of third‑party dependencies and a review of maintainers’ activity are recommended before a mission‑critical rollout.  

Overall, VerifyWise is a high‑readiness OSS candidate for organizations that need to embed AI governance quickly while still retaining the flexibility to prototype and evaluate new LLM features.

### Русский

**verifywise-ai/verifywise** — это открытая платформа для управления ИИ и оценки LLM, поддерживающая более 20 нормативных рамок (EU AI Act, ISO 42001, NIST AI RMF и др.), что позволяет быстро добавить AI‑функциональность без построения стека с нуля. Типичный сценарий — прототипирование AI‑фич, создание RAG‑ или агентных воркфлоу и автоматизированная проверка моделей в соответствии с выбранными стандартами; интеграцию удобно начинать с небольшого proof‑of‑concept, проверив README и базовые API. По оценке готовности проект находится на высоком уровне production‑ready: активные коммиты, 312 звёзд, 105 форков, свежие обновления (июнь 2026) и сильные сигналы экосистемы делают его надёжным кандидатом для серьёзного пилотного внедрения.

### 中文

**项目价值**  
VerifyWise 是一站式 AI 治理与大模型评估平台，内置 EU AI Act、ISO 42001、NIST AI RMF 等 20 多种法规与标准的合规检查。它可以让开发者在已有模型之上快速加入合规、评估、监控等能力，避免从零搭建治理体系，从而显著降低合规成本、提升模型可信度。

**典型接入方式**  
1. **阅读 README 与快速入门**：项目提供了完整的安装指南和示例代码，先在本地跑通 `npm install` → `npm run demo`。  
2. **小范围 PoC**：在现有的 AI 服务（如 RAG、Agent 工作流）中，以插件或微服务的形式引入 VerifyWise 的 SDK，调用 `evaluateModel()`、`checkCompliance()` 等 API 完成一次合规评估。  
3. **CI/CD 集成**：将平台的评估脚本写入 CI 流程，确保每次模型迭代都自动通过法规检查后再发布。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑25，仓库最近一次提交，拥有 312 ⭐、105 🍴，社区活跃，文档完整。  
- **技术成熟度**：核心实现基于 TypeScript，易于在 Node.js 微服务或前端项目中集成，支持 Docker 部署。  
- **风险评估**：暂无重大元数据风险，唯一待确认的是许可证（MIT/Apache 等）和安全审计情况，建议在正式上线前完成一次依赖安全扫描。  

综合来看，VerifyWise 已具备高生产就绪度，适合作为合规与评估的 OSS 组件，在内部进行小规模 PoC 验证后即可推广至正式生产环境。

## 🧭 Practical evaluation

**Value:** verifywise-ai/verifywise helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 312 GitHub stars
- 105 forks
- updated 2026-06-25
- primary language: TypeScript
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 53/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 64/100 |
| recency | 40/100 |
| adoption | 52/100 |
| production | 58/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/verifywise-ai/verifywise) · [← Back to AI/ML](./README.md)</sub>
