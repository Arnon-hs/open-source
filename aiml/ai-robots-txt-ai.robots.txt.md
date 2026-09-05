# ai-robots-txt/ai.robots.txt

[![Stars](https://img.shields.io/github/stars/ai-robots-txt/ai.robots.txt?style=flat-square&color=yellow)](https://github.com/ai-robots-txt/ai.robots.txt/stargazers) [![Forks](https://img.shields.io/github/forks/ai-robots-txt/ai.robots.txt?style=flat-square&color=blue)](https://github.com/ai-robots-txt/ai.robots.txt/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> A list of AI agents and robots to block.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4k |
| 🍴 **Forks** | 163 |
| 💻 **Language** | Python |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `crawlers` `crawling` `privacy`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
ai‑robots‑txt/ai.robots.txt is an open‑source Python library that maintains a curated list of AI agents and web‑crawling robots that should be blocked via robots.txt. By providing an up‑to‑date, community‑driven catalogue, it eliminates the need for developers to manually track and update disallowed user‑agents, streamlining compliance and security policies for web services.

**Value**  
- **Automation of a repetitive task** – Instead of manually curating a blocklist, teams can import the library and automatically generate the appropriate `Disallow` directives, saving engineering time and reducing human error.  
- **Consistent policy enforcement** – A single source of truth ensures that all environments (dev, staging, production) block the same set of AI agents, improving security posture and regulatory compliance.  
- **Community‑maintained freshness** – With thousands of GitHub stars and active contributions, the list stays current with emerging AI crawlers, lowering the risk of inadvertently allowing unwanted traffic.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the provided examples, and generate a `robots.txt` file for a non‑critical test site. Verify that the generated directives block the intended agents.  
2. **Integration** – Add the library as a dependency in your web framework (e.g., Flask, Django, FastAPI) and replace any hard‑coded `robots.txt` generation logic with a call to the library’s API.  
3. **CI/CD Validation** – Include a step in your pipeline that lints the generated `robots.txt` against a known baseline and runs the library’s unit tests to catch regressions.  
4. **Rollout** – Deploy the updated configuration to staging, monitor request logs for blocked agents, then promote to production once confidence is established.

**Production Readiness**  
- **Maturity** – Recent commits (as of 2026‑06‑23), a healthy star/fork count (≈4 k stars, 163 forks), and active issue discussion indicate a well‑maintained project.  
- **Stability** – The core functionality is small, pure‑Python, and has minimal external dependencies, making it easy to audit and vendor.  
- **Risk Management** – No major metadata or licensing concerns have been identified, but a final review of the license (MIT/Apache‑style) and a quick security scan of the repository are advisable before full production use.  
Overall, the project is sufficiently mature for a serious pilot, with a clear, low‑risk integration path and strong community backing.

### Русский

**ai-robots-txt/ai.robots.txt** — это открытый список AI‑агентов и роботов, которые следует блокировать, что позволяет автоматизировать очистку и защиту веб‑ресурсов без ручного ввода правил. Типичный сценарий — быстрое подключение проекта к CI/CD или к системе мониторинга, где список импортируется и применяется к правилам robots.txt, устраняя рутинные операции и обеспечивая повторяемость процессов. Проект имеет высокий уровень готовности к production: активные коммиты, более 3900 звёзд, постоянные форки и поддержка на Python, что делает его надёжным кандидатом для пилотного внедрения после небольшого proof‑of‑concept.

### 中文

**项目简介（2‑3 句）**  
ai-robots-txt/ai.robots.txt 是一个开源的 “AI 机器人黑名单”，提供了可直接使用的 `robots.txt` 规则文件，用于在网站、API 或其他可访问资源上阻止已知的 AI 爬虫和自动化工具。项目维护活跃、星标近 4 千，适合作为安全与合规防护的即插即用组件。

**价值**  
- **降低人力成本**：自动拦截大量已知的 AI 代理，免去手动维护黑名单的繁琐工作。  
- **提升安全合规**：帮助企业防止未经授权的模型抓取、数据泄露或违规使用，满足隐私与数据治理要求。  
- **可复用、可扩展**：列表以纯文本形式提供，易于在 CDN、Web 服务器或自定义代理层中嵌入，支持后续自行增删。

**典型接入方式**  
1. **Web 服务器层**：将 `ai.robots.txt` 放置在站点根目录或通过 Nginx/Apache 配置直接返回该文件。  
2. **反向代理或 CDN**：在 Cloudflare、Fastly 等边缘节点添加规则，返回 403/404 或自定义响应给匹配的 User‑Agent。  
3. **API 网关**：在 Kong、Apigee 等网关插件中读取列表，对请求的 `User-Agent` 进行过滤。  
4. **CI/CD 自动化**：使用项目提供的 Python 脚本定期拉取最新列表并同步到内部配置库，实现持续更新。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑23，GitHub ★3959、Fork 163，社区讨论活跃。  
- **成熟度**：代码基于 Python，结构简洁，已在多个开源项目中直接使用，具备生产级别的可靠性。  
- **集成门槛**：建议先在测试环境做小范围 POC（例如仅在 CDN 边缘层返回 `ai.robots.txt`），确认对现有流量和搜索引擎的影响后再推广。  
- **风险**：暂无重大元数据风险，但仍需完成许可证合规审查、依赖安全扫描以及维护者活跃度的最终确认。

总体而言，ai-robots-txt/ai.robots.txt 已具备高生产就绪度，可作为企业防护 AI 爬虫的快速落地方案，配合自动化部署即可实现可重复、可维护的安全控制。

## 🧭 Practical evaluation

**Value:** ai-robots-txt/ai.robots.txt helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3959 GitHub stars
- 163 forks
- updated 2026-06-23
- primary language: Python
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 55/100 |
| stars | 77/100 |
| topics | 50/100 |
| outlook | 72/100 |
| quality | 74/100 |
| recency | 80/100 |
| adoption | 71/100 |
| production | 70/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/ai-robots-txt/ai.robots.txt) · [← Back to AI/ML](./README.md)</sub>
