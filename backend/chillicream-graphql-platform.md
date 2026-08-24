# ChilliCream/graphql-platform

[![Stars](https://img.shields.io/github/stars/ChilliCream/graphql-platform?style=flat-square&color=yellow)](https://github.com/ChilliCream/graphql-platform/stargazers) [![Forks](https://img.shields.io/github/forks/ChilliCream/graphql-platform?style=flat-square&color=blue)](https://github.com/ChilliCream/graphql-platform/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Welcome to the home of the Hot Chocolate GraphQL server for .NET, the Strawberry Shake GraphQL client for .NET and Nitro the awesome Monaco based GraphQL IDE.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 5.7k |
| 🍴 **Forks** | 808 |
| 💻 **Language** | C# |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`asp-net` `asp-net-core` `c-sharp` `dataloader` `dotnet` `dotnet-core` `facebook` `graphql` `graphql-client` `graphql-dotnet` `graphql-fusion` `graphql-gateway`

## 🎯 Categories

Backend

## 📝 Summary

### English

**Brief Summary**  
ChilliCream’s graphql‑platform bundles the Hot Chocolate GraphQL server, the Strawberry Shake client, and the Nitro Monaco‑based IDE into a single, C#‑centric ecosystem for building, consuming, and debugging GraphQL services. With over 5 700 stars, active maintenance, and a rich set of integration points (API, SDK, CLI, and extensive metadata), it lets teams reuse proven backend infrastructure instead of reinventing common GraphQL layers.  

**Value**  
- **Accelerated delivery** – The server, client, and IDE are purpose‑built to work together, so developers can spin up a production‑grade GraphQL API and a type‑safe .NET client in minutes.  
- **Infrastructure reuse** – By standardizing on Hot Chocolate’s schema‑first approach and Strawberry Shake’s code‑generation, teams avoid duplicating authentication, paging, filtering, and error‑handling logic across services.  
- **Consistency & governance** – A single platform enforces common patterns (e.g., middleware, diagnostics, tracing) across microservices, making it easier to audit, monitor, and evolve the API surface.  

**Practical Adoption Path**  
1. **Evaluate** – Clone the repo, run the provided Docker compose or the `dotnet run` sample to spin up a Hot Chocolate server and Nitro IDE locally.  
2. **Prototype** – Use Strawberry Shake’s CLI (`dotnet graphql generate`) against the running server to generate a strongly‑typed client in an existing .NET solution.  
3. **Integrate** – Replace any ad‑hoc GraphQL calls with the generated client, and adopt Nitro for interactive schema exploration and debugging.  
4. **Extend** – Leverage Hot Chocolate’s extensibility (middleware, data loaders, schema stitching) to plug in existing data sources or business services.  
5. **Deploy** – Containerize the server (official Docker images are available) and roll it out with CI/CD pipelines; the client library is a regular NuGet package, so deployment follows standard .NET practices.  

**Production Readiness**  
- **Activity & community**: Recent commits (as of 2026‑06‑29), >5 700 stars, 808 forks, and a vibrant issue/PR discussion indicate strong maintainer engagement.  
- **Maturity**: Hot Chocolate is used in large‑scale .NET deployments, Strawberry Shake is production‑tested for type‑safe clients, and Nitro provides a reliable in‑browser IDE.  
- **Ecosystem fit**: The platform ships with clear API/SDK/CLI surfaces, extensive documentation, and integrates seamlessly with ASP.NET Core, EF Core, and other .NET libraries.  
- **Risk considerations**: No major licensing or metadata red flags, but a final security audit (dependency scanning, supply‑chain review) and confirmation of active maintainers are advisable before a full‑scale rollout.  

Overall, the graphql‑platform is a high‑readiness, low‑friction option for .NET teams that want to standardize GraphQL development and accelerate API delivery.

### Русский

Резюме ChilliCream/graphql-platform:

ChilliCream/graphql-platform - открытый исходный проект, предоставляющий Hot Chocolate GraphQL-сервер для .NET, Strawberry Shake GraphQL-клиент для .NET и Nitro - мощный Monaco-базированный GraphQL-редактор. Этот проект позволяет командам повторно использовать инфраструктуру сервисов, вместо того чтобы восстанавливать общую backend-часть. Это особенно полезно для команд, которые хотят ускорить развертывание API-сервисов, использовать готовую инфраструктуру backend и стандартизировать шаблоны сервисов. Проект готов к использованию в production, поскольку имеет высокий уровень активности, адопции и экосистемных сигналов.

### 中文

**项目简介**  
ChilliCream/graphql-platform 是 .NET 生态下的完整 GraphQL 解决方案，包含 Hot Chocolate 服务器、Strawberry Shake 客户端以及基于 Monaco 的 Nitro IDE，帮助团队快速构建、消费和调试 GraphQL API。

**价值**  
- **复用后端基础设施**：统一的服务器、客户端和 IDE，使团队无需重复实现常见的 GraphQL 栈，降低维护成本。  
- **加速 API 上线**：开箱即用的组件和丰富的示例，帮助业务在几天内交付可靠的 GraphQL 服务。  
- **标准化服务模式**：通过统一的约定和工具链，提升跨团队协作的一致性和代码质量。

**典型接入方式**  
1. **服务器端**：在 .NET 项目中通过 NuGet 引入 `HotChocolate.AspNetCore`，按照官方文档配置 Schema、Resolver 和中间件，即可将现有业务逻辑暴露为 GraphQL API。  
2. **客户端**：使用 `StrawberryShake` 生成强类型的 C# 客户端代码，直接在业务代码中调用 GraphQL 查询/变更，享受编译时检查和自动重试等特性。  
3. **IDE**：在本地或 CI 环境中部署 Nitro（Docker 镜像或 npm 包），提供可视化的查询编辑、文档浏览和实时调试体验。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑29，项目拥有 5 723 星、808 Fork，最近一次提交在 2026‑06‑29，且持续接受 PR 与 Issue。  
- **生态成熟**：核心库使用 C# 编写，兼容 .NET 6/7/8，已在多个大型企业项目中上线。  
- **质量与安全**：提供完整的单元/集成测试、CI/CD 流水线以及 SPDX 许可证声明，安全审计报告可在仓库的 `SECURITY.md` 中查阅。  
- **适合试点**：凭借上述活跃度、社区采纳和完善的文档，完全可以在生产环境中进行正式评估并逐步推广。  

总体而言，ChilliCream/graphql-platform 是一个成熟、易集成且具备生产级别保障的 .NET GraphQL 平台，适合希望快速交付统一 API 并降低后端重复建设成本的团队使用。

## 🧭 Practical evaluation

**Value:** ChilliCream/graphql-platform helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 5723 GitHub stars
- 808 forks
- updated 2026-06-29
- primary language: C#
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 73/100 |
| stars | 80/100 |
| topics | 100/100 |
| outlook | 65/100 |
| quality | 75/100 |
| recency | 40/100 |
| adoption | 78/100 |
| production | 60/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/ChilliCream/graphql-platform) · [← Back to Backend](./README.md)</sub>
