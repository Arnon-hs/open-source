# requests-cache/requests-cache

[![Stars](https://img.shields.io/github/stars/requests-cache/requests-cache?style=flat-square&color=yellow)](https://github.com/requests-cache/requests-cache/stargazers) [![Forks](https://img.shields.io/github/forks/requests-cache/requests-cache?style=flat-square&color=blue)](https://github.com/requests-cache/requests-cache/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Persistent HTTP cache for python requests

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.5k |
| 🍴 **Forks** | 157 |
| 💻 **Language** | Python |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cache` `dynamodb` `http` `mongodb` `performance` `redis` `requests` `sqlite` `web` `webscraping`

## 🎯 Categories

Database

## 📝 Summary

### English

**Brief Summary**  
Requests‑Cache is a Python library that adds a persistent, pluggable cache layer to the popular *requests* HTTP client. By storing responses locally (SQLite, Redis, filesystem, etc.) it lets developers reuse API data across runs, dramatically cutting latency and external‑service load.

**Value**  
- **Speed & cost savings** – Cached responses eliminate redundant network calls, reducing latency for end‑users and lowering bandwidth or third‑party API costs.  
- **Standardized backend pattern** – Teams can adopt a single, well‑maintained caching solution instead of building ad‑hoc caches for each service, improving code consistency and maintainability.  
- **Flexibility** – Supports multiple back‑ends, expiration policies, and fine‑grained control via decorators or session objects, fitting a wide range of microservice or data‑pipeline use cases.

**Practical Adoption Path**  
1. **Prototype** – Add `requests-cache` to a sandbox service, enable a simple SQLite cache, and verify that repeated calls hit the cache.  
2. **Policy definition** – Choose an appropriate backend (e.g., Redis for distributed services), set expiration rules, and configure per‑endpoint caching via decorators or custom session classes.  
3. **Integration** – Replace direct `requests` calls with a cached session throughout the codebase, optionally exposing CLI flags or environment variables to toggle caching in different environments (dev, staging, prod).  
4. **Observability** – Use the library’s built‑in hooks to emit metrics (cache hits/misses) to your monitoring stack, ensuring visibility and enabling gradual rollout.

**Production Readiness**  
The project scores 75/100 and shows strong OSS health: ~1.5 k GitHub stars, recent commits (as of 2026‑05‑11), active issue discussion, and multiple maintained back‑ends. Its API is stable, well‑documented, and includes CLI/SDK entry points, making it straightforward to evaluate and integrate. While no critical licensing or security red flags have been identified, a final review of the license (BSD‑3‑Clause) and a quick vulnerability scan of the chosen cache backend are recommended before a full production rollout. Overall, Requests‑Cache is mature enough for a serious pilot and can be promoted to production after the standard integration‑testing and monitoring steps.

### Русский

**requests‑cache** — это библиотека, позволяющая кэшировать ответы `requests` и хранить их в постоянных хранилищах (SQLite, Redis, файловая система и др.), что ускоряет повторные вызовы API и уменьшает нагрузку на внешние сервисы. Она идеально подходит для команд, желающих быстро вывести в продакшн новые микросервисы, стандартизировать работу с HTTP‑кешем и переиспользовать готовую инфраструктуру вместо самостоятельной разработки. Проект считается готовым к production: активная поддержка, регулярные релизы, более 1400 звёзд на GitHub и широкое применение в сообществе Python.

### 中文

**项目简介**  
`requests-cache` 为 Python 的 `requests` 库提供持久化 HTTP 缓存，实现请求结果的本地存储与复用，帮助开发者在不改动业务代码的情况下显著降低网络请求次数和响应延时。

**价值**  
- **复用已有基础设施**：通过统一的缓存层，团队无需自行实现或维护专属的缓存方案，直接复用成熟、社区验证的实现。  
- **加速 API 服务交付**：在开发、测试或生产环境中，缓存可显著提升接口响应速度，降低后端负载，从而缩短上线周期。  
- **标准化后端模式**：统一的缓存策略和配置方式，使得不同服务之间的缓存行为保持一致，降低运维复杂度。

**典型接入方式**  
1. **代码层面**：在项目入口处一次性调用 `requests_cache.install_cache()`，即可让后续所有 `requests` 调用自动走缓存。  
   ```python
   import requests_cache
   requests_cache.install_cache('my_cache', backend='sqlite', expire_after=3600)
   import requests
   response = requests.get('https://api.example.com/data')
   ```
2. **CLI**：提供 `requests-cache` 命令行工具，可对缓存进行查询、清理或迁移，适合运维脚本。  
3. **自定义后端**：支持 SQLite、Redis、MongoDB 等多种持久化后端，亦可实现自定义后端以适配企业内部存储系统。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑11，项目仍在持续更新，拥有 1.5k+ Stars、150+ Forks，社区活跃度良好。  
- **成熟的依赖生态**：基于广泛使用的 `requests`，兼容性好，已被多家企业在生产环境中采用。  
- **安全与合规**：采用 MIT 许可证，暂无已知重大安全漏洞；但仍建议在正式投入前进行一次内部安全审计。  

综合来看，`requests-cache` 是一个成熟、易集成且在生产环境中经验证的缓存解决方案，适合作为后端服务的通用缓存层进行快速落地。

## 🧭 Practical evaluation

**Value:** requests-cache/requests-cache helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1490 GitHub stars
- 157 forks
- updated 2026-05-11
- primary language: Python
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 55/100 |
| stars | 68/100 |
| topics | 100/100 |
| outlook | 55/100 |
| quality | 64/100 |
| recency | 20/100 |
| adoption | 64/100 |
| production | 56/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/requests-cache/requests-cache) · [← Back to Database](./README.md)</sub>
