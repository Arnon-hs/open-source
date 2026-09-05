# Scille/parsec-cloud

[![Stars](https://img.shields.io/github/stars/Scille/parsec-cloud?style=flat-square&color=yellow)](https://github.com/Scille/parsec-cloud/stargazers) [![Forks](https://img.shields.io/github/forks/Scille/parsec-cloud?style=flat-square&color=blue)](https://github.com/Scille/parsec-cloud/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Open source Dropbox-like file sharing with full client encryption !

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 307 |
| 🍴 **Forks** | 43 |
| 💻 **Language** | Rust |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cloud` `dropbox` `file-sharing` `privacy` `security` `sharing-data`

## 🎯 Categories

Data · Security

## 📝 Summary

### English

**Brief Summary**  
Scille/parsec‑cloud is an open‑source, Dropbox‑style file‑sharing service that encrypts data end‑to‑end on the client, letting engineers store and sync code, assets, or any files securely. Built in Rust with a clean API/SDK/CLI, it aims to speed up daily development loops, automate local engineering tasks, and give faster CI feedback.

**Value**  
- **Security‑first sharing** – client‑side encryption means the server never sees plaintext, satisfying compliance and internal security policies.  
- **Developer productivity** – the CLI and SDK let you script file sync into build pipelines, pull‑request checks, or local test environments, cutting the friction of manual copy‑paste or ad‑hoc file servers.  
- **Open‑source flexibility** – you can self‑host, extend the Rust codebase, or integrate with existing CI/CD tools without vendor lock‑in.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Docker compose or binary, and test the CLI against a small project repository.  
2. **Integrate** – Add the SDK or CLI commands to your build scripts (e.g., `parsec sync` before a test run or `parsec upload` after a build).  
3. **Automate CI** – Wrap the CLI in your CI pipeline to fetch encrypted artifacts at the start of a job and push results back at the end, ensuring no plaintext leaves the runner.  
4. **Scale** – Deploy the server component on a controlled environment (K8s, VM, or on‑prem), configure TLS, and enforce access policies through the provided API keys or OAuth flow.

**Production Readiness**  
- **Maturity** – Medium. The project is actively maintained (last update 2026‑06‑23), has 307 ★ and 43 forks, and is written in Rust, which offers strong safety guarantees.  
- **Suitability** – Ideal for internal tools, prototypes, or environments where security is a priority; it can be hardened for production after a review of its dependency tree, licensing, and security audit.  
- **Risks** – No major metadata issues, but a final check on the license, long‑term maintainer commitment, and any disclosed vulnerabilities is recommended before a mission‑critical rollout.

### Русский

Scille/parsec‑cloud — это открытая платформа для безопасного обмена файлами, похожая на Dropbox, но с полным сквозным шифрованием на клиенте, реализованная на Rust. Она позволяет инженерам ускорить рабочие процессы, автоматизировать локальные задачи и получать быстрый CI‑фидбэк, используя простой API/SDK/CLI. Готовность к production — средняя: проект подходит для прототипов и внутренних сервисов, однако перед выводом в продакшн требуется проверка лицензии, безопасности и активности поддержки.

### 中文

**项目简介**  
Scille/parsec‑cloud 是一款开源的类 Dropbox 文件共享系统，所有文件在客户端完成端到端加密，服务端仅存储密文。基于 Rust 实现，提供 API、SDK 与 CLI，可快速集成到现有开发流程中。

**价值体现**  
- **提升研发效率**：通过安全的云端同步与共享，开发者可以随时获取最新的代码、配置或数据文件，缩短本地环境搭建和手动拷贝的时间。  
- **安全合规**：全客户端加密确保敏感代码和资产在传输、存储全过程中保持机密，满足内部合规与数据保护要求。  
- **灵活自动化**：API/SDK/CLI 支持在 CI/CD 流水线、脚本或自定义工具中调用，实现自动化拉取/上传、权限管理等操作，提升 CI 反馈速度。

**典型接入方式**  
1. **CLI**：在 CI 脚本或本地开发机器上直接使用 `parsec` 命令行工具进行文件同步、共享链接生成等。  
2. **SDK**：通过 Rust（或通过社区提供的语言绑定）调用库函数，实现自定义的上传、下载、权限校验等业务逻辑。  
3. **REST API**：在不使用 Rust 的环境（如 Python、Go、Node.js）时，可直接调用公开的 HTTP API，配合 API‑Key/Token 完成身份验证。

**生产可用性评估**  
- **成熟度**：目前在 GitHub 上拥有约 300+ 星、40+ Fork，最近一次提交在 2026‑06‑23，代码基于 Rust，具备较好的性能和安全特性。  
- **适用场景**：适合原型开发、内部协作平台或受限的业务流程（如内部文档、配置文件同步）。在对高可用、跨地域容灾有严格要求的生产环境中，仍需进行依赖审计、容错设计及运维监控。  
- **风险与注意事项**：需进一步确认许可证兼容性、长期维护者的活跃度以及安全审计报告；如计划在面向外部用户的产品中使用，建议在正式上线前进行安全评估和灾备演练。

**总结**  
Scille/parsec‑cloud 为开发团队提供了“一键加密、即插即用”的文件共享能力，能够显著加速开发与 CI 流程，同时保持数据机密性。通过 CLI、SDK 或 REST API 任意方式接入即可快速验证，适合作为内部原型或安全敏感的工作流工具，经过额外的可靠性与安全加固后亦可进入生产环境。

## 🧭 Practical evaluation

**Value:** Scille/parsec-cloud helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 307 GitHub stars
- 43 forks
- updated 2026-06-23
- primary language: Rust
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 53/100 |
| topics | 75/100 |
| outlook | 70/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 50/100 |
| production | 68/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/Scille/parsec-cloud) · [← Back to Data](./README.md)</sub>
