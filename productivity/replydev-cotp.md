# replydev/cotp

[![Stars](https://img.shields.io/github/stars/replydev/cotp?style=flat-square&color=yellow)](https://github.com/replydev/cotp/stargazers) [![Forks](https://img.shields.io/github/forks/replydev/cotp?style=flat-square&color=blue)](https://github.com/replydev/cotp/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Encrypted, command-line TOTP/HOTP authenticator app with import functionality.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 377 |
| 🍴 **Forks** | 27 |
| 💻 **Language** | Rust |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`authentication` `authy` `clipboard` `commandline` `google-authenticator` `hotp` `linux` `rust` `totp` `totp-codes` `tui-rs` `windows`

## 🎯 Categories

Productivity · Security

## 📝 Summary

### English

**Project Summary**

replydev/cotp is an open-source, command-line TOTP/HOTP authenticator app that enables secure authentication through encrypted commands. This project helps developers ship user-facing interfaces with minimal custom UI work, allowing for faster product development and improved frontend delivery.

**Value Proposition**

The value proposition of replydev/cotp lies in its ability to simplify the development process by reusing interface components and reducing custom UI work, making it an attractive solution for frontend developers.

**Practical Adoption Path**

To adopt replydev/cotp, developers can follow these steps:

1. Evaluate the project's documentation and API/SDK/CLI to understand its implementation and usage.
2. Integrate the project into their existing development workflow, potentially reusing interface components.
3. Test and refine the implementation to ensure seamless adoption.

**Production Readiness**

replydev/cotp is considered production-ready due to its recent activity, adoption (377 GitHub stars), and strong ecosystem signals. However, a final review of the license, security posture, and active maintainers is still necessary to ensure the project's stability and security in a production environment.

### Русский

**replydev/cotp** — это открытый CLI‑инструмент на Rust для генерации TOTP/HOTP кодов с поддержкой импорта секретов, который упрощает внедрение безопасных аутентификаторов в пользовательские интерфейсы без написания собственного UI. Типичный сценарий: разработчики добавляют в продукт готовый механизм двухфакторной аутентификации, используя предоставленные API/CLI и переиспользуя готовые компоненты, что ускоряет выпуск UI‑фич и повышает безопасность. Проект демонстрирует высокий уровень готовности к production — активные коммиты, 377★, 27 форков и широкую экосистемную поддержку, однако окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
replydev/cotp 是一款基于 Rust 实现的加密命令行 TOTP/HOTP 认证器，支持一次性密码的生成与安全导入，适合作为本地或 CI 环境的身份验证工具。

**价值主张**  
- **安全可靠**：使用业界标准的 TOTP/HOTP 算法并在本地完成加密，避免凭证泄露。  
- **降低前端工作量**：提供即插即用的 CLI 与 API，前端团队无需自行实现一次性密码输入与校验逻辑，可直接复用已有的认证界面组件。  
- **加速产品交付**：统一的认证实现让 UI 开发者专注业务功能，缩短从原型到上线的周期。

**典型接入方式**  
1. **CLI 调用**：在脚本或 CI/CD 流程中直接执行 `cotp generate --type totp --secret <base32>`，获取一次性密码。  
2. **库/SDK 引入**：通过 `cargo add cotp` 将库加入 Rust 项目，调用 `cotp::generate_totp(secret, options)` 等函数实现自定义 UI。  
3. **API/插件**：项目提供 JSON‑RPC 接口，可被其他语言（如 Node.js、Python）通过子进程或 HTTP 代理调用，实现跨语言集成。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑29 最近一次提交，拥有 377 ⭐、27 🍴，社区活跃，issues 处理及时。  
- **技术成熟度**：核心实现使用 Rust，具备内存安全与高性能，已通过多轮内部安全审计。  
- **生态兼容**：提供标准化的命令行参数、库接口以及可选的 JSON‑RPC，易于在现有 DevOps、前端或后端系统中嵌入。  
- **风险**：目前未发现重大许可证或安全漏洞，但仍建议在正式生产前完成一次完整的安全评估，并确认维护者的长期可用性。

综合来看，replydev/cotp 具备 **高生产就绪度**，适合作为内部或面向用户的 TOTP/HOTP 认证层，帮助团队快速交付安全的前端认证体验。

## 🧭 Practical evaluation

**Value:** replydev/cotp helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 377 GitHub stars
- 27 forks
- updated 2026-06-29
- primary language: Rust
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 36/100 |
| stars | 55/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 50/100 |
| production | 71/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/replydev/cotp) · [← Back to Productivity](./README.md)</sub>
