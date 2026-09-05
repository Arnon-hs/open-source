# sunflower0305/claude-proxy

[![Stars](https://img.shields.io/github/stars/sunflower0305/claude-proxy?style=flat-square&color=yellow)](https://github.com/sunflower0305/claude-proxy/stargazers) [![Forks](https://img.shields.io/github/forks/sunflower0305/claude-proxy?style=flat-square&color=blue)](https://github.com/sunflower0305/claude-proxy/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> Claude Code / Claude Agent SDK proxy for DeepSeek, Qwen, GLM, MiniMax, Kimi and MiMo via Anthropic Messages API

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 34 |
| 🍴 **Forks** | — |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anthropic` `claude` `claude-agent-sdk` `claude-code` `llm-proxy`

## 🎯 Categories

AI/ML · Networking · Libraries & SDKs

## 📝 Summary

### English

**Summary**  
sunflower0305/claude-proxy is a TypeScript‑based SDK and CLI that routes Anthropic‑style messages to a range of LLM providers (DeepSeek, Qwen, GLM, MiniMax, Kimi, MiMo). It lets developers add multi‑model AI capabilities to their apps without building a custom inference stack, making it ideal for rapid prototyping of RAG pipelines, autonomous agents, or feature‑level AI experiments.

**Value**  
- **Model‑agnostic front‑end**: By presenting a single Anthropic‑compatible API, the proxy abstracts away the differences between the supported providers, reducing integration effort and vendor lock‑in.  
- **Speed to prototype**: Teams can spin up AI‑enhanced features (e.g., chat assistants, document retrieval, tool‑use agents) with just a few lines of code or a CLI call, bypassing the need to set up separate SDKs or API wrappers for each vendor.  
- **Evaluation sandbox**: Because the same request format works across models, developers can benchmark performance, cost, and behavior side‑by‑side, informing model selection before committing to production.

**Practical adoption path**  
1. **Clone & install** (`npm i @sunflower0305/claude-proxy`) and configure API keys for the desired back‑ends in a `.env` file.  
2. **Replace existing Anthropic calls** with the proxy endpoint (or use the provided CLI for quick tests).  
3. **Iterate**: use the proxy to experiment with different providers, adjusting prompts or system messages without code changes.  
4. **Integrate**: once a model/provider is chosen, embed the proxy as a thin service (Docker container or serverless function) within your backend, exposing the same Anthropic‑style endpoint to downstream services.

**Production readiness**  
- **Maturity**: Medium. The project has 34 stars, recent updates (June 2026), and a clear TypeScript codebase, making it suitable for internal prototypes and low‑traffic services.  
- **Considerations before production**:  
  - Verify the license compatibility with your stack.  
  - Conduct a security audit of the proxy (especially handling of API keys and request sanitisation).  
  - Assess dependency health and plan for maintenance (e.g., pinning versions, monitoring upstream SDK changes).  
  - Perform load testing to ensure the proxy can handle your expected request volume, and implement observability (metrics, logging) around latency and error rates.  

With these checks in place, the proxy can be promoted to production for non‑mission‑critical workloads, while more critical services may still prefer direct, vendor‑specific integrations.

### Русский

Sunflower0305/claude-proxy — это TypeScript‑прокси, позволяющий подключать модели DeepSeek, Qwen, GLM, MiniMax, Kimi и MiMo к Anthropic Messages API, что упрощает добавление AI‑функциональности без построения собственного стека. Он идеален для быстрого прототипирования RAG‑систем, агентных воркфлоу и оценки разных моделей через единый SDK/CLI. Готовность к продакшну — средняя: проект подходит для внутренних и экспериментальных сервисов, но требует проверки лицензии, безопасности и обеспечения поддержки зависимостей перед масштабированием.

### 中文

**项目简介**  
sunflower0305/claude-proxy 是一款基于 Anthropic Messages API 的代理层，统一包装了 DeepSeek、Qwen、GLM、MiniMax、Kimi、MiMo 等主流大模型的 SDK/CLI 接口，帮助开发者在不自行搭建模型栈的情况下快速引入 AI 能力。

**价值**  
- **即插即用**：通过统一的消息 API，开发者只需改动少量配置即可在项目中切换或组合多家模型，省去各模型 SDK 的学习成本。  
- **加速原型**：适合快速验证 RAG、Agent、代码生成等 AI 场景，缩短 PoC 周期。  
- **统一治理**：统一的调用入口便于日志、审计、费用监控以及统一的错误处理。

**典型接入方式**  
1. **npm 安装**：`npm i @sunflower0305/claude-proxy`（或使用 yarn/pnpm）。  
2. **配置凭证**：在 `.env` 或配置文件中填写对应模型的 API Key 与 Endpoint。  
3. **代码调用**：使用 `ClaudeProxy` 类或提供的 CLI，示例  
   ```ts
   import { ClaudeProxy } from '@sunflower0305/claude-proxy';

   const client = new ClaudeProxy({ provider: 'deepseek', apiKey: process.env.DEEPSEEK_KEY });
   const resp = await client.sendMessage({ role: 'user', content: '写一个冒泡排序的 TypeScript 实现' });
   console.log(resp.content);
   ```
4. **CLI 使用**：`npx claude-proxy chat --provider qwen --message "解释一下 RAG 工作原理"`，适合调试或脚本化调用。

**生产可用性**  
- **成熟度**：项目已获得 34 个 GitHub Stars，最近一次提交在 2026‑06‑24，代码基于 TypeScript，结构清晰。  
- **适用场景**：非常适合作为内部原型、内部工具或业务实验平台的 AI 接入层。  
- **上线注意**：在生产环境使用前需完成以下检查  
  - **依赖审计**：确认所有第三方 SDK（DeepSeek、Qwen 等）版本安全且无已知漏洞。  
  - **安全合规**：核对各模型服务的使用许可与数据隐私政策，确保符合公司合规要求。  
  - **可观测性**：在代理层添加统一的日志、监控（如调用时延、错误率）以及费用追踪。  
  - **容错机制**：实现超时、重试以及降级策略，以防单一模型服务不可用。  

总体而言，`sunflower0305/claude-proxy` 在原型阶段和内部业务流程中具备较高的实用价值，经过上述生产化检查后可用于正式业务，但仍需持续关注其维护状态和安全更新。

## 🧭 Practical evaluation

**Value:** sunflower0305/claude-proxy helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 34 GitHub stars
- updated 2026-06-24
- primary language: TypeScript
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 33/100 |
| topics | 63/100 |
| outlook | 68/100 |
| quality | 55/100 |
| recency | 80/100 |
| adoption | 24/100 |
| production | 67/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/sunflower0305/claude-proxy) · [← Back to AI/ML](./README.md)</sub>
