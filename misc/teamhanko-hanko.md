# teamhanko/hanko

[![Stars](https://img.shields.io/github/stars/teamhanko/hanko?style=flat-square&color=yellow)](https://github.com/teamhanko/hanko/stargazers) [![Forks](https://img.shields.io/github/forks/teamhanko/hanko?style=flat-square&color=blue)](https://github.com/teamhanko/hanko/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Modern authentication, on your terms. Open source alternative to Auth0, Clerk, WorkOS, Stytch.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 9k |
| 🍴 **Forks** | 1k |
| 💻 **Language** | Go |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`2fa` `authentication` `ciam` `fido2` `iam` `jwt` `mfa` `oauth` `passkeys` `passwordless` `saml` `sso`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
teamhanko/hanko is an open‑source authentication platform that lets developers implement modern, password‑less login flows (WebAuthn, OTP, OAuth, etc.) without relying on commercial services like Auth0 or Clerk. With a Go‑centric codebase, strong community traction (≈9 k stars, 1 k forks) and recent updates, it is positioned as a production‑ready alternative for teams that need full control over identity management.

**Value**  
Hanko provides a self‑hosted, standards‑compliant auth stack that eliminates vendor lock‑in, reduces recurring SaaS costs, and enables custom security policies (e.g., on‑prem deployment, GDPR compliance). Because it is written in Go and exposes clean APIs/SDKs, it can be extended with AI‑driven features (risk‑based authentication, anomaly detection) without rebuilding the core auth logic.

**Practical adoption path**  
1. **Proof‑of‑concept** – clone the repo, follow the README to spin up the Docker‑compose demo, and integrate the JavaScript/Web SDK into a sandbox app.  
2. **Pilot** – replace the existing login provider in a low‑traffic service, configure desired flows (WebAuthn, magic‑link, social OAuth) and connect to your user database.  
3. **Production rollout** – harden the deployment (TLS, secret management, monitoring), enable audit logging, and gradually migrate users from the legacy system while keeping the Hanko instance behind a reverse‑proxy or service mesh.

**Production readiness**  
The project shows high readiness: recent commits (as of 2026‑06‑29), active maintainers, extensive community adoption, and a mature Go codebase. While the license and security audit still need a final check, the overall health signals (stars, forks, issue activity) make Hanko a solid candidate for a serious pilot in production environments.

### Русский

Резюме проекта teamhanko/hanko:

teamhanko/hanko - это open-source альтернатива приложениям для авторизации, такие как Auth0, Clerk и WorkOS. Этот проект предлагает современную систему авторизации на своих условиях, добавляя в нее возможности искусственного интеллекта без необходимости начинать с нуля. teamhanko/hanko готово к serious пилоту и имеет высокий уровень готовности к production, с сильными сигналами внедрения и экосистеме.

### 中文

**项目介绍**

teamhanko/hanko 是一个开源项目，提供现代认证解决方案，旨在替代 Auth0、Clerk、WorkOS 和 Stytch 等服务。该项目得到了强大的采用和生态系统支持，且具有高生产可用性。

**价值**

teamhanko/hanko 帮助开发者在不从头构建模型堆栈的情况下添加 AI 能力。它适用于以下场景：

* prototype AI 特性
* 构建 RAG 或代理工作流
* 评估模型工具

**接入方式**

接入 teamhanko/hanko 需要从小的 PoC (Proof of Concept) 开始，并检查 README 文档。该项目使用 Go 语言编写，支持 14 个主题。

**生产可用性**

teamhanko/hanko 在生产环境中具有高可用性，主要原因是：

* 近期活动
* 强大的采用
* 生态系统信号

但是，仍然需要对以下方面进行最终审查：

* 许可证
* 安全态势
* 主维护者

## 🧭 Practical evaluation

**Value:** teamhanko/hanko helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 8957 GitHub stars
- 1013 forks
- updated 2026-06-29
- primary language: Go
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 75/100 |
| stars | 84/100 |
| topics | 100/100 |
| outlook | 63/100 |
| quality | 77/100 |
| recency | 40/100 |
| adoption | 82/100 |
| production | 61/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/teamhanko/hanko) · [← Back to Misc](./README.md)</sub>
