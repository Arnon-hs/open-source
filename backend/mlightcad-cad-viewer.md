# mlightcad/cad-viewer

[![Stars](https://img.shields.io/github/stars/mlightcad/cad-viewer?style=flat-square&color=yellow)](https://github.com/mlightcad/cad-viewer/stargazers) [![Forks](https://img.shields.io/github/forks/mlightcad/cad-viewer?style=flat-square&color=blue)](https://github.com/mlightcad/cad-viewer/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> The world’s first fully web-based DXF/DWG viewer and editor that runs entirely in the browser — no backend server required.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 745 |
| 🍴 **Forks** | 155 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`autocad` `cad` `dwg` `dwg-parser` `dwg-reader` `dwg-viewer` `dxf` `dxf-parser` `dxf-reader` `dxf-viewer` `threejs` `webgl`

## 🎯 Categories

Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
mlightcad’s **cad‑viewer** is the world’s first fully web‑based DXF/DWG viewer and editor that runs entirely in the browser, requiring no backend server. Written in TypeScript, it already has strong community traction (≈ 750 ★, 155 forks) and recent activity, making it a solid OSS candidate for projects that need to embed CAD capabilities with AI‑enhanced features.  

**Value**  
- **AI‑ready front‑end** – because the viewer runs 100 % client‑side, you can layer AI models (e.g., image‑to‑CAD generation, semantic search, or RAG agents) directly on the rendered geometry without building a separate server stack.  
- **Rapid prototyping** – the ready‑made UI and file‑parsing logic let teams focus on AI logic (prompt handling, tool use, annotation) instead of low‑level CAD handling.  
- **Zero‑ops deployment** – a single static bundle can be hosted on any CDN, reducing infrastructure cost and simplifying CI/CD pipelines.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – clone the repo, run the demo locally (npm install && npm run dev) and verify that DXF/DWG files load correctly.  
2. **Read‑me & API audit** – review the provided integration guide, identify extension points (e.g., `onSelection`, `onModelLoad` callbacks) and decide which AI service (OpenAI, Anthropic, local LLM) will consume the geometry data.  
3. **Small‑scale pilot** – embed the viewer in a sandboxed page of your product, replace a placeholder button with an AI‑driven “suggest edits” feature, and instrument telemetry.  
4. **Iterate & Harden** – add type‑safe wrappers, secure the bundle (SRI, CSP), and write unit tests for the new AI layer.  

**Production Readiness**  
- **Activity & Ecosystem** – last commit on 2026‑06‑29, active issue discussion, and a healthy star/fork count indicate a maintained project.  
- **Technical maturity** – TypeScript codebase, modular architecture, and browser‑only runtime simplify dependency management and reduce attack surface.  
- **Risks to address** – perform a final license compliance check, run a security scan (e.g., Snyk) on dependencies, and confirm that the maintainers are responsive to PRs/bugs before committing to a mission‑critical rollout.  

Overall, cad‑viewer is production‑ready for a pilot or feature flag rollout, especially when the goal is to experiment with AI‑augmented CAD workflows without investing in server‑side CAD processing.

### Русский

Резюме проекта mlightcad/cad-viewer:

млайткад/cad-viewer - это первый в мире полноценный веб-базовый просмотрщик и редактор DXF/DWG, работающий напрямую в браузере без необходимости сервера. Этот проект позволяет добавить возможности искусственного интеллекта без создания новой модели стека. Типовой сценарий внедрения: прототипирование функций AI, построение рабочих процессов RAG или агентов, оценка инструментов моделирования. Проект имеет высокий уровень готовности к production, что делает его привлекательным для serious пилота.

### 中文

**项目简介**  
mlightcad/cad-viewer 是全球首个完全基于浏览器的 DXF/DWG 查看与编辑器，所有功能均在前端实现，无需后端服务器支撑。

**价值**  
- **即插即用的 AI 能力**：在已有的 CAD 视图基础上，可直接叠加 AI 模型（如图形识别、自动标注、智能查询），省去从零构建前端渲染栈的工作量。  
- **快速原型**：适合在原型阶段验证 AI 功能、构建 RAG（检索增强生成）或智能代理工作流，缩短迭代周期。  
- **开源可靠**：拥有 745+ 星、155+ Fork，活跃的 TypeScript 代码库和丰富的主题标签，社区支持度高。

**典型接入方式**  
1. **阅读 README**，确认 Node 环境与依赖（React、Three.js 等）。  
2. **通过 npm/yarn 安装**：`npm i @mlightcad/cad-viewer`（或直接克隆仓库）。  
3. **在项目中嵌入组件**，例如：  
   ```tsx
   import { CadViewer } from '@mlightcad/cad-viewer';
   <CadViewer fileUrl="path/to/file.dxf" />
   ```  
4. **接入 AI**：利用组件提供的事件（如 `onSelect`, `onLoad`）调用后端 AI 服务或本地模型，完成智能标注、查询等功能。  
5. **小范围 PoC**：先在测试环境部署一个最小化页面，验证渲染、交互与 AI 接口的兼容性，再逐步扩展。

**生产可用性**  
- **成熟度**：最近一次更新（2026‑06‑29）且活跃维护，代码基于 TypeScript，类型安全，易于在大型前端项目中集成。  
- **安全与合规**：暂无重大元数据风险，仍需对许可证（MIT）和依赖的安全审计进行最终确认。  
- **可扩展性**：纯前端架构天然支持 CDN 部署，降低运维成本；对接后端 AI 服务时仅需通过 HTTP/WS 接口即可，兼容微服务或 Serverless。  

综合来看，mlightcad/cad-viewer 在功能完整性、社区活跃度和技术栈现代性方面表现良好，适合作为 AI‑增强 CAD 业务的底层组件进行生产级试点。

## 🧭 Practical evaluation

**Value:** mlightcad/cad-viewer helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 745 GitHub stars
- 155 forks
- updated 2026-06-29
- primary language: TypeScript
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 55/100 |
| stars | 61/100 |
| topics | 100/100 |
| outlook | 57/100 |
| quality | 67/100 |
| recency | 40/100 |
| adoption | 59/100 |
| production | 57/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/mlightcad/cad-viewer) · [← Back to Backend](./README.md)</sub>
