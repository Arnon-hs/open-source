# regyssilveira/RadIA-Plugin

[![Stars](https://img.shields.io/github/stars/regyssilveira/RadIA-Plugin?style=flat-square&color=yellow)](https://github.com/regyssilveira/RadIA-Plugin/stargazers) [![Forks](https://img.shields.io/github/forks/regyssilveira/RadIA-Plugin?style=flat-square&color=blue)](https://github.com/regyssilveira/RadIA-Plugin/network) [![Language](https://img.shields.io/badge/lang-Pascal-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Assistente de IA avançado para a IDE Embarcadero Delphi (usando Open Tools API) com chat acoplável VCL/WebView2, streaming SSE e refatoração visual. 🇧🇷 (English docs available in README.en.md 🇺🇸)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 24 |
| 🍴 **Forks** | 7 |
| 💻 **Language** | Pascal |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-assistent` `claude` `codex` `deepseek` `delphi` `delphi-ide` `gemini` `groq` `object-pascal` `ollama` `open-tools-api` `pascal`

## 🎯 Categories

AI/ML · Backend

## 📝 Summary

### English

**Brief Summary**  
RadIA‑Plugin is an advanced AI assistant that plugs into the Embarcadero Delphi IDE via the Open Tools API. It offers a detachable VCL/WebView2 chat UI, Server‑Sent Events (SSE) streaming, and visual refactoring tools, letting developers embed generative‑AI capabilities directly into their Delphi workflow. (Documentation is available in Portuguese and English.)

**Value Proposition**  
- **Accelerated AI integration** – developers can add conversational and code‑generation features to Delphi projects without building a model stack from scratch.  
- **Rich IDE experience** – the VCL‑based chat and visual refactoring panels work natively inside the IDE, reducing context‑switching.  
- **Extensible architecture** – the plugin exposes APIs/SDKs and a CLI, making it easy to hook up custom LLM back‑ends, Retrieval‑Augmented Generation (RAG) pipelines, or autonomous agents.

**Practical Adoption Path**  
1. **Clone & build** – the repository is a standard Pascal project; compile it with Delphi’s compiler and install the resulting BPL into the IDE.  
2. **Configure the AI back‑end** – set the endpoint, API key, and optional SSE streaming URL in the provided `RadIA.Config.json`.  
3. **Enable the UI** – choose between the native VCL chat window or the embedded WebView2 browser panel, depending on UI preferences.  
4. **Prototype** – start by using the built‑in chat for code suggestions, then experiment with the visual refactoring actions (e.g., rename, extract method).  
5. **Extend** – leverage the exposed SDK/CLI to add custom prompts, integrate a private model, or connect a RAG knowledge base.

**Production‑Readiness Assessment**  
- **Maturity**: Medium. The plugin is functional and actively updated (last commit 2026‑06‑23) and has modest community traction (24 ★, 7 forks).  
- **Strengths**: Clear integration points (API/SDK/CLI), native IDE UI, streaming support, and multilingual docs.  
- **Caveats**:  
  * **Dependency management** – relies on WebView2 and specific Delphi versions; these must be validated in the target environment.  
  * **Security & licensing** – the repository does not yet expose a formal security audit or a permissive license review; organizations should perform their own vetting.  
  * **Maintenance** – only a single maintainer is visible; consider a fallback plan for long‑term support.  
- **Fit for production**: Suitable for internal tools, prototypes, or controlled‑release features after a short validation sprint. For public‑facing or mission‑critical products, conduct additional security testing, lock down dependency versions, and possibly fork the repo to guarantee maintenance.

### Русский

**RadIA‑Plugin** — это расширяемый плагин‑ассистент ИИ для среды Embarcadero Delphi, реализованный через Open Tools API и предоставляющий чат на VCL/WebView2, потоковое SSE‑сообщение и визуальную рефакторинг‑поддержку. Он позволяет быстро добавить функции генеративного ИИ (прототипы, RAG‑агенты, оценка моделей) в существующие проекты без необходимости строить собственный стек, при этом интеграция проста: доступны API/SDK/CLI и метаданные языка. Готовность к продакшну — средняя: плагин подходит для прототипов и внутренних воркфлоу, но перед выпуском в продакшн требуется проверка лицензии, безопасности и актуальности поддержки.

### 中文

**项目简介**  
RadIA‑Plugin 是一款面向 Embarcadero Delphi IDE 的高级 AI 助手插件，基于 Open Tools API 实现。它提供可嵌入的 VCL/WebView2 聊天窗口、SSE 流式响应以及可视化代码重构功能，帮助开发者在 Delphi 环境中直接使用 LLM（支持 RAG 与 Agent 工作流）。  

**价值**  
- **快速赋能**：无需自行搭建模型堆栈，直接在 Delphi 中调用聊天、代码生成和重构等 AI 能力。  
- **原型友好**：适合验证 AI 功能、构建 RAG/Agent 流程或内部工具原型，极大缩短概念验证周期。  
- **跨平台 UI**：通过 VCL 与 WebView2 双模式实现，既能在传统桌面窗口中使用，也可在嵌入式浏览器中呈现更丰富的交互界面。  

**典型接入方式**  
1. **插件安装**：将源码编译为 Delphi 包（*.bpl），通过 IDE 的 *Component → Install Packages* 完成插件注册。  
2. **API/SDK 调用**：插件公开的 Pascal 接口（如 `TRadIAChat.StartSession`, `TRadIARefactor.Apply`）可在项目代码中直接调用，也支持命令行/CLI 方式启动 AI 会话。  
3. **配置**：在 `RadIA.config.json` 中填写 OpenAI、Claude、Gemini 等 LLM 的 API Key 与模型参数，支持自定义后端（如本地 Ollama）以及 RAG 数据源。  

**生产可用性**  
- **成熟度**：当前在 GitHub 上拥有 24 ★、7 Fork，最近一次提交于 2026‑06‑23，代码基于 Pascal，适合 Delphi 10.4 及以上版本。  
- **适用场景**：非常适合作为内部工具、原型或研发阶段的 AI 辅助；在生产环境使用前需评估以下因素：  
  - **依赖管理**：插件依赖 WebView2 运行时和外部 LLM 服务，需确保网络连通性和许可证合规。  
  - **安全与合规**：审查所调用的模型服务的隐私政策、数据加密以及插件本身的许可证（默认 MIT），确认符合企业合规要求。  
  - **维护成本**：项目维护者活跃度一般，建议自行 fork 并制定内部升级策略，以应对未来 API 变更或安全补丁。  

综上，RadIA‑Plugin 为 Delphi 开发者提供了一条“即插即用”的 AI 能力路径，适合快速原型和内部工具开发；在正式生产环境部署前，需完成依赖、合规和维护三方面的审查与准备。

## 🧭 Practical evaluation

**Value:** regyssilveira/RadIA-Plugin helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 24 GitHub stars
- 7 forks
- updated 2026-06-23
- primary language: Pascal
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 23/100 |
| stars | 30/100 |
| topics | 100/100 |
| outlook | 56/100 |
| quality | 52/100 |
| recency | 40/100 |
| adoption | 28/100 |
| production | 54/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/regyssilveira/RadIA-Plugin) · [← Back to AI/ML](./README.md)</sub>
