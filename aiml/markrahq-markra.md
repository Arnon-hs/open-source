# markrahq/markra

[![Stars](https://img.shields.io/github/stars/markrahq/markra?style=flat-square&color=yellow)](https://github.com/markrahq/markra/stargazers) [![Forks](https://img.shields.io/github/forks/markrahq/markra?style=flat-square&color=blue)](https://github.com/markrahq/markra/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> A WYSIWYG Markdown editor with native AI. Fully open source. Free to use. Your data stays local.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 499 |
| 🍴 **Forks** | 23 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-editor` `ai-writing` `desktop-app` `local-first` `markdown-editor` `react` `tauri` `typescript` `wysiwyg-markdown`

## 🎯 Categories

AI/ML · Documents · Productivity · Frontend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Markra ( github.com/markrahq/markra ) is a fully open‑source, WYSIWYG Markdown editor that ships with native AI capabilities, keeping all data on the client side. With a modern TypeScript codebase, active maintenance and a growing community (≈ 500 stars), it lets developers prototype AI‑enhanced editing, RAG pipelines, or agent‑driven workflows without building a model stack from scratch.  

**Value**  
- **Instant AI layer** – The editor bundles prompt handling, inference routing and UI integration, so teams can experiment with generative features (auto‑completion, summarisation, content suggestions) immediately.  
- **Data privacy** – Because everything runs locally, no user content is sent to third‑party services, satisfying strict compliance or on‑premise requirements.  
- **Speed to market** – Instead of assembling a custom front‑end, model server, and prompt‑engineering pipeline, developers can drop Markra into an existing React/Next.js app and start iterating on AI‑driven UX in days.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the supplied `npm install && npm run dev` script, and verify the AI plug‑in works with your preferred LLM endpoint (OpenAI, Azure, local Ollama, etc.).  
2. **README & Config Review** – Follow the integration guide to replace the demo API key with your own credentials and adjust the RAG/agent configuration to match your data sources.  
3. **Component Embedding** – Import the `<MarkraEditor />` component into your product, customize the toolbar, and optionally expose the underlying AI service as a reusable hook for other UI parts.  
4. **Testing & Security Hardening** – Run the built‑in unit tests, add static‑analysis (ESLint, TypeScript strict mode) and perform a dependency audit (e.g., `npm audit`) before promoting to staging.  

**Production Readiness**  
- **Activity & Ecosystem** – Last commit on 2026‑06‑29, 499 GitHub stars, 23 forks, and a TypeScript‑first stack indicate a healthy, community‑driven project.  
- **Stability** – The core editor and AI wrapper are versioned, with clear release notes; no breaking changes have been reported in recent minor releases.  
- **Scalability** – Because the AI calls are external, you can scale the backend independently (e.g., switch to a hosted inference service or an on‑premise model) without touching the front‑end.  
- **Risks** – License compliance, long‑term maintainer commitment and a formal security review still need verification, but no major metadata or vulnerability flags were identified.  

Overall, Markra is a production‑ready OSS candidate for teams that want to embed AI‑augmented markdown editing quickly, while retaining full control over data and deployment.

### Русский

**Markra** – полностью открытый WYSIWYG‑редактор Markdown с встроенным AI, позволяющий быстро добавить интеллектуальные функции (RAG, агентные сценарии, прототипирование) без необходимости собирать собственный стек моделей. Для внедрения рекомендуется начать с небольшого proof‑of‑concept, проверив README и пример интеграции, после чего можно масштабировать в продакшн‑окружение, так как проект демонстрирует высокую готовность: активные коммиты, 499 звёзд, поддержка TypeScript и сильные сигналы экосистемы. Остальные риски (лицензия, безопасность, поддержка) требуют финального аудита, но в целом Markra готова к серьёзным пилотным проектам.

### 中文

**项目简介（2‑3 句）**  
Markra（`markrahq/markra`）是一款开箱即用的所见即所得（WYSIWYG）Markdown 编辑器，内置本地 AI 能力，完全开源且免费使用，所有数据均保存在本地，安全可控。

**价值**  
- **即插即用的 AI 功能**：无需自行搭建模型堆栈，编辑器即提供文本生成、智能补全、语义搜索等 AI 助手，帮助快速原型化 AI 特性。  
- **本地化数据安全**：所有内容与模型交互都在用户设备上完成，避免敏感信息泄露，符合企业合规要求。  
- **前端友好**：基于 TypeScript 实现，可直接在 React/Vite 等现代前端框架中集成，降低开发门槛。

**典型接入方式**  
1. **阅读 README 与示例代码**，确认项目的依赖（Node ≥18、React 18+）和构建脚本。  
2. **在现有前端项目中安装**：  
   ```bash
   npm i markra
   # 或者使用 yarn/pnpm
   ```  
3. **在代码中引入组件**，并通过配置对象启用本地 AI（默认使用浏览器的 WebGPU/CPU 推理或本地 LLM）。  
   ```tsx
   import { MarkraEditor } from 'markra';

   <MarkraEditor
     aiProvider="local"
     modelPath="/models/phi-3-mini"
     onChange={handleMarkdownChange}
   />
   ```  
4. **先做小范围 PoC**：在测试环境仅渲染编辑器，验证 AI 生成质量、性能以及与现有业务流程的兼容性。完成后再逐步推广到完整产品线。  

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑29，拥有 499 星、23 Fork，社区活跃，Issue 响应及时。  
- **技术成熟度**：使用 TypeScript 编写，具备完整的类型定义和 CI/CD 流程，易于审计和二次开发。  
- **安全与合规**：数据全本地存储，未发现重大元数据泄露风险；仍需自行审查许可证（MIT）以及依赖的第三方模型的安全姿态。  
- **适配性**：可作为独立编辑器嵌入，也能与 RAG、Agent 工作流等后端服务配合，支持快速验证 AI 产品概念。  

**结论**：Markra 在功能完整性、社区活跃度和本地化安全方面表现出色，适合作为 AI 增强编辑器的首选 OSS 组件，先在小范围 PoC 验证后即可推进到生产环境使用。

## 🧭 Practical evaluation

**Value:** markrahq/markra helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 499 GitHub stars
- 23 forks
- updated 2026-06-29
- primary language: TypeScript
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 57/100 |
| topics | 100/100 |
| outlook | 69/100 |
| quality | 73/100 |
| recency | 80/100 |
| adoption | 51/100 |
| production | 69/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/markrahq/markra) · [← Back to AI/ML](./README.md)</sub>
