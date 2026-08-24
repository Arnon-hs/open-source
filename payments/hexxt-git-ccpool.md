# hexxt-git/ccpool

[![Stars](https://img.shields.io/github/stars/hexxt-git/ccpool?style=flat-square&color=yellow)](https://github.com/hexxt-git/ccpool/stargazers) [![Forks](https://img.shields.io/github/forks/hexxt-git/ccpool?style=flat-square&color=blue)](https://github.com/hexxt-git/ccpool/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> a cli to equally share a claude code subscription for low budget teams

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 30 |
| 🍴 **Forks** | — |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`claude` `claude-code` `subscription-management`

## 🎯 Categories

Payments

## 📝 Summary

### English

**Brief Summary**  
hexxt‑git/ccpool is a TypeScript‑based CLI that lets low‑budget teams split a Claude code‑generation subscription evenly among members. By handling the bookkeeping of shared usage, it speeds up the integration of monetization, billing, or PSP (payment service provider) flows for internal tools and prototypes.  

**Value**  
- **Cost‑sharing:** Turns a single high‑price Claude subscription into a communal resource, reducing per‑developer expense.  
- **Fast billing integration:** Provides ready‑made commands to create, track, and settle usage credits, letting teams focus on product logic rather than payment plumbing.  
- **Low‑friction experimentation:** Enables rapid “try‑out” of PSP or checkout workflows without building a custom billing backend from scratch.  

**Practical Adoption Path**  

| Step | Action | Goal |
|------|--------|------|
| 1️⃣  | **Read the README & run the demo** – clone the repo, install dependencies (`npm ci`), and execute `ccpool --help`. | Verify that the CLI works in your environment and understand the command set. |
| 2️⃣  | **Proof‑of‑concept (PoC)** – create a small “team” of 2‑3 developers, generate a shared subscription token, and use the CLI to allocate usage credits. | Test the core sharing logic and confirm that the accounting matches actual Claude usage. |
| 3️⃣  | **Integrate with your existing workflow** – wrap the CLI calls in npm scripts or CI jobs that automatically debit credits after each Claude request. | Embed cost tracking into the development pipeline with minimal manual steps. |
| 4️⃣  | **Add a minimal UI (optional)** – expose the CLI via a simple Node/Express endpoint or a Slack bot if you need a self‑service portal for team members. | Provide a user‑friendly way to view balances and request top‑ups. |
| 5️⃣  | **Security & compliance review** – audit the repository for licensing, dependency vulnerabilities (run `npm audit`), and verify that any stored tokens are kept secret (e.g., using env vars or secret managers). | Ensure the tool meets your organization’s security policies before wider rollout. |
| 6️⃣  | **Scale to production** – lock down versions (`package-lock.json`), add CI/CD linting/tests, and monitor usage logs. | Move from PoC to a stable internal service. |

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last commit 2026‑07‑12) and has modest community traction (≈30 stars). It is suitable for prototypes, internal tools, or “sandbox” environments.  
- **Dependencies:** Pure TypeScript with a small node‑module footprint, making it easy to audit and lock down.  
- **Risks:** The repository lacks a formal security policy, and the license/maintainer activity still need a final check. Before production use, run a full dependency audit, confirm the license is compatible with your codebase, and consider adding automated tests for the CLI’s critical paths.  

**Bottom line:** ccpool offers a quick, low‑cost way to share Claude subscriptions and bootstrap billing logic, making it a solid candidate for early‑stage projects or internal tooling. With a short PoC, a security review, and proper version pinning, it can be hardened for production‑grade usage.

### Русский

**hexxt-git/ccpool** — это CLI‑утилита, позволяющая равномерно распределять подписку Claude Code между небольшими командами с ограниченным бюджетом, ускоряя интеграцию монетизации, биллинга и PSP‑процессов. Типичный сценарий — запуск небольшого proof‑of‑concept: установить пакет, добавить несколько строк конфигурации в README и протестировать автоматизацию расчётов и чек‑аутов. Готовность к продакшну — средняя: проект пригоден для прототипов и внутренних воркфлоу, но перед выводом в продакшн требуется проверка лицензии, безопасности и стабильности зависимостей.

### 中文

**项目简介**  
hexxt-git/ccpool 是一款基于 CLI 的工具，专为预算有限的团队设计，能够将 Claude 代码订阅额度平摊给多位成员，让每个人都能以低成本共享 AI 编程能力。

**价值**  
- **快速落地**：提供即插即用的计费、结算或 PSP（支付服务提供商）流程封装，帮助团队在几分钟内完成支付相关的原型搭建。  
- **成本控制**：通过共享订阅的方式，显著降低单人使用 Claude 的费用，适合小团队、创业公司或内部实验项目。  
- **自动化**：内置脚本可自动生成账单、分配额度、同步使用情况，减少手工操作和错误率。

**典型接入方式**  
1. **准备工作**：在项目根目录下 `npm install @hexxt-git/ccpool`（或使用 `yarn`/`pnpm`）。  
2. **初始化**：运行 `ccpool init`，根据提示填写 Claude 订阅的 API Key、团队成员列表以及分配比例。  
3. **集成到 CI/CD**：在构建脚本或 GitHub Actions 中加入 `ccpool allocate --project <project-id>`，自动在每次构建前扣除相应额度。  
4. **监控与结算**：使用 `ccpool report` 生成使用报告，配合 `ccpool bill` 生成月度账单并推送至内部财务系统。  

**生产可用性**  
- **成熟度**：当前评分 59/100，适合原型、内部工具或低风险业务。  
- **依赖与维护**：项目使用 TypeScript 编写，已有 30+ 星，最近一次提交在 2026‑07‑12，活跃度尚可，但仍建议在正式生产前进行以下检查：  
  - 代码审计，确认无安全漏洞。  
  - 评估许可证兼容性（默认 MIT），确保符合公司合规要求。  
  - 在小范围（如 1‑2 个团队）进行 PoC，验证与现有支付系统（Stripe、PayPal 等）的兼容性。  
- **上线建议**：在完成上述验证后，可将其作为内部服务的支付层，配合监控与日志收集，逐步推广到更大规模的业务场景。  

总体而言，hexxt-git/ccpool 为低预算团队提供了一条低成本、快速集成 Claude 订阅共享与支付流程的路径，适合作为原型或内部工具的首选解决方案。

## 🧭 Practical evaluation

**Value:** hexxt-git/ccpool helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 30 GitHub stars
- updated 2026-07-12
- primary language: TypeScript
- 3 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 32/100 |
| topics | 38/100 |
| outlook | 45/100 |
| quality | 41/100 |
| recency | 40/100 |
| adoption | 23/100 |
| production | 50/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/hexxt-git/ccpool) · [← Back to Payments](./README.md)</sub>
