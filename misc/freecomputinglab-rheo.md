# freecomputinglab/rheo

[![Stars](https://img.shields.io/github/stars/freecomputinglab/rheo?style=flat-square&color=yellow)](https://github.com/freecomputinglab/rheo/stargazers) [![Forks](https://img.shields.io/github/forks/freecomputinglab/rheo?style=flat-square&color=blue)](https://github.com/freecomputinglab/rheo/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-47%2F100-brightgreen?style=flat-square)](#)

> Typesetting and static site engine based on Typst

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 166 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | Rust |
| 📈 **Score** | 47/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
Rheo is a Rust‑based static‑site generator that leverages Typst for high‑quality typesetting, letting developers produce mathematically‑rich web pages without a separate PDF workflow. With ~166 GitHub stars and recent activity (last updated 2026‑06‑26), it’s mature enough for prototyping but still requires manual vetting of its integration points.  

**Value**  
- **Typst‑driven layout**: Generates clean, responsive HTML from Typst source, ideal for documentation, blogs, or academic sites that need precise formula rendering.  
- **All‑in‑one engine**: Eliminates the need for a separate PDF → HTML conversion step, simplifying the toolchain for teams already using Typst.  

**Practical adoption path**  
1. **Clone the repo** and run the provided examples to confirm the build environment (Rust 1.70+).  
2. **Map your content pipeline**: replace existing markdown or HTML sources with Typst files and adjust the site configuration (e.g., theme, asset folders).  
3. **Integrate into CI**: add a Cargo build step that outputs the static site to a `public/` directory, then deploy with any static‑host (Netlify, Vercel, GitHub Pages).  
4. **Validate**: run a small internal pilot to check for missing plugins, custom asset handling, or build‑time dependencies.  

**Production readiness**  
- **Medium**: Suitable for prototypes, internal documentation sites, or niche publications where Typst’s rendering is a core requirement.  
- **Considerations before production**: verify dependency licensing, ensure the Rust toolchain is locked to a stable version, and test long‑term maintenance (e.g., handling of breaking changes in Typst or Rust). Once these checks are passed, Rheo can be promoted to production for low‑to‑moderate traffic sites.

### Русский

**freecomputinglab/rheo** — это лёгкий движок для генерации статических сайтов и наборов типографики, построенный на основе Typst и написанный на Rust. Он подходит для прототипов и внутренних рабочих процессов, где требуется быстро собрать красиво оформленную документацию или блог, но перед внедрением следует вручную проверить совместимость и оценить затраты на настройку, так как готовых интеграционных инструкций мало. Уровень готовности — средний: проект активно поддерживается (166 звёзд, последний коммит 2026‑06‑26), однако для production‑использования рекомендуется провести дополнительный аудит зависимостей и процесса сборки.

### 中文

**项目简介**  
freecomputinglab/rheo 是一个基于 **Typst** 的排版与静态站点生成引擎，使用 Rust 实现，旨在让用户通过 Typst 的强大排版能力快速构建轻量、可定制的静态网站。

**价值**  
- **Typst 原生支持**：直接复用 Typst 文档的排版特性，省去 Markdown→HTML 的转换步骤，适合技术文档、学术报告、博客等对排版质量有要求的场景。  
- **轻量高效**：全程基于 Rust 编译，构建速度快、二进制体积小，易于在 CI/CD 中嵌入。  
- **可扩展**：提供插件式的页面生成管线，开发者可以自行添加自定义模板、资产处理或数据注入。

**典型接入方式**  
1. **本地快速试用**  
   ```bash
   cargo install rheo          # 安装二进制
   rheo init mysite           # 初始化项目结构
   cd mysite && rheo build    # 编译生成 static/ 目录
   ```  
2. **CI/CD 集成**（以 GitHub Actions 为例）  
   ```yaml
   name: Build Rheo Site
   on: [push, pull_request]
   jobs:
     build:
       runs-on: ubuntu-latest
       steps:
         - uses: actions/checkout@v3
         - uses: actions/setup-rust@v2
           with:
             toolchain: stable
         - run: cargo install rheo
         - run: rheo build
         - uses: actions/upload-artifact@v3
           with:
             name: site
             path: static/
   ```  
   生成的 `static/` 目录可直接部署到 Netlify、Vercel、GitHub Pages 等静态托管平台。

**生产可用性**  
- **成熟度**：已有 166 ⭐、4 🍴，最近一次提交在 2026‑06‑26，活跃度尚可，适合作为内部原型或中小型站点的生产工具。  
- **风险点**：项目文档和集成示例相对有限，需自行评估以下事项后再投入生产：  
  - 与现有 CI/CD 流程的兼容性（尤其是自定义插件或资产管线）。  
  - 依赖的 Rust 生态（编译器版本、平台支持）在目标部署环境中的可用性。  
  - 维护成本：项目活跃度虽有，但社区规模小，遇到 bug 时可能需要自行修复或提交 PR。  
- **建议**：在正式上线前，先在预生产环境进行完整的构建‑部署‑回滚测试；若项目满足业务需求且维护成本在可接受范围内，可视为 **Medium** 级别的生产就绪方案。

## 🧭 Practical evaluation

**Value:** freecomputinglab/rheo may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 166 GitHub stars
- 4 forks
- updated 2026-06-26
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 47/100 |
| topics | 0/100 |
| outlook | 56/100 |
| quality | 53/100 |
| recency | 80/100 |
| adoption | 39/100 |
| production | 60/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/freecomputinglab/rheo) · [← Back to Misc](./README.md)</sub>
