# asciidoctor/asciidoctor.js

[![Stars](https://img.shields.io/github/stars/asciidoctor/asciidoctor.js?style=flat-square&color=yellow)](https://github.com/asciidoctor/asciidoctor.js/stargazers) [![Forks](https://img.shields.io/github/forks/asciidoctor/asciidoctor.js?style=flat-square&color=blue)](https://github.com/asciidoctor/asciidoctor.js/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-48%2F100-brightgreen?style=flat-square)](#)

> :scroll: A JavaScript port of Asciidoctor, a modern implementation of AsciiDoc

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 797 |
| 🍴 **Forks** | 153 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 48/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`asciidoc` `asciidoctor` `hacktoberfest` `javascript`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
asciidoctor/asciidoctor.js is a JavaScript implementation of the Asciidoctor engine, enabling AsciiDoc rendering directly in Node.js or the browser. With ~800 GitHub stars and recent commits, it offers a modern, cross‑platform way to generate HTML, PDF, or other formats from AsciiDoc sources without relying on a Ruby runtime.  

**Value**  
- **Unified stack** – Teams already using JavaScript for front‑end or server‑side code can keep the entire toolchain in one language, simplifying build pipelines and reducing context‑switching.  
- **Live preview & client‑side rendering** – Because it runs in the browser, it powers real‑time editors, documentation portals, and static‑site generators that need on‑the‑fly AsciiDoc conversion.  
- **Compatibility** – It mirrors the feature set of the original Asciidoctor, so existing AsciiDoc documents and extensions largely work unchanged.  

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Add the package (`npm i asciidoctor`) to a sandbox project and render a sample AsciiDoc file using the API shown in the README. Verify that the output matches expectations (HTML, PDF via a converter plugin, etc.).  
2. **Integration test** – Wrap the renderer in a small build step (e.g., a Gulp/Grunt/Webpack task or a Node script) and run it on your documentation source tree. Check for missing extensions or Ruby‑only features.  
3. **CI validation** – Add a CI job that runs the renderer on a representative set of docs to catch regressions early.  
4. **Production rollout** – Once the CI job passes, replace the existing Ruby‑based Asciidoctor step (or external service) with the JavaScript version in your build pipeline, monitoring build times and output quality.  

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑06‑24) and has a healthy star/fork count, indicating community interest.  
- **Stability**: Sufficient for internal tools, prototypes, and documentation pipelines, but you should audit the dependency tree for security updates and confirm that any required Asciidoctor extensions are supported.  
- **Risk mitigation**: Because the integration path is not fully documented, allocate time for a small PoC and for checking edge‑case features (e.g., custom macros, PDF back‑ends). Once those are validated, the library can be promoted to production with confidence.

### Русский

**asciidoctor/asciidoctor.js** — это JavaScript‑порт Asciidoctor, позволяющий преобразовывать AsciiDoc‑документы в HTML, PDF и другие форматы прямо в браузере или Node.js. Типичный сценарий — интеграция в веб‑приложения, CI‑конвейеры или генерацию статических сайтов, где нужен быстрый клиент‑сайд рендеринг без установки Ruby‑окружения. Проект имеет средний уровень готовности к production: активные обновления, 800+ звёзд и 150 форков, но перед запуском в продакшн рекомендуется проверить процесс сборки, совместимость зависимостей и провести небольшой proof‑of‑concept.

### 中文

**项目简介（2‑3 句）**  
asciidoctor/asciidoctor.js 是 Asciidoctor（现代 AsciiDoc 解析与渲染引擎）的 JavaScript 移植版，能够在浏览器或 Node.js 环境中直接将 AsciiDoc 文本转换为 HTML、PDF 等格式。它保留了原生 Asciidoctor 的语法特性和扩展能力，同时提供了 npm 包的便捷分发方式。

---

## 价值点

1. **统一前后端渲染**：无需在后端使用 Ruby 或 Java 版 Asciidoctor，前端即可完成文档渲染，适合单页应用、文档编辑器或静态站点生成器。  
2. **生态兼容**：遵循 Asciidoctor 语法标准，已有的 AsciiDoc 文档、宏和扩展可以直接迁移，降低学习成本。  
3 **轻量可嵌入**：作为 npm 包发布，依赖仅限 JavaScript，易于在现有 Node.js 项目或前端构建链中引入。  

---

## 典型接入方式

| 场景 | 步骤 | 示例代码 |
|------|------|----------|
| **Node.js 脚本或构建工具** | 1. `npm i asciidoctor.js`  <br>2. 在代码中 `require` 或 `import`  <br>3. 调用 `asciidoctor()` 进行转换 | ```js\nconst asciidoctor = require('asciidoctor.js')();\nconst html = asciidoctor.convert('= Title\\n\\nHello *AsciiDoc*');\nconsole.log(html);\n``` |
| **浏览器实时预览** | 1. 通过 `<script type="module">` 引入 CDN（如 jsDelivr）或本地打包的文件 <br>2. 调用全局 `asciidoctor()` <br>3. 将返回的 HTML 插入页面 | ```html\n<script type="module">\nimport asciidoctor from 'https://cdn.jsdelivr.net/npm/asciidoctor.js/dist/browser/asciidoctor.min.js';\nconst ad = asciidoctor();\nconst html = ad.convert('# Demo');\ndocument.getElementById('preview').innerHTML = html;\n</script>\n<div id="preview"></div>\n``` |
| **与静态站点生成器（如 Eleventy、Gatsby）结合** | 在生成器的插件或自定义过滤器里调用 `asciidoctor.convert`，把 `.adoc` 文件转为 HTML 再交给生成器渲染 | ```js\n// Eleventy filter example\nmodule.exports = function(eleventyConfig) {\n  const asciidoctor = require('asciidoctor.js')();\n  eleventyConfig.addFilter('adoc', content => asciidoctor.convert(content));\n};\n``` |

> **小技巧**：如果项目需要 PDF 输出，可配合 `asciidoctor-pdf`（Ruby）或使用 `asciidoctor.js` 生成 HTML 后交由 `puppeteer`/`playwright` 打印为 PDF。

---

## 生产可用性评估

| 维度 | 现状 | 结论 |
|------|------|------|
| **活跃度** | 最近一次提交：2026‑06‑24，拥有 797 ★、153 Fork，社区仍在维护。 | ✅ 可接受 |
| **成熟度** | 已经是 Asciidoctor 官方的 JavaScript 移植版，功能基本覆盖 Asciidoctor 2.x 的核心特性。 | ✅ 稳定 |
| **依赖风险** | 仅依赖 Node.js 标准库和少量轻量 polyfill，未引入大型二进制依赖。 | ✅ 低风险 |
| **文档与示例** | README 提供基本用法，GitHub Wiki 与社区博客有不少集成案例。 | ✅ 足够 |
| **生产建议** | - 在正式环境前先做 **小规模 PoC**（如单文件渲染或编辑器插件）<br>- 通过 CI 检查 `asciidoctor.js` 版本升级的兼容性<br>- 若需要 PDF，考虑额外的渲染链路或使用服务器端 Asciidoctor 进行二次处理 | ⚙️ 可在内部系统或面向用户的文档平台投入使用，前提做好版本锁定和回归测试。 |

**总体判断**：asciidoctor.js 具备中等到高的生产可用性，适合作为原型、内部工具或面向终端用户的文档编辑/渲染服务的核心组件。只要在上线前完成依赖锁定、兼容性回归以及性能基准（尤其是大文档渲染时），即可安全投入生产。

## 🧭 Practical evaluation

**Value:** asciidoctor/asciidoctor.js may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 797 GitHub stars
- 153 forks
- updated 2026-06-24
- primary language: JavaScript
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 55/100 |
| stars | 62/100 |
| topics | 50/100 |
| outlook | 52/100 |
| quality | 59/100 |
| recency | 40/100 |
| adoption | 60/100 |
| production | 52/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/asciidoctor/asciidoctor.js) · [← Back to Misc](./README.md)</sub>
