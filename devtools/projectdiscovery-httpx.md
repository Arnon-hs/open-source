# projectdiscovery/httpx

[![Stars](https://img.shields.io/github/stars/projectdiscovery/httpx?style=flat-square&color=yellow)](https://github.com/projectdiscovery/httpx/stargazers) [![Forks](https://img.shields.io/github/forks/projectdiscovery/httpx?style=flat-square&color=blue)](https://github.com/projectdiscovery/httpx/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-80%2F100-brightgreen?style=flat-square)](#)

> httpx is a fast and multi-purpose HTTP toolkit that allows running multiple probes using the retryablehttp library.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 9.9k |
| 🍴 **Forks** | 1.1k |
| 💻 **Language** | Go |
| 📈 **Score** | 80/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bugbounty` `cli` `cybersecurity` `hacktoberfest` `http` `lib` `osint` `pentest-tool` `pipeline` `ssl-certificate`

## 🎯 Categories

DevTools · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
projectdiscovery/httpx is a high‑performance, multi‑purpose HTTP toolkit built in Go that leverages the retryablehttp library to run a wide range of probes quickly and reliably. With over 9 900 GitHub stars and active maintenance, it offers a simple API/CLI/SDK that can be dropped into any Go‑centric workflow. The tool is positioned as a developer‑productivity accelerator for faster local testing, CI feedback loops, and automated engineering tasks.  

**Value**  
- **Speed & Efficiency:** By handling retries, redirects, and connection pooling out of the box, httpx reduces the amount of boiler‑plate code engineers write for HTTP interactions, shaving minutes off each development or review cycle.  
- **Security‑Focused Probing:** The built‑in probes (e.g., header inspection, fingerprinting, vulnerability checks) let security teams surface issues early without adding a separate scanner.  
- **Unified Interface:** Whether used as a library, a CLI, or through its generated SDK, teams can standardise HTTP testing across local development, CI pipelines, and production monitoring.  

**Practical Adoption Path**  
1. **Evaluation:** Pull the binary or import the Go module; run a few sample probes against internal services to verify correctness and performance.  
2. **Integration:**  
   - *Local Development:* Wrap httpx calls in test scripts or IDE extensions to validate endpoints during coding.  
   - *CI/CD:* Add the CLI to pipeline steps (e.g., `httpx -list urls.txt -probe ...`) to provide immediate feedback on broken or insecure endpoints.  
   - *Automation:* Use the Go SDK to embed probing logic in custom tooling or monitoring agents.  
3. **Roll‑out:** Gradually replace ad‑hoc curl/wget scripts with httpx across teams, tracking metrics such as mean time to detect HTTP‑related failures.  

**Production Readiness**  
- **Activity & Adoption:** Recent commits (as of 2026‑05‑13), >9 900 stars, >1 000 forks, and a vibrant issue/PR community indicate strong momentum.  
- **Stability:** The project follows semantic versioning, provides pre‑built binaries for major OS/arch, and has a clear release cadence.  
- **Ecosystem Fit:** Written in Go, it integrates cleanly with existing Go services and can be called from any language via the CLI.  
- **Risk Profile:** No major licensing or metadata concerns have surfaced; a final review of the security posture and maintainer responsiveness is recommended, but overall the toolkit is ready for a serious pilot in production environments.

### Русский

**projectdiscovery/httpx** — это высокопроизводительный набор инструментов для работы с HTTP, построенный на библиотеке retryablehttp. Он позволяет инженерам быстро выполнять множество запросов (пробы, сканирование, проверку статусов) из CLI, SDK или API, что ускоряет локальные задачи, CI‑проверки и общие рабочие процессы разработки. Проект демонстрирует высокий уровень готовности к production: активные коммиты, более 9 тыс. звёзд на GitHub, широкое принятие в сообществе и стабильный набор функций, требующий лишь финального аудита лицензии и безопасности.

### 中文

**项目简介（2‑3 句）**  
`projectdiscovery/httpx` 是一款基于 Go 的高速多功能 HTTP 工具箱，利用 retryablehttp 实现可靠的请求重试与并发探测。它提供 CLI、SDK 与 API 接口，能够在一次运行中执行多种网络探针，帮助开发者快速获取目标站点的状态、标题、指纹等信息。

**价值**  
- **提升开发效率**：在本地调试、代码审查以及 CI 流水线中自动化执行 HTTP 检测，显著缩短反馈周期。  
- **统一安全与运维检测**：一次调用即可完成端口探测、标题抓取、指纹识别等多项任务，减少工具链碎片化。  

**典型接入方式**  
1. **CLI**：直接在终端运行 `httpx` 命令，配合文件或标准输入输出进行批量扫描。  
2. **SDK / API**：在 Go 项目中引入 `github.com/projectdiscovery/httpx` 包，调用其公开函数实现自定义探测逻辑。  
3. **CI 集成**：在 GitHub Actions、GitLab CI 等流水线中通过 Docker 镜像或二进制文件执行，结合 `--json`、`--output` 等参数将结果回写至构建报告。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑13，项目拥有 9 928+ Stars、1 064+ Forks，最近一次提交在当天，表明持续维护。  
- **技术成熟**：使用 Go 编写，依赖成熟的 `retryablehttp` 库，具备并发控制、自动重试等可靠特性。  
- **生态兼容**：提供完整的 CLI、SDK 与 OpenAPI 风格的调用方式，易于在现有工具链中嵌入。  
- **风险**：目前未发现重大元数据风险，但仍需对许可证（Apache‑2.0）和安全审计报告进行最终确认。  

综上，`projectdiscovery/httpx` 在功能完整性、社区活跃度和易用性方面均表现优秀，适合作为生产环境中 HTTP 探测与自动化任务的首选 OSS 组件。

## 🧭 Practical evaluation

**Value:** projectdiscovery/httpx helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 9928 GitHub stars
- 1064 forks
- updated 2026-05-13
- primary language: Go
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 76/100 |
| stars | 85/100 |
| topics | 100/100 |
| outlook | 90/100 |
| quality | 92/100 |
| recency | 100/100 |
| adoption | 82/100 |
| production | 83/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/projectdiscovery/httpx) · [← Back to DevTools](./README.md)</sub>
