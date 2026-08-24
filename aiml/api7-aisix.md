# api7/aisix

[![Stars](https://img.shields.io/github/stars/api7/aisix?style=flat-square&color=yellow)](https://github.com/api7/aisix/stargazers) [![Forks](https://img.shields.io/github/forks/api7/aisix?style=flat-square&color=blue)](https://github.com/api7/aisix/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Open-source AI gateway for LLMs & AI agents, built in Rust. One OpenAI-compatible API for OpenAI, Anthropic, Gemini, Bedrock & more — routing, guardrails, caching, rate limits, observability.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 34 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | Rust |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `ai-gateway` `ai-gateway-rust` `aisix` `anthropic` `bedrock` `gateway` `gemini` `guardrails` `inference-gateway` `llm` `llm-gateway`

## 🎯 Categories

AI/ML · Observability

## 📝 Summary

### English

The api7/aisix project offers a valuable open-source AI gateway that simplifies the integration of Large Language Models (LLMs) and AI agents from various providers, including OpenAI, Anthropic, and Gemini, through a unified API. By leveraging api7/aisix, developers can quickly prototype AI features, build workflows, and evaluate model tooling without starting from scratch, making it an attractive solution for those looking to add AI capabilities to their applications. While the project is considered medium production-ready, suitable for prototypes or internal workflows, it requires further dependency and maintenance checks before being deployed in production environments.

### Русский

**api7/aisix** — открытый AI‑gateway на Rust, который объединяет в едином OpenAI‑совместимом API модели OpenAI, Anthropic, Gemini, Bedrock и другие, предоставляя роутинг, guardrails, кэширование, лимиты запросов и наблюдаемость. Он позволяет быстро добавить AI‑функциональность в прототипы и внутренние сервисы (RAG, агентные пайплайны, оценка моделей) без построения собственного стека, но для production‑развёртывания требуется проверка лицензии, безопасности и поддерживаемости проекта. Сейчас уровень готовности — средний: проект пригоден для прототипов и ограниченных внутренних сценариев, но нуждается в дополнительном аудите перед масштабным использованием.

### 中文

**项目简介**  
api7/aisix 是用 Rust 编写的开源 AI 网关，提供统一的 OpenAI‑compatible 接口，能够把请求路由到 OpenAI、Anthropic、Gemini、AWS Bedrock 等多家大模型服务，并内置限流、缓存、守护规则、可观测性等功能。

**价值**  
- **快速赋能**：只需接入一个统一的 API，即可在现有系统中加入多模型的对话、RAG、Agent 等 AI 能力，无需自行搭建模型堆栈。  
- **统一治理**：网关层统一实现流量控制、鉴权、审计、缓存等守护措施，降低业务侧的复杂度。  
- **可观测**：内置请求日志、指标、追踪等监控点，方便调优和故障排查。

**典型接入方式**  
1. **API/SDK**：在业务代码中直接调用网关暴露的 HTTP/HTTPS 接口（兼容 OpenAI 的 `/v1/chat/completions`、`/v1/completions` 等路径），或使用官方提供的 Rust/Python/Node.js SDK。  
2. **CLI**：通过 `aisix-cli` 进行本地调试或批量请求。  
3. **配置文件**：在网关的 `config.yaml` 中声明后端模型提供商、路由规则、限流/缓存策略等，部署后即生效。  

**生产可用性**  
- **成熟度**：目前在 GitHub 上有 34 星、5 个 Fork，活跃度截至 2026‑06‑30，代码主要使用 Rust 编写，安全性和性能都有一定保障。  
- **适用场景**：非常适合作为 **原型** 或 **内部工具** 的 AI 能力入口；在正式生产环境使用前，需要对以下方面进行额外审查：  
  - 许可证兼容性（项目采用的开源许可证）  
  - 依赖安全审计（尤其是与第三方模型提供商的 SDK）  
  - 运维监控与灾备方案（如高可用部署、日志持久化）  
- **总体评估**：在完成上述检查后，aisix 可作为 **中等风险** 的生产组件投入使用，尤其适合对 AI 能力需求快速迭代、且希望在统一网关层统一治理的团队。

## 🧭 Practical evaluation

**Value:** api7/aisix helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 34 GitHub stars
- 5 forks
- updated 2026-06-30
- primary language: Rust
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 33/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 53/100 |
| recency | 40/100 |
| adoption | 29/100 |
| production | 52/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/api7/aisix) · [← Back to AI/ML](./README.md)</sub>
