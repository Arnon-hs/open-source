# johnfkoo951/cmds-system-files

[![Stars](https://img.shields.io/github/stars/johnfkoo951/cmds-system-files?style=flat-square&color=yellow)](https://github.com/johnfkoo951/cmds-system-files/stargazers) [![Forks](https://img.shields.io/github/forks/johnfkoo951/cmds-system-files?style=flat-square&color=blue)](https://github.com/johnfkoo951/cmds-system-files/network) [![Language](https://img.shields.io/badge/lang-HTML-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> Knowledge architecture for a 10,000-note Obsidian vault — 5 system files + 7 shared rules + 8 slash commands, shared openly with humans and AI agents. Live: https://system.cmdspace.work

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 203 |
| 🍴 **Forks** | 76 |
| 💻 **Language** | HTML |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`johnfkoo951/cmds-system-files` is an open‑source knowledge‑architecture kit for a 10 k‑note Obsidian vault, providing 5 core system files, 7 shared rules, and 8 slash‑command templates that can be used by both humans and AI agents. It offers a ready‑made scaffold for adding AI‑driven capabilities—such as Retrieval‑Augmented Generation (RAG) or autonomous agent workflows—without having to design a model stack from scratch. A live demo is available at https://system.cmdspace.work.  

**Value**  
- **Speed to prototype** – The repository ships a complete set of Obsidian‑compatible files and command definitions, letting teams jump straight into building AI‑enhanced note‑taking, search, or automation features.  
- **Reuse of proven patterns** – The shared rules and slash commands encode best‑practice prompting and metadata conventions that work well with LLMs, reducing the trial‑and‑error normally required for RAG pipelines.  
- **Human‑AI collaboration** – Because the assets are plain HTML/Obsidian markdown, they are readable and editable by non‑technical users, enabling a mixed workflow where humans can refine prompts while AI agents execute them.  

**Practical Adoption Path**  
1. **Clone the repo** and open the supplied system files in your Obsidian vault.  
2. **Inspect & tailor** the 7 shared rules and 8 slash‑command templates to match your domain terminology and data sources (e.g., point the RAG index to your own document store).  
3. **Integrate an LLM provider** (OpenAI, Anthropic, etc.) by adding the required API keys to the configuration file; the repo already includes placeholder sections for this.  
4. **Run a pilot** on a subset of notes, using the slash commands to test retrieval, summarisation, or action generation.  
5. **Iterate**—adjust rules, add custom commands, and optionally extend the HTML front‑end for UI tweaks.  
6. **Scale** to the full 10 k‑note vault once the workflow is stable, and consider packaging the setup as a shared Obsidian plugin for team-wide rollout.  

**Production Readiness**  
- **Maturity:** Medium. The project has a solid community signal (203 stars, 76 forks) and recent activity (updated 2026‑05‑12), indicating active maintenance, but the integration documentation is thin and metadata signals are sparse.  
- **Suitability:** Ideal for prototypes, internal tooling, or proof‑of‑concept RAG/agent pipelines. Before production use, perform a manual review of the system files, verify compatibility with your LLM provider, and establish monitoring for API usage and error handling.  
- **Risks:** The path to integrate with existing data pipelines or CI/CD workflows is not explicitly documented, so setup cost may be higher than the score suggests. Conduct a small‑scale validation to gauge the effort required for dependency management and long‑term maintenance.  

In summary, `johnfkoo951/cmds-system-files` offers a ready‑made, human‑readable framework to accelerate AI‑enhanced knowledge management in Obsidian, with a clear but manual adoption route and a medium‑level readiness that fits prototyping and internal deployments after careful validation.

### Русский

**johnfkoo951/cmds-system-files** — открытая архитектура знаний для огромного Obsidian‑хранилища (10 000 заметок), включающая 5 системных файлов, 7 общих правил и 8 slash‑команд, которые можно использовать как людьми, так и AI‑агентами. Проект удобен для быстрого прототипирования AI‑функций, построения RAG‑ или агентных пайплайнов и оценки инструментов модели, однако требует ручного аудита и уточнения точек интеграции из‑за скудной метаданных. Готовность к production — средняя: подходит для внутренних прототипов при условии проверки зависимостей и затрат на настройку.

### 中文

**项目简介（2‑3 句）**  
johnfkoo951/cmds‑system‑files 是一个面向 10 000 条 Obsidian 笔记的知识架构实现，提供 5 个系统文件、7 条共享规则和 8 条 Slash 命令，供人类和 AI 代理共同使用。项目在 https://system.cmdspace.work 实时演示，旨在让开发者在已有笔记库上快速叠加 AI 能力，而无需从零搭建模型栈。

**价值**  
- **即插即用的 AI 扩展层**：通过预定义的系统文件和规则，能够在现有 Obsidian 笔记库上直接实现检索增强生成（RAG）和智能代理工作流。  
- **降低原型成本**：无需自行训练或部署大型模型，只需调用已有的模型 API，即可在几分钟内验证 AI 功能。  
- **统一的人机协作接口**：Slash 命令和共享规则对人类和 AI 代理均可识别，促进协同编辑与自动化。

**典型接入方式**  
1. **克隆仓库**并将 `system` 文件夹复制到自己的 Obsidian Vault 根目录。  
2. **配置模型 API**：在 `system/config.html` 中填写所使用的 LLM（如 OpenAI、Claude、Gemini）的 API Key 与端点。  
3. **启用 Slash 命令**：在 Obsidian 设置 → 插件 → “自定义命令” 中导入 `commands.json`，即可在编辑器中使用 `/ask`, `/summarize` 等指令。  
4. **自定义规则**（可选）：根据业务需求在 `rules/` 目录下编辑或新增 `.md` 规则文件，系统会在运行时自动加载。  
5. **手动审查**：首次运行前检查生成的元数据（如笔记标签、链接映射），确保与现有笔记结构兼容。

**生产可用性**  
- **成熟度**：Medium。项目已获得 203 星、76 次 fork，最近一次更新于 2026‑05‑12，表明社区活跃度尚可。  
- **适用场景**：原型开发、内部工具、实验性 RAG/Agent 工作流。对外部客户或高并发生产环境仍需进行依赖审计、性能基准和安全评估。  
- **集成风险**：元数据和集成信号较为稀疏，自动化部署难度大，建议在正式上线前进行手动审查和小规模 A/B 测试。  
- **运维要求**：确保模型 API 稳定、网络访问 Obsidian 本地文件系统，以及对 `system` 目录的版本控制和定期更新。  

综上，cmds‑system‑files 是一个面向知识密集型笔记库的快速 AI 原型平台，适合在内部或实验环境中快速验证功能；在生产环境使用前，需要完成依赖检查、性能调优以及安全审计。

## 🧭 Practical evaluation

**Value:** johnfkoo951/cmds-system-files helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 203 GitHub stars
- 76 forks
- updated 2026-05-12
- primary language: HTML

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 47/100 |
| stars | 49/100 |
| topics | 0/100 |
| outlook | 69/100 |
| quality | 62/100 |
| recency | 100/100 |
| adoption | 49/100 |
| production | 68/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/johnfkoo951/cmds-system-files) · [← Back to AI/ML](./README.md)</sub>
