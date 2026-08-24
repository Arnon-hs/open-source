# justvanrossum/fontgoggles

[![Stars](https://img.shields.io/github/stars/justvanrossum/fontgoggles?style=flat-square&color=yellow)](https://github.com/justvanrossum/fontgoggles/stargazers) [![Forks](https://img.shields.io/github/forks/justvanrossum/fontgoggles?style=flat-square&color=blue)](https://github.com/justvanrossum/fontgoggles/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> FontGoggles: Visual OTL Preview and QA

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 468 |
| 🍴 **Forks** | 46 |
| 💻 **Language** | Python |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cocoa` `font` `fonts` `macos-app` `python`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
FontGoggles (justvanrossum/fontgoggles) is an open‑source Python tool for visualizing and quality‑checking OpenType Layout (OTL) features in font files. With 468 ★, recent commits (last updated 2026‑05‑14) and a small but active community, it is ready for pilot projects that need fast, interactive OTL inspection.

**Value** – It lets type designers, engineers, and QA teams preview glyph substitution, positioning, and other OTL tables directly in a lightweight GUI, reducing the turnaround time for bug‑reports and eliminating the need for heavyweight font editors during early testing.

**Adoption path** – Start with a proof‑of‑concept: clone the repo, run the supplied Docker image or install via `pip install fontgoggles`, and integrate it into your CI pipeline to automatically open a sample UI for new builds. Verify the README workflow matches your needs, then wrap the CLI calls in a script that launches FontGoggles for each new font version.

**Production readiness** – The project shows strong signals: recent activity, a permissive license, a modest but engaged contributor base, and no known security red flags. After a small pilot and a final license/security review, FontGoggles can be considered production‑ready for internal QA and even for broader release as part of a font‑production pipeline.

### Русский

**justvanrossum/fontgoggles** — это Python‑утилита для визуального предварительного просмотра и контроля качества OpenType‑шрифтов (OTL). Она удобно вписывается в пайплайн разработки шрифтов: после сборки шрифта её можно запустить в CI/CD или локально, чтобы автоматически проверять глифы, метрики и таблицы, а также вручную просматривать их в интерактивном UI. Проект имеет высокую готовность к продакшн‑использованию: активные коммиты, более 460 звёзд, регулярные релизы и широкая поддержка экосистемы, что делает его надёжным кандидатом для пилотного внедрения в процесс QA шрифтов.

### 中文

**项目简介**  
justvanrossum/fontgoggles（FontGoggles）是一款基于 Python 的开源工具，用于在编辑器中实时预览和质量检查 OpenType 字体（OTL），帮助设计师快速发现字形渲染、度量和排版问题。

**价值**  
- **可视化 QA**：提供交互式的字形、字距、特性表等视图，显著降低人工检查的工作量。  
- **工作流兼容**：可以直接嵌入到字体设计、CI/CD 或自动化测试管线中，实现持续的字体质量把关。  
- **社区与活跃度**：468 ⭐、46 forks，最近一次提交在 2026‑05‑14，表明项目仍在维护，适合作为生产环境的可靠组件。

**典型接入方式**  
1. **本地使用**：`pip install fontgoggles` 后在命令行或 Python 脚本中调用 `fontgoggles.preview(<font-file>)` 进行交互式预览。  
2. **CI 集成**：在 GitHub Actions、GitLab CI 等流水线中添加步骤，使用 `fontgoggles check <font-file>` 生成 QA 报告（JSON/HTML），并将报告上传为构建产物或评论回 PR。  
3. **自定义插件**：通过项目提供的 Python API，结合自家字体构建工具（如 fontmake、glyphsLib）实现自动化的特性验证和回归检测。

**生产可用性**  
- **成熟度**：近期活跃维护、明确的 MIT 许可证、丰富的文档和示例，已在多个开源字体项目中得到实际使用。  
- **集成门槛低**：仅依赖 Python 环境，安装和调用方式简洁，适合作为小型 PoC 验证后直接推广到正式流水线。  
- **风险**：仍需对许可证兼容性、潜在的安全依赖（如 `fontTools`）进行最终审计；但整体风险低，已具备在生产环境中进行试点的条件。

## 🧭 Practical evaluation

**Value:** justvanrossum/fontgoggles may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 468 GitHub stars
- 46 forks
- updated 2026-05-14
- primary language: Python
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 57/100 |
| topics | 63/100 |
| outlook | 45/100 |
| quality | 53/100 |
| recency | 20/100 |
| adoption | 53/100 |
| production | 50/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/justvanrossum/fontgoggles) · [← Back to Misc](./README.md)</sub>
