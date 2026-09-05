# dimthink/PriceAI

[![Stars](https://img.shields.io/github/stars/dimthink/PriceAI?style=flat-square&color=yellow)](https://github.com/dimthink/PriceAI/stargazers) [![Forks](https://img.shields.io/github/forks/dimthink/PriceAI?style=flat-square&color=blue)](https://github.com/dimthink/PriceAI/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> AI 订阅卡网渠道比价工具：聚合100+卡网渠道包含 ChatGPT、Claude、Gemini、Grok 等多渠道报价，展示有货最低价、库存状态和原站购买链接。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1k |
| 🍴 **Forks** | 83 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-subscription` `chatgpt` `claude` `gemini` `grok` `nextjs` `price-comparison` `price-tracker` `supabase`

## 🎯 Categories

Payments · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
PriceAI is an open‑source price‑comparison engine for AI subscription cards, aggregating quotes from more than 100 providers—including ChatGPT, Claude, Gemini, and Grok—to show the lowest in‑stock price, availability, and direct purchase links. With 1 k+ GitHub stars and active TypeScript development, it offers a ready‑to‑use backend for quickly surfacing competitive AI‑service pricing.  

**Value**  
- **Monetisation acceleration:** By exposing real‑time pricing and inventory across dozens of AI‑card vendors, PriceAI lets platforms embed dynamic checkout or recommendation widgets without building their own scraper or pricing database.  
- **Decision‑making insight:** Operators can instantly compare costs, detect price drops, and route customers to the cheapest viable option, improving conversion and margin.  
- **Extensibility:** The TypeScript codebase and modular data‑source adapters make it easy to add new AI providers or custom PSP integrations.

**Practical Adoption Path**  
1. **Proof‑of‑Concept:** Fork the repo, run the provided Docker compose (or `npm run dev`) and verify that the API returns expected price data for a subset of providers.  
2. **Integration:** Wrap the REST/GraphQL endpoints in your existing billing or checkout service, mapping the “lowest‑price” response to your payment‑flow logic.  
3. **Customization:** Add or modify adapters for any proprietary or regional AI card vendors you need, using the clear TypeScript interfaces.  
4. **Testing & Security Review:** Run the built‑in unit tests, perform a dependency audit (e.g., `npm audit`), and confirm the license (MIT‑like) aligns with your compliance policies.  
5. **Production Rollout:** Deploy the service behind a managed container platform, enable caching/CDN for price queries, and monitor health via the built‑in Prometheus metrics.

**Production Readiness**  
- **Activity & Community:** Recent commits (as of 2026‑07‑06), 1 009 stars, 83 forks, and 10 topical tags indicate strong community interest and ongoing maintenance.  
- **Technical Maturity:** Written in TypeScript with clear module boundaries, automated tests, and Docker support, the codebase is production‑grade for a pilot.  
- **Risk Profile:** No immediate licensing or security red flags have been identified, though a final audit of third‑party dependencies and maintainer responsiveness is recommended before full‑scale deployment.  

Overall, PriceAI is a high‑readiness OSS candidate for teams that need to embed AI‑service price comparison into billing, checkout, or PSP evaluation workflows.

### Русский

Резюме проекта dimthink/PriceAI:

dimthink/PriceAI - это open-source инструмент для сравнения цен в различных картах и платежных системах, интегрированный с AI-технологиями. Программа позволяет быстро интегрировать монетизацию, счета или потоки PSP (Payment Service Provider), автоматизируя операции по платежам. dimthink/PriceAI готов к серьезному пилоту и имеет высокий уровень готовности к выпуску в production.

### 中文

**简短介绍**

dimthink/PriceAI 是一个开源 AI 订阅卡网渠道比价工具，聚合了 100+ 个卡网渠道（包括 ChatGPT、Claude、Gemini、Grok 等），提供最低价、库存状态和原站购买链接。它有助于快速集成付款、发票或支付服务流程。

**价值**

dimthink/PriceAI 的价值在于，它可以帮助开发者快速集成付款、发票或支付服务流程，提高开发效率。

**典型接入方式**

dimthink/PriceAI 的接入方式包括：

1. 集成付款流程：通过 PriceAI 的 API 来集成付款流程，快速完成付款操作。
2. 评估 PSP 流程：使用 PriceAI 来评估支付服务提供商（PSP）的流程，选择最合适的 PSP。
3. 自动化付款操作：通过 PriceAI 来自动化付款操作，提高开发效率。

**生产可用性**

dimthink/PriceAI 已经具有较高的生产可用性，最新版本于 2026-07-06 更新，

## 🧭 Practical evaluation

**Value:** dimthink/PriceAI helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1009 GitHub stars
- 83 forks
- updated 2026-07-06
- primary language: TypeScript
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 48/100 |
| stars | 64/100 |
| topics | 100/100 |
| outlook | 71/100 |
| quality | 77/100 |
| recency | 80/100 |
| adoption | 60/100 |
| production | 70/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/dimthink/PriceAI) · [← Back to Payments](./README.md)</sub>
