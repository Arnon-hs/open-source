# Khan/perseus

[![Stars](https://img.shields.io/github/stars/Khan/perseus?style=flat-square&color=yellow)](https://github.com/Khan/perseus/stargazers) [![Forks](https://img.shields.io/github/forks/Khan/perseus?style=flat-square&color=blue)](https://github.com/Khan/perseus/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Perseus is Khan Academy's exercise question editor and renderer.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.6k |
| 🍴 **Forks** | 368 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Perseus is the open‑source exercise authoring and rendering engine that powers Khan Academy’s interactive questions. Written in TypeScript, it provides a rich UI for creating, previewing, and delivering a wide variety of problem types (multiple‑choice, numeric entry, graphs, etc.). With over 1.5 k stars and recent activity, Perseus can serve as a solid foundation for any platform that needs a turnkey, web‑based learning‑content editor.

**Value Proposition**  
- **Feature‑complete question workflow** – Perseus already handles authoring, validation, and client‑side rendering, saving you from building a custom editor from scratch.  
- **Extensible architecture** – The codebase is modular and TypeScript‑typed, making it straightforward to add new question types or integrate with existing learning‑management systems.  
- **Community credibility** – A sizable star/fork count and ongoing commits indicate a mature, battle‑tested component that can accelerate product development.

**Practical Adoption Path**  
1. **Initial Feasibility Check** – Clone the repo, run the demo locally, and verify that the supported question types align with your curriculum.  
2. **Integration Planning** – Map Perseus’s data model (Item, Content, Widgets) to your backend schema; decide whether to embed the editor as an iframe or as a direct React component.  
3. **Security & License Review** – Confirm the MIT license meets your policy and run a dependency scan (e.g., npm audit) to address any known vulnerabilities.  
4. **Pilot Implementation** – Deploy a sandbox version for a small group of content creators, gather feedback, and adjust the build pipeline (Webpack/Babel) to match your production stack.  
5. **Scale‑up** – Once the pilot validates stability and workflow fit, integrate Perseus into your CI/CD, add automated tests for custom widgets, and document the onboarding process for authors.

**Production Readiness Assessment**  
- **Maturity** – Medium. The project is actively maintained (last commit 2026‑06‑25) and widely used internally at Khan Academy, but it is not a turnkey SaaS component; integration work is required.  
- **Stability** – The core editor is stable, yet you must verify compatibility with your version of React/TypeScript and monitor upstream updates for breaking changes.  
- **Maintenance** – With 1.5 k stars and a modest fork base, community support exists, but you should allocate an engineer to track upstream releases and handle security patches.  
- **Risk** – No major licensing or metadata red flags, but a final security audit and a check on active maintainers are recommended before committing to production use.  

Overall, Perseus is a viable choice for prototypes, internal tooling, or as the backbone of a custom learning platform, provided you perform the necessary integration and security checks before scaling to production.

### Русский

**Khan/perseus** — это открытый редактор и рендерер вопросов для упражнений Khan Academy, написанный на TypeScript. Он подходит для быстрой интеграции в прототипы или внутренние инструменты, где требуется настраиваемый UI для создания и отображения интерактивных заданий, но перед переходом в продакшн требуется проверить лицензирование, безопасность и наличие активных мейнтейнеров. Текущий уровень готовности — средний: проект стабилен и активно обновляется, однако интеграцию следует выполнить после ручного аудита зависимостей.

### 中文

**项目简介**  
Khan/perseus 是 Khan Academy 开源的练习题编辑器和渲染引擎，使用 TypeScript 实现，拥有 1500+ 星、300+ Fork，近期仍在维护。它提供所见即所得的题目编辑 UI、丰富的交互组件（选择题、填空题、绘图等）以及统一的渲染管线，帮助开发者快速构建在线练习或测评系统。

**价值**  
- **快速搭建题库**：无需从头实现题目编辑与渲染，直接复用 Khan Academy 成熟的交互组件。  
- **统一体验**：编辑器与渲染器保持一致的样式和交互逻辑，提升学习平台的 UI/UX 统一性。  
- **可定制**：基于 TypeScript，开发者可以在现有组件上扩展自定义题型或 UI。

**典型接入方式**  
1. **依赖引入**：在项目的 `package.json` 中加入 `@khanacademy/perseus`（或直接使用 GitHub 包），并通过 npm/yarn 安装。  
2. **编辑器嵌入**：在 React/Vue/Plain JS 页面中引入 `PerseusEditor` 组件，配置 `onChange` 回调保存题目 JSON。  
3. **渲染器使用**：将保存的题目 JSON 通过 `PerseusRenderer` 渲染到学习页面，配合 `apiOptions` 注入评分、计时等业务逻辑。  
4. **样式与资源**：复制或自定义 `perseus` 提供的 CSS/字体资源，确保题目在不同主题下保持一致。  

**生产可用性**  
- **成熟度**：中等（Medium）。代码已在 Khan Academy 大规模使用，适合原型、内部工具或对题目交互要求不高的生产系统。  
- **准备工作**：在正式上线前建议进行以下检查：  
  - **依赖审计**：确认所有子依赖的安全性与许可证兼容（MIT）。  
  - **维护情况**：关注最近的提交记录和 Issue 响应速度，必要时自行 fork 并维护。  
  - **性能评估**：在目标前端环境下测量渲染时延，尤其在移动端或低功耗设备上。  
- **风险**：暂无重大元数据风险，但仍需对许可证（MIT）进行合规审查，并对潜在的安全漏洞进行内部审计。  

总体而言，Khan/perseus 是一个功能完整、社区认可的题目编辑/渲染解决方案，适合作为学习平台或测评系统的核心组件，只要完成上述集成与安全检查，即可投入生产使用。

## 🧭 Practical evaluation

**Value:** Khan/perseus may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1573 GitHub stars
- 368 forks
- updated 2026-06-25
- primary language: TypeScript

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 64/100 |
| stars | 68/100 |
| topics | 0/100 |
| outlook | 66/100 |
| quality | 65/100 |
| recency | 80/100 |
| adoption | 67/100 |
| production | 66/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/Khan/perseus) · [← Back to Misc](./README.md)</sub>
