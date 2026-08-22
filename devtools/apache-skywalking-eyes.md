# apache/skywalking-eyes

[![Stars](https://img.shields.io/github/stars/apache/skywalking-eyes?style=flat-square&color=yellow)](https://github.com/apache/skywalking-eyes/stargazers) [![Forks](https://img.shields.io/github/forks/apache/skywalking-eyes?style=flat-square&color=blue)](https://github.com/apache/skywalking-eyes/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> A full-featured license tool to check and fix license headers and resolve dependencies' licenses.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 312 |
| 🍴 **Forks** | 69 |
| 💻 **Language** | Go |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-07-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `license` `licensing` `tools`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Summary**  
Apache SkyWalking‑Eyes is a Go‑based, open‑source utility that scans source files for missing or malformed license headers, can automatically insert or correct them, and can resolve the licenses of third‑party dependencies. It offers a CLI, an API/SDK, and CI‑friendly output, making it easy to embed into local developer workflows and automated pipelines.

**Value**  
By handling license‑header compliance automatically, SkyWalking‑Eyes eliminates a repetitive manual step, reduces the risk of non‑compliant releases, and provides immediate feedback in pull‑requests or CI jobs. This speeds up code reviews, keeps repositories clean, and helps teams stay audit‑ready without sacrificing developer velocity.

**Practical adoption path**  

1. **Local setup** – Install the binary (`go install github.com/apache/skywalking-eyes/cmd/skywalking-eyes@latest`) or add it as a dev‑dependency in your `go.mod`. Run `skywalking-eyes header check` locally to detect missing headers and `skywalking-eyes header fix` to apply them.  
2. **CI integration** – Add a simple step to your CI (GitHub Actions, GitLab CI, Jenkins, etc.) that runs the `check` command and fails the build on violations. The tool’s JSON/YAML output can be consumed by existing lint‑report aggregators.  
3. **Dependency license audit** – Use the `license` sub‑command to generate a bill of materials (BOM) of third‑party licenses, feeding the result into compliance dashboards or security scans.  

Because the CLI is self‑contained and the API can be called from scripts, adoption can start with a single repository and then be rolled out organization‑wide via shared CI templates.

**Production readiness**  
SkyWalking‑Eyes scores high on readiness: it has recent activity (last commit 2026‑07‑13), a healthy community (312 ★, 69 forks), and is written in Go, a language with strong tooling support. The project is already used in several Apache and downstream projects, indicating real‑world validation. While a final review of licensing, security posture, and maintainer responsiveness is advisable, the existing signals suggest the tool is mature enough for a pilot in production environments and can be safely promoted to a standard part of the development pipeline.

### Русский

**apache/skywalking-eyes** — это многофункциональный инструмент на Go для автоматической проверки и исправления заголовков лицензий, а также анализа лицензий зависимостей. Он позволяет интегрировать проверку лицензий в локальные скрипты, CI‑pipeline и ревью‑процессы, тем самым ускоряя рабочие циклы разработчиков и повышая качество обратной связи в сборках. Проект имеет высокую готовность к продакшн: активные коммиты, более 300 звёзд, широкое принятие в сообществе и стабильный набор API/CLI, что делает его надёжным выбором для пилотного внедрения в любой Go‑ориентированной инфраструктуре.

### 中文

**项目简介**  
Apache SkyWalking‑Eyes 是一款功能完整的开源许可证工具，能够自动检查和修复源码文件的许可证头，并解析项目依赖的许可证信息。  

**价值**  
- **节省时间**：在日常编码、代码审查以及合并请求（PR）阶段自动校验许可证，避免手工检查的重复工作。  
- **提升质量**：统一许可证声明，防止因许可证不一致导致的合规风险；在 CI 中即时反馈，帮助团队在代码进入主分支前修正问题。  
- **自动化**：支持 CLI、API 与 SDK，能够轻松嵌入本地开发脚本、Makefile 或 CI/CD 流水线，实现“一键检查/修复”。  

**典型接入方式**  
1. **本地开发**：在项目根目录下执行 `eyes`（或 `eyes-cli`）命令，自动扫描源码并在发现缺失或错误的许可证头时进行修复。  
2. **CI/CD 集成**：在 CI 脚本（如 GitHub Actions、GitLab CI、Jenkins 等）中添加步骤  
   ```yaml
   - name: Check license headers
     run: eyes check --path ./src
   - name: Fix license headers (optional)
     if: failure()
     run: eyes fix --path ./src
   ```  
   通过返回码即可让构建在许可证不合规时直接失败。  
3. **作为库使用**：项目提供 Go SDK，开发者可以在自定义工具或内部平台中调用 `eyes` 的核心 API，实现更细粒度的许可证分析与报告。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑07‑13，星标 312、Fork 69，社区活跃，Issue 与 PR 响应及时。  
- **技术成熟度**：核心实现使用 Go，具备跨平台二进制发布，易于在容器或裸机环境部署。  
- **安全与合规**：项目已通过 Apache 基金会治理，许可证为 Apache‑2.0，符合企业开源合规要求。  
- **风险**：暂无重大安全漏洞报告，但仍建议在正式生产环境前进行一次内部安全审计，并确认维护者活跃度。  

综合来看，Apache SkyWalking‑Eyes 已具备较高的生产就绪度，适合作为代码库许可证管理的标准化工具在企业内部推广使用。

## 🧭 Practical evaluation

**Value:** apache/skywalking-eyes helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 312 GitHub stars
- 69 forks
- updated 2026-07-13
- primary language: Go
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 46/100 |
| stars | 53/100 |
| topics | 50/100 |
| outlook | 78/100 |
| quality | 71/100 |
| recency | 100/100 |
| adoption | 51/100 |
| production | 75/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/apache/skywalking-eyes) · [← Back to DevTools](./README.md)</sub>
