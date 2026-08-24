# hugovk/norwegianblue

[![Stars](https://img.shields.io/github/stars/hugovk/norwegianblue?style=flat-square&color=yellow)](https://github.com/hugovk/norwegianblue/stargazers) [![Forks](https://img.shields.io/github/forks/hugovk/norwegianblue?style=flat-square&color=blue)](https://github.com/hugovk/norwegianblue/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> CLI to show end-of-life dates

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 144 |
| 🍴 **Forks** | 9 |
| 💻 **Language** | Python |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `end-of-life` `eol` `hacktoberfest` `python` `python3`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Summary**  
hugovk/norwegianblue is a Python‑based CLI that instantly reports the end‑of‑life dates for popular software packages, letting engineers spot deprecated dependencies before they break builds. With 144 stars, recent commits (as of 2026‑06‑24), and a clean, single‑binary interface, it fits naturally into local dev environments and CI pipelines.

**Value**  
By surfacing EOL information on demand, the tool eliminates manual version look‑ups, shortens the feedback loop in code reviews, and reduces the risk of runtime failures caused by unsupported libraries. This translates into faster iteration cycles, fewer emergency patches, and more predictable release schedules.

**Adoption path**  
1. **Local setup** – Install via `pip install norwegianblue` and add the `norwegianblue` command to developers’ shell profiles.  
2. **CI integration** – Include a step such as `norwegianblue check requirements.txt` in build scripts; fail the job if any listed dependency is past its EOL date.  
3. **Automation** – Wrap the CLI in a pre‑commit hook or a GitHub Action to enforce continuous compliance across the team.

**Production readiness**  
The project shows strong OSS maturity signals: recent activity, a modest but active contributor base, clear Python implementation, and well‑defined CLI semantics. While a final review of licensing and security (e.g., dependency audits) is still required, the overall health and community traction make it a safe candidate for pilot deployment in production‑grade workflows.

### Русский

**NorwegianBlue** — это удобный CLI‑инструмент на Python, который быстро выводит даты окончания поддержки (EOL) для различных технологий, позволяя инженерам сразу видеть, какие зависимости требуют обновления. Его типичное применение — автоматизация проверок в локальных скриптах и CI‑pipeline: один вызов команды возвращает актуальные даты EOL, что ускоряет рабочие циклы и повышает качество обратной связи в процессе разработки. Проект считается почти готовым к production: активные коммиты, 144 звёзды, поддержка сообществом и ясный API/CLI делают его надёжным кандидатом для пилотного внедрения.

### 中文

**项目简介**  
`hugovk/norwegianblue` 是一个基于 Python 的命令行工具，用于快速查询各类软件或库的 **EOL（End‑of‑Life）日期**，帮助开发者在日常开发和代码审查时避免使用即将停止维护的依赖。

**价值**  
- **节省时间**：一条命令即可获取组件的生命周期信息，省去在文档或官网上手动查找的过程。  
- **提升工作流**：可在本地脚本、CI/CD 流水线或代码审查工具中自动化检查，提前发现即将淘汰的依赖，降低技术债务风险。  
- **增强反馈**：在 CI 中集成后，构建失败或警告信息会直接指出过期依赖，帮助团队保持依赖的健康状态。

**典型接入方式**  
1. **本地 CLI**：直接在终端运行 `norwegianblue <package>` 查询单个包的 EOL 信息。  
2. **脚本/自动化**：在 Bash、PowerShell 或 Python 脚本中调用 `norwegianblue`，将结果解析为 JSON（`--json`）后用于自定义报告或依赖审计。  
3. **CI 集成**：在 GitHub Actions、GitLab CI、Jenkins 等流水线中添加一步，例如：  
   ```yaml
   - name: Check EOL of dependencies
     run: |
       pip install norwegianblue
       norwegianblue -r requirements.txt --json > eol-report.json
       # 根据报告决定是否阻止合并
   ```

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑24，星标 144，Fork 9，表明社区仍在使用和维护。  
- **技术成熟度**：实现简洁、仅依赖标准库和少量 HTTP 请求，易于审计和二次封装。  
- **风险**：暂无重大元数据风险，但在正式投入前仍需确认许可证兼容性、潜在的安全漏洞以及维护者的响应时效。总体而言，`norwegianblue` 已具备在生产环境中试点使用的条件。

## 🧭 Practical evaluation

**Value:** hugovk/norwegianblue helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 144 GitHub stars
- 9 forks
- updated 2026-06-24
- primary language: Python
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 25/100 |
| stars | 46/100 |
| topics | 75/100 |
| outlook | 53/100 |
| quality | 54/100 |
| recency | 40/100 |
| adoption | 40/100 |
| production | 57/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/hugovk/norwegianblue) · [← Back to DevTools](./README.md)</sub>
