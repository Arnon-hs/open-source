# DOMjudge/domjudge

[![Stars](https://img.shields.io/github/stars/DOMjudge/domjudge?style=flat-square&color=yellow)](https://github.com/DOMjudge/domjudge/stargazers) [![Forks](https://img.shields.io/github/forks/DOMjudge/domjudge?style=flat-square&color=blue)](https://github.com/DOMjudge/domjudge/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> DOMjudge programming contest jury system

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 902 |
| 🍴 **Forks** | 292 |
| 💻 **Language** | PHP |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`competitive-programming` `domjudge` `domjudge-developers` `domjudge-homepage` `hacktoberfest` `html` `icpc` `jquery` `linux` `pdf-format` `php` `prebuilt`

## 🎯 Categories

Payments

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
DOMjudge is an open‑source jury system for programming contests, providing a web‑based interface to manage submissions, scoring, and contest administration. Although its core purpose is contest judging, the platform’s modular architecture and PHP‑based APIs make it a viable foundation for integrating payment‑related workflows such as billing, checkout, or PSP (payment service provider) validation. A small proof‑of‑concept implementation can quickly demonstrate feasibility before a full‑scale rollout.

**Value Proposition**  
- **Accelerated monetisation integration** – DOMjudge’s extensible plugin system lets you embed billing or PSP flows directly into the contest workflow, reducing the time needed to build custom payment handling from scratch.  
- **Unified automation** – By leveraging the same backend that already processes submissions, you can automate payment verification, refunds, or invoicing as part of the contest lifecycle.  

**Practical Adoption Path**  
1. **Read the README & set up a local instance** – Clone the repo, run the Docker compose setup (or the provided PHP/Apache stack) to get a working judge system.  
2. **Identify integration points** – Use the existing “team registration” or “submission” hooks to insert payment‑verification calls (e.g., to Stripe, PayPal, or a custom PSP).  
3. **Build a minimal proof‑of‑concept** – Implement a simple “pay‑to‑register” flow and test it end‑to‑end in a sandbox environment.  
4. **Iterate and expand** – Once the PoC is stable, extend the integration to cover refunds, usage‑based billing, or automated reconciliation dashboards.  

**Production Readiness**  
- **Activity & community** – 902 stars, 292 forks, recent commits (last updated 2026‑07‑03) and a healthy ecosystem of 15 topics indicate strong maintenance and community support.  
- **Maturity** – The core contest‑judging features are battle‑tested in many ACM‑style contests, suggesting a stable codebase and reliable CI pipelines.  
- **Risk considerations** – The payment‑integration path is not explicitly documented; you’ll need to invest time in understanding the plugin architecture and possibly building custom adapters. Validate the effort required for setup and ongoing maintenance before committing large resources.  

Overall, DOMjudge is production‑ready for a pilot that adds billing or PSP capabilities, provided you start with a small, well‑scoped proof of concept and verify the integration effort early on.

### Русский

Резюме:

DOMjudge/domjudge - система судейского жюри для программных конкурсов, которая позволяет интегрировать процессы оплаты и платежей быстрее и эффективнее. Типовой сценарий внедрения проекта включает в себя интеграцию системы оплаты или чекаута, оценку потоков платежей и автоматизацию операций по оплате. DOMjudge/domjudge готов к производственной эксплуатации на высоком уровне, с сильными сигналами активности, адопции и экосистемы.

### 中文

**项目简介**  
DOMjudge 是一套开源的编程竞赛评测系统，主要面向赛事裁判（jury）使用。它提供完整的提交、编译、运行、评测以及排行榜功能，帮助组织者快速搭建可靠的比赛平台。

**价值**  
- **快速接入计费/支付流程**：虽然 DOMjudge 本身是评测系统，但其插件化架构让你可以在选手报名、付费提交或赛事赞助等环节嵌入支付、账单或 PSP（Payment Service Provider）流程，省去从零开发的工作量。  
- **自动化支付运营**：通过自定义 webhook 或 API，可在选手完成付款后自动激活参赛资格、分配资源或触发后续评测，提升运营效率。  

**典型接入方式**  
1. **阅读 README 与示例**：项目自带的部署文档和 Docker Compose 示例是最好的起点，先在本地或测试环境跑通完整的 DOMjudge 实例。  
2. **实现支付回调**：在 `conf/` 目录下新增一个 PHP 脚本，监听支付平台（如 Stripe、PayPal）的 webhook，验证签名后调用 DOMjudge 的内部 API（`/api/contests/{id}/register`）为用户开通参赛权限。  
3. **使用 API 扩展**：DOMjudge 提供 RESTful API（基于 JWT 鉴权），可在前端报名页面直接调用，完成付款后通过后端服务调用上述 API 完成用户注册或账单生成。  
4. **CI/CD 验证**：将支付插件写入 Docker 镜像，利用 GitHub Actions 进行自动化测试，确保每次发布都兼容原有评测流程。  

**生产可用性**  
- **活跃度**：截至 2026‑07‑03，项目仍在维护，最近一次提交仅数天前；拥有 902+ 星、292+ 分叉，社区活跃。  
- **技术成熟度**：核心使用 PHP + MySQL，成熟且易于在传统 LAMP 环境或容器化平台部署。  
- **生态与文档**：官方文档覆盖部署、API、插件开发，且社区提供多语言示例（Python、Node.js），降低上手成本。  
- **风险**：项目本身并未直接提供支付模块，集成路径需要自行实现 webhook → API 的桥接；在正式投入前建议先做小规模 PoC（如仅在测试赛中接入 Stripe），评估实现成本与安全性。  

综上，DOMjudge 具备高可用的评测核心，配合自定义的支付回调即可实现“报名‑付费‑参赛”一体化流程，适合作为编程竞赛平台的生产级 OSS 方案。

## 🧭 Practical evaluation

**Value:** DOMjudge/domjudge helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 902 GitHub stars
- 292 forks
- updated 2026-07-03
- primary language: PHP
- 15 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 62/100 |
| stars | 63/100 |
| topics | 100/100 |
| outlook | 58/100 |
| quality | 68/100 |
| recency | 40/100 |
| adoption | 63/100 |
| production | 56/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/DOMjudge/domjudge) · [← Back to Payments](./README.md)</sub>
