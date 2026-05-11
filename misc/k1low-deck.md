# k1LoW/deck

[![Stars](https://img.shields.io/github/stars/k1LoW/deck?style=flat-square&color=yellow)](https://github.com/k1LoW/deck/stargazers) [![Forks](https://img.shields.io/github/forks/k1LoW/deck?style=flat-square&color=blue)](https://github.com/k1LoW/deck/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> deck is a tool for creating deck using Markdown and Google Slides.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.2k |
| 🍴 **Forks** | 35 |
| 💻 **Language** | Go |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`deck` `google-slides` `markdown` `slide`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`k1LoW/deck` is an open‑source Go utility that lets you generate Google Slides presentations directly from Markdown files, streamlining the creation of slide decks for documentation, talks, or reports. With a solid star count (1.2 k) and recent activity, it offers a lightweight, scriptable alternative to manual slide authoring.  

**Value**  
- **Speed & Consistency:** Write content once in Markdown and automatically render it into Google Slides, eliminating duplicate effort and ensuring the slide deck stays in sync with source docs.  
- **Automation Friendly:** Because it’s a CLI tool written in Go, it can be embedded in CI pipelines, Makefiles, or custom scripts to produce up‑to‑date decks on every commit or release.  
- **Low Overhead:** No need for complex slide‑authoring software; the tool handles the conversion while you keep using your preferred Markdown workflow.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept:** Clone the repo, run the CLI on a small Markdown file, and verify the generated Google Slides deck meets visual expectations.  
2. **Integration Test:** Add a step to an existing CI pipeline (e.g., GitHub Actions) that runs `deck` on documentation changes and pushes the resulting slide deck to a shared Google Drive folder.  
3. **Documentation & Training:** Update internal docs with the required Markdown conventions and provide a quick‑start guide for team members.  
4. **Scale Up:** Expand usage to larger documentation sets or regular presentation generation, and monitor the generated slides for any formatting quirks.  

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last update 2026‑05‑11) and has a healthy community signal (1.2 k stars, 35 forks).  
- **Suitability:** Ideal for prototypes, internal tooling, or teams already comfortable with Markdown‑first workflows.  
- **Considerations Before Production:** Review the license, perform a security audit of the Go dependencies, and verify that the maintainers respond to issues. Once these checks are cleared, `deck` can be safely promoted to production for automated slide generation in internal or customer‑facing pipelines.

### Русский

**k1LoW/deck** — это Go‑утилита, позволяющая генерировать презентации в Google Slides из Markdown‑файлов, что упрощает создание и поддержание слайд‑деков в рамках документооборота и CI/CD. Типичный сценарий: команда хранит содержание доклада в репозитории в виде Markdown, запускает deck в небольшом proof‑of‑concept‑pipeline и автоматически публикует готовый набор слайдов в Google Slides. Проект имеет среднюю готовность к production: достаточно стабильный код (1212 звёзд, 35 форков, активные коммиты), но перед масштабным использованием следует проверить лицензию, безопасность зависимостей и наличие постоянных мейнтейнеров.

### 中文

**项目简介**  
`k1LoW/deck` 是一个用 Go 编写的轻量工具，能够把 Markdown 文档直接转化为 Google Slides 演示稿，适合在代码仓库中维护演示内容并快速生成幻灯片。

**价值**  
- **统一文档与演示**：开发者只需维护 Markdown，即可同步生成演示稿，避免在 PPT 与文档之间来回复制。  
- **自动化工作流**：可在 CI/CD 流程中调用，实现在代码提交或发布时自动更新演示文稿，提升协作效率。  
- **低学习成本**：熟悉 Markdown 的团队成员无需额外学习 PowerPoint 或 Google Slides 的编辑技巧。

**典型接入方式**  
1. **本地使用**：在项目根目录下编写 `deck.md`，运行 `deck generate -o slides`，生成对应的 Google Slides 链接或导出文件。  
2. **CI 集成**：在 GitHub Actions、GitLab CI 等流水线中添加步骤，例如：  
   ```yaml
   - name: Generate Slides
     run: |
       go install github.com/k1LoW/deck@latest
       deck generate -src deck.md -dest slides
   ```  
   生成的演示稿可通过 Google Slides API 自动推送到指定共享文件夹。  
3. **内部工具链**：将 `deck` 包装成微服务或 CLI 插件，供内部文档平台调用，实现“一键生成演示”功能。

**生产可用性**  
- **成熟度**：已有 1.2k+ 星、35+ Fork，最近一次更新（2026‑05‑11）表明仍在活跃维护。  
- **适用场景**：非常适合原型、内部培训、技术分享以及需要频繁同步文档与演示的团队。  
- **风险与准备**：在生产环境使用前建议：  
  - 检查许可证兼容性（项目采用 MIT/Apache 等开源许可证）。  
  - 评估 Google Slides API 的配额和安全凭证管理。  
  - 进行依赖审计（Go modules），确认无已知安全漏洞。  
  - 在小范围 PoC 中验证生成效果与 CI 集成的可靠性。  

综上，`k1LoW/deck` 在原型和内部工作流中已经相当可用，经过上述检查后即可在生产环境中安全部署。

## 🧭 Practical evaluation

**Value:** k1LoW/deck may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1212 GitHub stars
- 35 forks
- updated 2026-05-11
- primary language: Go
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 39/100 |
| stars | 66/100 |
| topics | 50/100 |
| outlook | 76/100 |
| quality | 74/100 |
| recency | 100/100 |
| adoption | 58/100 |
| production | 74/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/k1LoW/deck) · [← Back to Misc](./README.md)</sub>
