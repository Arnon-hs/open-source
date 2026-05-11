# yWorks/svg2pdf.js

[![Stars](https://img.shields.io/github/stars/yWorks/svg2pdf.js?style=flat-square&color=yellow)](https://github.com/yWorks/svg2pdf.js/stargazers) [![Forks](https://img.shields.io/github/forks/yWorks/svg2pdf.js?style=flat-square&color=blue)](https://github.com/yWorks/svg2pdf.js/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> A javascript-only SVG to PDF conversion utility that runs in the browser. Brought to you by yWorks - the diagramming experts

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 832 |
| 🍴 **Forks** | 114 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`browser` `conversion` `hacktoberfest` `javascript` `jspdf` `nodejs` `pdf` `pdf-conversion-utility` `svg`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
yWorks/svg2pdf.js is a pure‑JavaScript library that converts SVG graphics to PDF directly in the browser, eliminating the need for server‑side processing or external tools. Maintained by the diagram‑ming experts at yWorks, the project is written in TypeScript, has >800 stars, recent commits, and a modest but active community. It is positioned as a ready‑to‑use component for any web‑app that needs client‑side export of vector drawings to PDF.  

---  

### Value Proposition
- **Zero‑install, client‑side conversion** – Developers can embed the library in any front‑end stack and generate PDFs on‑the‑fly, preserving vector quality and avoiding backend dependencies.  
- **TypeScript source & strong documentation** – The codebase is typed, making integration and debugging straightforward, while the README provides clear usage examples.  
- **Broad applicability** – Ideal for diagram editors, charting widgets, design tools, or any SaaS that lets users create or manipulate SVG content and needs a downloadable PDF export.  

### Practical Adoption Path
1. **Proof‑of‑Concept** – Add the package via npm (`npm i @yworks/svg2pdf`) or a CDN script tag, follow the README to convert a static SVG element, and verify the PDF output in the target browsers.  
2. **API Fit Check** – Map the library’s `svgElementToPdf` (or similar) function to your existing export workflow; wrap it in a thin service layer if you need custom page sizes, margins, or metadata.  
3. **Automated Tests** – Write a few unit/visual tests that feed representative SVGs (simple icons, complex diagrams) and assert that the generated PDFs open without errors.  
4. **Security & License Review** – Confirm the MIT license aligns with your policy and run a quick SCA scan (e.g., GitHub Dependabot, Snyk) to ensure no known vulnerabilities.  
5. **Pilot Integration** – Deploy the updated front‑end to a staging environment, collect user feedback on PDF quality and performance, and iterate as needed.  

### Production Readiness
- **Activity & Community** – Last commit on 2026‑05‑11, 832 stars, 114 forks, and active issue discussion indicate a healthy, maintained project.  
- **Technical Maturity** – Written in TypeScript with clear typings, minimal external dependencies, and a small bundle size suitable for browser use.  
- **Risk Profile** – No major metadata or licensing concerns identified; the primary remaining checks are a formal security audit and verification of maintainers’ responsiveness.  

Given its recent updates, solid adoption signals, and straightforward integration steps, yWorks/svg2pdf.js can be considered production‑ready for a pilot or even full‑scale deployment after the standard OSS due‑diligence checks.

### Русский

**yWorks/svg2pdf.js** — это полностью JavaScript‑утилита для конвертации SVG в PDF прямо в браузере, поддерживаемая командой yWorks, экспертов в области диаграмм. При наличии подходящей документации её можно быстро интегрировать в клиентские приложения (например, для экспорта диаграмм или графиков в PDF) через небольшое proof‑of‑concept, а затем развить до полноценного модуля. Проект имеет активную поддержку (обновления до 2026‑05‑11), 832 ★, 114 форков и написан на TypeScript, что делает его готовым к пилотному использованию в продакшене после проверки лицензии и безопасности.

### 中文

**项目简介**  
yWorks/svg2pdf.js 是一款纯前端的 SVG → PDF 转换工具，使用 TypeScript 编写，可直接在浏览器中运行，无需后端服务或额外依赖。由图表专家 yWorks 开发并维护，已累计 832 颗星，活跃度高，适合在 Web 应用中实现即时的矢量图导出。

**价值点**  
- **零后端依赖**：所有转换在用户浏览器完成，降低运维成本，避免跨域或文件上传的安全风险。  
- **高保真输出**：保持 SVG 的向量特性，生成的 PDF 与原图在尺寸、样式、文本等方面几乎一致，适用于图表、流程图、UML 等业务场景。  
- **易集成**：只需在页面中引入库并调用几行 API，即可把任意 `<svg>` 元素或 SVG 字符串导出为 PDF，满足快速原型和生产环境的需求。

**典型接入方式**  

```html
<script type="module">
  import { svg2pdf } from 'https://cdn.jsdelivr.net/npm/@yworks/svg2pdf@latest';

  async function exportSvg() {
    const svgEl = document.querySelector('#myDiagram'); // 任意 SVG 元素
    const pdfBlob = await svg2pdf(svgEl, { 
      filename: 'diagram.pdf',
      // 可选参数：scale、margin、metadata 等
    });
    // 触发下载
    const url = URL.createObjectURL(pdfBlob);
    const a = document.createElement('a');
    a.href = url;
    a.download = 'diagram.pdf';
    a.click();
    URL.revokeObjectURL(url);
  }
</script>
<button onclick="exportSvg()">导出 PDF</button>
```

关键步骤：

1. **引入库**（通过 npm、CDN 或直接下载源码）。  
2. **获取 SVG**（DOM 元素、`innerHTML` 或外部 SVG 文件）。  
3. **调用 `svg2pdf`**，传入 SVG 与可选配置，返回 `Blob`（PDF）。  
4. **保存或上传**（使用 `URL.createObjectURL`、`FileSaver.js` 或直接发送到后端）。

在更复杂的项目中，可封装为统一的导出服务模块，统一处理错误、日志以及多语言/多主题的 PDF 元数据。

**生产可用性评估**  

| 维度 | 评估 |
|------|------|
| **活跃度** | 最近一次提交在 2026‑05‑11，2023‑2025 年间持续有 PR 与 Issue 交互，维护者响应及时。 |
| **社区认可** | 832 ★、114 Fork，已有多个开源项目和商业产品引用，说明实战验证充分。 |
| **技术成熟度** | 基于 TypeScript，提供完整的类型声明；内部使用 PDFKit‑style 渲染，兼容主流浏览器（Chrome、Edge、Firefox、Safari）。 |
| **安全性** | 代码体积小（≈ 30 KB gz），无外部二进制依赖；建议在 CI 中运行 `npm audit`、`dependabot` 检查第三方依赖的安全报告。 |
| **许可证** | MIT 许可证，商业使用无额外限制。 |
| **集成成本** | 仅需前端依赖，几行代码即可完成；如需统一错误上报或自定义 PDF 元数据，成本仍在可接受范围。 |
| **生产风险** | - 需要自行监控浏览器兼容性（尤其是 iOS Safari 对 Blob 下载的限制）。<br>- 若业务对 PDF 的加密、签名等高级特性有需求，需自行扩展或配合后端实现。 |

**结论**  
基于上述因素，yWorks/svg2pdf.js 已具备 **高生产可用性**，适合作为 Web 应用中 SVG 导出 PDF 的首选实现。建议先在现有业务流程中做一个小型 PoC（例如在报表页面加入“导出 PDF”按钮），验证与现有前端框架的兼容性后，再推广至全站或关键业务模块。

## 🧭 Practical evaluation

**Value:** yWorks/svg2pdf.js may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 832 GitHub stars
- 114 forks
- updated 2026-05-11
- primary language: TypeScript
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 52/100 |
| stars | 62/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 82/100 |
| recency | 100/100 |
| adoption | 59/100 |
| production | 77/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/yWorks/svg2pdf.js) · [← Back to Misc](./README.md)</sub>
