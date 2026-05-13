# dotenvx/dotenvx

[![Stars](https://img.shields.io/github/stars/dotenvx/dotenvx?style=flat-square&color=yellow)](https://github.com/dotenvx/dotenvx/stargazers) [![Forks](https://img.shields.io/github/forks/dotenvx/dotenvx?style=flat-square&color=blue)](https://github.com/dotenvx/dotenvx/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> a secure dotenv–from the creator of `dotenv`

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 5.4k |
| 🍴 **Forks** | 143 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `configuration-file` `curl` `dotenv` `dotenvx` `end-to-end-encryption` `env` `environment-variables` `homebrew` `secret-management` `secret-manager` `secrets`

## 🎯 Categories

DevTools · Security

## 📝 Summary

### English

**Summary**  
dotenvx/dotenvx is a security‑focused replacement for the classic `dotenv` library, offering encrypted environment variable storage and seamless decryption at runtime. With a robust CLI, SDK, and language‑agnostic API, it lets engineers automate local secret management, speed up development cycles, and tighten CI feedback loops.

**Value**  
- **Time savings:** Developers no longer need to manually copy, encrypt, or rotate `.env` files; dotenvx handles encryption, decryption, and version‑controlled secret sharing in a single command.  
- **Security boost:** Secrets are stored encrypted at rest and only decrypted in the process environment, reducing the risk of accidental leaks in repositories or CI logs.  
- **Workflow integration:** The CLI can be dropped into existing npm/yarn scripts, Docker entrypoints, or CI pipelines, making the switch painless for teams already using `dotenv`.

**Practical adoption path**  
1. **Pilot:** Add the `dotenvx` npm package to a small service, replace the existing `.env` load with `dotenvx run -- node app.js`.  
2. **Encrypt existing secrets:** Run `dotenvx encrypt` to generate an encrypted `.envx` file and commit only the encrypted version.  
3. **CI/CD integration:** Insert `dotenvx run --` before test or build steps so CI agents automatically decrypt the needed variables without exposing them in logs.  
4. **Scale:** Roll the same pattern out to other services, optionally using the shared vault feature for cross‑team secret distribution.

**Production readiness**  
- **Activity & adoption:** 5,434 GitHub stars, 143 forks, recent commits (as of 2026‑05‑13), and a healthy set of topics indicate an active community.  
- **Maturity:** The project provides a stable CLI, SDK, and clear documentation, with no known critical bugs; licensing and security audits still need a final check but no red flags have surfaced.  
- **Fit for pilot:** Given the strong signal of recent maintenance, widespread language support (JavaScript), and straightforward integration points, dotenvx is ready for a serious production pilot in any JavaScript/Node.js stack.

### Русский

**dotenvx/dotenvx** — это безопасная реализация dotenv от создателей оригинального пакета, позволяющая инженерам быстро шифровать, хранить и подгружать переменные окружения без лишних ручных шагов. Типичный сценарий: в CI/CD и локальных проектах заменяется обычный `.env` на зашифрованные файлы, которые автоматически расшифровываются через CLI/SDK, ускоряя разработку, упрощая ревью и повышая качество обратной связи в пайплайнах. Проект считается готовым к production‑использованию: активные коммиты, более 5 000 звёзд, широкая экосистема и поддержка JavaScript, однако окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
dotenvx/dotenvx 是由 `dotenv` 创始人打造的安全版 dotenv，提供加密、版本管理和团队共享的环境变量解决方案。它让开发者在本地和 CI 环境中安全、快速地加载和管理密钥，避免明文泄露。

**价值**  
- **提升开发效率**：一条命令即可加密、解密并注入环境变量，省去手动编辑 `.env` 的繁琐。  
- **加速审查与 CI 反馈**：在 CI 中自动解密并验证变量，减少因缺失或错误配置导致的构建失败。  
- **安全合规**：支持对敏感变量进行端到端加密，符合企业对机密信息的管理要求。

**典型接入方式**  
1. **CLI**：在项目根目录运行 `dotenvx push`、`dotenvx pull`、`dotenvx run <command>` 等命令，即可在本地或 CI 中自动加载加密的变量。  
2. **SDK/API**：通过 npm 包 `@dotenvx/dotenvx` 在代码中调用 `dotenvx.config()`，与传统 `dotenv` 用法保持一致，只是背后会完成解密。  
3. **语言/框架集成**：支持 JavaScript/Node.js、TypeScript、Python 等，多数框架（Express、Next.js、NestJS 等）只需添加一行初始化代码即可。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑13，项目拥有 5.4k+ Stars、143 Fork，最近一次提交在当日，表明持续维护。  
- **生态兼容**：主语言为 JavaScript，提供 npm 包和 CLI，易于在现有 Node.js 项目中直接替换 `dotenv`。  
- **风险可控**：暂无重大许可证或安全漏洞报告，仍需在正式投产前完成许可证合规和安全审计。  
综合以上因素，dotenvx/dotenvx 已具备在生产环境中试点使用的条件，适合作为安全环境变量管理的首选方案。

## 🧭 Practical evaluation

**Value:** dotenvx/dotenvx helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 5434 GitHub stars
- 143 forks
- updated 2026-05-13
- primary language: JavaScript
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 54/100 |
| stars | 79/100 |
| topics | 100/100 |
| outlook | 88/100 |
| quality | 88/100 |
| recency | 100/100 |
| adoption | 72/100 |
| production | 79/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/dotenvx/dotenvx) · [← Back to DevTools](./README.md)</sub>
