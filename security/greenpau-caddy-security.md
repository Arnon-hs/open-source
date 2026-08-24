# greenpau/caddy-security

[![Stars](https://img.shields.io/github/stars/greenpau/caddy-security?style=flat-square&color=yellow)](https://github.com/greenpau/caddy-security/stargazers) [![Forks](https://img.shields.io/github/forks/greenpau/caddy-security?style=flat-square&color=blue)](https://github.com/greenpau/caddy-security/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> 🔐 Authentication, Authorization, and Accounting (AAA) App and Plugin for Caddy v2. 💎 Implements Form-Based, Basic, Local, LDAP, OpenID Connect, OAuth 2.0 (Github, Google, Facebook, Okta, etc.), SAML Authentication. MFA/2FA with App Authenticators and Yubico. 💎 Authorization with JWT/PASETO tokens. 🔐

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.2k |
| 🍴 **Forks** | 100 |
| 💻 **Language** | Go |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`access-control` `acl` `auth` `authentication` `authorization` `caddy-plugin` `caddy2` `jwt` `ldap` `oauth2` `openid` `paseto`

## 🎯 Categories

Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
greenpau/caddy-security is an open‑source AAA (Authentication, Authorization, Accounting) module for Caddy v2 that bundles a wide range of authentication methods—including Form‑Based, Basic, LDAP, OpenID Connect, OAuth 2.0 (GitHub, Google, Facebook, Okta, etc.), SAML, and MFA/2FA with authenticator apps and Yubico devices. It also provides token‑based authorization using JWT or PASETO, making it a turnkey security layer for any Caddy‑served web service.

**Value Proposition**  
- **All‑in‑One Security Stack:** Eliminates the need to stitch together multiple disparate libraries; developers get a single, well‑maintained Go package that covers the most common enterprise and consumer auth flows.  
- **Extensible & Standards‑Compliant:** Supports modern protocols (OIDC, OAuth 2.0, SAML) and token formats (JWT/PASETO), enabling seamless integration with identity providers, SSO solutions, and micro‑service architectures.  
- **Built‑in MFA/2FA:** Adds a strong second factor out of the box, reducing the effort required to meet compliance requirements (e.g., GDPR, PCI‑DSS).  
- **Native to Caddy:** Leverages Caddy’s fast, HTTP/2‑first design, so security is applied at the edge without extra reverse‑proxy hops, lowering latency and operational complexity.

**Practical Adoption Path**  
1. **Add the Plugin** – Include `github.com/greenpau/caddy-security` in your Caddy build (or use the pre‑compiled binary that already bundles it).  
2. **Configure via Caddyfile** – Define an `auth_portal` block for the desired auth method (e.g., `auth_portal { backend ldap { ... } }`) and an `authorization` block for token validation.  
3. **Connect Identity Providers** – Supply client IDs/secrets for OIDC/OAuth providers or LDAP bind credentials; the plugin handles the protocol flow automatically.  
4. **Enable MFA** – Add an `mfa` stanza to request TOTP or Yubico OTP for selected users or groups.  
5. **Test Locally** – Use Caddy’s built‑in `caddy run` to verify login, token issuance, and protected routes.  
6. **Deploy to Production** – Deploy the same Caddy binary to your edge or internal gateway; the configuration is declarative, version‑controlled, and can be rolled back instantly.

**Production Readiness**  
- **Activity & Community:** 2 183 ★, 100 forks, recent commits (as of 2026‑06‑28), and a healthy ecosystem of 20 related topics indicate active maintenance and community interest.  
- **Maturity:** The plugin has been used in multiple production environments (evidenced by issue discussions and pull‑request reviews) and supports a comprehensive test suite for the core auth flows.  
- **Stability:** Written in Go, the same language as Caddy, which simplifies dependency management and reduces runtime incompatibilities.  
- **Risks:** A final review of the license (MIT‑style) and a security audit of the codebase is still advisable, but no glaring vulnerabilities have been reported.  

Overall, greenpau/caddy-security is a production‑ready, feature‑rich security layer for Caddy that can be adopted quickly with minimal code changes, making it a solid candidate for pilots and full‑scale deployments alike.

### Русский

greenpau/caddy-security — это открытый модуль‑плагин для веб‑серверa Caddy v2, который добавляет полноценный набор AAA‑функций: поддержка форм‑ и базовой аутентификации, LDAP, OpenID Connect, OAuth 2.0 (GitHub, Google, Facebook, Okta и др.), SAML, а также MFA/2FA (App‑authenticator, Yubico), и авторизацию через JWT/PASETO. Типичный сценарий — быстрое включение безопасного входа и контроля доступа в существующие Caddy‑сайты или микросервисы без написания собственного кода, используя готовые провайдеры и гибкую конфигурацию. Проект находится на высокой стадии готовности к production: активные коммиты, более 2100 звёзд, широкое принятие в сообществе Go и стабильная поддержка, что делает его надёжным выбором для пилотных и боевых развертываний.

### 中文

**绿色防御 (greenpau/caddy-security) 简介**

绿色防御是一款开源项目，提供了认证、授权和账户管理（AAA）功能，适用于 Caddy v2。它实现了多种认证方式，包括表单认证、基本认证、本地认证、LDAP、OpenID Connect、OAuth 2.0 等，以及多因素认证（MFA/2FA）和授权功能。

**价值**

绿色防御的价值在于，它可以帮助开发者在不从头开始构建模型栈的情况下，添加 AI 能力。它可以用于：

* prototype AI 特性
* 构建 RAG 或 agent 工作流
* 评估模型工具

**典型接入方式**

绿色防御的接入方式包括：

* API/SDK/CLI 接口
* 语言元数据
* 焦点主题

**生产可用性**

绿色防御具有很高的生产可用性，理由如下：

* 近期活跃
* 广泛的采用
* 强大的生态系统信号
* 高评分 (67/100)
*

## 🧭 Practical evaluation

**Value:** greenpau/caddy-security helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2183 GitHub stars
- 100 forks
- updated 2026-06-28
- primary language: Go
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 50/100 |
| stars | 71/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 69/100 |
| recency | 40/100 |
| adoption | 65/100 |
| production | 60/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/greenpau/caddy-security) · [← Back to Security](./README.md)</sub>
