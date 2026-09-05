# asciidoctor/asciidoctor-vscode

[![Stars](https://img.shields.io/github/stars/asciidoctor/asciidoctor-vscode?style=flat-square&color=yellow)](https://github.com/asciidoctor/asciidoctor-vscode/stargazers) [![Forks](https://img.shields.io/github/forks/asciidoctor/asciidoctor-vscode?style=flat-square&color=blue)](https://github.com/asciidoctor/asciidoctor-vscode/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> AsciiDoc support for Visual Studio Code using Asciidoctor

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 368 |
| 🍴 **Forks** | 109 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`asciidoc` `asciidoctor` `hacktoberfest` `vscode` `vscode-extension`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
The *asciidoctor‑vscode* extension brings full‑featured AsciiDoc editing to Visual Studio Code by leveraging the Asciidoctor engine. It provides live preview, syntax highlighting, IntelliSense for AsciiDoc directives, and seamless integration with the VS Code UI, making it a convenient tool for developers and technical writers who already work in VS Code. With 368 ★ and active updates (last commit 2026‑06‑23), it is a mature, community‑driven project written in TypeScript.

**Value**  
- **Productivity boost**: Write, preview, and validate AsciiDoc documents without leaving the editor, eliminating context‑switching.  
- **Consistency**: Uses the same Asciidoctor engine that powers many documentation pipelines, ensuring that what you see locally matches the final rendered output.  
- **Extensibility**: The TypeScript codebase and open‑source license make it easy to add custom macros or integrate with CI/CD pipelines.

**Practical adoption path**  
1. **Proof‑of‑concept** – Install the extension in a sandbox VS Code workspace and validate that the live preview renders your existing AsciiDoc files correctly.  
2. **Readme & workflow check** – Review the repository’s README for configuration options (e.g., custom attributes, PDF generation) and align them with your documentation workflow.  
3. **Pilot** – Roll the extension out to a small team or a single project, collecting feedback on performance, required settings, and any missing features.  
4. **Scale** – Once the pilot is stable, standardize the extension in your organization’s VS Code configuration (e.g., via workspace settings or a shared devcontainer) and integrate it with your build pipeline if you generate PDFs or HTML as part of CI.

**Production readiness**  
The project sits at a **medium** readiness level: it is feature‑complete for typical AsciiDoc authoring and actively maintained, making it suitable for prototypes, internal documentation sites, or as a stepping stone to a full documentation pipeline. Before production use, perform the usual due‑diligence steps—verify the MIT‑style license compatibility, run a security scan of the dependency tree, and confirm that a maintainer is responsive to issues. With those checks in place, the extension can be trusted for internal workflows and, with proper testing, for external‑facing documentation.

### Русский

**asciidoctor/asciidoctor-vscode** — это расширение для Visual Studio Code, предоставляющее полноценную поддержку AsciiDoc через движок Asciidoctor. Оно удобно для разработки технической документации и прототипирования внутри IDE: достаточно установить расширение, открыть *.adoc*‑файлы и пользоваться подсветкой синтаксиса, автодополнением и предпросмотром в реальном времени. Готовность к production — средняя: проект достаточно популярен (368 ★, 109 forks), активно обновляется (последний коммит 2026‑06‑23) и написан на TypeScript, но перед масштабным внедрением следует проверить лицензирование, безопасность зависимостей и наличие активных мейнтейнеров.

### 中文

**项目简介（2‑3 句）**  
asciidoctor/asciidoctor‑vscode 是一款基于 Asciidoctor 的 VS Code 扩展，为编辑和预览 AsciiDoc 文档提供语法高亮、实时渲染、代码片段、链接校验等功能，让开发者在 VS Code 中即可完成完整的 AsciiDoc 编写与预览工作流。

**价值**  
- **提升编辑效率**：在熟悉的 VS Code 环境中直接获得 AsciiDoc 的智能感知、自动补全和即时预览，省去切换工具的时间。  
- **统一技术栈**：采用 TypeScript 实现，便于在前端/Node.js 项目中统一依赖管理和二次扩展。  
- **社区与生态**：已有 368+ ⭐、109+ 🍴，活跃的社区提供插件、主题和问题解答，降低学习成本。

**典型接入方式**  
1. **VS Code 市场安装**：在 VS Code 插件市场搜索 “AsciiDoc” 或直接执行 `code --install-extension asciidoctor.asciidoctor-vscode`。  
2. **项目级配置**（可选）：在工作区根目录添加 `.vscode/settings.json`，如  
   ```json
   {
     "asciidoc.preview.command": "asciidoctor",
     "asciidoc.extensions": ["asciidoctor-diagram"]
   }
   ```  
   这样可以指定使用本地的 Asciidoctor CLI 或额外扩展。  
3. **CI/CD 集成**：在构建脚本中使用 `asciidoctor`（npm 包 `@asciidoctor/core`）或 Docker 镜像生成 PDF/HTML，确保文档在 CI 中自动生成，VS Code 插件仅负责本地编辑体验。  

**生产可用性**  
- **成熟度**：中等（Medium）。插件已持续更新至 2026‑06‑23，代码量适中且依赖明确，适合作为内部或原型项目的文档工具。  
- **准备工作**：在正式生产环境使用前，建议进行以下检查：  
  1. **许可证合规**：确认 MIT 许可证符合贵司开源使用政策。  
  2. **安全审计**：审查插件依赖的 npm 包（尤其是 `asciidoctor`、`asciidoctor-diagram`）是否存在已知漏洞。  
  3. **维护者活跃度**：查看最近的 Issue/PR 响应速度，确保在出现问题时能得到社区或维护者的及时支持。  
- **适用场景**：适合技术文档、内部手册、API 文档等需要 AsciiDoc 编写的业务；不建议直接用于高并发的文档生成服务，建议在生产流水线中使用 Asciidoctor CLI 或 Docker 镜像进行离线渲染。  

综上，asciidoctor‑vscode 可快速提升团队的 AsciiDoc 编写体验，接入成本低，经过适当的安全与合规审查后即可在内部或原型项目中投入使用。若需大规模、自动化的文档生成，建议配合 Asciidoctor CLI 或容器化方案作为后端渲染引擎。

## 🧭 Practical evaluation

**Value:** asciidoctor/asciidoctor-vscode may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 368 GitHub stars
- 109 forks
- updated 2026-06-23
- primary language: TypeScript
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 55/100 |
| topics | 63/100 |
| outlook | 66/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 54/100 |
| production | 68/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/asciidoctor/asciidoctor-vscode) · [← Back to Misc](./README.md)</sub>
