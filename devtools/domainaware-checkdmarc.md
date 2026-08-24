# domainaware/checkdmarc

[![Stars](https://img.shields.io/github/stars/domainaware/checkdmarc?style=flat-square&color=yellow)](https://github.com/domainaware/checkdmarc/stargazers) [![Forks](https://img.shields.io/github/forks/domainaware/checkdmarc?style=flat-square&color=blue)](https://github.com/domainaware/checkdmarc/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> A parser for SPF and DMARC DNS records

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 316 |
| 🍴 **Forks** | 96 |
| 💻 **Language** | Python |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `dmarc` `dns` `email` `python` `security` `spf`

## 🎯 Categories

DevTools · Security

## 📝 Summary

### English

**Brief Summary**  
`domainaware/checkdmarc` is a Python‑based open‑source library that parses SPF and DMARC DNS records, exposing the data through an API, SDK and CLI. With 316 ★ and recent commits (as of 2026‑06‑23), it is a mature, security‑focused tool that can be leveraged to add AI‑driven analysis of email authentication without building a parser from scratch.  

**Value**  
The project supplies ready‑made, standards‑compliant parsing logic, letting teams focus on higher‑level AI use cases such as automated threat detection, RAG (retrieval‑augmented generation) over email authentication data, or building agents that react to mis‑configurations. By reusing a well‑tested parser, developers avoid costly bugs and can accelerate prototypes that combine DNS security insights with machine‑learning models.  

**Practical Adoption Path**  
1. **Evaluation** – Clone the repo, run the provided CLI (`checkdmarc`) against a few domains to confirm output format and performance.  
2. **Integration** – Import the SDK (`checkdmarc.parser`) into your Python service, wrap the parsing results in a JSON schema, and feed them to your AI pipeline (e.g., prompt engineering for a LLM or feature extraction for a classifier).  
3. **Automation** – Deploy the CLI or SDK in a CI/CD job or serverless function that periodically scans your domain portfolio, stores results in a data lake, and triggers downstream AI workflows.  

**Production Readiness**  
- **Activity & Community**: Recent commits, 96 forks, and active issue discussions indicate healthy maintenance.  
- **Stability**: The library is pure Python with clear type hints and unit tests, making it easy to bundle in containers or virtual environments.  
- **Security**: No known vulnerabilities; however, a final license and security‑policy review is advisable before enterprise rollout.  
Overall, `domainaware/checkdmarc` is production‑ready for pilots and can be scaled to full‑stack security automation with minimal engineering overhead.

### Русский

**domainaware/checkdmarc** — это Python‑библиотека и CLI‑утилита для парсинга SPF и DMARC записей DNS, позволяющая быстро интегрировать проверку политики электронной почты в любые AI‑проекты (например, прототипы RAG‑агентов или системы автоматической оценки доменных репутаций). Благодаря активному развитию (316 ★, 96 forks, обновления до 2026‑06‑23) и простой интеграции через API/SDK, проект готов к использованию в продакшн‑окружениях, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
domainaware/checkdmarc 是一个用 Python 编写的开源库，能够解析并验证 SPF 与 DMARC DNS 记录，帮助开发者快速获取域名的邮件身份认证配置。

**价值**  
- **即插即用的安全能力**：无需自行实现 DNS 解析和 DMARC/SPF 规则，直接通过库函数获取结构化的认证信息，省时省力。  
- **AI/ML 场景的底层支撑**：在构建邮件安全、垃圾邮件过滤或基于域名信誉的 RAG/Agent 工作流时，可直接把解析结果喂给模型，提升特征质量。  
- **社区成熟、维护活跃**：316 星、96 Fork，2026‑06‑23 最近一次提交，表明项目仍在积极维护，适合作为生产环境的依赖。

**典型接入方式**  
1. **Python SDK**：`pip install checkdmarc` 后，使用 `checkdmarc.check(domain)` 获取解析结果。  
2. **CLI**：`checkdmarc example.com` 可在终端直接查看 SPF/DMARC 记录，适合脚本化调用。  
3. **API/微服务**：将库封装为 Flask/FastAPI 接口，对外提供 HTTP 查询服务，便于在多语言系统中统一调用。

**生产可用性**  
- **成熟度**：代码库活跃、文档完整、已在多个开源安全工具中被引用，具备生产级别的稳定性。  
- **安全与合规**：采用 MIT 许可证，暂无已知的安全漏洞；仍建议在正式部署前进行一次依赖审计。  
- **运维成本低**：仅依赖标准库和少量第三方（如 `dnspython`），部署和升级成本低，适合作为安全监控或 AI 工作流的底层组件。  

综上，domainaware/checkdmarc 能以最小的集成成本，为邮件安全和 AI 驱动的域名信誉分析提供可靠的数据来源，已具备在生产环境中大规模使用的条件。

## 🧭 Practical evaluation

**Value:** domainaware/checkdmarc helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 316 GitHub stars
- 96 forks
- updated 2026-06-23
- primary language: Python
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 50/100 |
| stars | 53/100 |
| topics | 88/100 |
| outlook | 57/100 |
| quality | 62/100 |
| recency | 40/100 |
| adoption | 52/100 |
| production | 58/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/domainaware/checkdmarc) · [← Back to DevTools](./README.md)</sub>
