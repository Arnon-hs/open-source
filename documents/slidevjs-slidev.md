# slidevjs/slidev

[![Stars](https://img.shields.io/github/stars/slidevjs/slidev?style=flat-square&color=yellow)](https://github.com/slidevjs/slidev/stargazers) [![Forks](https://img.shields.io/github/forks/slidevjs/slidev?style=flat-square&color=blue)](https://github.com/slidevjs/slidev/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Presentation Slides for Developers

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 47.4k |
| 🍴 **Forks** | 2.1k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`markdown` `presentation` `slides` `vite` `vue` `vueuse`

## 🎯 Categories

Documents · Frontend

## 📝 Summary

### English

**Summary**  
Slidev (slidevjs/slidev) is an open‑source, TypeScript‑based tool that lets developers create presentation slides as code, turning UI components into reusable, version‑controlled slide decks. With over 47 k GitHub stars, frequent releases, and strong community adoption, it is production‑ready for pilots, especially when the goal is to accelerate UI delivery and reuse existing component libraries.  

**Value** – By authoring slides in the same stack as the product UI, teams can reuse components, apply the same design system, and ship polished, interactive demos without building a separate presentation layer. This cuts down on custom UI work, ensures visual consistency, and speeds up feedback loops for product and marketing demos.  

**Practical adoption path** – Start with a small proof‑of‑concept: clone the repo, follow the README to generate a minimal Slidev project, and import a few existing UI components. Validate the build pipeline, test live‑reload and export options, then gradually replace static slide decks with Slidev‑driven ones across a feature team.  

**Production readiness** – The project shows high readiness: recent commits (as of 2026‑06‑25), a large star/fork base, active maintainers, and a TypeScript codebase that aligns with modern frontend stacks. While the license and security posture should be double‑checked, there are no major metadata risks, making Slidev a solid candidate for a serious pilot in production environments.

### Русский

slidevjs/slidev — это open‑source инструмент для создания презентаций, ориентированный на разработчиков; он позволяет быстро собрать пользовательские интерфейсы, переиспользовать готовые UI‑компоненты и ускорить доставку фронтенда. Для внедрения рекомендуется начать с небольшого proof‑of‑concept, проверив README и запустив пример, после чего можно масштабировать в продакшн‑окружение. Проект считается готовым к production: активная поддержка, регулярные обновления, 47 k звёзд и более 2 k форков подтверждают его надёжность, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**简短介绍**  
slidevjs/slidev 是面向开发者的交互式演示文稿框架，使用 Markdown+Vue 语法即可快速生成高质量的 PPT。它把前端组件化思路直接搬进演示稿，让代码、数据和 UI 能在同一个项目里统一管理与迭代。

**价值**  
- **复用 UI 组件**：演示页面本质上是 Vue 组件，开发中已有的 UI 库、布局和动画可以直接在幻灯片中使用，省去重复实现。  
- **加速产品 UI 输出**：通过 Markdown 编写内容、即时热重载预览，开发者可以在几分钟内完成一个完整的产品演示或内部培训材料。  
- **提升前端交付一致性**：演示稿与实际业务代码共享同一套技术栈（TypeScript、Vite），从而保证样式、交互和数据处理的一致性，降低维护成本。

**典型接入方式**  
1. **创建小型 POC**：在现有项目根目录下 `npm init slidev@latest my-presentation`，生成 `slides.md` 与默认配置。  
2. **在 README 中加入快速启动脚本**：`npm i -D slidev && npx slidev`，确保团队成员能够一键本地预览。  
3. **逐步迁移已有演示**：把原有的 Markdown 或 HTML 幻灯片内容拷贝进 `slides.md`，必要时引入业务组件（如 UI 库的 Button、Chart）进行演示。  
4. **CI/CD 集成**：使用 `slidev export --format pdf` 或 `slidev export --format html` 在 CI 中生成静态产出，部署到 GitHub Pages、Vercel 等静态站点。

**生产可用性**  
- **活跃度**：截至 2026‑06‑25，项目拥有 47 370+ 星、2 111+ Fork，最近一次提交在同一天，说明社区与维护者非常活跃。  
- **技术成熟度**：基于 TypeScript 与 Vite，具备完整的类型安全和现代前端构建链，易于与现有前端生态集成。  
- **安全与合规**：暂无重大元数据风险，仍需对许可证（MIT）和依赖的安全报告进行最终审查。  
- **适合试点**：可以先在内部技术分享或产品演示中使用，验证与业务组件的兼容性后，再推广到正式的客户演示或营销页面。总体来看，slidev 已具备高生产就绪度，适合作为正式项目的演示层解决方案。

## 🧭 Practical evaluation

**Value:** slidevjs/slidev helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 47370 GitHub stars
- 2111 forks
- updated 2026-06-25
- primary language: TypeScript
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 83/100 |
| stars | 100/100 |
| topics | 75/100 |
| outlook | 78/100 |
| quality | 89/100 |
| recency | 80/100 |
| adoption | 95/100 |
| production | 75/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/slidevjs/slidev) · [← Back to Documents](./README.md)</sub>
