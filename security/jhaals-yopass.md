# jhaals/yopass

[![Stars](https://img.shields.io/github/stars/jhaals/yopass?style=flat-square&color=yellow)](https://github.com/jhaals/yopass/stargazers) [![Forks](https://img.shields.io/github/forks/jhaals/yopass?style=flat-square&color=blue)](https://github.com/jhaals/yopass/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Secure sharing of secrets, passwords and files

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.9k |
| 🍴 **Forks** | 423 |
| 💻 **Language** | Go |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`encryption-decryption` `hacktoberfest` `password-sharing` `sharing-secrets`

## 🎯 Categories

Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Yopass (jhaals/yopass) is an open‑source Go application for securely sharing secrets, passwords, and files via one‑time, self‑destructing links. With a strong community (2,869 ★, 423 forks) and recent commits, it offers a lightweight, browser‑friendly way to transmit sensitive data without exposing it to long‑term storage. It’s well‑positioned for a quick pilot to test security‑by‑design workflows.

**Value**  
- **Early risk detection** – By providing a controlled, expiring channel for secrets, teams can surface credential‑leakage and misconfiguration issues before they reach production.  
- **Privacy and compliance** – One‑time links and automatic deletion help meet data‑privacy requirements and reduce the attack surface for credential reuse.  
- **Ease of integration** – Simple HTTP API and minimal dependencies let you embed Yopass in CI/CD pipelines, internal tools, or as a standalone “share‑a‑secret” service.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Deploy the official Docker image or run the binary in a sandboxed environment; use the README examples to generate a test secret and verify expiration behavior.  
2. **Auth/Policy Layer** – Add optional authentication (e.g., OAuth2, LDAP) or reverse‑proxy it behind an SSO gateway to restrict who can create or retrieve links.  
3. **CI/CD Integration** – Wrap the CLI in build scripts to automatically share temporary credentials (e.g., database passwords) between pipeline stages, then retire the link after use.  
4. **Monitoring & Auditing** – Enable logging of link creation and access events, and integrate with existing SIEM tools to track secret usage.

**Production Readiness**  
Yopass scores high for production use: it is actively maintained (last commit 2026‑06‑24), has strong adoption signals, and is written in Go, which offers static binaries and low runtime overhead. While the license and long‑term maintainer commitment still need a final check, there are no glaring security or metadata concerns, making it a solid candidate for a serious pilot in security‑sensitive environments.

### Русский

**jhaals/yopass** — это open‑source сервис на Go для безопасного обмена паролями, секретами и файлами, позволяющий выявлять проблемы с безопасностью и конфиденциальностью ещё на ранних этапах рабочего процесса. Типичный сценарий внедрения: в рамках небольшого proof‑of‑concept добавить сервис в пайплайн CI/CD, настроить аутентификацию/контроль доступа и использовать его для передачи чувствительных данных между командами. Проект демонстрирует высокий уровень готовности к production: активные коммиты, более 2 тыс. звёзд, широкое принятие в сообществе и надёжную экосистему, что делает его подходящим кандидатом для серьёзного пилотного развертывания после финальной проверки лицензии и поддержки.

### 中文

**项目简介（2‑3 句）**  
yopass（jhaals/yopass）是一款基于 Go 的开源工具，用于在浏览器或命令行中安全地一次性分享密码、密钥和文件。它通过端到端加密和一次性链接，确保敏感信息在传输和存储过程中的机密性与完整性。

**价值**  
- **提前发现安全风险**：在 CI/CD、内部审计或临时协作环节中直接使用 yopass，可避免明文泄露，帮助团队在工作流早期捕获隐私和凭证泄漏风险。  
- **简化合规控制**：支持可选的身份验证、访问期限和一次性读取，满足 GDPR、PCI‑DSS 等合规要求的最小特权原则。  
- **降低运维成本**：无需自建加密存储或临时文件服务器，直接部署即能提供安全的临时共享服务。

**典型接入方式**  
1. **Docker/Compose 快速部署**：`docker run -p 1337:1337 jhaals/yopass`，即可在内部网络或 Kubernetes 中提供 HTTPS（可配合 Ingress/TLS）入口。  
2. **CI/CD 集成**：在 GitHub Actions、GitLab CI 等流水线里使用 `yopass-cli`，将构建产物或凭证一次性推送给审计人员或下游系统。  
3. **内部工具或自助门户**：通过 REST API（`/api/v1/secret`）或 Web UI 嵌入到内部安全门户，实现“一键生成一次性链接 + 可选登录”。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑24，项目拥有 2,869 星、423 Fork，最近一次提交在同日，表明仍在积极维护。  
- **成熟的技术栈**：使用 Go 编写，单二进制文件易于容器化和跨平台部署，社区提供了完整的 Helm Chart 与 Docker 镜像。  
- **安全审计准备**：项目默认使用 AES‑GCM 加密，支持 HTTPS，且代码已通过多次社区审计；但在正式投产前仍建议进行内部安全评估并确认许可证（MIT）符合公司合规。  
- **适合作为试点**：建议先在非生产环境进行 PoC（如内部测试环境），验证身份验证、审计日志和链接失效策略后，再推广至生产环境。  

综上，yopass 具备高可用、易集成、符合安全合规的特性，是在内部工作流中实现一次性机密共享的可靠 OSS 方案。

## 🧭 Practical evaluation

**Value:** jhaals/yopass helps catch security and privacy issues earlier in the workflow.

**Best use cases**

- strengthen security checks
- add auth or privacy controls
- audit risk earlier

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2869 GitHub stars
- 423 forks
- updated 2026-06-24
- primary language: Go
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 66/100 |
| stars | 74/100 |
| topics | 50/100 |
| outlook | 69/100 |
| quality | 75/100 |
| recency | 80/100 |
| adoption | 71/100 |
| production | 70/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/jhaals/yopass) · [← Back to Security](./README.md)</sub>
