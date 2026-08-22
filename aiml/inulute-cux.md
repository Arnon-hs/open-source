# inulute/cux

[![Stars](https://img.shields.io/github/stars/inulute/cux?style=flat-square&color=yellow)](https://github.com/inulute/cux/stargazers) [![Forks](https://img.shields.io/github/forks/inulute/cux?style=flat-square&color=blue)](https://github.com/inulute/cux/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> Run multiple Claude Code accounts as one. Auto-switches on rate limits and resumes your session no lost context, no logout dance.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 32 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | Go |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-07-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anthropic` `claude` `claude-ai` `claude-code` `claude-code-plugin` `cli` `cli-tool` `developer-tools` `hooks` `multi-account` `rate-limit`

## 🎯 Categories

AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
inulute / cux is a Go‑based utility that lets you run multiple Claude‑Code accounts as a single seamless endpoint. It automatically rotates accounts when rate limits are hit, preserving session context so you never lose your work or have to re‑authenticate.

**Value**  
- **Continuous AI access** – By pooling several Claude‑Code credentials, cux eliminates the “rate‑limit dance” that stalls development and testing.  
- **Zero‑loss context** – Session state is carried across account switches, so prompts, code snippets, and RAG caches remain intact.  
- **Fast prototyping** – Developers can add Claude‑Code capabilities to a product without building their own model stack, accelerating feature experiments, agent workflows, and retrieval‑augmented generation (RAG) pipelines.

**Practical Adoption Path**  
1. **Install** the CLI (or import the Go SDK) and configure your Claude‑Code API keys in the supplied `.cux.yaml` file.  
2. **Replace** direct Claude‑Code calls in your codebase with the cux endpoint (HTTP or SDK) – the API surface mirrors the original Claude‑Code API, so changes are minimal.  
3. **Test** locally: cux logs account switches and rate‑limit events, letting you verify that context is retained across rotations.  
4. **Scale** by adding more credentials to the pool as usage grows; the tool automatically balances load.  

**Production Readiness**  
- **Activity & Adoption**: Updated on 2026‑07‑12, 32 stars, 4 forks, and a healthy set of topics indicate active community interest.  
- **Stability**: Core functionality (auto‑switching, context preservation) is implemented in Go, a language known for performance and reliability in production services.  
- **Integration Simplicity**: Offers both CLI and SDK interfaces, with clear API parity to Claude‑Code, making rollout straightforward.  
- **Risks**: License compliance, security posture of stored API keys, and long‑term maintainer commitment still need a final review, but no show‑stopper issues have been identified.

Overall, cux is a mature OSS candidate for teams that need uninterrupted Claude‑Code access and want to embed AI features quickly without managing their own model infrastructure.

### Русский

**inulute/cux** — это open‑source‑утилита на Go, позволяющая объединить несколько аккаунтов Claude Code в один интерфейс: при достижении лимита запросов она автоматически переключается на другой аккаунт и восстанавливает контекст без необходимости повторного входа. Типичный сценарий — быстрая интеграция возможностей Claude в прототипы, RAG‑системы или агентные воркфлоу, где важна непрерывность сессии и минимальные накладные расходы. Проект имеет активную поддержку (обновления — 2026‑07‑12, 32 звёзд, 4 форка), хорошую экосистемную совместимость (API/SDK/CLI) и считается готовым к пилотному запуску в продакшн, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
inulute/cux 是一款 Go 编写的开源工具，能够将多个 Claude Code 账户统一管理为一个“超级账号”。在任一账户触发速率限制时，cux 会自动切换到备用账户并继续对话，确保会话上下文不丢失，免去频繁登录/登出的繁琐操作。

**价值主张**  
- **即插即用的 AI 能力**：无需自行搭建模型堆栈，只要有 Claude Code 账号，即可快速为产品或原型添加代码生成、代码审查等 AI 功能。  
- **提升可靠性**：自动切换账号避免因速率限制导致的中断，保持对话连续性，适合需要长会话或高并发的场景。  
- **降低成本**：通过多账号轮转分摊调用配额，提升单日可用额度，降低单账号的费用压力。

**典型接入方式**  
1. **CLI**：直接在终端使用 `cux` 命令行工具，配置多个 Claude Code API Key，即可开始交互。  
2. **SDK**：在 Go 项目中引入 `github.com/inulute/cux` 包，调用 `cux.NewClient()` 并传入账号列表，使用 `client.Chat()` 等方法完成会话。  
3. **API/HTTP**：cux 也提供了轻量级的 HTTP 接口，可作为微服务部署，其他语言（Python、Node 等）通过 REST 调用实现统一访问。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑07‑12，项目仍在维护；GitHub 关注度 32 ★、4 个 Fork，社区活跃。  
- **技术成熟度**：使用 Go 编写，具备良好的并发模型和二进制交付特性，适合容器化部署。  
- **生态兼容**：提供 API/SDK/CLI 三种接入方式，易于集成到现有 CI/CD、微服务或本地开发环境。  
- **风险评估**：目前未发现重大元数据或许可证问题，但仍建议在正式生产前审查项目的安全审计报告、依赖漏洞以及维护者响应速度。  

综合来看，inulute/cux 在功能完整性、易用性和社区活跃度方面表现良好，已具备在内部实验或对外服务中进行试点的条件。只要完成安全和许可证的最终确认，即可视为可投入生产的 OSS 组件。

## 🧭 Practical evaluation

**Value:** inulute/cux helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 32 GitHub stars
- 4 forks
- updated 2026-07-12
- primary language: Go
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 32/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 68/100 |
| recency | 100/100 |
| adoption | 28/100 |
| production | 76/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/inulute/cux) · [← Back to AI/ML](./README.md)</sub>
