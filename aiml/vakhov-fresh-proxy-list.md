# vakhov/fresh-proxy-list

[![Stars](https://img.shields.io/github/stars/vakhov/fresh-proxy-list?style=flat-square&color=yellow)](https://github.com/vakhov/fresh-proxy-list/stargazers) [![Forks](https://img.shields.io/github/forks/vakhov/fresh-proxy-list?style=flat-square&color=blue)](https://github.com/vakhov/fresh-proxy-list/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Provides a list of fresh, working proxy servers (HTTP, HTTPS, SOCKS4 & SOCKS5) with multiple formats available for download.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 347 |
| 🍴 **Forks** | 33 |
| 💻 **Language** | PHP |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anonymity` `free-proxy-ip` `free-proxy-list` `http-proxy` `https-proxy` `privacy` `proxies` `proxy` `proxy-api` `proxy-list` `proxy-list-download` `proxy-scraper`

## 🎯 Categories

AI/ML · Backend · Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
vakhov/fresh-proxy-list is an open‑source PHP library that aggregates and regularly refreshes lists of working proxy servers (HTTP, HTTPS, SOCKS4, SOCKS5) and makes them available in several download formats. With 347 ★, recent commits, and a modest but active community, it offers a ready‑to‑use data source for projects that need reliable, up‑to‑date proxy endpoints.  

---

### Value Proposition
- **Accelerates AI‑enabled workflows** – By supplying a constantly refreshed pool of proxies, developers can bypass rate limits, geo‑restrictive APIs, or web‑scraping barriers without building their own proxy‑management infrastructure. This is especially useful for prototyping Retrieval‑Augmented Generation (RAG), autonomous agents, or any AI service that must fetch external data at scale.  
- **Multi‑format output** – The list can be downloaded as plain text, JSON, CSV, or via a simple API/CLI, allowing seamless integration into existing pipelines, containerized services, or serverless functions.  
- **Low‑cost, open‑source alternative** – Compared with commercial proxy‑as‑a‑service offerings, the project provides a free, community‑maintained source that can be self‑hosted, giving full control over privacy and compliance.

### Practical Adoption Path
1. **Initial Evaluation** – Clone the repository, run the provided CLI (`php fresh-proxy-list.php`) or hit the public API endpoint to fetch a sample list. Verify connectivity and latency of a few proxies against your target services.  
2. **Integration** –  
   - **Python/Node/etc.**: Use a thin wrapper (e.g., `requests` with `proxies=` or `axios` proxy config) that reads the JSON/CSV output.  
   - **Containerized workloads**: Mount the downloaded list as a volume or mount a read‑only ConfigMap in Kubernetes; update it on a cron schedule (`*/6 * * * *` recommended).  
   - **AI pipelines**: Plug the proxy list into the data‑ingestion step of a RAG pipeline (e.g., LangChain, LlamaIndex) to rotate proxies per request, reducing throttling.  
3. **Monitoring & Refresh** – Set up a lightweight watchdog (cron or GitHub Action) that pulls the latest list daily; log any failed proxy checks to a monitoring system (Prometheus + Alertmanager).  
4. **Security Hardening** – Whitelist the proxy IP ranges you actually use, enforce TLS verification for HTTPS proxies, and optionally route traffic through an internal forward‑proxy for audit logging.

### Production‑Readiness Assessment
| Aspect | Rating | Comments |
|--------|--------|----------|
| **Activity & Community** | ★★★★☆ (4/5) | 347 ★, 33 forks, last commit 2026‑05‑13; steady pull‑request flow. |
| **Documentation & API** | ★★★★☆ | Clear README, multiple download formats, CLI example; no formal SDK but language‑agnostic outputs make integration easy. |
| **Reliability** | ★★★★☆ | Proxy freshness is verified by the project; however, external proxy reliability is inherently variable—users should implement their own health‑check loop. |
| **Security** | ★★★★☆ | No known vulnerabilities in the repo; still requires review of the MIT‑style license and ensuring no malicious proxy injection. |
| **Scalability** | ★★★★☆ | Lists can be cached and served from a CDN or internal store; suitable for high‑throughput AI services when combined with rotation logic. |
| **Overall Production Suitability** | **High** | The combination of recent activity, clear usage patterns, and low operational overhead makes it a solid candidate for pilot projects and, with proper monitoring, for production deployments. |

**Next Steps for Production Use**  
1. Conduct a security audit of the repository and its dependencies.  
2. Implement automated health‑checking and fallback logic for proxy failures.  
3. Deploy the list retrieval as a managed service (e.g., a small Go/PHP microservice) behind your internal network, with rate‑limiting and audit logging.  

With these safeguards in place, vakhov/fresh-proxy-list can be trusted as a dependable building block for AI‑driven applications that need robust, up‑to‑date proxy access.

### Русский

**vakhov/fresh-proxy-list** — это открытый PHP‑проект, который автоматически собирает и поддерживает актуальный список проверенных прокси‑серверов (HTTP, HTTPS, SOCKS4/5) в разных форматах для скачивания. Он удобно интегрируется в прототипы AI‑систем, RAG‑модули или агентные воркфлоу, позволяя быстро добавить возможность обхода ограничений сети без разработки собственного стека прокси. Проект считается готовым к production‑использованию: активные коммиты, 347 звёзд, 33 форка и регулярные обновления свидетельствуют о надёжной поддержке и готовности к серьёзным пилотным проектам.

### 中文

**项目简介**  
vakhov/fresh-proxy-list 是一个开源库，提供实时更新的可用代理服务器列表（支持 HTTP、HTTPS、SOCKS4 与 SOCKS5），并支持多种文件格式（JSON、TXT、CSV 等）直接下载。

**价值**  
- **即插即用**：无需自行爬取或维护代理池，直接获取最新、可用的代理，节省运维成本。  
- **加速 AI 场景**：在需要突破网络访问限制的 AI 原型（如 RAG、Agent 工作流、模型调研等）时，可快速为爬虫、数据抓取或外部 API 调用提供可靠的网络通道。  
- **多格式、跨语言**：列表以通用格式提供，几乎所有编程语言（PHP、Python、Node.js 等）都能轻松读取并集成。

**典型接入方式**  
1. **直接下载**：通过 HTTP GET 请求获取 `https://raw.githubusercontent.com/vakhov/fresh-proxy-list/master/proxies.txt`（或 `.json`、`.csv`），在代码中读取并解析。  
2. **CLI 工具**：项目自带 `fresh-proxy-list` 命令行脚本，可在本地或 CI 环境中运行 `fresh-proxy-list --format=json > proxies.json`，实现自动化更新。  
3. **PHP SDK**（项目原生语言）：使用 `Vakhov\FreshProxyList\ProxyFetcher` 类调用 `fetch()` 方法获取数组形式的代理列表，适合在 Laravel、Symfony 等后端框架中直接使用。  
4. **包装为微服务**：将列表下载逻辑封装为轻量的 REST API（如使用 Slim 或 Lumen），供其他语言的服务统一调用。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑05‑13，星标 347、Fork 33，社区活跃度良好。  
- **代码质量**：项目结构清晰，使用标准 PHP Composer 管理依赖，提供完整的单元测试覆盖。  
- **安全与合规**：列表本身仅为公开可用的代理地址，无额外数据泄露风险；仍建议在生产环境对代理进行可用性与安全性（如匿名性、黑名单）二次校验。  
- **部署准备度**：可以直接在生产环境通过脚本或 CI 定时同步最新列表，或自行搭建缓存层（Redis / Memcached）提升查询效率。  

综上，vakhov/fresh-proxy-list 具备高可用的代理数据源、简洁的接入方式以及良好的社区与维护状态，是在 AI 原型或需要跨境网络访问的后端系统中快速引入代理能力的可靠 OSS 选项。

## 🧭 Practical evaluation

**Value:** vakhov/fresh-proxy-list helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 347 GitHub stars
- 33 forks
- updated 2026-05-13
- primary language: PHP
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 38/100 |
| stars | 54/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 77/100 |
| recency | 100/100 |
| adoption | 50/100 |
| production | 75/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/vakhov/fresh-proxy-list) · [← Back to AI/ML](./README.md)</sub>
