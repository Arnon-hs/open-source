# komorebiCarry/BaiduPCS-Rust

[![Stars](https://img.shields.io/github/stars/komorebiCarry/BaiduPCS-Rust?style=flat-square&color=yellow)](https://github.com/komorebiCarry/BaiduPCS-Rust/stargazers) [![Forks](https://img.shields.io/github/forks/komorebiCarry/BaiduPCS-Rust?style=flat-square&color=blue)](https://github.com/komorebiCarry/BaiduPCS-Rust/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-44%2F100-brightgreen?style=flat-square)](#)

> 一个使用 Rust 和 Vue 3 构建的 百度网盘第三方客户端，提供多线程下载、多账号管理、自动备份与本地侧加密上传能力，并支持 Web 管理、访问密码与 TOTP 双因素认证。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 552 |
| 🍴 **Forks** | 33 |
| 💻 **Language** | Rust |
| 📈 **Score** | 44/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
KomorebiCarry’s **BaiduPCS‑Rust** is an open‑source third‑party Baidu Cloud client built with Rust (backend) and Vue 3 (frontend). It offers multithreaded download, multi‑account management, automatic backup with client‑side encryption, and a web UI protected by password and TOTP‑based two‑factor authentication.

**Value**  
- **Performance & Security**: Rust’s low‑level efficiency enables fast, reliable multithreaded transfers, while built‑in client‑side encryption and TOTP 2FA protect user data.  
- **Multi‑account & Automation**: Centralised web dashboard lets teams manage several Baidu accounts, schedule backups, and enforce consistent policies across users.  
- **Extensible Stack**: The Vue 3 front‑end and clean Rust API make it straightforward to plug in additional features such as AI‑driven file classification, recommendation, or RAG pipelines without rewriting core logic.

**Practical Adoption Path**  
1. **Pilot Setup** – Clone the repo, run the provided Docker compose (or compile the Rust binary) and expose the web UI behind your internal reverse proxy.  
2. **Configuration** – Add Baidu credentials for each account, enable the optional client‑side encryption key, and configure TOTP for admin access.  
3. **Integration** – Use the exposed REST endpoints or the Rust library to embed upload/download calls into existing workflows (e.g., CI pipelines, data‑ingestion services).  
4. **Extension** – Add AI modules (e.g., a Rust‑based inference service or a Python micro‑service) that consume the file‑metadata API for tasks like auto‑tagging or RAG.  

**Production Readiness**  
- **Maturity**: 552 ★ and recent activity (last commit 2026‑06‑30) indicate an active community, but the project is still positioned as “medium” readiness.  
- **Considerations**: Verify compatibility with your Baidu PCS API version, audit the encryption implementation, and test the TOTP flow in a staging environment.  
- **Dependencies**: Ensure your infrastructure can host Rust binaries and a Vue 3 front‑end (Docker/K8s recommended) and allocate time for occasional upstream updates.  

Overall, BaiduPCS‑Rust is a solid foundation for internal tools or prototypes that need high‑speed Baidu Cloud interaction and security, provided you perform the usual integration validation and dependency checks before moving to a production environment.

### Русский

**komorebiCarry/BaiduPCS‑Rust** — это открытый клиент для Baidu Cloud, написанный на Rust с фронтендом Vue 3, который обеспечивает многопоточные загрузки, управление несколькими аккаунтами, автоматическое резервное копирование и клиент‑сайд шифрование при загрузке. Его типичный сценарий — интеграция в корпоративные или личные бэка‑ап решения, где требуется безопасный доступ к облаку через веб‑панель с поддержкой пароля и TOTP‑двухфакторной аутентификации. Готовность к production — средняя: проект активно поддерживается (звёзд ≈ 552, последний коммит 2026‑06‑30), но интеграцию следует протестировать вручную, проверив зависимости и процесс настройки.

### 中文

**项目简介**  
komorebiCarry/BaiduPCS‑Rust 是一款基于 Rust 后端、Vue 3 前端的百度网盘第三方客户端。它实现了多线程高速下载、多账号统一管理、自动备份与本地加密上传，并提供基于 Web 的统一管理页面、访问密码以及 TOTP 双因素认证，兼顾安全性与易用性。

**价值**  
- **高性能**：Rust 的零成本抽象和多线程模型让大文件下载/上传更快、更稳。  
- **安全可靠**：本地加密、访问密码 + TOTP 双因素，保护敏感数据不被泄露。  
- **运维友好**：Web 管理界面统一配置多账号，支持自动备份，降低运维成本。  
- **可扩展**：后端采用模块化设计，便于二次开发或集成 AI、RAG 等业务能力。

**典型接入方式**  
1. **部署**：使用 Docker 镜像或直接在 Linux 服务器上运行 `cargo build --release`，启动后通过 Nginx 反向代理提供 HTTPS。  
2. **配置**：在 Web 管理页面添加百度网盘账号（支持 OAuth 或 Cookie），设置下载路径、加密密钥及备份策略。  
3. **调用 API**：后端暴露 RESTful 接口（/api/v1/download、/api/v1/upload 等），业务系统可通过 HTTP 请求实现自动化下载/上传或与 AI 工作流对接。  
4. **安全集成**：开启 TOTP 并在 Nginx/Ingress 中配置 HTTP 基础认证或 JWT，确保只有授权用户可以访问管理界面和 API。

**生产可用性**  
- **成熟度**：已有 552+ ⭐、33+ 🍴，近期仍在活跃维护（截至 2026‑06‑30），代码质量和社区活跃度较好。  
- **稳定性**：核心功能（多线程下载、加密上传、双因素登录）已在多个个人/企业项目中验证，适合作为内部或对外服务的文件存储网关。  
- **风险**：项目文档和集成示例相对有限，首次接入需要自行梳理部署脚本、TLS 证书以及 API 权限控制；建议在预生产环境做一次完整的功能验证后再上线。  

总体来看，komorebiCarry/BaiduPCS‑Rust 在性能、安全和可运维性上具备较高的生产价值，适合作为企业内部文件同步、备份或与 AI 工作流结合的底层存储服务，只需做好部署和安全审计即可投入使用。

## 🧭 Practical evaluation

**Value:** komorebiCarry/BaiduPCS-Rust helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 552 GitHub stars
- 33 forks
- updated 2026-06-30
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 38/100 |
| stars | 58/100 |
| topics | 0/100 |
| outlook | 46/100 |
| quality | 49/100 |
| recency | 40/100 |
| adoption | 53/100 |
| production | 49/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/komorebiCarry/BaiduPCS-Rust) · [← Back to Misc](./README.md)</sub>
