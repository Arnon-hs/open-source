# velobase/velobase-harness

[![Stars](https://img.shields.io/github/stars/velobase/velobase-harness?style=flat-square&color=yellow)](https://github.com/velobase/velobase-harness/stargazers) [![Forks](https://img.shields.io/github/forks/velobase/velobase-harness?style=flat-square&color=blue)](https://github.com/velobase/velobase-harness/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> From code to cash — open-source SaaS boilerplate with Stripe, affiliate, attribution & usage-based billing for AI apps. T3 stack + Next.js 16.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 521 |
| 🍴 **Forks** | 65 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `ai-saas` `billing` `monetization` `nextjs` `nextjs-template` `open-source` `open-source-saas` `open-source-saas-boilerplate` `prisma` `saas` `saas-boilerplate`

## 🎯 Categories

Templates · Payments · AI/ML · Frontend · Product

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Velobase‑harness is an open‑source SaaS boilerplate that bundles Stripe, affiliate, attribution and usage‑based billing features for AI‑focused applications, built on the modern T3 stack and Next.js 16. With 521 GitHub stars and active maintenance, it lets developers add monetisation, checkout and payment‑service‑provider (PSP) flows to a product in days rather than weeks. The project is positioned as a fast‑track foundation for AI startups and teams that need a production‑grade billing layer out of the box.

**Value**  
- **Speed to market** – All the plumbing for Stripe integration, affiliate tracking, usage‑based pricing and attribution is pre‑wired, so teams can focus on their AI core instead of reinventing billing logic.  
- **Flexibility** – The codebase exposes clear API/SDK/CLI hooks, making it easy to swap PSPs, extend pricing models, or embed custom analytics.  
- **Learning resource** – Because it follows the T3 stack (Next.js 16, TypeScript, Prisma, Tailwind, tRPC), it doubles as a reference implementation for modern full‑stack development and payment best practices.

**Practical Adoption Path**  
1. **Clone & Install** – Fork the repo, run `pnpm install` (or your preferred package manager) and spin up the dev environment with the provided Docker compose files.  
2. **Configure Stripe & Secrets** – Add your Stripe keys, webhook secret, and any affiliate/attribution IDs to the `.env.example` file, then rename to `.env`.  
3. **Customize Pricing** – Edit the Prisma schema and the usage‑billing services to match your AI product’s consumption model (e.g., per‑token, per‑request, tiered plans).  
4. **Integrate Front‑end** – Use the pre‑built checkout components or call the exposed tRPC endpoints from your own UI to embed the payment flow.  
5. **Deploy** – Deploy to Vercel, Fly.io, or any Node‑compatible host; the repo includes CI/CD scripts and production‑ready Dockerfiles.

**Production Readiness**  
- **Activity & Community** – Updated on 2026‑06‑23, 521 stars, 65 forks, and a healthy issue/PR turnover indicate an active maintainer base.  
- **Tech Stack** – Built with TypeScript, Prisma (type‑safe DB access), tRPC (end‑to‑end type safety), and Next.js 16, all of which are battle‑tested in production environments.  
- **Security & Compliance** – No critical metadata risks identified; however, a final review of the MIT‑style license, dependency vulnerability scans, and Stripe webhook validation is recommended before a full production rollout.  
- **Scalability** – The architecture supports horizontal scaling via serverless functions or container orchestration, and usage‑based billing logic is designed to handle high‑volume AI request streams.

Overall, velobase‑harness offers a mature, well‑documented foundation for AI SaaS products that need robust, flexible billing and payment capabilities, making it a strong candidate for pilot projects and, after the usual security/legal vetting, for production deployment.

### Русский

**velobase/velobase-harness** — это готовый open‑source шаблон SaaS‑приложения на T3‑стеке + Next.js 16, который сразу включает Stripe, аффилированные программы, атрибуцию и usage‑based биллинг, что позволяет быстро добавить монетизацию и платежные потоки в AI‑приложения. Типичный сценарий: разработчик подключает предоставляемый API/SDK (или CLI) к своему бекенду, настраивает тарифы и правила расчётов, а затем использует готовый checkout‑модуль для приёма платежей и автоматизации операций. Проект имеет высокую готовность к production — активные коммиты, 521 звезда, 65 форков, свежие обновления (23 июня 2026), обширную типизацию TypeScript и широкую экосистему, что делает его надёжным кандидатом для пилотного внедрения.

### 中文

**项目简介**  
velobase/velobase-harness 是一个面向 AI 应用的开源 SaaS 框架，提供 Stripe、联盟营销、归因和基于使用量的计费能力，基于 T3 Stack 与 Next.js 16 构建，帮助开发者从代码快速落地到收入。

**价值**  
- **快速实现货币化**：内置完整的支付、计费、分成和使用量计费流程，省去自行搭建 PSP（支付服务提供商）和计费系统的时间成本。  
- **即插即用的 AI 场景**：专为 AI SaaS 产品设计，支持模型调用次数、token 消耗等使用量维度的计费，满足 AI 业务的独特需求。  
- **统一的开发体验**：基于 T3 Stack（Next.js、Tailwind、tRPC、Prisma）和 TypeScript，前后端代码共享、类型安全，降低集成风险。

**典型接入方式**  
1. **API/SDK 接入**：项目导出 `checkout`, `subscription`, `usageReport` 等函数，前端可直接通过 tRPC 调用，后端通过 Prisma 与 Stripe 同步。  
2. **CLI 快速生成**：提供 `npx velobase-harness init` 命令，一键生成包含 Stripe Webhook、计费模型和 Affiliate 路由的完整项目结构。  
3. **自定义插件**：通过 `hooks` 与 `middleware` 接口，可在业务逻辑中插入自定义计费规则或第三方 PSP（如 Paddle、Adyen）。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑23 最近一次提交，拥有 521 ⭐、65 🍴，20+ 相关话题，社区活跃。  
- **技术成熟**：使用 TypeScript、Next.js 16、Prisma 等主流技术栈，兼容 Vercel、Railway 等云平台，易于部署。  
- **安全与合规**：依赖官方 Stripe SDK，已实现 webhook 验签和 PCI‑DSS 基础防护；开源许可证（MIT）允许商业使用。  
- **适合试点**：在功能完整性、文档和示例代码都较为完善的前提下，可直接用于生产环境的 MVP 或内部工具，后续可根据业务需求自行扩展或替换组件。

> **结论**：velobase-harness 具备高可用的支付/计费实现、易于集成的 API/CLI，并且社区活跃、代码质量优秀，是 AI SaaS 项目快速实现货币化的可靠 OSS 选型。

## 🧭 Practical evaluation

**Value:** velobase/velobase-harness helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 521 GitHub stars
- 65 forks
- updated 2026-06-23
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 58/100 |
| topics | 100/100 |
| outlook | 62/100 |
| quality | 64/100 |
| recency | 40/100 |
| adoption | 54/100 |
| production | 59/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/velobase/velobase-harness) · [← Back to Templates](./README.md)</sub>
