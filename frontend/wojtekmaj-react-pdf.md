# wojtekmaj/react-pdf

[![Stars](https://img.shields.io/github/stars/wojtekmaj/react-pdf?style=flat-square&color=yellow)](https://github.com/wojtekmaj/react-pdf/stargazers) [![Forks](https://img.shields.io/github/forks/wojtekmaj/react-pdf?style=flat-square&color=blue)](https://github.com/wojtekmaj/react-pdf/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Display PDFs in your React app as easily as if they were images.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 11.1k |
| 🍴 **Forks** | 1k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`pdf` `pdf-viewer` `react`

## 🎯 Categories

Frontend

## 📝 Summary

### English

**Summary**  
`wojtekmaj/react-pdf` lets you render PDF documents in a React application with the same simplicity as embedding an image tag. With over 11 000 stars, active maintenance, and a TypeScript codebase, it’s a mature, community‑driven solution for adding PDF viewing capabilities to user‑facing interfaces.  

**Value**  
The library abstracts away the low‑level PDF rendering logic, letting teams ship UI features—such as document previews, invoices, or reports—without writing custom canvas or PDF.js wrappers. This accelerates product development, encourages reuse of a single, well‑tested component across multiple pages, and reduces the front‑end engineering effort needed to support PDF display.  

**Practical adoption path**  
1. **Prototype** – Install the package, import the `<Document>` and `<Page>` components, and replace static image placeholders with PDF previews in a sandbox branch.  
2. **Manual review** – Verify that the PDF rendering meets visual and performance expectations in your target browsers and that any required polyfills (e.g., for older Safari) are in place.  
3. **Security & licensing check** – Confirm the MIT license aligns with your policy and run a dependency scan (e.g., Snyk) to ensure no known vulnerabilities.  
4. **Integration** – Wrap the component in your design system (theme, loading states, error handling) and add unit/integration tests. Deploy to a staging environment for stakeholder sign‑off before rolling out to production.  

**Production readiness**  
The project scores high on production readiness: recent commits (as of 2026‑05‑12), strong community adoption, and a healthy fork/star ratio indicate active maintenance and a low risk of abandonment. While a final review of licensing, security posture, and maintainer responsiveness is still advisable, the library is robust enough for a serious pilot or full‑scale deployment in production front‑end stacks.

### Русский

**wojtekmaj/react-pdf** — это библиотека на TypeScript, позволяющая отображать PDF‑файлы в React‑приложениях так же просто, как изображения, что ускоряет создание пользовательских интерфейсов и снижает объём кастомного UI‑кода. Типичный сценарий — интеграция компонента в существующий фронтенд для быстрого вывода документов (например, счета, отчёты или справочники) без необходимости писать собственный рендерер PDF. Проект обладает высокой готовностью к production: активные коммиты, более 10 тыс. звёзд, широкое применение в сообществе, однако перед масштабным внедрением рекомендуется проверить лицензию, безопасность и наличие активных мейнтейнеров.

### 中文

**项目简介**  
`wojtekmaj/react-pdf` 是一个基于 TypeScript 的 React 组件库，能够像展示图片一样在 React 应用中直接渲染 PDF 文档，使用方式简洁、性能优秀。

**价值**  
- **降低前端开发成本**：无需自行实现 PDF 渲染或处理复杂的 Canvas/Worker 逻辑，直接复用成熟的组件即可完成 PDF 展示。  
- **提升交付速度**：在产品 UI 中快速嵌入文档预览、合同、报告等场景，减少自研 UI 工作量。  
- **生态兼容**：遵循 React 生态惯例，可与现有的 UI 框架（如 Material‑UI、Ant Design）无缝组合，复用已有的布局和样式系统。

**典型接入方式**  

```bash
# 安装
npm i @react-pdf/renderer   # 运行时依赖
npm i react-pdf             # 组件库
```

```tsx
import { Document, Page, pdfjs } from 'react-pdf';

// 必须显式指定 worker（可放在入口文件）
pdfjs.GlobalWorkerOptions.workerSrc = `//cdnjs.cloudflare.com/ajax/libs/pdf.js/${pdfjs.version}/pdf.worker.min.js`;

function PdfViewer({url}: {url: string}) {
  return (
    <Document file={url} onLoadSuccess={...}>
      <Page pageNumber={1} width={600} />
    </Document>
  );
}
```

- **核心步骤**：  
  1. 安装库并在项目入口配置 PDF.js worker。  
  2. 使用 `<Document>` 包裹 PDF 源（URL、Blob、ArrayBuffer 等），在内部通过 `<Page>` 渲染单页或多页。  
  3. 可配合 `onLoadSuccess`、`onError` 等回调实现进度条、错误提示等业务需求。

**生产可用性**  
- **活跃度**：截至 2026‑05‑12，项目最近一次提交，拥有 11 064 ⭐、1 003 forks，社区活跃度高。  
- **技术成熟度**：基于 Mozilla PDF.js，已在多个大型前端项目中使用，兼容主流浏览器（Chrome、Firefox、Edge）以及移动端 WebView。  
- **风险**：目前未发现重大许可证或安全漏洞；仍建议在正式上线前进行一次安全审计和兼容性验证（尤其是 worker 脚本的加载方式）。  
- **结论**：在经过基本的手动检查后，可视为 **高生产就绪度**，适合作为正式项目的 PDF 展示解决方案。

## 🧭 Practical evaluation

**Value:** wojtekmaj/react-pdf helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 11064 GitHub stars
- 1003 forks
- updated 2026-05-12
- primary language: TypeScript
- 3 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 75/100 |
| stars | 86/100 |
| topics | 38/100 |
| outlook | 78/100 |
| quality | 83/100 |
| recency | 100/100 |
| adoption | 83/100 |
| production | 78/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/wojtekmaj/react-pdf) · [← Back to Frontend](./README.md)</sub>
