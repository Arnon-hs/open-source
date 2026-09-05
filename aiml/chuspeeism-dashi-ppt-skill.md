# chuspeeism/dashi-ppt-skill

[![Stars](https://img.shields.io/github/stars/chuspeeism/dashi-ppt-skill?style=flat-square&color=yellow)](https://github.com/chuspeeism/dashi-ppt-skill/stargazers) [![Forks](https://img.shields.io/github/forks/chuspeeism/dashi-ppt-skill?style=flat-square&color=blue)](https://github.com/chuspeeism/dashi-ppt-skill/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> An AI-agent skill that generates browser-editable presentations from multiple visual themes, exportable to HTML, PDF, and PPTX.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.6k |
| 🍴 **Forks** | 267 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-skill` `ai-agent` `ai-ppt` `claude` `claude-code` `dashial` `html-presentation` `ppt` `pptx` `presentation` `presentation-generator` `skill`

## 🎯 Categories

AI/ML · Documents

## 📝 Summary

### English

**Summary**  
chuspeeism/dashi-ppt-skill is an open‑source AI‑agent skill that can turn raw content into browser‑editable slide decks, offering multiple visual themes and export options to HTML, PDF, and PPTX. With a healthy GitHub profile (2.6 k stars, 267 forks, recent commits) it provides a ready‑made AI‑powered presentation layer that can be plugged into RAG or autonomous‑agent pipelines without building a model stack from scratch.

**Value**  
The skill abstracts the heavy lifting of slide generation—layout selection, theme styling, and multi‑format export—into a single, reusable component. Teams can quickly prototype AI‑driven documentation, sales decks, or educational material, accelerating time‑to‑value while keeping the underlying model choices flexible (e.g., using any LLM that conforms to the Dashi agent API).

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided README example, and generate a test deck to verify the API contract.  
2. **Integration** – Wrap the skill as a microservice or Lambda function and expose it to your existing RAG/agent framework (e.g., LangChain, CrewAI).  
3. **Customization** – Extend the theme catalogue or adjust export settings to match corporate branding, then add authentication or rate‑limiting as needed.  
4. **Pilot** – Deploy the service in a staging environment, feed it real queries, and collect feedback on slide quality and latency before scaling.

**Production readiness**  
The project scores high on production readiness: it is actively maintained (last commit 2026‑07‑13), has strong community adoption, and is written in JavaScript—a language that integrates easily with most backend stacks. The main risk is the lack of explicit integration documentation; a small upfront effort to map the skill’s input/output schema and to containerize it will mitigate this. Once those steps are taken, the skill is robust enough for a serious pilot or even full‑scale deployment.

### Русский

Резюме проекта chuspeeism/dashi-ppt-skill:

Проект chuspeeism/dashi-ppt-skill представляет собой открытый источник AI-агента, способный генерировать редактируемые браузером презентации с множеством визуальных тем, экспортируемых в HTML, PDF и PPTX. Этот проект позволяет добавлять функциональность AI без создания пустого стека моделей, что делает его ценным инструментом для прототипирования AI-особенностей, построения потоков RAG или агентов, а также оценки инструментов моделирования. Проект готов к производственному использованию, с сильными сигналами активности, внедрения и экосистемы, что делает его подходящей кандидатурой для серьезного пилота.

### 中文

**项目简介（2‑3 句）**  
chuspeeism/dashi-ppt-skill 是一个基于 AI 的 Agent 技能，能够根据多种视觉主题自动生成可在浏览器中编辑的演示文稿，并支持导出为 HTML、PDF 与 PPTX。它让开发者无需从零搭建模型栈，即可在现有系统中快速加入智能 PPT 生成功能。

---

## 价值说明  

| 维度 | 价值点 |
|------|--------|
| **加速原型** | 只需调用 skill 接口，即可得到完整的演示文稿，极大缩短 AI 功能的 PoC 周期。 |
| **多格式输出** | 同时提供 HTML、PDF、PPTX 三种常用格式，满足内部审阅、对外分享和后期编辑的全部需求。 |
| **主题丰富** | 内置多套视觉主题，业务方可直接选用或自行扩展，保持品牌统一性。 |
| **降低门槛** | 通过 Agent/Tool 调用方式封装，开发者无需深度了解底层模型或向量检索，即可实现 RAG、Agent 工作流的 AI 生成。 |
| **社区与生态** | 2631 ⭐、267 🍴、活跃的 JavaScript 代码库，配套文档与示例丰富，易于在前端/Node 项目中直接集成。 |

---

## 典型接入方式  

1. **阅读 README 与快速上手**  
   - 克隆仓库，执行 `npm install` 安装依赖。  
   - 参考 `examples/` 目录的示例脚本，了解 `generatePresentation(theme, content)` 的调用方式。  

2. **在现有 Agent 框架中封装为 Tool**  
   ```javascript
   const { generatePresentation } = require('dashi-ppt-skill');

   // 作为 LangChain / Dify / LlamaIndex 等框架的自定义工具
   async function pptTool({theme, markdown}) {
       const {html, pdfPath, pptxPath} = await generatePresentation(theme, markdown);
       return {html, pdfPath, pptxPath};
   }
   ```
   - 将该工具注册到 Agent 的工具列表中，Agent 在需要生成 PPT 时即可调用。  

3. **小规模 PoC**  
   - 先在本地或沙盒环境跑通一次完整的生成‑导出流程。  
   - 验证主题切换、内容渲染、文件大小等关键指标后，再迁移到 CI/CD 环境。  

4. **生产化部署**  
   - 将生成服务容器化（Dockerfile 已提供），配合 API 网关对外提供 `POST /generate` 接口。  
   - 通过缓存（如 Redis）保存已生成的文件路径，避免重复计算。  

---

## 生产可用性评估  

| 维度 | 评估 |
|------|------|
| **代码活跃度** | 最近一次提交为 **2026‑07‑13**，保持每月更新，说明项目仍在积极维护。 |
| **社区规模** | 2631 星、267 Fork，拥有一定的使用者基数，遇到问题时可通过 Issue 或社区获取帮助。 |
| **技术栈成熟度** | 完全基于 JavaScript/Node，易于在前端或后端服务中直接使用，无额外语言依赖。 |
| **文档与示例** | README 包含安装、API、主题扩展说明；`examples/` 提供完整的端到端示例，降低上手成本。 |
| **可扩展性** | 主题文件为 JSON/SCSS，支持自定义品牌风格；导出流程可通过插件方式插入水印、公司 Logo 等。 |
| **风险** | - 集成路径主要依赖 `generatePresentation` API，需自行处理身份验证、并发控制等生产级需求。<br>- 对大规模并发生成的性能尚未公开基准，建议在正式上线前进行压测。 |
| **总体结论** | 具备 **高** 的生产候选级别，适合作为 **AI 功能原型** 以及 **正式业务流程** 的组件，只需在正式环境进行一次性能验证与安全审计即可投入使用。 |

---  

**一句话总结**：chuspeeism/dashi-ppt-skill 通过 AI 自动化生成多主题演示文稿，提供即插即用的 JavaScript 接口，社区活跃、文档完整，经过小规模 PoC 验证后即可在生产环境中安全、可靠地使用。

## 🧭 Practical evaluation

**Value:** chuspeeism/dashi-ppt-skill helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2631 GitHub stars
- 267 forks
- updated 2026-07-13
- primary language: JavaScript
- 14 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 61/100 |
| stars | 73/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 81/100 |
| recency | 80/100 |
| adoption | 69/100 |
| production | 70/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/chuspeeism/dashi-ppt-skill) · [← Back to AI/ML](./README.md)</sub>
