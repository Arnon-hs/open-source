# TecharoHQ/anubis

[![Stars](https://img.shields.io/github/stars/TecharoHQ/anubis?style=flat-square&color=yellow)](https://github.com/TecharoHQ/anubis/stargazers) [![Forks](https://img.shields.io/github/forks/TecharoHQ/anubis?style=flat-square&color=blue)](https://github.com/TecharoHQ/anubis/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> Weighs the soul of incoming HTTP requests to stop AI crawlers

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 20.6k |
| 🍴 **Forks** | 655 |
| 💻 **Language** | Go |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`defense` `security`

## 🎯 Categories

Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Anubis (TecharoHQ/anubis) is a Go‑based open‑source library that evaluates incoming HTTP requests and assigns a “soul weight” to block AI‑driven crawlers while allowing legitimate traffic. It provides a lightweight, plug‑and‑play security layer that can be added to existing services without building a custom model stack from scratch. With strong recent activity, a large community (20 k+ stars) and solid ecosystem signals, it is ready for serious pilot deployments.

**Value**  
- **AI‑aware protection:** By scoring requests for AI‑generated patterns, Anubis helps services defend against automated scraping, data harvesting, and model‑training bots that traditional firewalls miss.  
- **Fast integration:** Since it ships as a Go module with a simple middleware interface, teams can add AI‑crawler detection to APIs or microservices in minutes, avoiding the overhead of training or maintaining their own ML models.  
- **Extensible for prototyping:** The library can be combined with Retrieval‑Augmented Generation (RAG) or agent workflows to test AI‑enhanced security policies before committing to a full‑scale solution.

**Practical Adoption Path**  
1. **Evaluate locally:** Clone the repo, run the provided examples, and inspect the request‑scoring logic to ensure it aligns with your traffic patterns.  
2. **Integrate as middleware:** Add the Anubis Go module to your HTTP server (e.g., net/http, Echo, Gin) and configure thresholds or custom rules via the provided config file.  
3. **Manual review phase:** Deploy the middleware in a staging environment with logging enabled; manually review blocked requests to fine‑tune sensitivity and avoid false positives.  
4. **Roll‑out to production:** Once thresholds are validated, enable the blocking mode, monitor metrics (blocked vs. allowed requests), and optionally feed logs into your existing observability stack.

**Production Readiness**  
- **Maturity:** Recent commits (as of 2026‑07‑12), active fork activity, and a large star count indicate a healthy, maintained project.  
- **Stability:** The core middleware is small, well‑documented, and written in Go, which is known for low runtime overhead and easy deployment.  
- **Risk considerations:** No major metadata issues were found, but a final review of the license (MIT/Apache‑style) and an independent security audit are recommended before mission‑critical use. Overall, Anubis is a strong OSS candidate for a pilot and can be promoted to production once the manual‑inspection tuning phase is completed.

### Русский

**TecharoHQ/anubis** – лёгкая Go‑библиотека, которая «взвешивает» входящие HTTP‑запросы и блокирует AI‑краулеров, позволяя добавить AI‑функциональность без построения модели с нуля. Типичный сценарий — быстрая интеграция в прототипы AI‑фич, RAG‑или агентные воркфлоу, где требуется защита от нежелательного автоматизированного трафика; перед внедрением рекомендуется ручная проверка из‑за ограниченной метаданных‑интеграции. Проект считается готовым к production‑использованию: активная разработка, более 20 тыс. звёзд, многочиские форки и положительные экосистемные сигналы, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
TecharoHQ / anubis 是一款用 Go 编写的开源安全中间件，它通过对进入的 HTTP 请求进行“灵魂称重”，识别并拦截 AI 爬虫，从而保护后端服务不被自动化抓取。

**价值**  
- **即插即用的 AI 防护**：无需自行训练模型或搭建复杂的检测流水线，直接利用已有的 AI 行为特征库即可过滤恶意请求。  
- **降低研发成本**：帮助团队在原型阶段快速加入 AI 防护能力，适配 RAG、Agent 等工作流时只需少量配置。  
- **社区与活跃度**：拥有 20 k+ 星、数百次 Fork，近期仍在维护，适合作为正式项目的安全基线。

**典型接入方式**  
1. **作为反向代理或中间件**：在 Nginx/Traefik 前层或直接在 Go 项目中通过 `http.Handler` 包装现有路由。  
2. **配置规则文件**：提供 JSON/YAML 格式的检测规则，可根据业务需求增删特征。  
3. **手动审查**：首次部署前建议在测试环境跑一次流量审计，确认拦截误报率符合预期，因为元数据的信号相对稀疏。

**生产可用性**  
- **成熟度**：近期（2026‑07‑12）仍有更新，社区活跃，适合作为 OSS 级别的 Pilot 项目。  
- **风险**：需进一步核实许可证兼容性、完整的安全审计报告以及维护者的响应时效。除这些细节外，整体可视为高可用的生产候选。

## 🧭 Practical evaluation

**Value:** TecharoHQ/anubis helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 20620 GitHub stars
- 655 forks
- updated 2026-07-12
- primary language: Go
- 2 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 70/100 |
| stars | 92/100 |
| topics | 25/100 |
| outlook | 56/100 |
| quality | 67/100 |
| recency | 40/100 |
| adoption | 86/100 |
| production | 57/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/TecharoHQ/anubis) · [← Back to Security](./README.md)</sub>
