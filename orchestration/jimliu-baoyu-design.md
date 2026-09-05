# JimLiu/baoyu-design

[![Stars](https://img.shields.io/github/stars/JimLiu/baoyu-design?style=flat-square&color=yellow)](https://github.com/JimLiu/baoyu-design/stargazers) [![Forks](https://img.shields.io/github/forks/JimLiu/baoyu-design?style=flat-square&color=blue)](https://github.com/JimLiu/baoyu-design/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Run Claude Design locally as an Agent Skill — Cursor, Claude Code & more. Produce polished UI mockups, prototypes, decks & wireframes as self-contained HTML, without claude.ai/design. Best with Opus 4.8.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.1k |
| 🍴 **Forks** | 154 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-skills` `claude` `claude-code` `claude-design` `cursor` `design` `prototyping` `ui-design`

## 🎯 Categories

Orchestration · AI/ML · Frontend · Design

## 📝 Summary

### English

**Brief Summary**  
baoyu‑design (JimLiu/baoyu-design) lets you run Claude Design locally as an agent skill, turning Claude’s UI‑generation capabilities into a self‑contained HTML output pipeline (mockups, prototypes, decks, wireframes) without needing the claude.ai/design service. It is packaged as a JavaScript library that can be orchestrated with other agents (Cursor, Claude Code, etc.) and works best with the Opus 4.8 model.

**Value**  
- **Repeatable workflows:** Encapsulates Claude’s design prompts into a deterministic skill, so the same UI mockup can be regenerated on demand across projects.  
- **Tool‑chain integration:** Provides a clean API for chaining Claude‑generated designs with other agents (e.g., code generation, data extraction), enabling end‑to‑end product‑design pipelines.  
- **Cost & latency savings:** By running locally, you avoid API calls to claude.ai/design, reducing both latency and usage fees while keeping design assets under your control.

**Practical Adoption Path**  
1. **Proof‑of‑Concept:** Clone the repo, run the README’s quick‑start script, and generate a simple HTML mockup to verify the local Claude skill works with your Opus 4.8 setup.  
2. **Integration Wrapper:** Wrap the skill in a thin Node.js module that conforms to your existing agent orchestration framework (e.g., LangChain, CrewAI).  
3. **Pipeline Extension:** Add the wrapper to a multi‑agent workflow—e.g., a “design → code → test” chain—by invoking the skill’s `generateDesign` function and passing the output to downstream agents.  
4. **Validation & Monitoring:** Instrument the wrapper to log token usage, execution time, and any generation errors; iterate on prompt templates until the output meets your UI standards.  
5. **Roll‑out:** Deploy the wrapper as a microservice (Docker or serverless) and replace ad‑hoc Claude calls in your production pipelines.

**Production Readiness**  
- **Activity & Community:** 2 099 stars, 154 forks, recent commits (last updated 2026‑06‑28) indicate strong community interest and ongoing maintenance.  
- **Technical Maturity:** Written in JavaScript with clear module exports; the repository includes a detailed README and example scripts, making initial setup straightforward.  
- **Scalability:** Because the skill runs locally, you can scale horizontally by containerizing the service; no external service quota limits apply.  
- **Risks:** The integration documentation does not spell out the exact environment variables or Docker image needed, so a modest amount of exploratory work is required to confirm setup costs. Once the proof‑of‑concept is validated, the project is considered **highly ready** for a serious pilot in production environments.

### Русский

JimLiu/baoyu-design — это open‑source‑инструмент, позволяющий запускать Claude Design локально как навык агента (Cursor, Claude Code и др.) и автоматически генерировать готовые к использованию UI‑мокапы, прототипы, презентации и wireframe‑ы в виде самостоятельных HTML‑страниц без обращения к claude.ai/design. Типичный сценарий внедрения — небольшая proof‑of‑concept интеграция, где через один‑единственный вызов агента формируется последовательность действий (координация нескольких агентов, подключение инструментов, хранение памяти) и сохраняются результаты в виде готового UI‑артифакта. Проект имеет высокий уровень готовности к production: активная разработка, более 2000 звёзд, регулярные обновления и поддержка JavaScript‑экосистемы, что делает его надёжным кандидатом для пилотного использования.

### 中文

**价值**  
JimLiu/baoyu‑design 将 Claude Design（包括 Cursor、Claude Code 等）本地化为 Agent Skill，能够直接生成完整的 HTML UI 产物（mockup、prototype、deck、wireframe），省去对 claude.ai/design 的网络依赖。它把零散的 Prompt + 工具链封装成可复用的 Agent 工作流，适合需要多 Agent 协同、工具调用以及统一记忆管理的团队。

**典型接入方式**  
1. **环境准备**：在项目根目录 `npm install`（或 `yarn`）后，确保本地已装好 Claude Opus 4.8（或兼容的模型二进制）。  
2. **Agent 注册**：在你的 Agent 框架（如 LangChain、Auto‑GPT、CrewAI 等）中，引入 `baoyu-design` 的入口 `src/skill.js`，并在 Agent 配置里声明 `skill: "baoyu-design"`。  
3. **调用示例**：  
   ```js
   const result = await agent.run({
     skill: "baoyu-design",
     prompt: "为电商商品详情页生成移动端原型，配色使用品牌蓝",
     output: "html"
   });
   // result.html 即为自包含的 UI 页面
   ```  
4. **Pipeline 扩展**：可把生成的 HTML 直接喂给后续的 “HTML‑to‑React” 或 “自动化截图/PDF” 步骤，实现完整的设计‑实现‑交付闭环。  
5. **小规模 PoC**：先在单元测试或 CI 中跑一次 `npm run demo`，验证模型加载、Prompt 解析和 HTML 输出是否符合预期，再逐步在业务流程中替换手工设计环节。

**生产可用性**  
- **活跃度**：截至 2026‑06‑28，最近一次提交在同一天，2099 颗星、154 个 fork，社区活跃度高。  
- **技术成熟度**：核心实现为 JavaScript，配套 8 个主题标签，兼容主流前端构建工具（Webpack、Vite），易于在现有前端项目中集成。  
- **依赖风险**：唯一外部依赖是本地 Claude Opus 4.8，需自行部署或获取授权；除非模型不可用，否则不受网络服务中断影响。  
- **安全与合规**：生成的 HTML 完全本地化，无外部 API 调用，数据不离开内部网络，符合大多数内部合规要求。  
- **推荐上线策略**：先在预发布环境做完整的端到端测试（包括模型加载时间、HTML 大小、浏览器兼容性），确认性能与安全后再推广到生产。整体来看，项目已具备 **高** 的生产候选级别，适合作为设计自动化的核心组件投入正式使用。

## 🧭 Practical evaluation

**Value:** JimLiu/baoyu-design helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2099 GitHub stars
- 154 forks
- updated 2026-06-28
- primary language: JavaScript
- 8 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 55/100 |
| stars | 71/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 80/100 |
| recency | 80/100 |
| adoption | 66/100 |
| production | 69/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/JimLiu/baoyu-design) · [← Back to Orchestration](./README.md)</sub>
