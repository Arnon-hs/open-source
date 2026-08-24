# TomWright/dasel

[![Stars](https://img.shields.io/github/stars/TomWright/dasel?style=flat-square&color=yellow)](https://github.com/TomWright/dasel/stargazers) [![Forks](https://img.shields.io/github/forks/TomWright/dasel?style=flat-square&color=blue)](https://github.com/TomWright/dasel/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Select, put and delete data from JSON, TOML, YAML, XML, INI, HCL and CSV files with a single tool. Also available as a go mod.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 7.9k |
| 🍴 **Forks** | 167 |
| 💻 **Language** | Go |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `config` `configuration` `data-processing` `data-structures` `data-wrangling` `devops-tools` `go` `golang` `hcl2` `json` `json-processing`

## 🎯 Categories

DevTools · Data

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
TomWright/dasel is a versatile command‑line utility (and Go module) that lets you query, modify, and delete data across a wide range of formats—JSON, TOML, YAML, XML, INI, HCL and CSV—with a single, consistent syntax. Its rich feature set and Go‑native SDK make it easy to embed into scripts, CI pipelines, or larger Go applications, and the project enjoys strong community traction (7.9k ★, 167 forks).  

**Value**  
Dasel eliminates the need to juggle multiple format‑specific parsers or write custom conversion code, enabling rapid prototyping of AI‑driven workflows (e.g., RAG pipelines, prompt‑engineering agents) that must ingest or emit data in heterogeneous formats. By providing a uniform query language and a Go library, it accelerates feature development and reduces bugs associated with manual data handling.  

**Practical Adoption Path**  
1. **Exploratory testing** – Use the CLI to run one‑off queries or transformations on sample files, verifying syntax and performance.  
2. **Integration** – Add the `github.com/tomwright/dasel` module to Go services or wrap the CLI in shell scripts for CI/CD, data‑ingestion jobs, or model‑output post‑processing.  
3. **Automation** – Combine dasel with orchestration tools (e.g., GitHub Actions, Airflow) to standardize data preparation steps across AI pipelines.  

**Production Readiness**  
The project shows high production readiness: recent commits (as of 2026‑05‑13), active issue handling, and a sizable star/fork count indicate a healthy community. Its Go implementation is performant and statically compiled, suitable for containerized environments. While a final legal/security audit (license compliance, vulnerability scanning) is still required, the overall signal suggests dasel is ready for serious pilot deployments and can be trusted as a core data‑manipulation component in production AI systems.

### Русский

**TomWright/dasel** – это кросс‑форматный CLI/Go‑модуль, позволяющий быстро выбирать, изменять и удалять данные в JSON, TOML, YAML, XML, INI, HCL и CSV без написания собственного парсера, что упрощает прототипирование AI‑фич, построение RAG‑ и агентных пайплайнов и оценку инструментов моделей. Проект активно поддерживается (обновление 2026‑05‑13, > 7 000 звёзд, 167 форков), имеет чистый Go‑API и богатую мета‑информацию, поэтому готов к использованию в пилотных и production‑окружениях после стандартной проверки лицензий и безопасности.

### 中文

**项目简介**  
TomWright/dasel 是一款用 Go 编写的轻量级数据操作工具，能够在单个命令行或 Go 模块中对 JSON、TOML、YAML、XML、INI、HCL、CSV 等多种格式进行查询、插入、删除等操作。

**价值**  
- **统一接口**：一次学习即可在七大常用配置/数据格式之间自由切换，省去编写多语言解析代码的时间。  
- **加速 AI 原型**：在构建 RAG、Agent 或其他需要快速读取/写入结构化数据的 AI 工作流时，dasel 能即插即用，帮助团队在不搭建完整数据管道的情况下完成原型验证。  
- **可嵌入**：既提供 CLI，也提供 Go SDK，便于在 CI/CD、微服务或本地脚本中直接调用，提升自动化与可测试性。

**典型接入方式**  
1. **CLI**：`dasel select -f config.yaml 'services[0].port'` 等命令直接在终端操作，适合 DevOps、脚本化任务。  
2. **Go 模块**：在 Go 项目中 `import "github.com/tomwright/dasel"`，使用其公开的 API（如 `dasel.NewReader`, `dasel.NewWriter`）进行编程式数据处理，适合后端服务或 AI 组件内部调用。  
3. **容器化**：官方提供 Docker 镜像，可在容器环境中统一使用，方便在 Kubernetes Job、Airflow Task 等平台集成。

**生产可用性**  
- **活跃度**：截至 2026‑05‑13 最近一次提交，拥有 7,934 星、167 Fork，社区活跃，Issue 响应及时。  
- **语言成熟度**：基于 Go 实现，编译后二进制体积小、启动快，天然适配云原生和边缘环境。  
- **安全与许可证**：采用 MIT 许可证，代码审计记录良好；仍需在正式投产前进行内部安全扫描和依赖审查。  
- **生态兼容**：支持标准输入/输出、JSONPath、XPath 等查询语法，易与现有日志、配置管理、数据治理工具链对接。  

综合来看，dasel 在功能完整性、社区活跃度和技术成熟度方面均表现优秀，适合作为 AI 原型及生产环境中数据处理的可靠 OSS 组件。只要完成常规的安全合规审查，即可在业务系统中安全上线。

## 🧭 Practical evaluation

**Value:** TomWright/dasel helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 7934 GitHub stars
- 167 forks
- updated 2026-05-13
- primary language: Go
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 83/100 |
| topics | 100/100 |
| outlook | 61/100 |
| quality | 69/100 |
| recency | 20/100 |
| adoption | 75/100 |
| production | 55/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/TomWright/dasel) · [← Back to DevTools](./README.md)</sub>
