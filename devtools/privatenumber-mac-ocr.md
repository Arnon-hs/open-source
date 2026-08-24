# privatenumber/mac-ocr

[![Stars](https://img.shields.io/github/stars/privatenumber/mac-ocr?style=flat-square&color=yellow)](https://github.com/privatenumber/mac-ocr/stargazers) [![Forks](https://img.shields.io/github/forks/privatenumber/mac-ocr?style=flat-square&color=blue)](https://github.com/privatenumber/mac-ocr/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> macOS CLI for OCR and searchable PDFs using Apple's Vision framework

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 419 |
| 🍴 **Forks** | 19 |
| 💻 **Language** | Swift |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`apple-vision` `cli` `command-line-tool` `image-to-text` `macos` `nodejs` `ocr` `pdf` `searchable-pdf` `swift` `text-recognition` `vision-framework`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*privatenumber/mac‑ocr* is a macOS command‑line tool that leverages Apple’s Vision framework to perform OCR on images and generate searchable PDFs. Written in Swift, it offers a simple CLI that can be dropped into local development workflows or CI pipelines to automate text extraction without needing external services. With active maintenance, 419 ★ on GitHub and recent updates, it’s a ready‑to‑use OSS component for macOS‑centric teams.

**Value**  
- **Time savings:** Engineers can convert screenshots, logs, or generated diagrams into searchable PDFs in a single command, eliminating manual copy‑paste or third‑party web services.  
- **Workflow automation:** The CLI can be scripted into pre‑commit hooks, test runners, or CI jobs to automatically produce searchable artifacts, improving code‑review and documentation cycles.  
- **Local, privacy‑first processing:** All OCR runs on the developer’s machine using Apple’s built‑in Vision framework, keeping proprietary data off the cloud.

**Practical Adoption Path**  
1. **Install** the binary via Homebrew (`brew install privatenumber/mac-ocr`) or build from source (Swift 5.9+).  
2. **Integrate** the `mac-ocr` command into existing scripts (e.g., `mac-ocr input.png -o output.pdf`).  
3. **Add to CI:** Include the binary in your macOS runner image and invoke it in a build step to generate searchable PDFs for test artifacts or documentation bundles.  
4. **Optional enhancements:** Wrap the CLI in a small shell or Makefile target to standardize options across the team.

**Production Readiness**  
- **Activity & community:** Recent commit (2026‑06‑22), 419 stars, 19 forks, and 12 relevant topics indicate healthy interest and ongoing maintenance.  
- **Stability:** Built on Apple’s native Vision SDK, which is mature and well‑supported on macOS; no external dependencies.  
- **Risk considerations:** License (MIT‑style) appears permissive, but a final legal review is recommended. Security posture is low‑risk given the local execution model, though a quick audit of the Swift codebase is advisable. Overall, the project is mature enough for a pilot in production environments, especially for teams already standardizing on macOS development machines.

### Русский

**privatenumber/mac-ocr** — это CLI‑утилита для macOS, позволяющая быстро преобразовывать изображения в OCR‑текст и создавать поисковые PDF с помощью встроенного фреймворка Apple Vision. Она отлично вписывается в ежедневные разработки: автоматизирует локальные задачи (например, генерацию документации из скриншотов) и ускоряет обратную связь в CI, экономя время инженеров. Проект имеет высокий уровень готовности к production — активные коммиты, 419 звёзд, поддержка Swift и открытый API, что делает его надёжным кандидатом для пилотного внедрения.

### 中文

**项目简介**  
privatenumber/mac-ocr 是一款基于 Apple Vision 框架的 macOS 命令行工具，能够快速对本地图片进行 OCR 识别并生成可搜索的 PDF。它使用 Swift 编写，轻量且无需额外依赖，适合在本地或 CI 环境中直接调用。

**价值**  
- **提升开发效率**：在代码评审、文档整理或日志截图等日常工作中，一键将图片转为可搜索的 PDF，省去手动复制粘贴的时间。  
- **自动化工程任务**：可在脚本或 CI 流水线中调用，实现批量 OCR、文档归档或错误日志的自动索引。  
- **改进 CI 反馈**：CI 运行后自动生成的可搜索 PDF 可直接附加到构建报告或审查页面，帮助团队快速定位问题。

**典型接入方式**  
1. **CLI 直接调用**：`mac-ocr input.png -o output.pdf`  
2. **脚本包装**：在 Bash、Zsh、Makefile 或 Xcode Build Phase 中嵌入上述命令，实现批量处理。  
3. **CI 集成**：在 GitHub Actions、GitLab CI、Jenkins 等流水线中添加步骤，使用 `mac-ocr` 对构建产出的截图或报告进行 OCR，随后上传生成的 PDF 作为构件或注释。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑22 最近一次提交，拥有 419 ★、19 Fork，且持续接受 Issue 与 PR。  
- **技术成熟**：依托 Apple 官方的 Vision 框架，提供稳定的 OCR 引擎，语言为 Swift，兼容 macOS 12+。  
- **生态兼容**：仅需 macOS 环境，无需额外库，易于在本地机器或 macOS Runner 上部署。  
- **风险**：许可证、长期维护者状态以及安全审计仍需进一步确认，但当前信号表明已具备在内部或受控生产环境中试点的条件。  

总体而言，privatenumber/mac-ocr 是一个即插即用、适合开发者日常和 CI 自动化的 OCR 解决方案，具备较高的生产可用性，值得在工程流程中进行评估和试点。

## 🧭 Practical evaluation

**Value:** privatenumber/mac-ocr helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 419 GitHub stars
- 19 forks
- updated 2026-06-22
- primary language: Swift
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 33/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 64/100 |
| quality | 62/100 |
| recency | 40/100 |
| adoption | 49/100 |
| production | 56/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/privatenumber/mac-ocr) · [← Back to DevTools](./README.md)</sub>
