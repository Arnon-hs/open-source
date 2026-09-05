# r-lib/roxygen2

[![Stars](https://img.shields.io/github/stars/r-lib/roxygen2?style=flat-square&color=yellow)](https://github.com/r-lib/roxygen2/stargazers) [![Forks](https://img.shields.io/github/forks/r-lib/roxygen2?style=flat-square&color=blue)](https://github.com/r-lib/roxygen2/network) [![Language](https://img.shields.io/badge/lang-R-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Generate R package documentation from inline R comments

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 649 |
| 🍴 **Forks** | 237 |
| 💻 **Language** | R |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`devtools` `documentation` `r`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary**  
`r-lib/roxygen2` lets R developers generate package documentation directly from specially‑formatted comments placed alongside the code, eliminating the need to write separate Rd files. With a solid user base (≈ 650 ★, 237 forks) and recent activity, it fits well into workflows that already rely on the tidyverse ecosystem.

**Value**  
- **Speed & consistency** – Documentation stays close to the source, reducing drift and manual editing.  
- **Automation** – `roxygen2` integrates with `devtools`/`usethis` to rebuild docs on every build, streamlining CI pipelines.  
- **Community support** – Backed by the r‑lib organization, it benefits from frequent updates and extensive examples.

**Practical adoption path**  
1. **Prototype**: Add `roxygen2` to a development environment (`install.packages("roxygen2")`) and convert a small package by adding `#'` comments and running `devtools::document()`.  
2. **Validate**: Review the generated `.Rd` files and the `man/` directory to ensure the output matches your style guidelines.  
3. **Integrate**: Hook `roxygen2` into your CI (e.g., GitHub Actions) to run `R CMD check` after each commit, and update any custom scripts that previously edited Rd files manually.  
4. **Finalize**: Freeze the version in your `DESCRIPTION` file and add it to your dependency lockfile (e.g., `renv.lock`).

**Production readiness**  
- **Maturity**: Medium – widely used for prototypes and internal projects; stable core API but requires manual verification of generated docs before shipping.  
- **Dependencies**: Relies on `R` (≥ 3.5) and other r‑lib tools; ensure version compatibility with your CI environment.  
- **Maintenance**: Actively maintained (last commit 2026‑06‑25) with a responsive maintainer community, making it a safe choice for production after a short validation phase.  

Overall, `roxygen2` offers a high‑value, low‑friction way to keep R package documentation in sync with code, provided you allocate a brief onboarding sprint to confirm the generated output meets your project’s standards.

### Русский

**r-lib/roxygen2** — это популярный open‑source инструмент (≈650 звёзд) для автоматической генерации документации R‑пакетов из комментариев непосредственно в коде, что ускоряет поддержание актуальной справки и упрощает процесс публикации. Его обычно внедряют в пайплайн разработки R‑пакетов: после написания функций добавляют roxygen‑теги, а при сборке пакет автоматически получает готовый *.Rd*‑файлы и *.html*‑документацию. Готовность к production — средняя: проект стабилен и активно поддерживается, но интеграция требует ручной проверки конфигурации и зависимостей, поэтому перед широким использованием стоит протестировать настройку в прототипе или внутреннем проекте.

### 中文

**价值**  
roxygen2 能把源码中以 `#'` 开头的 R 注释直接转换为符合 **Rd**、**HTML** 与 **PDF** 格式的帮助文档，免除手写 `.Rd` 文件的繁琐工作。它与 **devtools**、**usethis**、**pkgdown** 等 r‑lib 生态工具天然兼容，能够在一次 `R CMD build` 或 `devtools::document()` 时自动生成完整的包文档，使得文档维护成本大幅下降，尤其适合快速迭代的科研原型或内部工具。

**典型接入方式**  

1. **在项目中加入依赖**  
   ```r
   usethis::use_package("roxygen2")
   ```
2. **在 R 脚本或函数前添加 roxygen 注释**（以 `#'` 开头），例如：  
   ```r
   #' Compute the mean of a numeric vector  
   #' @param x numeric vector  
   #' @return numeric mean  
   #' @export  
   my_mean <- function(x) mean(x, na.rm = TRUE)
   ```
3. **生成文档**  
   - 使用 **devtools**：`devtools::document()`  
   - 或直接调用 **roxygen2**：`roxygen2::roxygenise()`  
   这一步会在 `man/` 目录下生成对应的 `.Rd` 文件，并更新 NAMESPACE。
4. **（可选）配合 pkgdown**：`pkgdown::build_site()`，自动生成网页化文档站点。

**生产可用性**  

| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | ★★★★☆（Medium） | 发行版已稳定，社区活跃（>600 星、200+ Fork），且持续更新至 2026‑06‑25。 |
| **依赖管理** | ★★★☆☆ | 依赖 R (≥3.5) 与 roxygen2 本身的版本，需在 CI 中锁定版本以防突变。 |
| **集成成本** | ★★☆☆☆ | 元数据未提供完整的 CI 示例，需自行验证与现有构建工具（如 renv、pak）的兼容性。 |
| **适用场景** | ★★★★★ | 原型开发、内部工具、教学包、以及需要快速迭代文档的公开包。 |
| **风险** | 中等 | 若项目已有手写 `.Rd`，迁移需要手动审查；在大型 monorepo 中，文档生成的时间可能显著增长。 |

**结论**  
roxygen2 是 R 生态中生成包文档的事实标准，适合在 **原型** 或 **内部工作流** 中快速上手，也完全可以用于 **生产** 环境，只要在 CI 中加入一次性验证（文档生成、NAMESPACE 检查）并锁定依赖版本，即可获得稳定、可维护的文档体系。

## 🧭 Practical evaluation

**Value:** r-lib/roxygen2 may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 649 GitHub stars
- 237 forks
- updated 2026-06-25
- primary language: R
- 3 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 59/100 |
| stars | 60/100 |
| topics | 38/100 |
| outlook | 68/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 60/100 |
| production | 65/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/r-lib/roxygen2) · [← Back to Misc](./README.md)</sub>
