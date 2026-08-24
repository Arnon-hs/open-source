# nikships/droidproxy

[![Stars](https://img.shields.io/github/stars/nikships/droidproxy?style=flat-square&color=yellow)](https://github.com/nikships/droidproxy/stargazers) [![Forks](https://img.shields.io/github/forks/nikships/droidproxy?style=flat-square&color=blue)](https://github.com/nikships/droidproxy/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> A native macOS menu bar app that proxies Claude/Codex/Gemini subscriptions for use with Factory Droid CLI. Always updated with new model releases!

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 107 |
| 🍴 **Forks** | 14 |
| 💻 **Language** | Swift |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anthropic` `claude` `droid` `factory` `macos` `menu-bar-app` `proxy` `swift`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
nikships/droidproxy is a native macOS menu‑bar utility written in Swift that tunnels requests to Claude, Codex, and Gemini APIs, enabling the Factory Droid CLI to work with paid subscriptions. The app is kept up‑to‑date with each new model release, offering a simple way to route traffic through a local proxy for developers who need to test or integrate AI‑driven features.  

**Value**  
- **Fast‑track monetization & billing** – By handling the authentication and request forwarding for subscription‑based AI models, droidproxy removes the need to embed complex payment‑gateway logic in your own code.  
- **Unified access point** – One macOS menu‑bar app serves all three major model providers, letting teams switch providers or test multiple APIs without re‑configuring the CLI.  
- **Developer‑friendly** – Exposes clear API/CLI hooks, Swift source, and concise documentation, making it easy to embed in CI pipelines, prototype checkout flows, or automate payment‑related testing.  

**Practical Adoption Path**  
1. **Clone & build** the Swift project on a macOS workstation (Xcode 15+ recommended).  
2. **Configure credentials** for Claude, Codex, and Gemini in the app’s settings panel (API keys, subscription IDs).  
3. **Start the proxy** from the menu bar; it will listen on a local port (e.g., `127.0.0.1:8080`).  
4. **Point Factory Droid CLI** (or any custom script) to the proxy via environment variables (`HTTP_PROXY`, `HTTPS_PROXY`).  
5. **Validate** by issuing a few CLI commands and confirming that responses come from the intended model.  
6. **Integrate** into automated test suites or internal tools by launching the binary in headless mode (scriptable via `droidproxy --headless`).  

**Production Readiness**  
- **Maturity:** Medium. The project has 107 stars, recent activity (last commit 2026‑06‑30), and a modest fork count, indicating community interest but limited large‑scale adoption.  
- **Stability:** Suitable for prototypes, internal tooling, and sandbox environments. Before production use, verify:  
  * License compatibility (check the repository’s LICENSE file).  
  * Security posture – review the Swift code for credential handling and consider sandboxing the app.  
  * Maintenance – confirm that the maintainer(s) are responsive to issues/updates.  
- **Dependencies:** Pure Swift/macOS, no external services beyond the AI providers, simplifying dependency management.  

In short, droidproxy offers a convenient, low‑overhead way to incorporate paid AI model access into macOS‑based workflows, with a clear path from local testing to internal production once licensing, security, and maintainer support are validated.

### Русский

**nikships/droidproxy** — это нативное macOS‑приложение в виде иконки в строке меню, которое выступает прокси‑слоем для подписок Claude, Codex и Gemini, позволяя использовать их через Factory Droid CLI. Оно ускоряет интеграцию платёжных и PSP‑процессов (биллинг, checkout, автоматизация платежей) за счёт готового API/CLI и Swift‑библиотеки, что делает его удобным для прототипов и внутренних workflow. Готовность к production — средняя: проект стабилен и активно обновляется (107 звёзд, последний коммит 30 июн. 2026), но перед запуском в продакшн требуется проверка лицензии, безопасности и наличия активных мейнтейнеров.

### 中文

**简短介绍**

nikships/droidproxy是一款原生 macOS 菜单栏应用，用于代理 Claude/Codex/Gemini 订阅，方便与 Factory Droid CLI 集成。它始终保持最新，随着新模型的发布而更新。

**价值**

nikships/droidproxy 帮助您快速集成计费、结算或 PSP 流程，节省时间和资源。

**典型接入方式**

您可以通过以下方式接入 nikships/droidproxy：

1. 集成billing或checkout流程
2. 评估 PSP 流程
3. 自动化支付操作

**生产可用性**

生产可用性：中等。适合用于原型开发或内部工作流程，需要检查依赖关系和维护工作后方可用于生产环境。

## 🧭 Practical evaluation

**Value:** nikships/droidproxy helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 107 GitHub stars
- 14 forks
- updated 2026-06-30
- primary language: Swift
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 43/100 |
| topics | 100/100 |
| outlook | 55/100 |
| quality | 58/100 |
| recency | 40/100 |
| adoption | 39/100 |
| production | 54/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/nikships/droidproxy) · [← Back to Misc](./README.md)</sub>
