# KorroAi/drunk-claude

[![Stars](https://img.shields.io/github/stars/KorroAi/drunk-claude?style=flat-square&color=yellow)](https://github.com/KorroAi/drunk-claude/stargazers) [![Forks](https://img.shields.io/github/forks/KorroAi/drunk-claude?style=flat-square&color=blue)](https://github.com/KorroAi/drunk-claude/network) [![Language](https://img.shields.io/badge/lang-TeX-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> Intensity slider from tipsy (0.1) to blackout (1.0). 5 moods, 8 creative techniques. Lowers inhibition, not intelligence. Unfiltered genius for Claude Code.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 165 |
| 🍴 **Forks** | 9 |
| 💻 **Language** | TeX |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-skills` `ai-tools` `brainstorming` `chaos-engineering` `claude` `claude-code` `creative-ai` `creative-coding` `creativity` `developer-tools` `fun` `ideation`

## 🎯 Categories

AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
KorroAi’s *drunk‑claude* adds an “intoxication” slider to Claude‑based code generation, letting users dial the model’s creativity from a mild “tipsy” (0.1) to a full‑blown “blackout” (1.0) across five moods and eight creative techniques. The tool lowers inhibition without sacrificing intelligence, offering an unfiltered “genius” mode that can be dropped into existing Claude workflows. It’s positioned as a quick way to enrich AI‑powered prototypes without rebuilding a model stack from scratch.  

---

### Value Proposition  
- **Instant creativity boost** – The intensity slider makes it trivial to explore more daring or unconventional code suggestions, which is especially useful during brainstorming or early‑stage prototyping.  
- **Low‑effort integration** – Because it sits on top of Claude’s API rather than requiring a custom model, teams can add the feature with a few dependency installs and a single configuration change.  
- **Versatile use cases** – Ideal for rapid prototyping of AI‑enhanced features, building Retrieval‑Augmented Generation (RAG) pipelines, or testing agent‑style workflows where “outside‑the‑box” thinking is valuable.  

### Practical Adoption Path  
1. **Proof‑of‑Concept (PoC)** – Clone the repo, run the provided README example, and verify that the slider API works with your Claude endpoint.  
2. **Sandbox Integration** – Wrap the slider logic in a thin service layer (e.g., a Flask or FastAPI endpoint) and plug it into a non‑production feature branch of your product.  
3. **Evaluation** – Compare output quality, latency, and token usage across the five moods and eight techniques to decide which intensity levels are useful for your domain.  
4. **Gradual Rollout** – Expose the selected intensity settings to a limited user group or internal team, gathering feedback before wider deployment.  

### Production Readiness  
- **Maturity**: Medium. The project has modest community traction (≈165 ★, recent updates) and is primarily written in TeX, which suggests the core logic is lightweight but may lack extensive test coverage.  
- **Dependencies**: Verify compatibility with your Claude client library and audit any third‑party packages for security and licensing.  
- **Maintenance**: With only a handful of forks, long‑term maintenance will likely fall on your team; consider forking and adding CI tests if you plan to keep it in production.  
- **Risk Mitigation**: Because the integration path isn’t fully documented, allocate time for a small setup validation (e.g., “does the slider config map cleanly to Claude’s `temperature` and `top_p` parameters?”). Once the PoC passes, the component is suitable for internal tools or beta features, but a thorough reliability review is advisable before mission‑critical deployment.

### Русский

Резюме проекта KorroAi/drunk-claude:

КorroAi/drunk-claude - это утилита, позволяющая добавить функциональность AI в проекты без необходимости начинать с полной реализации модели. Этот проект особенно полезен для прототипирования функций AI и построения рабочих процессов RAG или агентов. Проект имеет средний уровень готовности к production, что означает, что он может быть полезен для внутренних рабочих процессов или прототипирования, но требует тщательного проверки и поддержки перед внедрением в производство.

### 中文

**项目简介**  
KorroAi/drunk‑claude 提供了一个“醉度”滑块（0.1 ~ 1.0）和 5 种情绪、8 种创意技术，让 Claude‑Code 在降低抑制的同时保持原有智能，从而输出更“无滤镜”的创意代码。它可以直接在现有模型堆栈上叠加，省去从零训练模型的成本。

**价值**  
- **快速原型**：只需几行配置即可为产品或内部工具注入 AI 能力，适合 RAG、Agent 工作流等实验。  
- **多样创意**：通过调节醉度和情绪，获得从轻度灵感到“黑洞”式爆发的代码生成，帮助团队突破思维定式。  
- **低成本**：不需要自行训练或部署大型模型，直接调用 Claude‑Code 即可使用，降低算力和运维开销。

**典型接入方式**  
1. **阅读 README**，确认依赖（主要是 TeX 环境和 Claude‑API）。  
2. **创建小型 PoC**：在本地或 CI 中安装仓库，配置 `CLAUDE_API_KEY`，调用 `drunk_claude.run(intensity, mood, technique)` 获得代码输出。  
3. **集成到业务**：将 PoC 包装为内部微服务或 CLI，结合现有 RAG/Agent 框架（如 LangChain）进行调用。  
4. **验证与调优**：通过单元测试和用户反馈，微调 `intensity`、`mood`、`technique` 参数，以匹配业务需求。

**生产可用性**  
- **成熟度**：GitHub 165 ★、最近更新（2026‑06‑27），代码质量尚可，但主要语言为 TeX，文档和示例相对简略。  
- **适用场景**：非常适合作为内部原型或实验平台；在生产环境使用前，需要完成以下检查：  
  - 完整的依赖审计（尤其是 TeX 与 Claude‑API 的兼容性）。  
  - 错误处理与超时机制的补充。  
  - 安全审计（API 密钥管理、输出内容过滤）。  
- **结论**：在经过小规模验证并完成运维、监控和安全加固后，可用于内部业务流程的生产化；直接在面向外部用户的高并发场景使用仍需进一步成熟。

## 🧭 Practical evaluation

**Value:** KorroAi/drunk-claude helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 165 GitHub stars
- 9 forks
- updated 2026-06-27
- primary language: TeX
- 17 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 25/100 |
| stars | 47/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 41/100 |
| production | 65/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/KorroAi/drunk-claude) · [← Back to AI/ML](./README.md)</sub>
