# linux-credentials/credentialsd

[![Stars](https://img.shields.io/github/stars/linux-credentials/credentialsd?style=flat-square&color=yellow)](https://github.com/linux-credentials/credentialsd/stargazers) [![Forks](https://img.shields.io/github/forks/linux-credentials/credentialsd?style=flat-square&color=blue)](https://github.com/linux-credentials/credentialsd/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> Proposal for a Linux credential management xdg portal D-Bus specification, including webauthn/passkey support

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 226 |
| 🍴 **Forks** | 12 |
| 💻 **Language** | Rust |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`dbus` `linux` `webauthn` `xdg-portal`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary**  
linux‑credentials/credentialsd proposes a new XDG portal D‑Bus API for Linux credential management, adding first‑class support for WebAuthn/passkeys. By exposing a standardized, sandbox‑friendly interface, it lets applications request, store, and audit secrets without handling raw credential material themselves.  

**Value**  
The project tackles a long‑standing gap in the Linux desktop stack: a unified, secure way for applications to access credentials while respecting user privacy. By centralising credential handling in a dedicated daemon, developers can plug in stronger security checks, enforce privacy policies, and detect risky credential usage early in the development pipeline, reducing the chance of data‑leak bugs reaching production.  

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, build the Rust daemon, and run the supplied example client against the D‑Bus service. Verify that the portal works on your desktop environment (e.g., GNOME, KDE).  
2. **README & API validation** – Follow the README to register the portal with the XDG portal dispatcher and test the WebAuthn/passkey flows.  
3. **Integration shim** – Wrap the portal calls in a thin library (or use the existing Rust crate) and replace any ad‑hoc secret‑handling code in your application.  
4. **Policy testing** – Add unit‑ and integration‑tests that exercise the new security checks (e.g., disallowing credential export, logging access attempts).  

**Production readiness**  
*Rating: Medium* – The daemon is functional, actively maintained (last commit 2026‑06‑25) and has modest community traction (226 ★, 12 forks). It is suitable for prototypes, internal tools, or staged roll‑outs, but production deployments should first address a few open items:  

| Aspect | Status | Recommendation |
|--------|--------|----------------|
| **Stability** | Recent updates, but API surface still experimental | Pin a specific tag and monitor upstream changes |
| **Integration effort** | No out‑of‑the‑box packaging for major distros; manual D‑Bus registration required | Automate installation via Cargo or a container image; document the setup steps |
| **Security audit** | Core logic is in Rust (memory safe), but the daemon runs with elevated D‑Bus permissions | Perform an independent audit of the portal’s permission model and audit logs |
| **Maintenance** | Small maintainer team; low issue volume | Track issue tracker and consider contributing fixes if you rely on it long‑term |

If those checks are satisfied, credentialsd can be promoted from a sandboxed prototype to a production‑grade credential‑management layer for Linux applications.

### Русский

**linux-credentials/credentialsd** — это открытая спецификация и реализация XDG‑портала D‑Bus для управления учётными данными в Linux, с поддержкой WebAuthn/Passkey. Проект позволяет выявлять проблемы безопасности и конфиденциальности уже на этапе разработки, например — добавить проверку прав доступа или аудит риска перед выпуском продукта. Готовность к production — средняя: подходит для прототипов и внутренних процессов, но требует небольшого proof‑of‑concept, проверки зависимостей и уточнения пути интеграции.

### 中文

**项目简介**  
linux-credentials/credentialsd 是一个面向 Linux 的凭证管理 XDG Portal D‑Bus 规范提案，提供统一的 API 并原生支持 WebAuthn/Passkey。它旨在把安全与隐私检查前置到开发和运行时流程中，从而提前发现风险。

**价值**  
- **提前捕获安全/隐私问题**：统一的凭证入口让安全审计、权限检查和合规验证可以在业务代码之前完成。  
- **统一身份验证**：通过 D‑Bus 暴露的 portal，桌面应用、容器和服务都可以无缝使用系统级 WebAuthn/Passkey，无需自行实现硬件交互。  
- **降低重复工作**：一次实现后，所有使用 XDG Portal 的组件都能共享同一套凭证策略，提升团队效率。

**典型接入方式**  
1. **依赖添加**：在 Rust 项目中加入 `credentialsd-client`（或对应语言的 D‑Bus 绑定）作为依赖。  
2. **启动守护进程**：在目标机器上运行 `credentialsd`（可通过系统d服务或容器入口脚本启动），确保 D‑Bus 名称 `org.freedesktop.Credentials` 已注册。  
3. **调用 Portal API**：使用 D‑Bus 接口 `org.freedesktop.Credentials.Manager` 发起 `GetCredential`, `CreatePasskey`, `VerifyPasskey` 等方法；返回的 `Credential` 对象即为已验证的凭证。  
4. **小型 PoC 验证**：先在本地或 CI 环境写一个最小的 “获取凭证” 示例，确认 D‑Bus 通信、权限校验以及 WebAuthn 流程正常后，再在业务代码中替换原有的密码/令牌获取逻辑。

**生产可用性**  
- **成熟度**：当前评分 53/100，GitHub 226 星、12 Fork，活跃更新至 2026‑06‑25，代码基于 Rust，具备基本的社区关注度。  
- **适用场景**：非常适合作为原型、内部工具或安全审计平台的凭证统一层；在生产环境使用前，需要完成以下检查：  
  1. **依赖审计**：确认 `credentialsd` 及其 Rust 依赖的许可证、维护者活跃度以及是否有已知 CVE。  
  2. **运维方案**：为守护进程设计系统d/unit 文件、日志收集、容错（自动重启）以及升级策略。  
  3. **权限模型**：明确哪些用户/服务有权通过 D‑Bus 调用 portal，防止未授权的凭证访问。  
  4. **兼容性测试**：在目标发行版（如 Ubuntu 24.04、Fedora 40）上验证 D‑Bus 名称、Polkit 策略以及硬件安全密钥的兼容性。  

综上，`linux-credentials/credentialsd` 已具备可用于内部原型和安全审计的基础功能，若完成依赖安全审查和运维包装，可在生产环境中作为统一凭证管理层使用。

## 🧭 Practical evaluation

**Value:** linux-credentials/credentialsd helps catch security and privacy issues earlier in the workflow.

**Best use cases**

- strengthen security checks
- add auth or privacy controls
- audit risk earlier

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 226 GitHub stars
- 12 forks
- updated 2026-06-25
- primary language: Rust
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 28/100 |
| stars | 50/100 |
| topics | 50/100 |
| outlook | 62/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 44/100 |
| production | 63/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/linux-credentials/credentialsd) · [← Back to Misc](./README.md)</sub>
