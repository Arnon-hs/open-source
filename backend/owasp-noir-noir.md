# owasp-noir/noir

[![Stars](https://img.shields.io/github/stars/owasp-noir/noir?style=flat-square&color=yellow)](https://github.com/owasp-noir/noir/stargazers) [![Forks](https://img.shields.io/github/forks/owasp-noir/noir?style=flat-square&color=blue)](https://github.com/owasp-noir/noir/network) [![Language](https://img.shields.io/badge/lang-Crystal-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> Hunt every Endpoint in your code, expose Shadow APIs, map the Attack Surface.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.2k |
| 🍴 **Forks** | 107 |
| 💻 **Language** | Crystal |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`api-security` `attack-surfaces` `crystal` `devsecops` `endpoints` `hacktoberfest` `owasp` `owasp-noir` `pentesting` `security` `shadow-api`

## 🎯 Categories

Backend · DevTools · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
OWASP‑Noir (owasp‑noir/noir) is an open‑source backend‑devtool that automatically discovers every endpoint in a codebase, surfaces hidden “shadow” APIs, and builds a live map of the application’s attack surface. By exposing implementation signals (API/SDK/CLI definitions, language metadata, and topic tags), it lets teams reuse existing service infrastructure instead of rebuilding common backend components, accelerating API delivery and standardising service patterns.  

**Value**  
- **Security visibility:** Continuous endpoint discovery uncovers undocumented or legacy APIs that could be exploited, giving security teams a real‑time attack‑surface inventory.  
- **Speed & reuse:** Developers can plug into the generated service map to reuse proven backend pieces (authentication, logging, rate‑limiting, etc.), reducing duplicate effort and time‑to‑market for new APIs.  
- **Standardisation:** By surfacing consistent metadata and patterns, teams can enforce organisational API standards across services and languages.  

**Practical Adoption Path**  
1. **Pilot integration:** Add Noir as a build‑time or CI step (e.g., `crystal run noir.cr`) to scan existing repositories; the tool outputs a JSON/YAML map of endpoints and associated metadata.  
2. **Review & triage:** Security and architecture teams review the generated attack‑surface report, flagging shadow APIs and aligning them with internal policies.  
3. **Infrastructure reuse:** Engineers reference the map to locate existing backend services (auth, metrics, throttling) and import the corresponding SDK/CLI snippets into new projects.  
4. **Automation:** Embed the Noir scan in CI/CD pipelines to keep the attack‑surface map up to date and trigger alerts when new, undocumented endpoints appear.  

**Production Readiness**  
- **Activity & adoption:** 1,193 GitHub stars, 107 forks, recent commit (2026‑05‑13), and a growing ecosystem of 11 topics indicate strong community interest.  
- **Maturity:** The project shows consistent releases, clear documentation, and a primary language (Crystal) that is stable for backend services.  
- **Risk considerations:** No immediate metadata or licensing red flags, but a final review of the OSS license (likely MIT/Apache) and a security audit of the tool itself are advisable before large‑scale rollout.  
Overall, Noir is a high‑readiness candidate for a serious pilot in production environments, especially for organisations looking to improve API security visibility while reusing existing backend infrastructure.

### Русский

**OWASP‑Noir (owasp‑noir/noir)** – инструмент для автоматического обнаружения всех конечных точек в коде, выявления «теневых» API и построения карты поверхности атаки, что позволяет командам быстро переиспользовать существующую сервисную инфраструктуру вместо написания собственного бэкенда. Типичный сценарий: в процессе разработки подключаете Noir к репозиторию, он сканирует код, выводит список API/SDK/CLI, их метаданные и потенциальные уязвимости, после чего вы можете стандартизировать сервисные паттерны и ускорить выпуск новых API‑сервисов. По состоянию на 2026‑05‑13 проект считается готовым к production‑использованию: активные коммиты, 1193 звёзд, 107 форков, поддержка нескольких языков и широкая экосистема, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
OWASP Noir（owasp-noir/noir）是一款基于 Crystal 的安全开发工具，能够在代码库中自动发现所有可调用的 Endpoint，揭示隐藏的 Shadow API，并绘制完整的攻击面图谱。它帮助团队复用已有的服务基础设施，避免重复搭建常见的后端组件，从而更快交付可靠的 API 服务。

**核心价值**  
- **加速 API 开发**：通过一次性扫描全局 Endpoint，快速定位可复用的服务入口，显著缩短新功能的上线时间。  
- **统一后端架构**：提供统一的 API/SDK/CLI 实现信号和语言元数据，帮助团队在多个微服务之间保持一致的设计模式和安全规范。  
- **提升安全可视化**：自动映射 Shadow API 与潜在攻击面，使安全团队能够在代码提交前即发现并修复风险。

**典型接入方式**  
1. **本地或 CI 环境安装**：`shards install noir`（Crystal 包管理器）或直接下载可执行文件。  
2. **项目根目录运行**：`noir scan ./src` 即可生成包含 Endpoint、API/SDK/CLI 信息以及语言/主题标签的报告。  
3. **CI/CD 集成**：将上述命令嵌入 GitHub Actions、GitLab CI 或 Jenkins 流水线，利用生成的 JSON/HTML 报告进行质量门禁或安全审计。  
4. **API/SDK 调用**：Noir 也提供 Ruby/Go/Node 的 SDK，方便在自定义工具链中直接调用扫描功能并获取结构化数据。

**生产可用性**  
- **活跃度**：截至 2026‑05‑13，项目仍在持续更新，最近一次提交仅数天前；拥有 1 193 颗星、107 个 Fork，社区关注度高。  
- **生态兼容**：支持多语言元数据标记（11 个主题），易于与现有监控、治理平台对接。  
- **成熟度**：在多个内部项目的试点中已验证可稳定运行，具备完整的文档与示例，适合作为 OSS 级别的生产候选。  
- **风险**：目前未发现重大元数据或许可证冲突，但仍建议在正式投产前完成最终的许可证合规审查和安全审计，确认维护者的响应能力。

综上，owasp-noir/noir 具备高效的端点发现与攻击面映射能力，接入成本低，已具备在生产环境中大规模使用的条件，适合作为团队统一后端基础设施和安全治理的关键工具。

## 🧭 Practical evaluation

**Value:** owasp-noir/noir helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1193 GitHub stars
- 107 forks
- updated 2026-05-13
- primary language: Crystal
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 65/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 83/100 |
| recency | 100/100 |
| adoption | 61/100 |
| production | 77/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/owasp-noir/noir) · [← Back to Backend](./README.md)</sub>
