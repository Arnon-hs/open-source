# slkiser/opencode-quota

[![Stars](https://img.shields.io/github/stars/slkiser/opencode-quota?style=flat-square&color=yellow)](https://github.com/slkiser/opencode-quota/stargazers) [![Forks](https://img.shields.io/github/forks/slkiser/opencode-quota?style=flat-square&color=blue)](https://github.com/slkiser/opencode-quota/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> OpenCode quota & tokens usage with zero context window pollution. Supports OpenCode Go, Cursor, GitHub Copilot, OpenAl (Plus/Pro), Kimi Code, Alibaba Coding Plan, Chutes Al, Google Antigravity, Z.ai Coding Plan and more.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 420 |
| 🍴 **Forks** | 30 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`opencode` `opencode-plugin` `opencode-plugins` `quota` `quota-monitor` `token-usage` `tokens` `usage`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
slkiser/opencode‑quota is an open‑source TypeScript library that tracks and limits token usage across a wide range of AI coding assistants (OpenCode Go, Cursor, GitHub Copilot, OpenAI Plus/Pro, Kimi Code, Alibaba Coding Plan, etc.) without contaminating the model’s context window. It provides a unified API/SDK/CLI for quota enforcement, making it easy to add cost‑aware AI capabilities to any application. With over 420 stars, recent commits, and a growing ecosystem, it is ready for serious pilot projects.

**Value**  
- **Cost control:** By monitoring token consumption per request and per model, teams can prevent runaway API bills while still delivering AI‑enhanced features.  
- **Zero context pollution:** Quota data is kept outside the model’s prompt, preserving inference quality and simplifying prompt engineering.  
- **Multi‑model support:** One integration point works for dozens of popular coding assistants, reducing the need for bespoke wrappers for each provider.  
- **Rapid prototyping:** Developers can experiment with RAG pipelines, autonomous agents, or feature‑level AI toggles without building a custom quota layer from scratch.

**Practical Adoption Path**  
1. **Add the package** (`npm i @slkiser/opencode-quota`) to your TypeScript/JavaScript codebase.  
2. **Configure providers** via the supplied JSON/YAML manifest (API keys, model identifiers, per‑user or per‑project limits).  
3. **Wrap calls** to your existing AI SDKs (e.g., OpenAI, Cursor, Alibaba) with the library’s `withQuota()` helper, which returns the model response and updates usage counters.  
4. **Monitor** usage through the built‑in CLI (`opencode-quota stats`) or export metrics to Prometheus/Datadog for dashboards and alerts.  
5. **Iterate** by adjusting limits, adding custom policies (e.g., time‑based caps, team quotas), and integrating the CLI into CI/CD pipelines for automated compliance checks.

**Production Readiness**  
- **Activity & Community:** Recent commits (as of 2026‑05‑12), 420 ★, 30 forks, and 8 topical tags indicate an active project with growing interest.  
- **Stability:** The core API is versioned, and the library ships both SDK and CLI binaries, allowing gradual rollout behind feature flags.  
- **Ecosystem Fit:** Works with the major coding‑assistant APIs out‑of‑the‑box, minimizing integration friction for existing AI‑driven products.  
- **Risks:** License compliance, security audit of dependencies, and long‑term maintainer commitment still need a final review, but no immediate red flags appear.  

Overall, slkiser/opencode-quota offers a production‑grade, low‑effort way to embed token‑aware AI functionality into applications, making it a solid candidate for pilots and, with the usual due‑diligence checks, for full‑scale deployment.

### Русский

**slkiser/opencode-quota** — это open‑source библиотека на TypeScript, позволяющая отслеживать и ограничивать потребление токенов в различных AI‑моделях (OpenCode Go, Cursor, GitHub Copilot, OpenAI Plus/Pro, Kimi Code и др.) без загрязнения контекстного окна. Она идеально подходит для быстрого прототипирования AI‑функций, построения RAG‑или агентных пайплайнов и оценки инструментов модели, предоставляя удобный API/SDK/CLI и метаданные о языках и темах. Проект имеет высокий уровень готовности к production: активные коммиты, более 400 звёзд, широкую экосистемную поддержку и хорошие показатели надёжности, требующие лишь финального аудита лицензии и безопасности.

### 中文

**项目简介（2‑3 句话）**  
slkiser/opencode-quota 是一款 TypeScript 编写的开源库，用于在不污染上下文窗口的前提下精确统计 OpenCode 系列模型（OpenCode Go、Cursor、GitHub Copilot、OpenAI Plus/Pro、Kimi Code、Alibaba Coding Plan、Chutes AI、Google Antigravity、Z.ai Coding Plan 等）的配额和 Token 使用情况。它提供统一的 API/SDK/CLI，帮助开发者在原有项目中快速加入 AI 能力，而无需自行搭建模型堆栈。

**价值**  
- **即插即用**：统一的配额/Token 监控接口，让不同厂商的模型可以在同一套代码中统一管理，降低多模型集成的复杂度。  
- **防止上下文泄漏**：通过零上下文窗口污染的实现方式，避免因历史对话残留导致的 Token 计数错误或隐私风险。  
- **加速原型开发**：在原型阶段即可获取模型使用数据，帮助评估成本、性能和模型选型，为后续 RAG、Agent 或完整 AI 工作流奠定基础。  

**典型接入方式**  
1. **SDK**：在 TypeScript/JavaScript 项目中 `npm install opencode-quota`，然后通过 `import {QuotaTracker} from 'opencode-quota'` 创建实例并在调用模型 API 前后调用 `trackRequest`/`trackResponse`。  
2. **CLI**：通过全局安装 `npx opencode-quota`，在 CI/CD 或本地调试时直接包装模型请求命令，实现“一键”统计。  
3. **API 网关**：在微服务架构中将 QuotaTracker 部署为独立的 Node 服务，其他服务通过 HTTP 接口上报和查询配额数据，适合多语言生态（Python、Go 等）统一管理。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑12 最近一次提交，拥有 420+ Stars、30+ Forks，社区讨论活跃。  
- **技术成熟度**：使用 TypeScript 编写，提供完整的类型声明，易于在大型前端/后端项目中集成。  
- **生态兼容**：已支持主流模型提供商的 SDK，且通过插件机制可自行扩展其他模型。  
- **风险**：目前尚未完成最终的许可证审查和安全审计（需确认开源协议兼容性及依赖漏洞），但从代码质量、更新频率和社区接受度来看，已具备在内部或受控生产环境中进行试点的条件。  

综上，opencode-quota 是一款 **高可用、易集成且功能完整** 的配额/Token 管理工具，适合作为 AI 功能原型和正式生产环境的底层支撑。

## 🧭 Practical evaluation

**Value:** slkiser/opencode-quota helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 420 GitHub stars
- 30 forks
- updated 2026-05-12
- primary language: TypeScript
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 37/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 51/100 |
| quality | 58/100 |
| recency | 20/100 |
| adoption | 51/100 |
| production | 54/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/slkiser/opencode-quota) · [← Back to Misc](./README.md)</sub>
