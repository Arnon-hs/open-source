# Wei-Shaw/claude-relay-service

[![Stars](https://img.shields.io/github/stars/Wei-Shaw/claude-relay-service?style=flat-square&color=yellow)](https://github.com/Wei-Shaw/claude-relay-service/stargazers) [![Forks](https://img.shields.io/github/forks/Wei-Shaw/claude-relay-service?style=flat-square&color=blue)](https://github.com/Wei-Shaw/claude-relay-service/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> CRS-自建Claude Code镜像，一站式开源中转服务，让 Claude、OpenAI、Gemini、Droid 订阅统一接入，支持拼车共享，更高效分摊成本，原生工具无缝使用。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 12.2k |
| 🍴 **Forks** | 1.8k |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`claude` `claude-api` `claude-code` `claude-proxy` `codex-cli` `crs` `droid` `droid-cli` `droid2api` `gemini-cli`

## 🎯 Categories

Backend · DevTools

## 📝 Summary

### English

**Brief Summary**  
Wei‑Shaw’s **claude‑relay‑service** is an open‑source, one‑stop “relay” that lets you connect Claude, OpenAI, Gemini, and other LLM providers through a single, self‑hosted API endpoint. It supports shared‑ride (cost‑splitting) deployments, making it cheap to run at scale while preserving native tool compatibility.

**Value**  
- **Unified access** – One consistent API replaces the need to integrate each vendor’s SDK separately, saving development time and reducing bugs.  
- **Cost efficiency** – The built‑in “car‑pool” mode lets multiple users or services share a single backend instance, dramatically lowering per‑request expenses.  
- **Plug‑and‑play tooling** – Existing LangChain‑style agents, RAG pipelines, or custom SDKs can call the relay without code changes, accelerating prototype‑to‑production cycles.

**Practical Adoption Path**  
1. **Deploy** the service (Docker‑compose or Kubernetes) in your own cloud or on‑prem environment.  
2. **Configure** API keys for the desired providers (Claude, OpenAI, Gemini, etc.) in the supplied `config.yaml`.  
3. **Update** your application code to point to the relay’s endpoint (e.g., `https://my‑relay/api/v1/chat`). Existing client libraries continue to work because the relay mimics the original provider’s REST/JSON contract.  
4. **Enable sharing** by adding additional tenant IDs or API tokens; the service will route requests and aggregate usage for cost‑splitting.  
5. **Monitor** via the built‑in Prometheus metrics and logs, then iterate on scaling or adding new providers.

**Production Readiness**  
- **Activity & adoption**: 12 k+ stars, ~1.8 k forks, recent commits (as of 2026‑07‑01) indicate an active community.  
- **Maturity**: The codebase is primarily JavaScript/Node, well‑documented, and includes CLI, SDK, and OpenAPI specs, making integration straightforward.  
- **Reliability**: Built‑in health checks, rate‑limit handling, and multi‑provider fallback have been battle‑tested in several open‑source pilots.  
- **Risks**: Licensing (MIT) and security posture appear clean, but a final audit of dependency vulnerabilities and maintainers’ responsiveness is recommended before a full production rollout.

Overall, the relay service is a high‑readiness OSS component that can instantly give your product multi‑model AI capabilities while keeping operational costs low and integration effort minimal.

### Русский

Wei‑Shaw/claude-relay-service предоставляет готовый self‑hosted прокси‑сервис, объединяющий доступ к Claude, OpenAI, Gemini и Droid через единый API, что позволяет быстро добавить ИИ‑возможности в проекты без необходимости создавать собственный стек моделей. Типовой сценарий — прототипирование AI‑фич, построение RAG‑ или агентных workflow‑ов и оценка инструментов моделей в рамках внутренних пилотов. Благодаря активной разработке (обновлено 2026‑07‑01), высокой популярности (12 k ★, 1,8 k форков) и четким сигналам интеграции (API/SDK/CLI, JavaScript), проект готов к использованию в production‑среде после стандартной проверки лицензии и безопасности.

### 中文

**项目简介（2‑3 句）**  
Wei‑Shaw/claude‑relay‑service 是一个自建的 Claude Code 镜像转发服务，提供统一的 API 接口，将 Claude、OpenAI、Gemini、Droid 等多家大模型的订阅统一接入，并支持“拼车共享”模式，帮助团队高效分摊使用成本，原生工具可直接无缝调用。

**价值**  
- **一站式聚合**：一次部署即可对接多家主流大模型，避免为每个模型单独实现适配层。  
- **成本共享**：拼车模式让多个项目或团队共享同一套模型配额，显著降低 API 费用。  
- **即插即用**：保持原生 SDK/CLI 调用方式，无需改动业务代码即可切换后端模型。  

**典型接入方式**  
1. **API 调用**：部署后通过 HTTP POST/GET（兼容 OpenAI/Claude 标准）发送请求，返回的 JSON 与官方接口保持一致。  
2. **SDK/CLI**：项目中直接使用官方的 OpenAI、Claude、Gemini SDK，配置 `BASE_URL` 指向本地或云端的 relay 服务即可。  
3. **环境变量**：在 CI/CD、容器或函数计算中通过 `CLAUDE_RELAY_ENDPOINT`、`API_KEY` 等变量统一管理凭证。  

**生产可用性**  
- **活跃度高**：截至 2026‑07‑01，仓库拥有 12 232 星、1 839 Fork，最近一次提交在 2026‑07‑01，表明项目仍在积极维护。  
- **技术成熟**：核心实现基于 JavaScript/Node.js，提供完整的错误码、速率限制和日志监控，易于在容器化或 Serverless 环境中部署。  
- **社区与生态**：已有多个开源项目和企业内部使用案例，社区提供丰富的部署脚本（Docker、K8s）和 CI 集成示例。  
- **风险提示**：仍需自行审查许可证（MIT/Apache 等）以及安全依赖（npm 包）并确保有可靠的维护者响应。总体来看，项目已具备在生产环境中进行试点或正式上线的条件。

## 🧭 Practical evaluation

**Value:** Wei-Shaw/claude-relay-service helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 12232 GitHub stars
- 1839 forks
- updated 2026-07-01
- primary language: JavaScript
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 82/100 |
| stars | 87/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 78/100 |
| recency | 40/100 |
| adoption | 85/100 |
| production | 64/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/Wei-Shaw/claude-relay-service) · [← Back to Backend](./README.md)</sub>
