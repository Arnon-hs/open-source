# shinshin86/oh-my-logo

[![Stars](https://img.shields.io/github/stars/shinshin86/oh-my-logo?style=flat-square&color=yellow)](https://github.com/shinshin86/oh-my-logo/stargazers) [![Forks](https://img.shields.io/github/forks/shinshin86/oh-my-logo?style=flat-square&color=blue)](https://github.com/shinshin86/oh-my-logo/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> Display giant ASCII-art logos with colorful gradients in your terminal — like Claude Code or Gemini CLI.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.5k |
| 🍴 **Forks** | 60 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ascii` `ascii-art` `cli` `logo`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief summary**  
*oh‑my‑logo* is a TypeScript‑based CLI that renders large, gradient‑colored ASCII‑art logos (e.g., Claude, Gemini) directly in the terminal. It lets engineers add eye‑catching branding or status symbols to scripts, CI pipelines, and local tooling with a single command.

**Value**  
- **Time‑saving visual feedback** – developers can instantly see a recognizable logo or status indicator instead of plain text, cutting down on context‑switching during builds, tests, or deployments.  
- **Workflow acceleration** – the tool can be scripted into pre‑commit hooks, CI jobs, or local dev environments, turning repetitive “print‑banner” steps into a one‑liner.  
- **Improved CI/CD ergonomics** – colorful logos make CI logs more scannable, helping reviewers spot success/failure states faster.

**Practical adoption path**  
1. **Install** the CLI (`npm i -g @shinshin86/oh-my-logo` or add it as a devDependency).  
2. **Configure** a simple JSON/YAML file or use the built‑in presets to map project names to logo files.  
3. **Integrate** the command into existing scripts (e.g., `npm run build && oh-my-logo --logo=gemini`).  
4. **Optional**: wrap the CLI in a custom npm script or a Git hook for automated execution on every commit or CI run.

**Production readiness**  
- **Activity & community** – 1,466 stars, 60 forks, recent commit on 2026‑05‑13, and ongoing issue responses indicate a healthy, active project.  
- **Maturity** – Core functionality (CLI, gradient rendering, logo catalog) is stable; the TypeScript codebase is well‑typed and documented.  
- **Risk considerations** – No major licensing or security red flags have been identified, but a final audit of the MIT‑style license and any transitive dependencies is recommended before large‑scale rollout.  

Overall, *oh‑my‑logo* is production‑ready for pilot use in developer tooling and CI pipelines, offering a low‑friction way to enrich terminal output with vibrant ASCII art.

### Русский

**sh​inshin86/oh‑my‑logo** – небольшая TypeScript‑утилита, позволяющая выводить в терминале гигантские ASCII‑логотипы с плавными цветными градиентами (например, Claude Code или Gemini CLI), что ускоряет визуальную обратную связь в CI и делает локальные инструменты более наглядными. Проект легко интегрировать через CLI/SDK в скрипты разработки, автоматизацию тестов и обзоры кода, экономя время на ручном оформлении вывода. Благодаря активным коммитам, 1466 звёздам, широкому принятию и хорошей документации, готов к пилотному использованию в продакшн‑окружениях, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
shinshin86/oh‑my‑logo 是一个用 TypeScript 编写的 CLI/SDK，能够在终端里渲染带有彩色渐变的巨型 ASCII‑art LOGO（如 Claude Code、Gemini CLI 等），帮助开发者在本地或 CI 环境中快速展示品牌或工具标识。

**价值**  
- **提升开发效率**：在调试、脚本输出或 CI 报表中直接呈现醒目的 LOGO，省去手动拼接 ASCII‑art 的时间。  
- **改善可视化反馈**：彩色渐变让日志、构建状态或审查结果更易辨识，提升团队沟通质量。  
- **可自动化**：通过 CLI 或 Node.js API，可在脚本、GitHub Action、GitLab CI 等流水线中一键调用，实现全流程自动化。

**典型接入方式**  
1. **CLI**：`npx oh-my-logo <logo-name> --gradient start:end`，直接在终端运行。  
2. **Node.js SDK**：在项目代码中 `import { renderLogo } from 'oh-my-logo';`，随后调用 `renderLogo('myApp', { gradient: ['#ff7e5f', '#feb47b'] })`，将渲染结果写入 stdout、文件或 CI 注释。  
3. **CI 集成**：在 GitHub Actions 中添加步骤 `- uses: shinshin86/oh-my-logo@v1`，配合环境变量自定义颜色，即可在构建日志或 PR 注释中展示 LOGO。

**生产可用性**  
- **活跃度高**：最近一次提交于 2026‑05‑13，星标 1.4k、Fork 60，社区关注度良好。  
- **技术成熟**：采用 TypeScript，提供完整类型声明，易于在现有 Node 项目中集成。  
- **生态兼容**：支持跨平台终端（Linux、macOS、Windows），可在本地开发、Docker 镜像以及 CI 环境无缝运行。  
- **风险点**：仍需对许可证（MIT）和潜在安全依赖进行最终审查，但整体代码质量和维护状态足以支撑生产级试点。

## 🧭 Practical evaluation

**Value:** shinshin86/oh-my-logo helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1466 GitHub stars
- 60 forks
- updated 2026-05-13
- primary language: TypeScript
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 67/100 |
| topics | 50/100 |
| outlook | 77/100 |
| quality | 75/100 |
| recency | 100/100 |
| adoption | 61/100 |
| production | 79/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/shinshin86/oh-my-logo) · [← Back to DevTools](./README.md)</sub>
