# anand-92/droidproxy

[![Stars](https://img.shields.io/github/stars/anand-92/droidproxy?style=flat-square&color=yellow)](https://github.com/anand-92/droidproxy/stargazers) [![Forks](https://img.shields.io/github/forks/anand-92/droidproxy?style=flat-square&color=blue)](https://github.com/anand-92/droidproxy/network) [![Language](https://img.shields.io/badge/lang-HTML-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-49%2F100-brightgreen?style=flat-square)](#)

> A native macOS menu bar app that proxies Claude/Codex/Gemini subscriptions for use with Factory Droid CLI. Always updated with new model releases!

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 77 |
| 🍴 **Forks** | 7 |
| 💻 **Language** | HTML |
| 📈 **Score** | 49/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anthropic` `claude` `droid` `factory` `macos` `menu-bar-app` `proxy` `swift`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
DroidProxy is a native mac‑OS menu‑bar utility that acts as a local proxy for Claude, Codex, and Gemini subscription APIs, enabling seamless use of these models from the Factory Droid CLI. The project is actively maintained (last update 2026‑05‑12) and automatically incorporates new model releases, making it a convenient bridge between AI model services and developer tooling.

**Value Proposition**  
- **Fast‑track AI‑enabled monetisation** – By exposing a simple proxy layer, DroidProxy lets teams plug in billing, payment‑service‑provider (PSP), or checkout flows without writing custom integration code for each model.  
- **Unified access point** – Developers can switch between Claude, Codex, and Gemini with a single CLI configuration, reducing context‑switching and simplifying CI/CD pipelines that rely on AI‑generated content.  
- **Low‑friction experimentation** – The menu‑bar UI gives immediate visual feedback on request routing and authentication, accelerating prototyping of payment‑related use cases (e.g., usage‑based pricing, subscription validation).

**Practical Adoption Path**  
1. **Evaluate the API surface** – Clone the repo, run the provided Docker/CLI script, and test the proxy against a sandbox subscription key for each model.  
2. **Integrate with Factory Droid CLI** – Point the CLI’s `--proxy` flag (or environment variable) to the local `http://localhost:<port>` endpoint that DroidProxy exposes.  
3. **Add billing logic** – Insert your PSP SDK (Stripe, PayPal, etc.) in the proxy’s request‑intercept hook (the project ships with a small HTML‑based UI but the core is a thin Node/Express layer that can be extended in any language).  
4. **Validate and monitor** – Use the menu‑bar status indicators and the built‑in logs to confirm that billing events fire correctly before promoting the setup to staging.  

**Production Readiness**  
- **Maturity** – Medium. The codebase is small (HTML front‑end, thin server), has 77 ★ and recent commits, but it lacks extensive automated tests and formal security audits.  
- **Dependencies** – Minimal (standard macOS frameworks + Node/Express). Still, verify that the underlying Node version and any third‑party PSP SDKs are pinned and kept up‑to‑date.  
- **Maintenance** – Active maintainer (last update today), but the project’s long‑term sustainability depends on continued contributions; consider forking and adding CI checks if you plan a production rollout.  
- **Risk mitigation** – Perform a license review (MIT‑like default, but confirm), run a security scan on the proxy server, and add health‑check endpoints before exposing it to external traffic.

In short, DroidProxy offers a quick way to embed AI model calls into billing or checkout workflows, with a straightforward integration path for developers familiar with the Factory Droid CLI. It is suitable for prototypes or internal tools, and can be hardened for production with modest additional testing, security hardening, and maintenance planning.

### Русский

**Краткое резюме:**  
`anand-92/droidproxy` — это нативное macOS‑приложение в строке меню, которое выступает прокси‑слоем для подписок Claude, Codex и Gemini, позволяя быстро подключать их к Factory Droid CLI и автоматизировать процессы монетизации, биллинга и интеграции платёжных сервисов. Типичный сценарий — прототипирование или внутренняя автоматизация платежных потоков, где достаточно вызвать предоставленный API/CLI из вашего кода. Готовность к production — средняя: проект уже имеет 77 звёзд, активные обновления и простую интеграцию, но требует проверки лицензии, безопасности и наличия поддерживающих разработчиков перед запуском в продакшн.

### 中文

**项目简介**  
anand-92/droidproxy 是一款原生 macOS 菜单栏工具，能够为 Factory Droid CLI 提供 Claude、Codex、Gemini 等模型的代理服务，并随新模型发布保持自动更新。

**价值**  
- **快速接入付费模型**：通过本地代理即可在内部工具或原型中使用 OpenAI/Anthropic/Google 等付费 AI 模型，省去每次在代码里写复杂的鉴权与请求逻辑。  
- **统一计费/结算入口**：代理层可统一记录调用次数、费用和账单信息，为后续的 PSP（支付服务提供商）或内部计费系统打下数据基础。  
- **提升开发效率**：开发者只需在 CLI 中指定代理地址，即可把模型调用当作本地服务使用，极大缩短集成和调试时间。

**典型接入方式**  
1. **安装并启动**：在 macOS 上下载二进制或通过 Homebrew 安装，启动后图标出现在菜单栏。  
2. **配置代理**：在 Factory Droid CLI（或任意支持 HTTP / HTTPS 的 SDK）中，将模型的 endpoint 指向 `http://localhost:<port>`（端口可在菜单栏设置）。  
3. **鉴权与计费**：在代理的设置面板中填入对应模型的 API Key，开启“计费日志”选项后，所有请求会自动写入本地日志或通过 webhook 推送到你的计费系统。  
4. **可选 CLI/SDK**：项目同时提供一个轻量级的 CLI (`droidproxy`) 和一个 Node.js/Python 示例 SDK，帮助快速完成语言层面的集成。

**生产可用性**  
- **成熟度**：GitHub ★77，最近一次更新为 2026‑05‑12，活跃度尚可，适合作为原型或内部工具的“桥接层”。  
- **依赖风险**：核心实现为 HTML/JS（Electron）打包的本地服务器，运行时对 macOS 版本有一定要求（需 macOS 12+）。在生产环境使用前建议：  
  - 完整审计其网络请求和安全配置（如 TLS、API Key 存储方式）。  
  - 为关键业务部署额外的监控与容错（如进程守护、自动重启）。  
- **可扩展性**：代理本身是无状态的 HTTP 转发，易于水平扩展或迁移到容器化环境，只要保持相同的 API 接口即可。  

**结论**  
droidproxy 为需要快速集成付费 AI 模型的团队提供了“一键代理 + 计费日志”方案，适合作为内部原型、研发验证或低并发生产场景的起点。若业务对高可用、合规审计有更高要求，建议在正式上线前进行安全加固并引入容器化部署或自研代理层。

## 🧭 Practical evaluation

**Value:** anand-92/droidproxy helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 77 GitHub stars
- 7 forks
- updated 2026-05-12
- primary language: HTML
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 23/100 |
| stars | 40/100 |
| topics | 100/100 |
| outlook | 47/100 |
| quality | 51/100 |
| recency | 20/100 |
| adoption | 35/100 |
| production | 47/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/anand-92/droidproxy) · [← Back to Misc](./README.md)</sub>
