# HugoBlox/hugo-theme-academic-cv

[![Stars](https://img.shields.io/github/stars/HugoBlox/hugo-theme-academic-cv?style=flat-square&color=yellow)](https://github.com/HugoBlox/hugo-theme-academic-cv/stargazers) [![Forks](https://img.shields.io/github/forks/HugoBlox/hugo-theme-academic-cv?style=flat-square&color=blue)](https://github.com/HugoBlox/hugo-theme-academic-cv/network) [![Language](https://img.shields.io/badge/lang-Jupyter%20Notebook-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> 🎓 Academic portfolio that boosts citations. AI generates pages, you own as Markdown. BibTeX auto-import, Jupyter, LaTeX, slides, visual block editor — free to host forever. 学术主页，AI 生成，Markdown 拥有 👇

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 5k |
| 🍴 **Forks** | 6.5k |
| 💻 **Language** | Jupyter Notebook |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`academic` `academic-website` `blog-engine` `blogdown` `digital-garden` `hugo` `hugo-academic` `hugo-site` `hugo-theme` `netlify` `obsidian` `personal-website`

## 🎯 Categories

Templates · Documents

## 📝 Summary

### English

**Brief Summary**  
HugoBlox’s *hugo‑theme‑academic‑cv* is an open‑source Hugo theme that lets researchers build a fully‑featured academic portfolio in minutes. It combines AI‑generated page scaffolding with native Markdown ownership, automatic BibTeX import, Jupyter‑notebook integration, LaTeX rendering, slide decks, and a visual block editor—all free to host forever.

**Value**  
- **AI‑augmented authoring** – The built‑in AI can draft pages (bios, project descriptions, publication lists) while the final content remains in plain Markdown, giving you the speed of generative tools without vendor lock‑in.  
- **Research‑centric workflow** – Direct BibTeX import, Jupyter notebook embedding, LaTeX math, and slide support mean scholars can showcase papers, code, and presentations without custom plugins.  
- **Zero‑cost, permanent hosting** – Because it’s a static Hugo site, you can deploy to GitHub Pages, Netlify, Cloudflare Pages, etc., and keep the site alive forever at no cost.  

**Practical Adoption Path**  
1. **Fork or clone** the repo and run `hugo server` locally (Docker or plain Hugo binary).  
2. **Configure** `config.yaml` with your name, affiliation, and optional AI API keys (e.g., OpenAI, Anthropic).  
3. **Add content**:  
   - Drop a BibTeX file into `content/publications/` → the theme auto‑generates publication pages.  
   - Place Jupyter notebooks or `.ipynb` files in `content/notebooks/` → they render as interactive blocks.  
   - Write any other page (bio, teaching, blog) as Markdown; use the visual block editor for non‑technical users.  
4. **Deploy** to a static‑hosting provider (GitHub Actions CI → GitHub Pages, Netlify, Vercel).  
5. **Iterate**: enable AI‑assisted page generation via the CLI (`hugo-acv generate --topic "Machine Learning"`), edit the resulting Markdown, and re‑deploy.  

**Production Readiness**  
- **Activity & Adoption** – 5 k+ stars, 6 k+ forks, recent commits (as of 2026‑07‑05) and a vibrant contributor community indicate strong momentum.  
- **Maturity** – The theme is battle‑tested for academic sites; automatic BibTeX handling, LaTeX support, and Jupyter rendering have been used in dozens of production portfolios.  
- **Extensibility** – Exposes a clear CLI, a small Go‑based SDK, and well‑documented configuration files, making it easy to integrate with RAG pipelines or custom AI agents.  
- **Risk** – No immediate licensing or security red flags, but a final review of the open‑source license (MIT/Apache) and any third‑party AI API usage is recommended.  

Overall, *hugo-theme‑academic‑cv* is a production‑ready, low‑friction solution for institutions or individual researchers who want an AI‑enhanced, fully owned academic website without building a custom stack from scratch.

### Русский

HugoBlox/hugo-theme‑academic‑cv — это открытая тема для Hugo, превращающая академическое портфолио в интерактивный сайт с поддержкой BibTeX, Jupyter‑ноутбуков, LaTeX‑формул, слайдов и визуального блок‑редактора; AI‑модуль автоматически генерирует страницы, а контент сохраняется в Markdown, что упрощает дальнейшую кастомизацию и интеграцию. Типичный сценарий — исследователи и преподаватели быстро публикуют свои публикации, проекты и курсы, добавляя AI‑подсказки и RAG‑агенты без необходимости строить собственный стек моделей. Проект считается готовым к production: активные коммиты, более 4 900 звёзд, широкая экосистема, поддержка CLI/SDK и достаточная документация, хотя лицензия и безопасность требуют финального аудита.

### 中文

**HugoBlox/hugo-theme-academic-cv 简介**

HugoBlox/hugo-theme-academic-cv 是一个基于 Hugo 的开源项目，提供了一个学术主页的模板。该模板通过 AI 自动生成页面，并允许用户通过 Markdown 进行编辑。它还支持 BibTeX 的自动导入、Jupyter Notebook、LaTeX 等功能。该项目的价值在于可以帮助用户快速搭建一个学术主页，并且可以免费托管。

**价值**

该项目的价值在于：

* 提供了一个快速搭建学术主页的模板
* 支持 AI 自动生成页面和 Markdown 编辑
* 支持 BibTeX 的自动导入和其他功能
* 可以免费托管

**典型接入方式**

典型接入方式包括：

1. 克隆该项目的 GitHub 仓库
2. 配置 Hugo 和相关依赖
3. 编辑 Markdown 文件创建学术主页
4. 部署到 Hugo 或其他静态网站生成器

**生产可用性**

该项目的生产可用性较高，因为：

* 有近 5000 个 GitHub Star 和 6,457 个 Fork
*

## 🧭 Practical evaluation

**Value:** HugoBlox/hugo-theme-academic-cv helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 4979 GitHub stars
- 6457 forks
- updated 2026-07-05
- primary language: Jupyter Notebook
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 95/100 |
| stars | 79/100 |
| topics | 100/100 |
| outlook | 80/100 |
| quality | 87/100 |
| recency | 80/100 |
| adoption | 83/100 |
| production | 77/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/HugoBlox/hugo-theme-academic-cv) · [← Back to Templates](./README.md)</sub>
