# danog/MadelineProto

[![Stars](https://img.shields.io/github/stars/danog/MadelineProto?style=flat-square&color=yellow)](https://github.com/danog/MadelineProto/stargazers) [![Forks](https://img.shields.io/github/forks/danog/MadelineProto?style=flat-square&color=blue)](https://github.com/danog/MadelineProto/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Async PHP client API for the telegram MTProto protocol

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.4k |
| 🍴 **Forks** | 850 |
| 💻 **Language** | PHP |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`amphp` `async` `bot` `calls` `easy` `hacktoberfest` `inline-bots` `madelineproto` `mtproto` `mtproto-api` `php` `proxy`

## 🎯 Categories

Automation · Backend

## 📝 Summary

### English

**Summary**  
MadelineProto is an asynchronous PHP client library that implements Telegram’s MTProto protocol, letting developers automate interactions with Telegram without writing low‑level networking code. With 3.4 k ★ and active maintenance, it’s a mature, production‑ready OSS component for building repeatable, schedule‑driven Telegram workflows.

**Value**  
- Eliminates the need for manual Telegram actions (sending messages, handling updates, managing bots) by exposing a high‑level, event‑driven API.  
- Enables seamless integration of Telegram into existing backend pipelines, CI/CD jobs, or custom automation tools, turning ad‑hoc tasks into reliable, repeatable processes.

**Practical adoption path**  
1. **Evaluate**: Clone the repo, run the Composer install, and try the bundled CLI examples to verify connectivity with your Telegram account/bot.  
2. **Prototype**: Wrap the needed MTProto calls (e.g., sendMessage, getUpdates) in service classes within your PHP codebase; the library’s async model works with popular event loops like ReactPHP or Swoole.  
3. **Integrate**: Add the service to your orchestration layer (Docker, Kubernetes, or a simple cron job) and configure scheduled tasks or webhook listeners.  
4. **Test & Harden**: Use MadelineProto’s built‑in logging and error‑handling to simulate failure scenarios; add unit/integration tests around the wrapper.  

**Production readiness**  
- **Activity**: Recent commits (as of 2026‑05‑12), frequent releases, and a vibrant community (3420 stars, 850 forks).  
- **Ecosystem fit**: Provides API/SDK/CLI interfaces, clear PHP type hints, and extensive documentation, making integration straightforward for any PHP‑based stack.  
- **Stability**: Mature codebase with a well‑defined release process; no known critical security issues, though a final license and maintainer audit is advisable.  

Overall, MadelineProto offers a robust, low‑friction way to automate Telegram interactions in production PHP environments, with a clear path from proof‑of‑concept to fully managed operational use.

### Русский

MadelineProto — это асинхронный PHP‑клиент для MTProto, который позволяет полностью автоматизировать взаимодействие с Telegram: заменяя ручные запросы API, он легко встраивается в бэкенд‑процессы, скрипты и CI/CD‑конвейеры для периодических задач и интеграции с другими сервисами. Проект имеет высокую готовность к production — активные коммиты, более 3400 звёзд, широкое принятие в сообществе и стабильный набор функций, хотя перед запуском следует проверить лицензию и актуальность мер безопасности.

### 中文

**项目简介**  
MadelineProto（danog/MadelineProto）是一个基于 PHP 的异步客户端库，完整实现了 Telegram 的 MTProto 协议，帮助开发者在后端或自动化脚本中以高效、可靠的方式与 Telegram 交互。

**价值**  
- **消除手工操作**：提供统一的 API/SDK，能够把发送消息、管理群组、获取更新等日常 Telegram 操作自动化，显著降低人为错误和运维成本。  
- **可编排的工作流**：配合 PHP 的异步特性，可轻松嵌入到任务调度系统、CI/CD 流水线或其他业务系统，实现“一次编写、处处复用”。  

**典型接入方式**  
1. **Composer 安装**：`composer require danog/madelineproto`，即可在项目中引入库。  
2. **API/SDK 使用**：通过 `MadelineProto\API` 类实例化后调用 `messages->sendMessage()、channels->joinChannel()` 等方法进行业务实现。  
3. **CLI 工具**：库自带 `madeline.php` 脚本，可直接在命令行执行脚本或作为 Cron 任务调度，适合快速原型或运维脚本。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑12，项目拥有 3420+ Stars、850+ Forks，最近一次提交在同一天，表明仍在积极维护。  
- **成熟生态**：支持完整的 MTProto 功能、丰富的 PHP 类型提示和异常处理，已被多个开源 Bot 与企业项目采用。  
- **风险**：暂无重大许可证或安全警示，但仍建议在正式投产前审查许可证兼容性并进行安全审计。  

综上所述，MadelineProto 具备高可用的生产级别，适合作为 Telegram 自动化、后台服务或 DevOps 流程的核心组件。

## 🧭 Practical evaluation

**Value:** danog/MadelineProto helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3420 GitHub stars
- 850 forks
- updated 2026-05-12
- primary language: PHP
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 73/100 |
| stars | 75/100 |
| topics | 100/100 |
| outlook | 60/100 |
| quality | 69/100 |
| recency | 20/100 |
| adoption | 75/100 |
| production | 55/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/danog/MadelineProto) · [← Back to Automation](./README.md)</sub>
