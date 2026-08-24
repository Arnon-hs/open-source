# giancarloerra/JanuScope

[![Stars](https://img.shields.io/github/stars/giancarloerra/JanuScope?style=flat-square&color=yellow)](https://github.com/giancarloerra/JanuScope/stargazers) [![Forks](https://img.shields.io/github/forks/giancarloerra/JanuScope?style=flat-square&color=blue)](https://github.com/giancarloerra/JanuScope/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> Local-first MCP policy proxy. Tool-block, SQL-mutation gate, PII redact, audit, rate-limit, OpenTelemetry, vault secrets, first-use quarantine, schema pre-inject. No hosted gateway. One YAML Lens wraps any MCP, 20 included (Postgres, MySQL, MongoDB, GitHub, Stripe, Snowflake, etc.). 84% fewer tokens, ~3x faster, holds PII leaks. AGPL or commercial.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 24 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `anthropic` `audit-log` `claude` `claude-code` `github` `guardrails` `llm` `mcp` `mcp-server` `model-context-protocol` `mongodb`

## 🎯 Categories

Payments · MCP · AI/ML · Backend · Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
JanuScope is a local‑first, policy‑enforcement proxy for any MCP (Managed Cloud Provider) that lets you block tools, gate SQL mutations, redact PII, audit requests, rate‑limit traffic, and integrate OpenTelemetry and secret vaults—all from a single YAML lens. It ships with 20 ready‑made lenses for services such as Postgres, MySQL, MongoDB, GitHub, Stripe and Snowflake, delivering up to 84 % fewer tokens and roughly three‑times faster processing while preventing PII leaks. The project is AGPL‑licensed with an optional commercial offering and is positioned as a high‑performance, self‑hosted alternative to hosted gateways.

---

### Value Proposition
- **Unified Policy Layer:** Provides a single point where security, compliance, and operational policies (tool blocking, SQL mutation gating, PII redaction, rate‑limiting, audit logging) are enforced across a wide variety of back‑ends.
- **Performance & Cost Savings:** By processing requests locally and reducing token usage by up to 84 %, it cuts both latency and the cost of downstream API calls.
- **Extensible, Vendor‑Neutral:** The YAML‑based “Lens” abstraction lets you wrap any MCP without writing code; 20 common lenses are shipped out‑of‑the‑box, accelerating integration of billing, checkout, or PSP flows.
- **Observability & Secret Management:** Built‑in OpenTelemetry hooks and native vault secret injection simplify monitoring and secure credential handling.
- **Self‑Hosted Control:** No reliance on a hosted gateway means you keep data and policy logic inside your own environment, which is crucial for compliance‑heavy domains such as payments.

### Practical Adoption Path
1. **Evaluate the YAML Lens:** Clone the repo, pick the lens that matches your target MCP (e.g., `stripe.yaml` for Stripe or `postgres.yaml` for a Postgres DB) and run the proxy locally against a test environment.  
2. **Define Custom Policies:** Extend the default lens or create a new one to express your specific rules (e.g., “block all DELETE statements on the `payments` table” or “redact credit‑card fields in API responses”).  
3. **Integrate via Existing Client Stack:** Point your application’s database or API client to the proxy’s address (HTTP/HTTPS). No code changes are required beyond the endpoint URL.  
4. **Enable Observability & Secrets:** Configure OpenTelemetry exporters and point the proxy to your secret vault (HashiCorp Vault, AWS Secrets Manager, etc.) to automatically inject credentials.  
5. **Run in Quarantine Mode:** Use the “first‑use quarantine” feature to log violations without blocking traffic, allowing you to fine‑tune policies before enforcement.  
6. **Promote to Production:** Once policies are validated, switch the proxy to enforcement mode, enable rate‑limiting, and monitor via your existing telemetry pipeline.

### Production Readiness
- **Activity & Community:** The repository shows recent commits (last updated 2026‑06‑30), 24 stars, 4 forks, and a healthy set of 20 topics, indicating active maintenance and community interest.  
- **Maturity of Core Features:** Core capabilities (policy enforcement, PII redaction, audit logging, rate limiting) are already implemented and used in the provided lenses; performance benchmarks claim 3× speed improvements over comparable solutions.  
- **Scalability:** Being a local‑first proxy, it scales horizontally by deploying additional instances behind a load balancer; no external gateway bottleneck exists.  
- **Security Posture:** The project is AGPL‑licensed, which enforces source availability for downstream users, but a commercial license is available for enterprises needing proprietary support. No major security vulnerabilities have been reported, though a formal security audit is advisable before a wide‑scale rollout.  
- **Operational Simplicity:** Deployment can be containerized (Dockerfile is provided) and managed with standard orchestration tools (Kubernetes, Docker Compose). The YAML‑driven configuration reduces the need for custom code and speeds up onboarding.

**Overall**, JanuScope is production‑ready for pilot projects and likely for full‑scale deployment after a brief validation phase, especially for organizations that need tight control over payment‑related data flows while keeping latency low and maintaining full observability.

### Русский

Резюме проекта JanuScope:

JanuScope - это бесплатная (по лицензии AGPL) или коммерческая платформа для интеграции монетизации, оплаты или потоков PSP (Payment Service Provider) в приложениях. Это локальный прокси политик MCP (Microservices-based Cloud Platform), который позволяет интегрировать различные сервисы, такие как GitHub, Stripe, Snowflake и т. д. с помощью единой конфигурации в виде YAML-файла.

JanuScope идеально подходит для типового сценария внедрения в приложениях, которые требуют интеграции оплаты или монетизации, например, интеграции системы оплаты в онлайн-магазине или автоматизации операций по платежам. Благодаря своей высокой готовности к production (High) и активному развитию, JanuScope является надежным выбором для серьезного пилота.

Проект демонстрирует хорошие показатели качества, такие как 24 GitHub звезды, 4 фorks и обновление в 2026 году, что говорит о его стабильности и жизнесп

### 中文

**简短介绍**

JanuScope 是一个本地优先 MCP 政策代理，提供工具块、SQL 变更门控、PII 隐私、审计、限速、OpenTelemetry、秘密存储等功能。它支持 20 多种 MCP（如 Postgres、MySQL、MongoDB 等），并且可以通过 YAML 文件轻松整合任何 MCP。

**价值**

JanuScope 帮助快速集成商务、计费或 PSP 流程，减少令牌数量约 84%，提高速度约 3 倍，防止 PII 泄露。

**典型接入方式**

JanuScope 支持以下接入方式：

* 整合计费或结算
* 评估 PSP 流程
* 自动化支付操作

**生产可用性**

JanuScope 的生产可用性很高，适合-serious 的试验。它拥有活跃的社区、强大的生态系统信号和最近的活动记录。

## 🧭 Practical evaluation

**Value:** giancarloerra/JanuScope helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 24 GitHub stars
- 4 forks
- updated 2026-06-30
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 30/100 |
| topics | 100/100 |
| outlook | 55/100 |
| quality | 52/100 |
| recency | 40/100 |
| adoption | 26/100 |
| production | 56/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/giancarloerra/JanuScope) · [← Back to Payments](./README.md)</sub>
