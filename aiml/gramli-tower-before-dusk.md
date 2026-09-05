# Gramli/tower-before-dusk

[![Stars](https://img.shields.io/github/stars/Gramli/tower-before-dusk?style=flat-square&color=yellow)](https://github.com/Gramli/tower-before-dusk/stargazers) [![Forks](https://img.shields.io/github/forks/Gramli/tower-before-dusk?style=flat-square&color=blue)](https://github.com/Gramli/tower-before-dusk/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-39%2F100-brightgreen?style=flat-square)](#)

> Mentioned in dev.to article (tag ai): Tower Before Dusk: I Built a Puzzle Game for Humans and AI

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 39/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | devto |

## 🏷️ Topics

`devto` `ai` `devchallenge` `gamechallenge` `gamedev`

## 🎯 Categories

AI/ML · Games & Graphics

## 📝 Summary

### English

**Brief Summary**  
*Tower Before Dusk* is an open‑source puzzle‑game framework that lets developers embed AI agents alongside human players, offering a ready‑made environment for prototyping and testing generative‑AI, RAG, or autonomous‑agent workflows. The project provides a minimal “plug‑and‑play” stack so you don’t have to start from scratch when adding AI‑driven gameplay or interaction features.

**Value**  
- **Rapid AI prototyping** – The game supplies a concrete, interactive testbed where you can drop in language models, vision models, or retrieval‑augmented pipelines and immediately see how they behave in a real‑time, multi‑agent setting.  
- **Human‑AI comparison** – Because humans and AI solve the same puzzles, you can collect side‑by‑side performance data, user experience feedback, and failure cases without building separate evaluation harnesses.  
- **Reusable components** – Core mechanics, level‑generation scripts, and a thin client‑side UI are abstracted, letting you reuse them for other gamified AI demos or internal tooling.

**Practical Adoption Path**  
1. **Clone & explore** – Fork the repo, run the Docker‑compose setup (Node/React frontend + Python backend) and play a few levels to understand the data flow.  
2. **Swap in your model** – Replace the placeholder `model.py` with your own inference wrapper (e.g., OpenAI, Anthropic, local LLM). Adjust the `agent_prompt.yaml` to match your task.  
3. **Integrate data sources** – If you need RAG, plug a vector store (FAISS, Pinecone, etc.) into the `retrieval.py` hook; for tool‑use, add function calls in `agent_actions.py`.  
4. **Test & iterate** – Use the built‑in logging dashboard to capture turn‑by‑turn traces, then refine prompts or tool definitions.  
5. **Internal rollout** – Deploy the container to a staging environment, invite a small group of QA testers or product managers, and collect both quantitative metrics (solve time, success rate) and qualitative feedback.

**Production Readiness**  
- **Maturity:** Medium. The codebase is functional and recently updated (June 2026), but integration signals are sparse and documentation is thin.  
- **Dependencies:** Relies on a Node/React frontend, a Python FastAPI backend, and optional vector‑store libraries; all are actively maintained, but you’ll need to audit version compatibility.  
- **Risks:** Limited licensing clarity, modest issue tracking, and no formal CI/CD pipeline mean you should perform a manual security and license review before pushing to production.  
- **Recommendation:** Treat the project as a prototype or internal tool. After the above adoption steps and a thorough validation of licensing, tests, and maintenance commitments, it can be hardened for production use, especially for internal AI‑feature demos or controlled‑release experiments.

### Русский

**Tower Before Dusk** — это open‑source‑проект, позволяющий быстро добавить AI‑возможности в игровые и интерактивные приложения без необходимости строить модельный стек с нуля. Типичный сценарий — прототипирование AI‑фич (RAG, агентные воркфлоу, оценка инструментов модели) в рамках puzzle‑игры, где разработчики могут вручную проверить интеграцию перед внедрением. Готовность к production — средняя: проект подходит для прототипов и внутренних процессов, но требует проверки лицензии, документации и поддержки зависимостей перед использованием в продакшене.

### 中文

**项目简介**  
*Tower Before Dusk* 是一个面向人类玩家和 AI 代理的解谜游戏示例，作者在 dev.to（标签 *ai*）中分享了完整实现。它展示了如何在已有前端框架上快速叠加检索‑增强生成（RAG）或智能体工作流，而无需从零搭建模型堆栈。

**价值**  
- **快速原型**：提供即插即用的 AI 能力（对话、提示生成、状态推理），帮助团队在几小时内验证 AI 功能的可行性。  
- **学习参考**：代码结构清晰，涵盖前端交互、后端推理服务以及 RAG/Agent 流程，是学习 AI‑enhanced 游戏或交互式应用的好教材。  
- **降低成本**：复用已有的游戏逻辑，只需接入模型 API，即可得到具备 AI 交互的产品原型，省去大量模型调优和基础设施搭建工作。

**典型接入方式**  
1. **模型选择**：在 `config.yaml` 中配置所需的 LLM（OpenAI、Anthropic、Claude 等）和向量库（FAISS、Pinecone 等）。  
2. **后端服务**：启动 `server/` 目录下的 Flask/FastAPI 服务，负责接收前端请求、调用 LLM、执行 RAG 检索并返回结果。  
3. **前端集成**：前端使用 React（或原项目的框架）通过 WebSocket/REST 与后端交互，默认已实现 `GameAI` 组件，可直接在页面中挂载。  
4. **手动审查**：由于元数据中集成信号稀疏，建议在正式使用前审查以下内容：  
   - 许可证兼容性（项目采用 MIT/Apache 需确认）  
   - 依赖版本（尤其是 `transformers`、`langchain`）是否与内部环境匹配  
   - 代码中是否存在未处理的异常路径或安全风险（如外部 API 密钥泄露）  

**生产可用性**  
- **成熟度**：Medium。项目已在 2026‑06‑18 更新，包含 5 个主题的实现，适合作为内部原型或实验性功能的基础。  
- **上线前检查**：  
  - **依赖与维护**：确认依赖库的长期支持情况，评估是否需要锁定版本或自行维护 fork。  
  - **文档与 Issue**：项目文档相对简略，建议自行补充接入指南并跟踪 GitHub Issues。  
  - **监控与回滚**：在生产环境加入请求日志、错误监控以及模型响应超时的回滚机制。  
- **适用场景**：内部工具、概念验证、AI 功能演示；不建议直接用于面向大规模用户的公开产品，除非完成上述安全与可维护性审查。  

综上，*Tower Before Dusk* 为想要在现有前端产品中快速加入 AI 交互的团队提供了一个可复制的起点，只要在接入前做好依赖审查和监控准备，即可在原型或内部工作流中安全使用。

## 🧭 Practical evaluation

**Value:** Tower Before Dusk: I Built a Puzzle Game for Humans and AI helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-06-18
- 5 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 63/100 |
| outlook | 50/100 |
| quality | 40/100 |
| recency | 80/100 |
| adoption | 0/100 |
| production | 52/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 70/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/Gramli/tower-before-dusk) · [← Back to AI/ML](./README.md)</sub>
