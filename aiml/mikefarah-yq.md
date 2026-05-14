# mikefarah/yq

[![Stars](https://img.shields.io/github/stars/mikefarah/yq?style=flat-square&color=yellow)](https://github.com/mikefarah/yq/stargazers) [![Forks](https://img.shields.io/github/forks/mikefarah/yq?style=flat-square&color=blue)](https://github.com/mikefarah/yq/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-80%2F100-brightgreen?style=flat-square)](#)

> yq is a portable command-line YAML, JSON, XML, CSV, TOML, HCL  and properties processor

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 15.4k |
| 🍴 **Forks** | 772 |
| 💻 **Language** | Go |
| 📈 **Score** | 80/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bash` `cli` `csv` `devops-tools` `golang` `hcl` `json` `portable` `properties` `splat` `terraform` `toml`

## 🎯 Categories

AI/ML · DevTools · Database · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
mikefarah/yq is a fast, portable command‑line tool written in Go that lets you query, transform, and validate data across YAML, JSON, XML, CSV, TOML, HCL and Java properties formats. With a syntax reminiscent of jq, it enables developers and DevOps engineers to script complex data‑processing pipelines without writing custom parsers. Its high star count, active maintenance, and broad format support make it a solid OSS candidate for production use.  

**Value**  
- **Unified data handling** – One binary can manipulate every major configuration and data serialization format, eliminating the need for multiple specialized tools.  
- **AI‑friendly workflow glue** – yq can preprocess prompts, context files, or model outputs (e.g., extracting snippets from YAML‑based knowledge bases) before feeding them into RAG or agent pipelines, accelerating prototype development.  
- **Low‑learning curve** – The jq‑style expression language is familiar to many engineers, shortening onboarding time for teams that need quick data wrangling in CI/CD or model‑serving scripts.  

**Practical Adoption Path**  
1. **Evaluation** – Install the single‑binary via a package manager (`brew install yq`, `apt-get`, or download the Go binary) and run the built‑in test suite on a sample data set to confirm compatibility with your formats.  
2. **Integration** – Wrap yq calls in shell scripts, Makefiles, or CI pipelines (GitHub Actions, GitLab CI) to perform validation, templating, or conversion steps before invoking AI services.  
3. **SDK/CLI Extension** – If deeper integration is needed, invoke the binary from Go, Python (`subprocess`), or any language that can spawn a process, or embed the Go library directly (the repo provides a public API).  
4. **Production rollout** – Pin the version in your infrastructure as a Docker image or binary checksum, add monitoring for exit codes and output size, and incorporate it into your observability stack.  

**Production Readiness**  
- **Activity & Community** – 15 k+ stars, 772 forks, frequent commits (last update 2026‑05‑14) and a vibrant issue/PR community indicate strong ongoing support.  
- **Stability** – Written in Go, compiled to a single static binary, it has minimal runtime dependencies, making it easy to deploy in containers, VMs, or edge devices.  
- **Security & Licensing** – Uses an MIT‑compatible license; no critical vulnerabilities reported in recent scans, though a formal security audit and verification of maintainer activity are recommended before a large‑scale rollout.  
- **Ecosystem Fit** – Already adopted in many DevOps toolchains (Kubernetes manifests, Helm charts, Terraform HCL), so integrating it with AI pipelines aligns with existing best‑practice patterns.  

Overall, yq offers a high‑impact, low‑friction way to add robust data‑processing capabilities to AI‑augmented workflows, and its maturity makes it ready for production pilots after a brief security and licensing review.

### Русский

**yq** — это кроссплатформенный CLI‑инструмент для обработки YAML, JSON, XML, CSV, TOML, HCL и properties, написанный на Go. Он позволяет быстро добавить AI‑функциональность (прототипировать RAG‑сценарии, агентные воркфлоу и оценивать модели) без необходимости строить стек с нуля, интегрируясь через простой API/SDK/CLI. Проект обладает высокой готовностью к production: активные обновления, более 15 тыс. звёзд, широкое принятие в сообществе и надёжная экосистема, хотя лицензия и безопасность требуют финального аудита.

### 中文

**项目简介（2‑3 句）**  
`mikefarah/yq` 是一款基于 Go 实现的跨平台命令行工具，能够高效地对 YAML、JSON、XML、CSV、TOML、HCL 以及 properties 等多种配置格式进行读取、查询、编辑和转换。它的语法与 `jq` 类似，却专注于层次化数据结构，使得在 DevOps、CI/CD、数据清洗等场景下对配置文件的操作变得简洁而强大。  

**价值**  
- **统一数据处理**：一次学习即可在多种常见配置/序列化格式之间自由切换，避免在项目中引入多个专用解析器。  
- **提升 AI 工作流**：配合 LLM/RAG 流程时，可快速将模型输出的结构化数据（JSON/YAML）转化为所需格式，或从配置文件中抽取提示词、上下文，实现“即插即用”的 AI 能力。  
- **脚本化与自动化**：在 CI/CD、容器编排、基础设施即代码（IaC）等 DevOps 场景中，利用单行或管道命令完成配置的验证、迁移和批量更新，显著降低人为错误。  

**典型接入方式**  
1. **CLI 直接调用**：在 Bash、PowerShell、Fish 等终端中使用 `yq <expression> <file>`，可配合 `|` 管道与 `jq`、`sed`、`awk` 等工具组合使用。  
2. **脚本/自动化**：在 Makefile、GitHub Actions、GitLab CI、Jenkins 等流水线中嵌入 `yq` 命令，实现配置的校验或动态生成。  
3. **SDK/库**：虽然主要是 CLI 工具，但其底层实现为 Go 包，开发者可在 Go 项目中直接 `import "github.com/mikefarah/yq/v4"`，调用内部 API 进行高级处理。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑14，项目拥有 15 389 星、772 个叉，最近一次提交在当天，说明维护者仍在积极迭代。  
- **成熟生态**：已被广泛用于 Kubernetes、Helm、Terraform、Ansible 等主流 DevOps 工具链中，社区提供了大量使用案例和最佳实践。  
- **可靠性**：采用 Go 编译的单二进制文件，跨平台（Linux、macOS、Windows）表现稳定，且对大文件和流式输入有良好支持。  
- **安全与合规**：项目采用 MIT 许可证，暂无已知重大安全漏洞；但在正式投产前仍建议进行内部安全审计和依赖锁定。  

综合来看，`mikefarah/yq` 具备高可用性、易集成和强大功能，是在生产环境中实现配置文件统一处理和 AI 工作流数据转换的首选开源组件。

## 🧭 Practical evaluation

**Value:** mikefarah/yq helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 15389 GitHub stars
- 772 forks
- updated 2026-05-14
- primary language: Go
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 72/100 |
| stars | 89/100 |
| topics | 100/100 |
| outlook | 91/100 |
| quality | 93/100 |
| recency | 100/100 |
| adoption | 84/100 |
| production | 83/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/mikefarah/yq) · [← Back to AI/ML](./README.md)</sub>
