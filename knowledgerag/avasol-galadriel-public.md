# avasol/galadriel-public

[![Stars](https://img.shields.io/github/stars/avasol/galadriel-public?style=flat-square&color=yellow)](https://github.com/avasol/galadriel-public/stargazers) [![Forks](https://img.shields.io/github/forks/avasol/galadriel-public?style=flat-square&color=blue)](https://github.com/avasol/galadriel-public/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> A self-hosted Claude agent that actually remembers — verbatim memory palace at zero retrieval cost, Discord + web UI, and 90%-cheaper repeat calls via prompt caching.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 49 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | Python |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `ai-agent` `anthropic` `cache` `claude` `discord-bot` `memory-management` `mempalace` `prompt-caching` `prompt-engineering` `self-hosted`

## 🎯 Categories

Knowledge/RAG · Automation · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Galadriel‑public is a self‑hosted Claude‑based AI agent that retains verbatim “memory‑palace” context at zero retrieval cost, offering a Discord and web UI plus prompt‑caching that cuts repeat‑call expenses by up to 90 %. It lets teams index internal knowledge bases and use the cached context to ground assistant responses, turning static documents into searchable, conversational assets.

**Value**  
- **Persistent, cost‑effective memory:** The agent stores exact excerpts of source material, so follow‑up queries can be answered without re‑fetching or re‑embedding the data, dramatically lowering API spend.  
- **Unified front‑ends:** A ready‑made Discord bot and web dashboard let non‑technical users interact with the knowledge store instantly.  
- **Prompt caching:** By reusing previously computed prompts, the system reduces latency and token usage, making large‑scale internal RAG (retrieval‑augmented generation) affordable.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC):** Clone the repo, follow the README to spin up the Docker compose stack, and point the agent at a small, well‑structured knowledge source (e.g., a product FAQ).  
2. **Integration Test:** Connect the Discord bot or embed the web UI into an existing internal channel and run a handful of real queries to validate answer relevance and caching behavior.  
3. **Scale‑Up:** Gradually ingest larger document collections, tune the memory‑palace indexing parameters, and monitor cost savings from prompt caching.  
4. **Production Hardening:** Add authentication, audit logging, and CI/CD pipelines; lock down the underlying Claude API keys; and perform security and license compliance reviews.  

**Production Readiness**  
- **Maturity:** Medium. The project is functional for prototypes and internal workflows, with recent updates (June 2026) and modest community interest (≈50 stars).  
- **Dependencies:** Pure Python with Docker support; requires a Claude API key and a Redis/SQL backend for caching.  
- **Risks:** Limited external contributors, so long‑term maintenance rests on the core team; the license and security posture need final verification before a public‑facing deployment.  
- **Next Steps:** Conduct a small PoC, verify licensing, and implement operational safeguards (monitoring, rate‑limiting, secret management) before promoting Galadriel‑public to production use.

### Русский

**avasol/galadriel-public** — это самодостаточный агент на базе Claude, который хранит контекст в «вербатим‑памяти» (memory palace) без затрат на извлечение, предоставляет Discord и веб‑интерфейс и экономит до 90 % стоимости повторных запросов благодаря кэшированию промптов. Его типичное внедрение — небольшое POC‑проект: индексировать внутренние базы знаний, улучшить поиск по документам и использовать полученный контекст для более точных ответов ассистентов; после проверки README и базовых зависимостей проект готов к прототипам и внутренним рабочим процессам. Готовность к production — средняя: функционал стабилен, но требуется дополнительный аудит лицензии, безопасности и поддерживаемости перед масштабным развертыванием.

### 中文

**项目简介（2‑3 句）**  
Avasol/galadriel‑public 是一个自托管的 Claude 代理，拥有“逐字记忆宫殿”功能，可在零检索成本下完整记忆对话内容，并提供 Discord 与 Web UI 交互界面。通过提示缓存实现约 90% 的重复调用成本削减，适合在内部系统中构建高效的知识检索与问答助手。

**价值**  
- 将企业内部文档、知识库等非结构化信息快速索引，形成可搜索的记忆体，提升助手的上下文准确性。  
- 零检索成本的记忆机制让同一信息多次被调用时几乎不产生额外费用，显著降低运营成本。  
- 多渠道 UI（Discord、Web）方便团队直接在熟悉的工具中使用，降低学习门槛。

**典型接入方式**  
1. **准备知识库**：将需要检索的文档（Markdown、PDF、HTML 等）放入项目的 `data/` 目录或通过 API 上传。  
2. **运行服务**：使用 Docker Compose（或直接 `python -m galadriel`）启动后端服务，默认在 8000 端口提供 REST/WS 接口。  
3. **配置前端**：在 `config.yaml` 中填写 Discord Bot Token 与 Web UI 端口，启动对应的 UI 服务。  
4. **集成调用**：在业务系统中调用 `/api/query` 接口，传入用户提问，即可得到基于记忆宫殿的上下文丰富答案。  
5. **验证 & 调优**：先在小规模文档集上做 PoC，观察检索准确率与缓存命中率，再逐步扩大索引范围。

**生产可用性**  
- **成熟度**：目前评分 65/100，GitHub 有 49 星、8 个 fork，最近一次提交在 2026‑06‑23，代码以 Python 为主，社区活跃度一般。  
- **适用场景**：非常适合作为原型或内部工作流的知识检索层；在对成本敏感且需要多轮上下文保持的场景下表现突出。  
- **上线注意**：在正式生产前需完成以下检查：  
  1. **许可证合规**：确认项目使用的开源许可证与企业政策匹配。  
  2. **安全审计**：审查依赖库（尤其是网络、Discord 相关）是否存在已知漏洞。  
  3. **运维准备**：配置持久化存储（向量数据库或本地文件）、监控日志、自动重启容器等。  
  4. **性能验证**：在真实文档规模下测试缓存命中率与响应时延，确保满足 SLA。  

综合来看，galadriel‑public 在内部原型和中小规模生产环境中具备可用性，但在大规模、对安全合规要求严格的业务中仍需进行充分的评估与加固后方可上线。

## 🧭 Practical evaluation

**Value:** avasol/galadriel-public helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 49 GitHub stars
- 8 forks
- updated 2026-06-23
- primary language: Python
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 36/100 |
| topics | 100/100 |
| outlook | 57/100 |
| quality | 55/100 |
| recency | 40/100 |
| adoption | 33/100 |
| production | 53/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/avasol/galadriel-public) · [← Back to Knowledgerag](./README.md)</sub>
