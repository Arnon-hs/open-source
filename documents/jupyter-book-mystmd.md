# jupyter-book/mystmd

[![Stars](https://img.shields.io/github/stars/jupyter-book/mystmd?style=flat-square&color=yellow)](https://github.com/jupyter-book/mystmd/stargazers) [![Forks](https://img.shields.io/github/forks/jupyter-book/mystmd?style=flat-square&color=blue)](https://github.com/jupyter-book/mystmd/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Command line tools for working with MyST Markdown.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 507 |
| 🍴 **Forks** | 163 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`javascript-parser` `markdown-it` `myst` `myst-markdown` `myst-parser` `unifiedjs`

## 🎯 Categories

Documents

## 📝 Summary

### English

Here's a brief summary of the project:

jupyter-book/mystmd is an open-source project that provides command line tools for working with MyST Markdown. Its value proposition lies in its potential to streamline workflow when its documentation and activity align with specific use cases. The project's practical adoption path involves evaluating a small proof of concept and reviewing its README, followed by a thorough review of its license, security posture, and maintainers.

In terms of production readiness, jupyter-book/mystmd is considered high for an open-source candidate, with recent activity, adoption, and strong ecosystem signals. This suggests that the project is well-maintained and has a growing community of users, making it a viable option for serious pilots.

### Русский

**Краткое резюме:**  
`jupyter-book/mystmd` — это набор CLI‑утилит для работы с MyST‑Markdown, позволяющий быстро конвертировать, проверять и публиковать документы в формате, совместимом с Jupyter Book и другими научными платформами. Типичный сценарий внедрения — интеграция в CI/CD пайплайн: на этапе сборки проект проверяет синтаксис и генерирует статический сайт/документацию, после чего артефакты автоматически деплоятся. По готовности к production проект выглядит зрелым: активные коммиты, более 500 звёзд, широкое использование в сообществе и поддержка TypeScript, что делает его надёжным кандидатом для пилотного внедрения после небольшого proof‑of‑concept и проверки лицензии.

### 中文

**项目简介**  
`jupyter-book/mystmd` 是一套基于 TypeScript 的命令行工具，专门用于创建、转换和渲染 MyST（Markedly Structured) Markdown。它能够把 MyST 文档快速编译成 Jupyter Book、Sphinx、HTML、PDF 等多种格式，帮助科研、教学和技术文档团队在 Jupyter 生态中实现统一的文档工作流。

**价值**  
- **统一文档格式**：通过 MyST 语法在 Markdown 中直接使用 Sphinx 指令和 Jupyter 代码单元，实现“文档即代码”。  
- **高效构建**：一条 CLI 命令即可完成编译、链接检查和多格式输出，适配 CI/CD 流水线。  
- **生态兼容**：与 Jupyter Book、Sphinx、nbconvert 等工具天然集成，降低学习成本并提升团队协作效率。

**典型接入方式**  
1. **本地快速试用**：`npm i -g mystmd` → 在项目根目录运行 `myst build .` 生成 HTML/PDF。  
2. **CI/CD 集成**：在 GitHub Actions、GitLab CI 或 Azure Pipelines 中添加步骤：  
   ```yaml
   - name: Install mystmd
     run: npm i -g mystmd
   - name: Build docs
     run: myst build docs/ --output-dir public/
   ```  
   生成的 `public/` 目录可直接部署到 GitHub Pages、Read the Docs 等平台。  
3. **与 Jupyter Book 组合**：在 `jupyter-book/_config.yml` 中声明 `myst_parser`，随后使用 `jupyter-book build` 调用 mystmd 完成完整书籍的构建。

**生产可用性**  
- **活跃度**：最近一次提交（2026‑07‑06）且持续接受 PR，社区活跃。  
- **采用情况**：已有 500+ ⭐、160+ Fork，多个科研组织和教育机构在生产环境中使用。  
- **技术成熟度**：基于 TypeScript 实现，提供完整的类型声明和错误提示，易于在企业内部进行二次包装。  
- **风险**：目前未发现重大许可证或安全隐患，但建议在正式投产前完成一次依赖审计并确认维护者的响应速度。  

综合来看，`jupyter-book/mystmd` 已具备高生产就绪度，适合作为文档自动化流水线的核心组件，先在小范围（如单个项目的文档构建）进行 PoC 验证，随后逐步推广到全组织的文档标准化流程中。

## 🧭 Practical evaluation

**Value:** jupyter-book/mystmd may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 507 GitHub stars
- 163 forks
- updated 2026-07-06
- primary language: TypeScript
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 55/100 |
| stars | 58/100 |
| topics | 75/100 |
| outlook | 71/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 57/100 |
| production | 69/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/jupyter-book/mystmd) · [← Back to Documents](./README.md)</sub>
