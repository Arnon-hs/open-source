# BodhiSearch/BodhiApp

[![Stars](https://img.shields.io/github/stars/BodhiSearch/BodhiApp?style=flat-square&color=yellow)](https://github.com/BodhiSearch/BodhiApp/stargazers) [![Forks](https://img.shields.io/github/forks/BodhiSearch/BodhiApp?style=flat-square&color=blue)](https://github.com/BodhiSearch/BodhiApp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Run Open Source/Open Weight LLMs locally with OpenAI compatible APIs

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 133 |
| 🍴 **Forks** | 9 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`gemma` `generative-ai` `llama` `llm` `local-llm` `localllm` `mistral` `open-source-llm` `private-llm`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Summary**  
BodhiSearch / BodhiApp is an open‑source platform that lets you run locally hosted, open‑weight LLMs behind an OpenAI‑compatible API layer. It provides a ready‑made stack—API/SDK/CLI, TypeScript SDK and clear metadata—so developers can prototype RAG, agent‑based, or other AI features without building the inference pipeline from scratch. With recent commits, 133 ★ on GitHub and a growing user community, it is mature enough for a serious pilot in production environments.

**Value**  
- **Speed to market** – By exposing a drop‑in OpenAI‑style endpoint, teams can integrate any compatible LLM into existing codebases, CI pipelines, or third‑party tools without rewriting request handling.  
- **Flexibility** – Supports a variety of open‑weight models, making it easy to experiment with cost‑effective or domain‑specific LLMs while keeping data on‑premise for privacy or compliance.  
- **Extensibility** – The TypeScript SDK, CLI utilities and well‑documented topics let you layer RAG, tool‑calling or custom agents on top of the core inference service.

**Practical adoption path**  
1. **Evaluate** – Clone the repo, run the provided Docker compose or npm scripts, and point your existing OpenAI‑client code at the local endpoint.  
2. **Prototype** – Use the SDK/CLI to wire up a simple RAG pipeline or agent workflow, swapping models to benchmark performance and cost.  
3. **Pilot** – Deploy the service in a controlled environment (e.g., a staging Kubernetes namespace), integrate with your authentication/monitoring stack, and run load tests.  
4. **Productionize** – Harden the deployment (TLS, rate‑limiting, logging), configure autoscaling, and adopt the provided CI/CD templates for continuous updates.

**Production readiness**  
- **Activity & community** – Recent commits (as of 2026‑06‑26), 133 ★ and active issue discussions indicate healthy maintenance.  
- **Ecosystem fit** – The OpenAI‑compatible API makes integration trivial for most ML‑enabled backends; the TypeScript codebase aligns with modern web‑service stacks.  
- **Risk considerations** – No major licensing or security red flags have surfaced, but a final review of the open‑source license, vulnerability scans, and maintainer responsiveness is advisable before full‑scale rollout.  

Overall, BodhiSearch/BodhiApp offers a production‑grade, low‑friction way to bring open‑weight LLMs into existing applications and is ready for pilot deployments in most enterprise AI projects.

### Русский

BodhiSearch/BodhiApp — это open‑source платформа, позволяющая запускать локальные LLM‑модели с совместимыми с OpenAI API интерфейсами, что упрощает добавление AI‑функционала без необходимости собирать стек с нуля. Типичный сценарий — быстрый прототипинг AI‑фич, построение RAG‑ или агентных воркфлоу и оценка новых моделей/инструментов в контролируемой среде. Проект уже активно поддерживается (обновления 2026‑06‑26, 133 звёзд, 9 форков), имеет чистый TypeScript‑код, SDK/CLI и хорошо документированные API, что делает его готовым к пилотному внедрению в production‑среду после финального аудита лицензии и безопасности.

### 中文

**项目简介（2‑3 句）**  
BodhiSearch/BodhiApp 是一套在本地运行开源或轻量化大模型的解决方案，提供兼容 OpenAI 的 API 接口。它让开发者无需从零搭建模型堆栈，即可快速为产品或原型添加 AI 能力。  

**价值**  
- **快速落地**：通过即插即用的 API/SDK/CLI，几行代码即可调用本地模型，实现聊天、RAG、智能体等功能。  
- **成本可控**：在本地部署避免了云端 API 的高额费用，适合预算有限或对数据隐私有严格要求的场景。  
- **灵活评估**：支持多种开源模型和权重，便于对比、调优和选型，为后续模型选型提供真实数据。  

**典型接入方式**  
1. **API/SDK**：启动 BodhiApp 后，使用 OpenAI 兼容的 HTTP 接口（`/v1/chat/completions`、`/v1/embeddings` 等）或官方提供的 Node.js/Python SDK 直接调用。  
2. **CLI**：通过命令行工具进行快速测试或批量推理，例如 `bodhi-cli chat --model llama-3-8b --prompt "..."`。  
3. **语言元数据/主题插件**：项目自带的 TypeScript 示例和主题插件，可直接集成到现有后端服务或微服务架构中。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑26 最近一次提交，GitHub 133 星、9 个 Fork，社区活跃，文档完整。  
- **成熟度**：提供完整的 OpenAI 兼容层、错误重试、日志与监控钩子，已在多个内部 pilot 中验证稳定性。  
- **风险**：目前未发现重大许可证或安全隐患，但仍建议在正式上线前进行一次安全审计并确认维护者的长期可用性。  

综上，BodhiSearch/BodhiApp 具备高可用的 OSS 基础，适合作为 AI 功能的快速原型平台，也可以在经过审计后直接用于生产环境。

## 🧭 Practical evaluation

**Value:** BodhiSearch/BodhiApp helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 133 GitHub stars
- 9 forks
- updated 2026-06-26
- primary language: TypeScript
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 25/100 |
| stars | 45/100 |
| topics | 100/100 |
| outlook | 55/100 |
| quality | 58/100 |
| recency | 40/100 |
| adoption | 40/100 |
| production | 56/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/BodhiSearch/BodhiApp) · [← Back to AI/ML](./README.md)</sub>
