# lis186/ccxray

[![Stars](https://img.shields.io/github/stars/lis186/ccxray?style=flat-square&color=yellow)](https://github.com/lis186/ccxray/stargazers) [![Forks](https://img.shields.io/github/forks/lis186/ccxray?style=flat-square&color=blue)](https://github.com/lis186/ccxray/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> X-ray vision for AI agent sessions — a transparent HTTP proxy and dashboard for Claude Code

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 201 |
| 🍴 **Forks** | 31 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
lis186/ccxray is an open‑source HTTP proxy and dashboard that gives you “X‑ray” visibility into Claude Code sessions, letting you monitor, debug, and replay AI‑agent interactions in real time. It acts as a thin, language‑agnostic layer that can be dropped into existing Claude‑based workflows to surface request/response payloads, token usage, and latency metrics without having to rebuild the model stack from scratch.  

**Value**  
- **Instant observability:** Provides a clear, visual trace of every Claude request, which speeds up debugging and performance tuning for RAG pipelines, autonomous agents, or any Claude‑driven feature.  
- **Rapid prototyping:** By exposing the raw HTTP traffic, developers can experiment with prompt engineering, tool‑calling, and chaining logic without writing custom logging code.  
- **Cost‑effective augmentation:** You get richer insight into Claude usage without needing to host or fine‑tune your own model, lowering the barrier to add AI capabilities to existing products.  

**Practical Adoption Path**  
1. **Spin up the proxy** – Clone the repo, run `npm install && npm start` (or use the provided Docker image) and point your Claude client’s endpoint to the proxy URL.  
2. **Configure routing** – Update your application’s HTTP client (e.g., `fetch`, `axios`, or the official Claude SDK) to target the proxy; the proxy forwards traffic unchanged to Claude’s API.  
3. **Inspect the dashboard** – Open the web UI (default `http://localhost:3000`) to view live request/response logs, token counts, and latency charts.  
4. **Iterate** – Use the captured data to refine prompts, adjust tool‑calling logic, or benchmark different Claude versions.  
5. **Hardening for production** – Add TLS termination, authentication middleware, and persistent storage for logs; optionally integrate with existing observability stacks (Prometheus, Grafana, ELK).  

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last commit 2026‑07‑03) and has modest community traction (201 stars, 31 forks).  
- **Strengths:** Straightforward JavaScript codebase, clear separation of proxy and UI, and minimal runtime dependencies make it easy to embed in internal services.  
- **Caveats:** Integration signals are sparse in the repository metadata, so you’ll need to manually verify that the proxy fits your authentication scheme, rate‑limit handling, and any custom Claude SDK wrappers you use.  
- **Readiness checklist:**  
  1. Verify TLS and API‑key handling meet your security policies.  
  2. Add health‑check endpoints and monitoring for the proxy process.  
  3. Test failure modes (timeouts, 429 responses) to ensure graceful degradation.  
  4. Evaluate operational overhead (log retention, storage costs) before scaling.  

In short, ccxray is a solid tool for prototyping and internal debugging of Claude‑based agents, but production deployments should include additional hardening and a small proof‑of‑concept validation to confirm the integration effort aligns with your operational requirements.

### Русский

Резюме:

lis186/ccxray -.transparentный HTTP-прокси и панель мониторинга для сессий агента AI, предназначенная для добавления AI-способностей без создания нового стека моделей. Этот проект особенно полезен для прототипирования AI-функций и построения РАГ или агентных потоков. Хотя lis186/ccxray пока не готов к широкому внедрению (уровень готовности - средний), он может быть хорошей опцией для внутренних прототипов или рабочих процессов.

### 中文

**项目简介（2‑3 句）**  
lis186/ccxray 为 Claude Code 会话提供“X‑光透视”，通过透明的 HTTP 代理和可视化仪表盘，让开发者实时查看、调试和分析 AI 代理的请求与响应。它帮助在现有模型之上快速叠加 RAG、Agent 或其他 AI 功能，而无需从头搭建模型堆栈。

**价值**  
- **快速原型**：即插即用的代理层，让团队在几分钟内就能捕获和审视 Claude Code 的交互细节，极大缩短 AI 功能的验证周期。  
- **可观测性**：仪表盘直观展示请求流、上下文、工具调用等元数据，帮助定位错误、优化提示和评估模型工具链。  
- **降低门槛**：无需自行部署大型模型，只需将现有 Claude Code 接口通过代理转发，即可获得完整的调试与监控能力。

**典型接入方式**  
1. **部署代理**：在本地或容器中运行 `ccxray`（Node.js），配置 `TARGET_URL` 指向 Claude Code 的 API 端点。  
2. **修改客户端**：将原本直连 Claude Code 的 HTTP 请求地址改为代理地址（如 `http://localhost:3000`），其余请求结构保持不变。  
3. **打开仪表盘**：访问 `http://localhost:3000/dashboard` 查看实时会话流、请求/响应日志以及上下文可视化。  
4. **可选扩展**：通过自定义中间件在代理层加入日志持久化、身份认证或额外的 RAG 前置处理。

**生产可用性**  
- **成熟度**：GitHub 201 星、31 叉，最近一次更新于 2026‑07‑03，代码以 JavaScript 实现，适合作为内部原型或实验平台。  
- **就绪度**：**中等**。适合原型开发、内部工具或 CI/CD 测试环境；在正式生产环境使用前，需要：  
  - 完整的安全审计（代理会转发所有请求数据）。  
  - 稳定的部署方式（如容器化或服务网格），并监控代理本身的可用性。  
  - 对接入路径进行手动验证，因为元数据中对集成细节的描述较少，可能需要自行编写适配脚本。  
- **风险**：集成路径不够透明，初始配置和调试成本相对较高；在大流量生产场景下需评估代理的性能瓶颈和可靠性。  

综上，ccxray 是一个在 **原型阶段** 极具价值的可观测性工具，经过适当的安全与运维检查后，可逐步推广到内部生产工作流中。

## 🧭 Practical evaluation

**Value:** lis186/ccxray helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 201 GitHub stars
- 31 forks
- updated 2026-07-03
- primary language: JavaScript

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 38/100 |
| stars | 49/100 |
| topics | 0/100 |
| outlook | 50/100 |
| quality | 46/100 |
| recency | 40/100 |
| adoption | 46/100 |
| production | 47/100 |
| usefulness | 74/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/lis186/ccxray) · [← Back to AI/ML](./README.md)</sub>
