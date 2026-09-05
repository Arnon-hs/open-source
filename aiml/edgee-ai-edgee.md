# edgee-ai/edgee

[![Stars](https://img.shields.io/github/stars/edgee-ai/edgee?style=flat-square&color=yellow)](https://github.com/edgee-ai/edgee/stargazers) [![Forks](https://img.shields.io/github/forks/edgee-ai/edgee?style=flat-square&color=blue)](https://github.com/edgee-ai/edgee/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> Open-source AI gateway written in Rust, with token compression for Claude Code, Codex... and any other LLM client.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 66 |
| 🍴 **Forks** | 10 |
| 💻 **Language** | Rust |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic` `cli` `coding-assistant` `context-optimization` `cost-optimization` `edgee` `llm-gateway` `token-compression`

## 🎯 Categories

AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
edgee‑ai/edgee is an open‑source AI gateway written in Rust that adds token‑compression and request‑routing capabilities for Claude, Codex, and any other LLM client. It lets developers plug AI features into prototypes, RAG pipelines, or agent workflows without building a custom model stack from scratch.  

**Value**  
- **Speed to market** – By handling token compression, authentication, and API routing out‑of‑the‑box, edgee removes the boilerplate that normally consumes weeks of engineering time.  
- **Language‑agnostic integration** – A thin SDK/CLI and a well‑documented HTTP API let you call the gateway from any language, making it easy to embed AI into existing services.  
- **Cost efficiency** – Compressing tokens reduces the number of tokens sent to LLM providers, lowering inference costs for high‑volume workloads.  

**Practical Adoption Path**  
1. **Evaluate** – Clone the repo, run the provided Docker compose or binary, and point your existing Claude/Codex client to the local gateway endpoint.  
2. **Prototype** – Use the CLI or SDK to route a few calls through edgee, measuring token‑compression savings and latency.  
3. **Integrate** – Replace direct LLM calls in your codebase with the gateway’s endpoint; configure per‑model routing, authentication, and any custom middleware (e.g., logging or request throttling).  
4. **Scale** – Deploy the gateway as a sidecar or a Kubernetes service, enable TLS, and monitor health via the built‑in metrics endpoint.  

**Production Readiness**  
- **Maturity** – Medium. The project has 66 stars, recent commits (as of 2026‑05‑11), and a small but active Rust codebase, indicating functional stability for internal use.  
- **Considerations** – Before production you should:  
  * Verify the license compatibility with your organization.  
  * Conduct a security audit of the Rust dependencies and the exposed HTTP API.  
  * Test resilience under load (e.g., concurrent request handling, back‑pressure).  
  * Plan for long‑term maintenance or a fork if community activity wanes.  

Overall, edgee‑ai/edgee is a solid foundation for quickly adding LLM capabilities and token‑compression to prototypes and internal tools, with a clear upgrade path to production once security and operational checks are completed.

### Русский

**edgee-ai/edgee** — это открытый AI‑gateway на Rust, который умеет сжимать токены для Claude Code, Codex и любых других LLM‑клиентов, позволяя быстро добавить возможности ИИ без построения собственного стека моделей. Типичный сценарий — прототипирование AI‑фич, построение RAG‑ или агентных воркфлоу и оценка разных моделей через единый API/SDK/CLI. Готовность к production — средняя: проект подходит для прототипов и внутренних сервисов, но перед запуском в прод требует проверки зависимостей, лицензии и безопасности.

### 中文

**项目简介**  
edgee‑ai/edgee 是一款用 Rust 编写的开源 AI 网关，内置对 Claude Code、Codex 等模型的 token 压缩，并提供统一的 API/SDK/CLI 接口，方便在任何 LLM 客户端上使用。

**价值**  
- **快速赋能**：无需自行搭建模型堆栈，直接通过网关接入多种大模型，实现 AI 功能原型化。  
- **成本优化**：token 压缩降低了调用费用，特别适合高频率的代码生成或 RAG 场景。  
- **统一治理**：统一的入口可以统一鉴权、日志、监控，帮助团队在内部工作流中统一管理 AI 调用。

**典型接入方式**  
1. **API**：通过 HTTP/REST 调用网关提供的统一端点，发送标准化的请求体即可使用任意后端模型。  
2. **SDK**：项目提供 Rust（以及通过 FFI 的其他语言）SDK，直接在代码中创建 `EdgeeClient` 并调用 `invoke`、`compress` 等方法。  
3. **CLI**：使用 `edgee` 命令行工具进行快速测试或脚本化调用，适合 CI/CD 或本地调试。  

**生产可用性**  
- **成熟度**：当前得分 66/100，GitHub 66 星、10 Fork，活跃更新至 2026‑05‑11，适合作为原型或内部业务的实验平台。  
- **准备度**：在生产环境使用前需完成以下检查：  
  - 代码依赖审计（Rust 生态的安全漏洞）。  
  - 许可证合规（确认项目采用的开源许可证与企业政策匹配）。  
  - 维护者活跃度与社区响应速度（可通过 Issue/PR 交互评估）。  
- **可行性**：若满足上述检查，edgee 可在内部服务中作为 AI 网关投入使用，尤其适合对 token 成本敏感的 RAG、代码生成或智能代理工作流。

## 🧭 Practical evaluation

**Value:** edgee-ai/edgee helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 66 GitHub stars
- 10 forks
- updated 2026-05-11
- primary language: Rust
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 26/100 |
| stars | 39/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 66/100 |
| recency | 80/100 |
| adoption | 35/100 |
| production | 67/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/edgee-ai/edgee) · [← Back to AI/ML](./README.md)</sub>
