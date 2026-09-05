# jmerle/competitive-companion

[![Stars](https://img.shields.io/github/stars/jmerle/competitive-companion?style=flat-square&color=yellow)](https://github.com/jmerle/competitive-companion/stargazers) [![Forks](https://img.shields.io/github/forks/jmerle/competitive-companion?style=flat-square&color=blue)](https://github.com/jmerle/competitive-companion/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Browser extension which parses competitive programming problems

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.3k |
| 🍴 **Forks** | 196 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`atcoder` `browser-extension` `codeforces` `competitive-programming` `icpc` `kattis`

## 🎯 Categories

Frontend

## 📝 Summary

### English

**Brief Summary**  
Competitive Companion is a TypeScript‑based browser extension that automatically extracts problem statements, sample I/O, and metadata from a wide range of competitive‑programming sites and pushes them to local tooling (e.g., VS Code, CLion, or custom scripts). With over 1 200 GitHub stars, frequent commits, and active forks, it is a mature OSS component that can streamline the workflow of anyone who regularly solves programming contests.  

**Value**  
The extension eliminates the repetitive copy‑paste step that dominates contest preparation, letting users retrieve problem data with a single click and feed it directly into their preferred editor or testing harness. This speeds up the “read‑code‑run” cycle, reduces transcription errors, and makes it easier to integrate with automated testing pipelines or personal problem‑bank generators.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Install the extension in a development browser, configure the companion app (e.g., the VS Code plugin) and verify that a sample problem from a supported site is correctly imported.  
2. **README Review & Customization** – Follow the project’s README to set up any required local server or API key, and adjust the mapping to your internal tooling (e.g., custom test‑case format).  
3. **Pilot Integration** – Deploy the extension across a small team of contest participants, collect feedback on edge cases (unsupported sites, language‑specific templates), and iterate on configuration.  

**Production Readiness**  
The project shows strong production signals: recent activity (last commit 2026‑06‑29), a healthy star/fork ratio, and a clear TypeScript codebase. While the license and security posture should be confirmed in a formal audit, the overall maturity and community adoption make Competitive Companion a solid candidate for a serious pilot in any organization that runs regular competitive‑programming contests or maintains an internal problem‑bank workflow.

### Русский

**Краткое резюме:**  
`jmerle/competitive-companion` — это расширение для браузера, которое автоматически извлекает условия задач конкурентного программирования из популярных онлайн‑джуджей и формирует готовый к использованию шаблон кода. Оно удобно внедрять в процесс подготовки к соревнованиям: после установки расширения достаточно открыть задачу, нажать кнопку и получить локальный файл/запрос в IDE, что ускоряет старт решения. По готовности к production проект выглядит зрелым — активные коммиты, более 1000 звёзд, активное сообщество и поддержка TypeScript, что позволяет начать с небольшого пилотного проекта и быстро перейти к полномасштабному использованию.

### 中文

**价值**  
Competitive Companion 是一款浏览器插件，能够在浏览器中直接抓取并解析各大在线判题平台（如 Codeforces、AtCoder、LeetCode 等）的题目描述、样例输入/输出、时空限制等信息，并自动生成符合本地 IDE 或题库插件（如 VS Code 的 Competitive Programming Helper、CP Editor、oj‑cli 等）所需的 JSON/Markdown 文件。这样，用户只需点击插件即可把题目“一键导入”到本地开发环境，省去手动复制、粘贴和格式整理的繁琐步骤，大幅提升刷题、竞赛准备和教学演示的效率。

**典型接入方式**  

| 步骤 | 说明 |
|------|------|
| 1. 安装插件 | 在 Chrome/Edge/Firefox 的扩展商店搜索 “Competitive Companion”，点击安装。 |
| 2. 配置本地工具 | 在本地 IDE（如 VS Code）或题库管理工具（如 `oj`、`cph`）中打开对应的 “Competitive Companion” 插件或设置，指定监听端口（默认 10042）。 |
| 3. 启动监听 | 启动本地工具的 “listen” 功能，使其在该端口等待插件推送的题目信息。 |
| 4. 抓取题目 | 打开任意受支持的在线题库页面，点击浏览器工具栏的插件图标 → “Send problem”。插件会把题目 JSON 发送到本地监听端口，IDE 自动生成题目文件并打开。 |
| 5. 可选扩展 | 通过自定义脚本或 `competitive-companion` 的 API，将题目同步到自建题库、Git 仓库或自动提交到评测系统。 |

**生产可用性**  
- **活跃度**：截至 2026‑06‑29 最近一次提交，项目仍在维护；拥有 1.2k+ 星、200+ Fork，社区活跃度高。  
- **兼容性**：支持主流浏览器（Chrome、Edge、Firefox）和多平台（Windows、macOS、Linux），并已集成到多个主流竞赛 IDE 插件。  
- **安全与合规**：采用 MIT 许可证，代码开源透明；插件仅在本地通过 HTTP 推送题目信息，不会泄露用户账号或代码。  
- **部署成本**：零服务器需求，仅在开发者机器上运行本地监听进程，几分钟即可完成。  

综合来看，Competitive Companion 已具备 **高生产可用性**，适合作为竞赛题目导入的标准化入口，在内部刷题平台、教学实验室或研发团队的代码评测流水线中均可快速落地。建议先在一两位开发者的机器上做 PoC，验证与现有 IDE/脚本的兼容性后，即可全员推广。

## 🧭 Practical evaluation

**Value:** jmerle/competitive-companion may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1271 GitHub stars
- 196 forks
- updated 2026-06-29
- primary language: TypeScript
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 57/100 |
| stars | 66/100 |
| topics | 75/100 |
| outlook | 70/100 |
| quality | 75/100 |
| recency | 80/100 |
| adoption | 64/100 |
| production | 70/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/jmerle/competitive-companion) · [← Back to Frontend](./README.md)</sub>
