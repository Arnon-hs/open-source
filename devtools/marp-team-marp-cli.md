# marp-team/marp-cli

[![Stars](https://img.shields.io/github/stars/marp-team/marp-cli?style=flat-square&color=yellow)](https://github.com/marp-team/marp-cli/stargazers) [![Forks](https://img.shields.io/github/forks/marp-team/marp-cli?style=flat-square&color=blue)](https://github.com/marp-team/marp-cli/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> A CLI interface for Marp and Marpit based converters

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.7k |
| 🍴 **Forks** | 188 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-07-04 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `deck` `markdown` `marp` `marpit` `presentation` `slides`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Summary**  
marp‑team/marp‑cli is a TypeScript‑based command‑line tool that powers Marp and Marpit slide‑deck conversions, letting developers generate HTML, PDF, PPTX and image outputs directly from Markdown. With 3.6 k stars, frequent releases (last update 2026‑07‑04) and solid ecosystem adoption, it is positioned as a high‑readiness OSS component for automating presentation builds in CI/CD pipelines and local workflows.

**Value**  
The CLI compresses the “write‑markdown‑→‑render‑slides” loop into a single command, eliminating manual export steps and enabling scripts that produce consistent slide artifacts on every commit. This speeds up daily development, reduces context‑switching, and delivers immediate visual feedback in pull‑request checks, helping teams iterate faster and keep documentation in sync with code.

**Practical adoption path**  
1. **Local trial** – Install via npm (`npm i -g @marp-team/marp-cli`) and run `marp slide.md -o slide.pdf` to verify output quality.  
2. **Script integration** – Add the CLI to project `package.json` scripts (e.g., `"build:slides": "marp src/**/*.md -o dist/slides"`).  
3. **CI/CD rollout** – Include the script in CI pipelines (GitHub Actions, GitLab CI, Jenkins) to generate PDFs/HTML on each push and publish them as artifacts or comments.  
4. **Policy review** – Confirm the MIT license, run a security scan (e.g., Snyk) and ensure maintainers remain active before promoting to production.

**Production readiness**  
The project shows high production readiness: recent commits, active issue handling, a large star/fork base, and a clear TypeScript codebase. While no critical licensing or security red flags have been identified, a final audit of the MIT license compliance and a quick dependency vulnerability scan are recommended before committing to a long‑term pilot.

### Русский

marp-team/marp-cli — это CLI‑утилита для конвертации презентаций на базе Marp и Marpit, позволяющая инженерам быстро генерировать слайды из Markdown и интегрировать их в CI/CD‑конвейеры. Типичный сценарий — автоматизация локального построения презентаций и предоставление мгновенной обратной связи в pull‑request‑проверках, что ускоряет рабочие циклы разработки и ревью. Проект имеет высокий уровень готовности к production: активные коммиты, более 3 800 звёзд, широкое принятие в сообществе и поддержка TypeScript, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**Marp-cli简介**

marp-team/marp-cli 是 Marp 和 Marpit 基于的 CLI 接口，旨在帮助开发者节省在日常开发和审查循环中的时间。

**价值**

marp-team/marp-cli 帮助开发者在开发工作流中节省时间，自动化本地工程任务，并改善 CI 反馈。

**典型接入方式**

marp-team/marp-cli 可以通过以下方式接入：
- 加快开发者工作流的速度
- 自动化本地工程任务
- 改善 CI 反馈

**生产可用性**

marp-team/marp-cli 已经接近生产就绪，主要原因是：
- 有强烈的最近活动迹象
- 有足够的采用和生态系统信号
- 有高的质量信号（3680 个 GitHub 星标）

但是，需要进一步检查以下风险：
- 许可证风险
- 安全防御风险
- 主维护者风险

## 🧭 Practical evaluation

**Value:** marp-team/marp-cli helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3680 GitHub stars
- 188 forks
- updated 2026-07-04
- primary language: TypeScript
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 57/100 |
| stars | 76/100 |
| topics | 88/100 |
| outlook | 83/100 |
| quality | 85/100 |
| recency | 100/100 |
| adoption | 71/100 |
| production | 80/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-04 · [View on GitHub](https://github.com/marp-team/marp-cli) · [← Back to DevTools](./README.md)</sub>
