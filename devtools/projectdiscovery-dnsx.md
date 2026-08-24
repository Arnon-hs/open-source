# projectdiscovery/dnsx

[![Stars](https://img.shields.io/github/stars/projectdiscovery/dnsx?style=flat-square&color=yellow)](https://github.com/projectdiscovery/dnsx/stargazers) [![Forks](https://img.shields.io/github/forks/projectdiscovery/dnsx?style=flat-square&color=blue)](https://github.com/projectdiscovery/dnsx/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> dnsx is a fast and multi-purpose DNS toolkit allow to run multiple DNS queries of your choice with a list of user-supplied resolvers.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.8k |
| 🍴 **Forks** | 319 |
| 💻 **Language** | Go |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `dns-bruteforcer` `dns-client` `dns-records` `dns-resolution` `hacktoberfest` `wildcard-filtering`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Project Overview**

Projectdiscovery/dnsx is an open-source, multi-purpose DNS toolkit that accelerates DNS queries with user-supplied resolvers, saving engineers time in daily development and review loops. This tool can be used to speed up developer workflows, automate local engineering tasks, and improve CI feedback.

**Value Proposition**

The primary value proposition of projectdiscovery/dnsx lies in its ability to streamline engineering tasks, making it an essential tool for developers. By automating DNS queries and providing a fast and efficient solution, it enables engineers to focus on more critical tasks.

**Practical Adoption Path**

To adopt projectdiscovery/dnsx, follow these steps:

1. Evaluate the project's documentation and API/SDK/CLI integration to assess its ease of use.
2. Review the tool's performance and compare it to existing solutions.
3. Integrate projectdiscovery/dnsx into your existing development workflow, starting with local engineering tasks.
4. Monitor and refine the tool's performance to ensure seamless integration and optimal results.

**Production Readiness**

Projectdiscovery/dnsx demonstrates high production readiness due to its recent activity, strong adoption (2767 GitHub stars), and a well-maintained ecosystem. Its primary language, Go, is also a factor in its production

### Русский

Резюме проекта projectdiscovery/dnsx:

Проект dnsx представляет собой быстрый и многоцелевой инструментарий для работы с DNS, позволяющий выполнять различные запросы к DNS-серверам с помощью списка пользовательских резолверов. Это позволяет инженерам ускорять свои ежедневные разработки и облегчать ревью, автоматизируя локальные задачи и улучшая обратную связь в CI/CD процессе. Проект готов к производству на высоком уровне, с сильными метаданными об активности, приёме и экосистеме, но требует тщательной проверки лицензионной политики, безопасности и активности разработчиков.

### 中文

**项目简介**  
`projectdiscovery/dnsx` 是一款基于 Go 的高速多功能 DNS 工具箱，支持使用自定义解析器列表并行执行多种 DNS 查询，帮助开发者在本地或 CI 环境中快速获取 DNS 结果。

**价值**  
- **提升效率**：一次性并行发起大量 DNS 查询，显著缩短调试、配置检查和安全审计的等待时间。  
- **自动化**：可脚本化调用，轻松嵌入 CI/CD 流程，实现对域名解析状态的持续监控和回归检测。  
- **统一工具链**：提供 CLI、JSON 输出以及可复用的 Go SDK，便于在不同语言或平台的工具中统一使用。

**典型接入方式**  
1. **CLI**：直接在终端或 CI 脚本中调用 `dnsx -list domains.txt -r resolvers.txt -json -o result.json`。  
2. **Go SDK**：在自有 Go 项目中引入 `github.com/projectdiscovery/dnsx/v2` 包，使用 `dnsx.New()` 创建实例并调用 `Resolve()` 方法。  
3. **容器化**：官方提供 Docker 镜像 `projectdiscovery/dnsx:latest`，可在 Kubernetes Job 或 GitHub Actions 中以容器方式运行，无需额外环境配置。

**生产可用性**  
- **活跃度高**：截至 2026‑07‑02，最近一次提交，拥有 2767 ⭐、319 Fork，7 个相关话题，社区活跃。  
- **成熟度**：使用 Go 编写，二进制体积小，跨平台（Linux、macOS、Windows）均可直接运行。  
- **安全与合规**：许可证为 MIT，暂无已知重大安全漏洞；但在正式投产前仍建议进行内部安全审计并确认维护者响应速度。  
- **适配性**：提供明确的 API/CLI 文档，易于集成到现有 DevOps 流程，已被多家安全/运维团队在生产环境中使用。

综合来看，`dnsx` 具备高性能、易集成、社区活跃等优势，是在开发、测试及 CI 环境中实现 DNS 自动化的可靠 OSS 选型。

## 🧭 Practical evaluation

**Value:** projectdiscovery/dnsx helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2767 GitHub stars
- 319 forks
- updated 2026-07-02
- primary language: Go
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 63/100 |
| stars | 73/100 |
| topics | 88/100 |
| outlook | 65/100 |
| quality | 70/100 |
| recency | 40/100 |
| adoption | 70/100 |
| production | 61/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/projectdiscovery/dnsx) · [← Back to DevTools](./README.md)</sub>
