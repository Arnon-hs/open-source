# zed-industries/extensions

[![Stars](https://img.shields.io/github/stars/zed-industries/extensions?style=flat-square&color=yellow)](https://github.com/zed-industries/extensions/stargazers) [![Forks](https://img.shields.io/github/forks/zed-industries/extensions?style=flat-square&color=blue)](https://github.com/zed-industries/extensions/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Extensions for the Zed editor

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.7k |
| 🍴 **Forks** | 1.9k |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
`zed-industries/extensions` is a collection of community‑maintained plugins that add extra language support, UI widgets, and workflow shortcuts to the Zed editor. With thousands of stars and forks, the repo is actively maintained (last commit 2026‑05‑14) and written in JavaScript, making it a handy source of ready‑made extensions for teams that already use Zed.

**Value**  
The project supplies a curated set of reusable components that can accelerate the setup of a Zed‑based development environment—e.g., syntax highlighters, custom commands, and file‑type integrations—without having to roll them from scratch. Because the extensions are open‑source and modular, they can be inspected, tweaked, or combined to match a concrete workflow, reducing onboarding time for new developers and enabling rapid prototyping of editor‑centric tooling.

**Practical Adoption Path**  
1. **Review the README and individual extension directories** to identify the features that align with your workflow.  
2. **Clone the repo** and run the provided build scripts (usually `npm install && npm run build`).  
3. **Add the desired extensions to your Zed configuration** (e.g., by pointing Zed to the local `extensions/` folder or publishing them as npm packages).  
4. **Run a quick validation test** (open a sample project, trigger the new commands, and verify that the UI behaves as expected).  
5. **Iterate**: if an extension needs minor adjustments, fork the repo, apply patches, and keep the fork as a version‑controlled dependency.

**Production Readiness**  
The project sits at a **medium** readiness level: it is mature enough for prototypes, internal tools, or sandbox environments, but the integration surface is not fully documented, so a manual inspection is required before committing to production. Before a production rollout, teams should:

* Pin a specific commit or release tag to avoid unexpected breaking changes.  
* Run the full test suite (or add one) to confirm compatibility with your Zed version.  
* Evaluate the maintenance burden—track upstream updates and plan for periodic syncs.  

With these checks in place, `zed-industries/extensions` can be safely leveraged in production for teams that need a flexible, extensible editor experience.

### Русский

**z​ed‑industries/extensions** — набор расширений для редактора Zed, который позволяет добавить готовые функции (подсветка синтаксиса, автодополнение, интеграцию с CI и т.п.) в ваш рабочий процесс без написания собственного кода. Проект уже имеет значительное сообщество (≈ 1,7 к звёзд и 1,9 к форков) и активную поддержку (обновления — 14 мая 2026), поэтому его удобно использовать в прототипах и внутренних инструментах, однако перед выпуском в продакшн рекомендуется проверить совместимость с вашей конфигурацией Zed и оценить затраты на интеграцию, так как явных инструкций в метаданных мало. В целом готовность к production — средняя: подходит для быстрых внедрений при условии ручного аудита и контроля зависимостей.

### 中文

**项目简介**  
`zed-industries/extensions` 是为 **Zed** 编辑器提供的一系列插件与扩展，帮助用户快速在编辑器内部实现代码片段、语言服务、主题定制等常用功能。

**价值**  
- **提升生产力**：通过即插即用的扩展，开发者可以在 Zed 中直接获得常见语言的 LSP、代码片段、自动完成等功能，省去自行配置的时间。  
- **社区活跃**：已有 1.6k+ 星、1.8k+ Fork，说明社区对这些扩展的需求和维护力度较强。  
- **灵活可定制**：所有扩展均使用 JavaScript 编写，便于二次开发或根据内部工作流进行裁剪。

**典型接入方式**  
1. **克隆或直接在项目中引用**：`git clone https://github.com/zed-industries/extensions.git`，或在 Zed 的插件目录下添加对应子目录。  
2. **在 Zed 配置文件中声明**：编辑 `~/.config/zed/settings.json`（或对应平台的配置路径），加入  
   ```json
   {
     "extensions": [
       "path/to/extensions/<extension-name>"
     ]
   }
   ```  
3. **按需启用**：重启 Zed 后，在插件面板中勾选需要的扩展，或在工作区 `.zedrc` 中使用 `enableExtension` 指令进行项目级别的开启。  
4. **自定义**：如需修改或扩展功能，直接编辑对应的 JavaScript 文件并重新加载插件即可。

**生产可用性**  
- **成熟度**：代码最近更新于 2026‑05‑14，活跃度仍然较高，基本满足日常开发需求。  
- **适用场景**：适合原型开发、内部工具链或对 Zed 有明确使用计划的团队。  
- **风险与注意事项**：  
  - 集成路径在元数据中不够明确，建议在正式上线前进行一次完整的功能验证（包括 LSP、依赖冲突等）。  
  - 需要自行管理扩展的版本与安全审计，尤其在生产环境中使用时。  
- **总体评估**：**中等**（Medium）——在做好依赖检查和维护计划后，可安全用于内部生产环境；若对稳定性要求极高，建议在关键业务前进行额外的回归测试。

## 🧭 Practical evaluation

**Value:** zed-industries/extensions may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1674 GitHub stars
- 1859 forks
- updated 2026-05-14
- primary language: JavaScript

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 82/100 |
| stars | 69/100 |
| topics | 0/100 |
| outlook | 71/100 |
| quality | 73/100 |
| recency | 100/100 |
| adoption | 72/100 |
| production | 72/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/zed-industries/extensions) · [← Back to Misc](./README.md)</sub>
