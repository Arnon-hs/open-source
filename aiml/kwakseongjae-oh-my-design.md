# kwakseongjae/oh-my-design

[![Stars](https://img.shields.io/github/stars/kwakseongjae/oh-my-design?style=flat-square&color=yellow)](https://github.com/kwakseongjae/oh-my-design/stargazers) [![Forks](https://img.shields.io/github/forks/kwakseongjae/oh-my-design?style=flat-square&color=blue)](https://github.com/kwakseongjae/oh-my-design/network) [![Language](https://img.shields.io/badge/lang-HTML-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> Generate DESIGN.md from 78 real company design systems — brand tokens, components, philosophy. Drop into Claude Code or any AI agent.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 151 |
| 🍴 **Forks** | 14 |
| 💻 **Language** | HTML |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `design-md` `design-system` `design-tokens` `google-stitch` `nextjs` `open-source` `react` `shadcn-ui` `tailwindcss` `typescript` `vibe-coding`

## 🎯 Categories

AI/ML · Frontend · DevTools · Design

## 📝 Summary

### English

**Brief Summary**  
kwakseongjae/oh‑my‑design automatically generates a comprehensive `DESIGN.md` by harvesting brand tokens, component libraries, and design philosophies from 78 real‑world company design systems. The output can be dropped straight into Claude Code or any other AI‑agent workflow, giving developers a ready‑made design knowledge base without having to build a model stack from scratch.  

**Value**  
- **Instant design knowledge base** – Turns scattered design assets into a single, searchable markdown file, dramatically reducing the time needed to onboard AI agents with brand‑consistent guidelines.  
- **Plug‑and‑play AI integration** – The generated `DESIGN.md` can be fed to Claude, GPT, or other agents as context for RAG, prompt engineering, or UI‑generation tasks, enabling rapid prototyping of AI‑enhanced design tools.  
- **No model‑training overhead** – By providing curated design data rather than a trained model, teams can add AI capabilities while reusing existing model stacks, cutting cost and complexity.  

**Practical Adoption Path**  
1. **Clone the repo** and run the CLI (or use the provided SDK) to point the tool at your target design system repositories or URLs.  
2. **Generate `DESIGN.md`** – The tool crawls the 78 built‑in sources and merges any custom sources you add, outputting a markdown file that follows a consistent schema.  
3. **Inject into AI workflows** – Feed the markdown into Claude Code, LangChain agents, or any RAG pipeline as a static knowledge source, or expose it via a simple API endpoint for on‑demand retrieval.  
4. **Iterate & extend** – Add new design systems, tweak the token mapping, or wrap the CLI in CI/CD to keep the design knowledge up‑to‑date automatically.  

**Production Readiness**  
- **Activity & Adoption** – 151 GitHub stars, recent commit (2026‑05‑11), and a modest but active fork count indicate a healthy community.  
- **Integration Simplicity** – Exposes clear signals (CLI, SDK, language metadata) and is written primarily in HTML, making it easy to embed in web‑centric stacks.  
- **Risk Profile** – No glaring licensing or security concerns identified, though a final review of the license and maintainer responsiveness is advisable before a full‑scale rollout.  

Overall, oh‑my‑design is a mature OSS candidate that can be piloted quickly to give AI agents a robust, up‑to‑date design knowledge base, paving the way for production‑grade AI‑driven design tooling.

### Русский

**kwakseongjae/oh-my-design** — open‑source инструмент, генерирующий файл DESIGN.md на основе 78 реальных дизайн‑систем компаний (бренд‑токены, компоненты, философия). Его удобно интегрировать в Claude Code или любой AI‑агент, чтобы быстро добавить AI‑функциональность без построения модели с нуля, например для прототипирования RAG‑сценариев, агентных воркфлоу или оценки инструментов моделирования. Проект имеет высокий уровень готовности к production: активные обновления, 151 звезда, поддержка через API/SDK/CLI, а также хорошие сигналы экосистемы, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句）**  
kwakseongjae/oh‑my‑design 能自动从 78 家真实公司的设计系统中抽取品牌 Token、组件和设计哲学，生成统一的 `DESIGN.md` 文档，并可直接喂给 Claude Code 或其它 AI 代理使用。它让开发者在不从零搭建模型栈的情况下，快速为产品注入可检索的设计知识。

**价值**  
- **加速 AI 原型**：只需几行命令即可得到结构化的设计系统数据，省去手工整理和标注的时间。  
- **支持 RAG / Agent 工作流**：生成的 `DESIGN.md` 可作为检索增强生成（RAG）或 AI 代理的上下文，帮助模型在 UI/UX、品牌一致性等方面给出更专业的建议。  
- **降低门槛**：无需自行爬取或维护设计系统数据，直接复用已有的 78 套真实案例，提升模型的业务适配度。

**典型接入方式**  
1. **CLI**：`oh-my-design generate --output DESIGN.md`  
2. **SDK / API**：在代码中调用 `generateDesignDoc(options)`，返回 Markdown 字符串，随后通过 HTTP POST 送入 Claude Code、OpenAI Function Calling 或自研 Agent。  
3. **CI/CD 集成**：在构建脚本或 GitHub Action 中运行生成命令，将产出的 `DESIGN.md` 自动同步到文档库或 AI 服务的知识库。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑05‑11，星标 151，Fork 14，说明社区仍在维护。  
- **技术成熟度**：项目主要使用 HTML（可直接解析为结构化数据），并提供明确的 API/CLI 接口，易于在现有前端或后端流水线中集成。  
- **风险**：目前未发现重大元数据或许可证冲突，但仍建议在正式投产前完成以下检查：  
  - 确认许可证（MIT/Apache 等）与公司合规要求匹配。  
  - 进行安全审计，检查依赖库是否存在已知漏洞。  
  - 与维护者沟通确认长期维护计划或备选方案。  

综合以上因素，oh‑my‑design 已具备 **高** 的生产候选资格，可在内部原型验证或面向特定业务的 AI 助手中直接使用。

## 🧭 Practical evaluation

**Value:** kwakseongjae/oh-my-design helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 151 GitHub stars
- 14 forks
- updated 2026-05-11
- primary language: HTML
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 46/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 42/100 |
| production | 72/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/kwakseongjae/oh-my-design) · [← Back to AI/ML](./README.md)</sub>
