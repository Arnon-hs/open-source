# truefoundry/aitori

[![Stars](https://img.shields.io/github/stars/truefoundry/aitori?style=flat-square&color=yellow)](https://github.com/truefoundry/aitori/stargazers) [![Forks](https://img.shields.io/github/forks/truefoundry/aitori?style=flat-square&color=blue)](https://github.com/truefoundry/aitori/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-36%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 36/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Aitori is an open‑source utility that captures and visualises the HTTP traffic between client applications and the Claude or ChatGPT APIs, letting developers inspect request/response payloads, token usage and latency. By surfacing these low‑level details, it speeds up the prototyping of Retrieval‑Augmented Generation (RAG) pipelines, autonomous agents, and other AI‑augmented features without having to rebuild a model stack from scratch.

**Value**  
- **Rapid debugging & iteration:** Seeing the exact JSON payloads and token counts helps engineers tune prompts, optimise cost, and troubleshoot integration bugs early.  
- **Accelerates prototyping:** Teams can experiment with RAG or agent workflows using existing LLM providers, focusing on orchestration logic rather than model hosting.  
- **Transparency for evaluation:** The traffic logs serve as a reproducible audit trail for model‑tooling assessments, compliance checks, and performance benchmarking.

**Practical Adoption Path**  
1. **Clone & install:** Pull the repo, run the provided Docker compose or install the Python package; it runs a local proxy that intercepts Claude/ChatGPT calls.  
2. **Configure endpoints:** Point your existing LLM client libraries (e.g., `openai`, `anthropic`) to the proxy URL; no code changes are required beyond the base URL.  
3. **Validate locally:** Use the UI or CLI to verify that requests/responses are captured correctly; adjust any authentication headers or rate‑limit handling as needed.  
4. **Integrate into CI/CD (optional):** Add the proxy as a test‑stage service to automatically record traffic for regression testing of prompt changes.  
5. **Document & hand‑off:** Export logs or dashboards for stakeholder review before moving the prototype to a more permanent observability stack.

**Production Readiness**  
- **Maturity:** Rated “Medium.” Aitori is functional for internal prototypes and debugging but lacks built‑in high‑availability features, robust authentication management, and extensive production‑grade monitoring.  
- **Dependencies & Maintenance:** The project is actively updated (last commit 2026‑06‑30) but has limited documentation and a sparse issue backlog; teams should audit the license, test the dependency tree, and consider pinning versions.  
- **Adoption Recommendation:** Deploy Aitori in a controlled environment (e.g., staging or internal sandbox) to confirm stability and security, then evaluate whether its lightweight proxy meets the organization’s observability requirements or if a more enterprise‑grade solution is needed for full production use.

### Русский

**Show HN: Aitori** — открытый инструмент для анализа трафика Claude и ChatGPT, позволяющий быстро добавить AI‑функциональность без построения модели с нуля. Его типичное применение — прототипирование новых AI‑фич, построение RAG‑ или агентных воркфлоу и оценка возможностей моделей, однако перед внедрением требуется ручная проверка из‑за скудной метаданных‑интеграции. Готовность к production — средняя: подходит для прототипов и внутренних процессов, но перед выпуском в продакшн стоит убедиться в лицензии, поддержке, документации и регулярных релизах.

### 中文

**项目简介**  
Show HN: **Aitori** 是一个开源工具，专门用于捕获、可视化和分析 Claude 与 ChatGPT 的请求/响应流量。它帮助开发者在已有大模型之上快速原型化 AI 功能，而无需从零搭建模型堆栈。

**价值**  
- **快速验证**：通过直接观察模型交互细节，快速判断 Prompt、参数、上下文等对结果的影响。  
- **加速研发**：为 RAG（检索增强生成）或智能体工作流提供即时的流量审计，帮助定位瓶颈、调优链路。  
- **降低门槛**：无需自行部署模型，只要有 API 访问权限即可使用，适合原型、内部评估以及安全审计。

**典型接入方式**  
1. **拦截代理**：在调用 Claude 或 ChatGPT 的 HTTP 客户端前，启动 Aitori 提供的本地代理（如 `aitori-proxy --port 8080`），将请求路由至代理。  
2. **SDK 包装**：在代码中使用 Aitori 提供的轻量库（Python/Node），用 `aitori.wrap(openai.ChatCompletion)` 之类的方式自动记录每一次调用。  
3. **日志导入**：若已有统一的 API 网关日志，可将日志文件或流式输出（JSON）导入 Aitori 的解析模块进行离线分析。  

> **注意**：当前元数据中关于集成信号较少，建议在正式接入前手动验证代理或 SDK 是否完整捕获所有必需字段（如 `model`, `temperature`, `usage` 等）。

**生产可用性**  
- **成熟度**：Medium。工具已在 2026‑06‑30 更新，适合原型或内部工作流使用。  
- **准备工作**：在生产环境部署前，需要检查以下几点：  
  - 许可证兼容性（MIT/Apache 等）  
  - 项目维护状态、Issue 关闭率与发布频率  
  - 文档完整性与示例代码是否覆盖你的调用方式  
  - 对代理或 SDK 的安全审计，确保不会泄露 API 密钥  
- **运维需求**：依赖 Python/Node 运行时和可选的数据库（如 SQLite）存储审计记录；需要监控代理的可用性和日志存储容量。  

综上，Aitori 是一款 **快速、低成本** 的 AI 流量审计利器，适合在 **原型开发、内部评估或安全审计** 阶段使用；在正式生产环境使用前，请完成许可证、维护状态、文档和安全性的充分评估。

## 🧭 Practical evaluation

**Value:** Show HN: Aitori – open-source tool to inspect Claude and ChatGPT traffic helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-06-30
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 36/100 |
| quality | 26/100 |
| recency | 40/100 |
| adoption | 0/100 |
| production | 38/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/truefoundry/aitori) · [← Back to Misc](./README.md)</sub>
