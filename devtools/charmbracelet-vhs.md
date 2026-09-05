# charmbracelet/vhs

[![Stars](https://img.shields.io/github/stars/charmbracelet/vhs?style=flat-square&color=yellow)](https://github.com/charmbracelet/vhs/stargazers) [![Forks](https://img.shields.io/github/forks/charmbracelet/vhs?style=flat-square&color=blue)](https://github.com/charmbracelet/vhs/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> Your CLI home video recorder 📼

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 20.2k |
| 🍴 **Forks** | 440 |
| 💻 **Language** | Go |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ascii` `cli` `command-line` `gif` `recording` `terminal` `vhs` `video`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Summary:** charmbracelet/vhs is an open-source CLI home video recorder that enables engineers to streamline their daily development and review loops, saving time and increasing productivity. By automating local engineering tasks and improving CI feedback, this tool offers a practical adoption path for developers seeking to enhance their workflows. With its high production readiness, strong adoption, and recent activity, charmbracelet/vhs is a serious candidate for pilot projects.

**Value:**

* Saves time in daily development and review loops
* Automates local engineering tasks
* Improves CI feedback

**Practical Adoption Path:**

1. Evaluate the tool's API/SDK/CLI signals to assess its implementation and integration potential.
2. Assess the tool's language metadata, focused topics, and topics to determine its relevance to your project.
3. Review the tool's recent activity, adoption, and ecosystem signals to gauge its production readiness.
4. Explore the tool's use cases, such as speeding up developer workflows and improving CI feedback, to determine its potential value in your project.

**Production Readiness:**

charmbracelet/vhs boasts a high production readiness score, indicating strong adoption (76/100) and recent activity (updated 2026-06-27). Its primary language is Go, and it has a

### Русский

Резюме проекта charmbracelet/vhs:

charmbracelet/vhs - это CLI-инструмент для автоматизации локальных задач инженеров, позволяющий ускорить разработку и облегчить отзывы. Программа особенно полезна для speed up разработчиков, автоматизации локальных задач и улучшения обратной связи в CI. charmbracelet/vhs готов к использованию в production, получив высокие оценки по критериям активности, приёма и экосистемы, а также высокую оценку готовности к production.

### 中文

**项目简介**  
`charmbracelet/vhs` 是一个用 Go 编写的 CLI 工具，能够把终端交互过程录制成 GIF/MP4 视频，帮助开发者快速生成演示、调试日志或 CI 报告。它的目标是让日常开发、代码评审和文档编写的“录屏”环节变得像执行普通命令一样简单。

**价值体现**  
- **提升工作流效率**：在本地或 CI 中只需一条命令即可捕获终端输出，省去手动截图、录屏再裁剪的时间。  
- **自动化工程任务**：可在脚本或 Makefile 中嵌入 VHS，生成可视化的运行报告，帮助审查者快速了解命令执行结果。  
- **改进 CI 反馈**：将生成的 GIF/MP4 嵌入 CI 报告或 PR 评论，使错误复现、性能基准等信息一目了然，缩短 Review 循环。

**典型接入方式**  
1. **直接使用 CLI**  
   ```bash
   # 录制一次交互并输出为 GIF
   vhs record "npm test" -o test.gif
   ```
2. **在脚本/Makefile 中调用**  
   ```make
   test:
       vhs record "go test ./..." -o test.gif
   ```
3. **CI 集成**（GitHub Actions、GitLab CI 等）  
   ```yaml
   steps:
     - uses: actions/checkout@v3
     - name: Install VHS
       run: go install github.com/charmbracelet/vhs@latest
     - name: Run tests and record
       run: vhs record "go test ./..." -o test.gif
     - name: Upload artifact
       uses: actions/upload-artifact@v3
       with:
         name: test-recording
         path: test.gif
   ```

**生产可用性**  
- **活跃度**：截至 2026‑06‑27 最近一次提交，拥有 20 001+ 星、440+ Fork，社区活跃。  
- **技术成熟度**：使用 Go 编写，单二进制文件，无运行时依赖，易于在各种环境（本地、容器、CI）部署。  
- **生态兼容**：提供标准 CLI 接口，可直接在脚本、Makefile、CI 配置中使用；兼容常见的 CI 平台（GitHub Actions、GitLab CI、CircleCI 等）。  
- **风险**：许可证和安全审计尚需最终确认，但从开源活跃度和维护者响应速度来看，已具备在生产环境进行试点的条件。

综上，`charmbracelet/vhs` 是一款轻量、易集成且社区成熟的终端录屏工具，能够显著加速开发、审查和 CI 反馈的可视化流程，适合作为日常工程自动化的一环投入生产使用。

## 🧭 Practical evaluation

**Value:** charmbracelet/vhs helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 20201 GitHub stars
- 440 forks
- updated 2026-06-27
- primary language: Go
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 66/100 |
| stars | 92/100 |
| topics | 100/100 |
| outlook | 81/100 |
| quality | 88/100 |
| recency | 80/100 |
| adoption | 84/100 |
| production | 77/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/charmbracelet/vhs) · [← Back to DevTools](./README.md)</sub>
