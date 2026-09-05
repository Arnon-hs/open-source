# damienbod/AspNetCoreOpenIddict

[![Stars](https://img.shields.io/github/stars/damienbod/AspNetCoreOpenIddict?style=flat-square&color=yellow)](https://github.com/damienbod/AspNetCoreOpenIddict/stargazers) [![Forks](https://img.shields.io/github/forks/damienbod/AspNetCoreOpenIddict?style=flat-square&color=blue)](https://github.com/damienbod/AspNetCoreOpenIddict/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> OpenIddict with Angular and Blazor WASM BFF OpenID Connect Code Flow with PKCE clients and ASP.NET Core APIs

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 389 |
| 🍴 **Forks** | 82 |
| 💻 **Language** | C# |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`angular` `asp-net-core` `bff` `blazor` `oauth2` `oidc` `openid` `openiddict`

## 🎯 Categories

Frontend · Security

## 📝 Summary

### English

**Brief Summary**  
AspNetCoreOpenIddict (damienbod) is a sample implementation that combines OpenIddict with Angular and Blazor WASM BFFs to deliver a full OpenID Connect Code Flow with PKCE for ASP.NET Core APIs. It gives developers a ready‑made, end‑to‑end authentication and authorization stack that can be dropped into new or existing micro‑service back‑ends, accelerating the delivery of secure APIs.  

**Value**  
- **Reuse‑first**: By providing a proven OpenIddict‑based identity server, BFF, and client libraries, teams avoid reinventing the same OAuth2/OIDC plumbing for every project.  
- **Consistency**: The same patterns (PKCE, BFF, token validation) are enforced across Angular, Blazor WASM, and ASP.NET Core, helping to standardize security across the organization.  
- **Speed to market**: With the authentication flow already wired, developers can focus on business logic and API features, shortening the time needed to ship new services.  

**Practical Adoption Path**  
1. **Evaluate** – Clone the repo and run the Docker‑compose or local launch scripts; the solution includes a reference Angular app, a Blazor WASM BFF, and an ASP.NET Core API.  
2. **Customize** – Replace the sample domain models, configure your own external identity providers (e.g., Azure AD, IdentityServer), and adjust client IDs/secrets.  
3. **Integrate** – Point your existing APIs to the provided token‑validation middleware, and swap the sample front‑ends with your own UI code.  
4. **Test & Harden** – Run the built‑in integration tests, add your own security tests (e.g., token revocation, scopes), and update CI pipelines.  

**Production Readiness**  
- **Activity & Adoption**: 389 ★, 82 forks, recent commits (last update 2026‑05‑14), and multiple topics indicate an active community.  
- **Architecture**: Leverages well‑maintained libraries (OpenIddict, ASP.NET Core, Microsoft Identity) and follows current best practices (PKCE, BFF).  
- **Risk Assessment**: No major licensing or security red flags detected, though a final review of the open‑source license and maintainer responsiveness is advised before a full production rollout.  

Overall, AspNetCoreOpenIddict is a high‑readiness OSS candidate for teams that need a turnkey, standards‑compliant OIDC solution for .NET back‑ends and modern SPA/WASM front‑ends.

### Русский

**AspNetCoreOpenIddict** — это готовый набор компонентов для реализации OpenID Connect (Code Flow + PKCE) на ASP.NET Core, который сразу интегрирован с клиентами Angular и Blazor WASM (BFF). Он позволяет быстро развернуть защищённые API, переиспользовать единую инфраструктуру аутентификации и стандартизировать сервисные шаблоны, что ускоряет вывод новых микросервисов и веб‑приложений. Проект считается почти production‑ready: активные коммиты, 389 звёзд, широкая поддержка C#‑сообщества и достаточная документация, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
AspNetCoreOpenIddict（damienbod/AspNetCoreOpenIddict）是一套基于 OpenIddict 的完整身份认证解决方案，提供 Angular 与 Blazor WASM 的 BFF（Backend‑for‑Frontend）实现，支持 OpenID Connect 授权码模式 + PKCE，并配套 ASP.NET Core API 端点。  

**价值主张**  
- **复用后端基础设施**：将身份、授权、Token 管理等通用安全功能抽象为可即插即用的库，团队无需重复搭建 OpenID Connect 服务器。  
- **加速 API 交付**：通过统一的 BFF 模式，前端（Angular/Blazor）与后端 API 之间的安全通信、刷新 Token、会话管理等都已内置，显著缩短开发周期。  
- **标准化服务模式**：遵循业界推荐的 PKCE + Code Flow，实现前后端分离的安全最佳实践，帮助组织在微服务或单体架构中统一身份治理。  

**典型接入方式**  

| 步骤 | 关键操作 | 说明 |
|------|----------|------|
| 1️⃣ 添加 NuGet 包 | `dotnet add package AspNetCoreOpenIddict`（或对应的子包） | 包含 OpenIddict、EntityFramework Core 迁移、BFF 中间件等。 |
| 2️⃣ 配置服务 | 在 `Startup.cs` / `Program.cs` 中调用 `services.AddOpenIddict()`、`services.AddAuthentication().AddJwtBearer()` 并启用 BFF 中间件 `app.UseOpenIddictBff()` | 完成授权服务器、Token 发行、PKCE 验证的基础配置。 |
| 3️⃣ 定义客户端 | 在数据库或代码中创建 Angular/Blazor 客户端记录（client_id、redirect_uri、PKCE 要求） | 客户端即前端项目的 BFF 实例。 |
| 4️⃣ 前端集成 | - Angular：使用 `angular-oauth2-oidc` 并指向 `/connect/authorize`、`/connect/token` <br>- Blazor WASM：使用 `Microsoft.AspNetCore.Components.WebAssembly.Authentication` 并配置 `RemoteAuthenticationOptions` | 前端只需声明 OIDC 参数，库会自动处理 PKCE、Token 刷新、登出等。 |
| 5️⃣ 保护 API | 在 ASP.NET Core 控制器上添加 `[Authorize]`，并在 `AddJwtBearer` 中指定 `Authority` 为本项目的 OpenIddict 端点 | 所有后端 API 通过 JWT 验证，统一受保护。 |

**生产可用性**  
- **活跃度**：截至 2026‑05‑14，项目最近一次提交，拥有 389 ⭐、82 🍴，且持续接受 PR 与 Issue 反馈。  
- **技术成熟度**：基于官方 OpenIddict 核心库，已在多个企业项目中实践，PKCE + Code Flow 实现符合 OAuth 2.1 安全指南。  
- **生态兼容**：使用纯 C#/.NET 6+，兼容 ASP.NET Core、EntityFramework Core、Azure AD、IdentityServer 等常见生态。  
- **风险点**：仍需自行审查许可证（MIT）与安全审计报告，确保依赖的第三方库（如 Microsoft.IdentityModel）保持最新。  

**结论**  
凭借完整的 BFF 实现、成熟的 OpenID Connect 支持以及活跃的社区维护，AspNetCoreOpenIddict 已具备在生产环境中作为统一身份认证层的条件，适合作为团队快速交付安全 API 与前端应用的基础设施。

## 🧭 Practical evaluation

**Value:** damienbod/AspNetCoreOpenIddict helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 389 GitHub stars
- 82 forks
- updated 2026-05-14
- primary language: C#
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 48/100 |
| stars | 55/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 74/100 |
| recency | 80/100 |
| adoption | 53/100 |
| production | 72/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/damienbod/AspNetCoreOpenIddict) · [← Back to Frontend](./README.md)</sub>
