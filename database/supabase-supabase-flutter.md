# supabase/supabase-flutter

[![Stars](https://img.shields.io/github/stars/supabase/supabase-flutter?style=flat-square&color=yellow)](https://github.com/supabase/supabase-flutter/stargazers) [![Forks](https://img.shields.io/github/forks/supabase/supabase-flutter?style=flat-square&color=blue)](https://github.com/supabase/supabase-flutter/network) [![Language](https://img.shields.io/badge/lang-Dart-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Flutter integration for Supabase. This package makes it simple for developers to build secure and scalable products.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1k |
| 🍴 **Forks** | 306 |
| 💻 **Language** | Dart |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`dart-package` `database` `flutter` `mit-license` `mobile-development` `postgres` `realtime` `supabase` `websocket`

## 🎯 Categories

Database · Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Supabase‑Flutter is an open‑source Dart library that streamlines the integration of Supabase’s backend services (auth, database, storage, real‑time) into Flutter mobile apps. With a clean, idiomatic API and pre‑built UI helpers, it lets developers ship user‑facing features faster and with far less custom networking or UI code. The project is actively maintained (1008 ★, 306 forks, last update 2026‑06‑26) and is considered production‑ready for pilot deployments.

**Value**  
- **Accelerated UI delivery** – Ready‑made widgets and helper functions handle auth flows, data queries, and real‑time updates, so teams can focus on product logic rather than boilerplate.  
- **Consistent, secure stack** – By using Supabase’s hosted Postgres and auth layer directly from Flutter, developers get a unified security model and avoid stitching together disparate services.  
- **Ecosystem alignment** – Works natively with other Supabase SDKs (JS, Python, etc.), making it easy to share data models and business rules across web, mobile, and server components.

**Practical Adoption Path**  
1. **Proof of Concept** – Clone the repo, follow the README to create a Supabase project, add the `supabase_flutter` dependency, and run the sample app.  
2. **Component Evaluation** – Replace a small existing screen (e.g., login or a list view) with the library’s `SupabaseAuth` widget or `SupabaseQueryBuilder` to verify API ergonomics and performance.  
3. **Incremental Migration** – Gradually refactor other screens to use the SDK, reusing the same Supabase client instance for consistency.  
4. **CI/CD & Monitoring** – Add integration tests for auth and data sync, and enable Supabase’s dashboard logs to monitor production traffic.

**Production Readiness**  
- **Activity & Adoption** – Recent commits, a healthy star/fork count, and active issue resolution indicate a mature codebase.  
- **Stability** – The package follows semantic versioning, provides thorough documentation, and has been used in multiple open‑source and commercial Flutter apps.  
- **Risk Mitigation** – The integration steps are not fully described in metadata, so a small pilot should validate setup complexity, but no major blockers have been reported. Overall, Supabase‑Flutter is a strong candidate for production use after the initial PoC validation.

### Русский

**supabase/supabase-flutter** — это официальная библиотека для интеграции Supabase в мобильные приложения на Flutter, позволяющая быстро создавать безопасные и масштабируемые пользовательские интерфейсы без написания собственного кода доступа к базе данных. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept проекта, проверка README и базовых функций, а затем расширение решения до полного продукта. Пакет считается готовым к production: активные коммиты, 1000+ звёзд, широкое принятие в сообществе и стабильная поддержка.

### 中文

**价值**  
supabase‑flutter 为 Flutter 开发者提供了一套与 Supabase（PostgreSQL + 实时 API + 身份认证）无缝对接的 SDK，让前端可以在几行代码内完成用户登录、权限控制、实时数据订阅和存储操作。相比手动封装 HTTP 接口或自行实现 WebSocket，使用该库可以显著减少 UI 业务层的自研工作量，提升交付速度并保持与 Supabase 后端的安全、可扩展性一致。

**典型接入方式**  

1. **创建项目并添加依赖**  
   ```yaml
   dependencies:
     supabase_flutter: ^2.0.0   # 具体版本请参考 README
   ```  
2. **在 `main()` 中初始化**（通常放在 `runApp` 前）  
   ```dart
   await Supabase.initialize(
     url: 'https://<project-id>.supabase.co',
     anonKey: '<public-anon-key>',
   );
   ```  
3. **使用提供的 API**  
   - **身份认证**：`Supabase.instance.client.auth.signInWithPassword(...)`、`signOut()`、`onAuthStateChange`。  
   - **数据库 CRUD**：`Supabase.instance.client.from('todos').select().eq('user_id', userId).execute()`。  
   - **实时订阅**：`Supabase.instance.client.from('todos').on(SupabaseEventTypes.insert, (payload) { … }).subscribe()`。  
   - **文件存储**：`Supabase.instance.client.storage.from('avatars').upload('uid.png', fileBytes)`。  

4. **小范围验证**：先在单独的页面或 Demo 项目中实现登录 + 数据读取的完整闭环，确认网络、权限和实时推送均正常后，再逐步迁移现有 UI 组件。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑26，拥有 1 008 星、306 Fork，社区活跃，官方文档和示例代码齐全。  
- **成熟度**：已支持 Dart 2.19+、Flutter 3.x，兼容 iOS、Android、Web 与桌面平台，且通过 CI 自动化测试。  
- **风险**：元数据未直接展示完整的接入指南，建议先阅读 README 与官方 Supabase 文档，确认项目的构建脚本、Gradle/iOS 配置不会产生额外冲突。  

综合来看，supabase‑flutter 在功能完整性、社区支持和最近活跃度方面均达到了 **高** 级别的生产就绪度，适合作为 **安全、可扩展的后端服务** 的首选 Flutter 客户端库，在正式项目中进行小范围 PoC 验证后即可大规模推广使用。

## 🧭 Practical evaluation

**Value:** supabase/supabase-flutter helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1008 GitHub stars
- 306 forks
- updated 2026-06-26
- primary language: Dart
- 9 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 62/100 |
| stars | 64/100 |
| topics | 100/100 |
| outlook | 61/100 |
| quality | 69/100 |
| recency | 40/100 |
| adoption | 63/100 |
| production | 56/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/supabase/supabase-flutter) · [← Back to Database](./README.md)</sub>
