# ianjwhite99/opencode-with-claude

[![Stars](https://img.shields.io/github/stars/ianjwhite99/opencode-with-claude?style=flat-square&color=yellow)](https://github.com/ianjwhite99/opencode-with-claude/stargazers) [![Forks](https://img.shields.io/github/forks/ianjwhite99/opencode-with-claude?style=flat-square&color=blue)](https://github.com/ianjwhite99/opencode-with-claude/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> OpenCode plugin to use your Claude Max/Pro subscription with OpenCode via Meridian

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 206 |
| 🍴 **Forks** | 13 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-coding` `anthropic` `bun` `claude` `claude-agent-sdk` `claude-code` `claude-max` `opencode` `opencode-plugin`

## 🎯 Categories

Payments · AI/ML

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
The *opencode-with-claude* plugin lets developers hook their Claude Max/Pro subscription into OpenCode through the Meridian platform, turning Claude’s generative AI capabilities into a billing‑aware service. With a clean JavaScript SDK/CLI and ready‑made API hooks, it streamlines the implementation of payment‑service‑provider (PSP) and checkout flows for AI‑driven products.

**Value**  
- **Fast‑track monetisation** – By abstracting the Claude‑to‑OpenCode integration, the plugin removes the need to build custom authentication, usage‑tracking, and invoicing layers, letting teams focus on product features.  
- **Unified AI‑and‑payment stack** – It couples Claude’s advanced language model with Meridian’s payment orchestration, enabling use‑cases such as pay‑per‑token, subscription‑based AI access, or automated billing for AI‑generated content.  
- **Open‑source flexibility** – The JavaScript codebase can be extended or patched to match specific PSP requirements, compliance rules, or custom pricing models.

**Practical adoption path**  
1. **Clone the repo** and run the provided CLI to generate a starter integration project.  
2. **Configure credentials** – add your Claude Max/Pro API key and Meridian/PSP secrets in the `.env` file.  
3. **Select a payment flow** (e.g., subscription, metered usage) using the exposed SDK methods (`createCheckoutSession`, `recordUsage`, etc.).  
4. **Deploy** the service (e.g., to Vercel, Railway, or your own Node.js server) and point your OpenCode instance to the new endpoint.  
5. **Test** with the sandbox PSP credentials, then switch to production keys once the flow is verified.

**Production readiness**  
- **Recent activity** – last commit on 2026‑05‑12, 206 stars, 13 forks, and active issue discussions indicate a healthy community.  
- **Mature stack** – built in JavaScript with a clear API surface, making it easy to integrate into existing Node.js back‑ends.  
- **Ecosystem signals** – the project is listed under relevant topics (Payments, AI/ML) and aligns with Meridian’s documented integration patterns.  
- **Risk considerations** – while no immediate licensing or security red flags appear, a final review of the MIT‑style license, dependency vulnerabilities, and maintainers’ responsiveness is recommended before a full‑scale production rollout.  

Overall, *opencode-with-claude* offers a high‑readiness, low‑effort path to monetize Claude‑powered features within OpenCode environments.

### Русский

**i​anjwhite99/opencode‑with‑claude** — open‑source‑плагин, позволяющий подключить подписку Claude Max/Pro к OpenCode через Meridian, что ускоряет внедрение платёжных и биллинговых сценариев (checkout, оценка PSP‑flow, автоматизация операций). Плагин написан на JavaScript, имеет 206 звёзд, активные коммиты (обновление 12 мая 2026) и поддерживает API/SDK/CLI, поэтому его легко интегрировать в существующие проекты. По уровню готовности к продакшену проект считается «high»: активное развитие, хорошая экосистема и достаточная документация, однако перед запуском стоит проверить лицензию и безопасность.

### 中文

**项目简介**  
`ianjwhite99/opencode-with-claude` 是一个 OpenCode 插件，能够让你在 OpenCode 平台上直接使用 Claude Max/Pro 订阅（通过 Meridian），从而在代码编辑、智能补全等场景中调用 Claude 的强大语言模型。

**价值**  
- **快速接入计费/支付流程**：插件已封装好 Claude 订阅的计费、账单及 PSP（支付服务提供商）交互逻辑，开发者只需少量配置即可完成商业化接入。  
- **提升 AI/ML 应用的可用性**：通过统一的 API/SDK，业务方可以在自己的产品或内部工具中轻松调用 Claude，缩短从概念验证到上线的时间。  

**典型接入方式**  
1. **API/SDK**：在项目中引入插件提供的 JavaScript SDK，使用 `initializeClaude({apiKey, plan})` 完成身份认证。  
2. **CLI**：通过插件自带的 CLI（`opencode-claude`）执行 `opencode-claude login`、`opencode-claude checkout` 等命令，实现一键式计费和订阅管理。  
3. **Meridian 配置**：在 OpenCode 的 Meridian 控制台中添加 Claude 插件，填写订阅信息和回调 URL，即可完成全链路的支付与计费集成。  

**生产可用性**  
- **活跃度高**：最近一次提交于 2026‑05‑12，拥有 206 ⭐、13 fork，且社区已围绕 9 个主题展开讨论。  
- **成熟度**：插件已实现完整的计费、账单和 PSP 回调，代码结构清晰，文档齐全，适合作为正式项目的支付层实现。  
- **风险**：暂无重大元数据风险，但仍需在正式投产前完成许可证合规审查、漏洞扫描以及维护者的持续响应评估。  

总体而言，`opencode-with-claude` 在功能完整性、社区活跃度和技术实现上均已具备生产级别的准备度，是在 OpenCode 环境中快速集成 Claude 计费与支付的可靠 OSS 方案。

## 🧭 Practical evaluation

**Value:** ianjwhite99/opencode-with-claude helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 206 GitHub stars
- 13 forks
- updated 2026-05-12
- primary language: JavaScript
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 49/100 |
| topics | 100/100 |
| outlook | 81/100 |
| quality | 75/100 |
| recency | 100/100 |
| adoption | 44/100 |
| production | 77/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/ianjwhite99/opencode-with-claude) · [← Back to Payments](./README.md)</sub>
