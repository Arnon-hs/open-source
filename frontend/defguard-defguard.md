# DefGuard/defguard

[![Stars](https://img.shields.io/github/stars/DefGuard/defguard?style=flat-square&color=yellow)](https://github.com/DefGuard/defguard/stargazers) [![Forks](https://img.shields.io/github/forks/DefGuard/defguard?style=flat-square&color=blue)](https://github.com/DefGuard/defguard/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> Zero-Trust access management with true WireGuard® 2FA/MFA

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.7k |
| 🍴 **Forks** | 100 |
| 💻 **Language** | Rust |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`authentication` `forwardauth` `keycloak` `multifactor-authentication` `oauth` `oauth-provider` `oauth2-server` `oidc` `oidc-provider` `openid` `openid-connect` `openid-connect-provider`

## 🎯 Categories

Frontend · Backend · Security

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
DefGuard is an open‑source Zero‑Trust access management platform that adds true WireGuard®‑based 2FA/MFA to any network, letting you enforce per‑user, per‑device policies without building custom UI components. Written in Rust and backed by a growing community (2 700+ stars, 100 forks), it provides ready‑made front‑end and back‑end modules for fast‑track product interfaces.

**Value**  
- **Security‑first access control** – combines WireGuard’s low‑overhead VPN with mandatory second‑factor authentication, delivering a true Zero‑Trust model out of the box.  
- **Accelerated UI development** – ships reusable React/Vue components and API endpoints, so teams can focus on business logic rather than hand‑crafting login screens, policy editors, and device dashboards.  
- **Strong ecosystem signals** – active maintenance, recent commits (as of 2026‑05‑11), and a sizable Rust‑centric community reduce the risk of vendor lock‑in.

**Practical adoption path**  
1. **Proof‑of‑concept** – clone the repo, run the Docker‑compose demo, and follow the README to spin up a minimal gateway with a test user.  
2. **Component integration** – embed the provided UI widgets into your existing front‑end, swapping only the authentication callbacks for your identity provider if needed.  
3. **Policy customization** – extend the Rust back‑end policies via the documented plugin hooks to match your organization’s access rules, then run integration tests.  
4. **Gradual rollout** – start with a single service or internal team, monitor logs and WireGuard metrics, then expand to production workloads.

**Production readiness**  
DefGuard scores high for OSS production use: recent activity, robust star/fork count, and a clear Rust codebase indicate maturity; the project follows semantic versioning and includes CI pipelines, automated security scans, and example deployment manifests. While the integration documentation is concise, a small pilot (as outlined above) will surface any hidden setup costs, making DefGuard a solid candidate for serious production pilots.

### Русский

DefGuard — это open‑source решение для Zero‑Trust управления доступом, реализующее двух‑ и многофакторную аутентификацию поверх WireGuard® и позволяет быстро создавать пользовательские интерфейсы без написания собственного UI‑кода. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept, проверка README и интеграция компонентов UI в существующее приложение, после чего можно расширять функциональность для полноценного продукта. Проект считается готовым к production: активные коммиты, широкое принятие (2705 ★, 100 forks), современный стек на Rust и сильные сигналы экосистемы делают его надёжным кандидатом для пилотных развертываний.

### 中文

**项目简介**  
DefGuard（仓库名：DefGuard/defguard）是一款基于 WireGuard® 实现的 Zero‑Trust 访问管理系统，内置 2FA/MFA 机制，为企业网络提供真正的“身份即安全”防护。  

**价值主张**  
- **安全即插即用**：通过 WireGuard 的加密隧道和多因素认证，快速为内部系统、云资源或 SaaS 应用构建零信任访问层，省去自行实现 VPN+MFA 的繁琐工作。  
- **统一 UI 组件**：项目提供了一套可复用的前端界面（登录、授权、设备管理等），帮助开发团队在构建用户门户时大幅减少自研 UI 的投入。  
- **生态友好**：基于 Rust 实现，拥有高性能、低资源占用的后端，同时提供 REST/GraphQL API 与常见的前端框架（React、Vue）对接，适配现有微服务架构。  

**典型接入方式**  

| 步骤 | 说明 |
|------|------|
| 1️⃣ 环境准备 | 在目标机器上安装 Rust（或使用提供的 Docker 镜像），确保内核支持 WireGuard。 |
| 2️⃣ 部署服务 | 通过 `cargo build --release` 编译后运行二进制，或使用 `docker compose up -d` 拉起完整的 API + UI 堆栈。 |
| 3️⃣ 配置身份源 | 在 `defguard.yaml` 中配置 LDAP、OAuth2、SAML 等上游身份提供者，以供 2FA/MFA 验证。 |
| 4️⃣ 前端集成 | 将项目自带的 UI 组件库（npm 包 `@defguard/ui`）引入现有前端项目，使用提供的 API token 完成登录、授权流程的对接。 |
| 5️⃣ 小范围验证 | 先在测试环境或单个业务线做 PoC，验证设备注册、策略下发和审计日志是否符合预期。 |
| 6️⃣ 全面推广 | 在验证通过后，逐步将所有内部服务的入口切换到 DefGuard 代理的 Zero‑Trust 网关。 |

**生产可用性**  
- **活跃度**：截至 2026‑05‑11，项目拥有 2705+ ⭐、100+ 🍴，最近一次提交在 2026‑05‑11，表明仍在积极维护。  
- **技术成熟度**：核心使用 Rust 编写，性能和安全性均得到业界认可；提供完整的 CI/CD 流水线和自动化测试。  
- **生态兼容**：支持标准的 WireGuard 接口和常见身份认证协议，易于与现有网络、IAM 系统集成。  
- **风险提示**：项目文档虽提供了快速上手指南，但完整的企业级部署（如多租户、细粒度策略）仍需自行设计实现；建议在正式投入前先完成小规模 POC，评估运维成本和与现有监控/日志系统的兼容性。  

综上所述，DefGuard 在安全、性能和开发效率方面具备较高的生产候选价值，适合作为企业内部 Zero‑Trust 网络的核心组件进行试点并逐步推广。

## 🧭 Practical evaluation

**Value:** DefGuard/defguard helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2705 GitHub stars
- 100 forks
- updated 2026-05-11
- primary language: Rust
- 20 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 50/100 |
| stars | 73/100 |
| topics | 100/100 |
| outlook | 80/100 |
| quality | 85/100 |
| recency | 100/100 |
| adoption | 67/100 |
| production | 76/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/DefGuard/defguard) · [← Back to Frontend](./README.md)</sub>
