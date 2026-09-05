# mufeedvh/code2prompt

[![Stars](https://img.shields.io/github/stars/mufeedvh/code2prompt?style=flat-square&color=yellow)](https://github.com/mufeedvh/code2prompt/stargazers) [![Forks](https://img.shields.io/github/forks/mufeedvh/code2prompt?style=flat-square&color=blue)](https://github.com/mufeedvh/code2prompt/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> A CLI tool to convert your codebase into a single LLM prompt with source tree, prompt templating, and token counting.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 7.4k |
| 🍴 **Forks** | 426 |
| 💻 **Language** | Rust |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `chatgpt` `claude` `cli` `command-line` `command-line-tool` `gpt` `llm` `prompt` `prompt-engineering` `prompt-generator` `prompt-toolkit`

## 🎯 Categories

AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`mufeedvh/code2prompt` is a Rust‑based CLI that turns an entire codebase into a single, token‑aware LLM prompt, complete with a source‑tree view, templating support, and built‑in token counting. With over 7 k GitHub stars and active maintenance, it lets developers prototype AI‑enhanced features, RAG pipelines, or autonomous agents without building a custom model stack from scratch.

**Value**  
- **Rapid AI enablement** – By automatically formatting a repository as a concise, token‑budgeted prompt, teams can instantly feed code context into any LLM, accelerating proof‑of‑concepts and feature prototyping.  
- **Consistent prompt engineering** – Built‑in templating and token accounting remove guesswork, ensuring prompts stay within model limits and produce reproducible results.  
- **Low barrier to entry** – The CLI works out‑of‑the‑box with any language repository; no SDK integration or custom preprocessing is required.

**Practical Adoption Path**  
1. **Install the CLI** (`cargo install code2prompt` or download a binary).  
2. **Run** `code2prompt path/to/repo --template my_template.toml` to generate a prompt file and token report.  
3. **Feed** the resulting prompt into your LLM of choice (via API, LangChain, or an agent framework).  
4. **Iterate** by tweaking the template or selecting sub‑trees, using the token count feedback to stay within model limits.  
5. **Integrate** into CI/CD pipelines or developer tooling to automatically keep prompts up‑to‑date for RAG or code‑assist agents.

**Production Readiness**  
- **Activity & Adoption** – 7 431 stars, 426 forks, recent commits (as of 2026‑06‑22), and a vibrant Rust community indicate strong momentum.  
- **Stability** – The CLI is self‑contained, with clear API/CLI contracts and no external runtime dependencies, making it easy to sandbox and monitor.  
- **Risk Considerations** – Licensing, security posture, and maintainer continuity still require a final review, but the project shows no immediate red flags. Overall, it is a solid OSS candidate for pilot deployments and can be promoted to production once the standard compliance checks are completed.

### Русский

**mufeedvh/code2prompt** — это CLI‑утилита на Rust, позволяющая быстро превратить любой кодовый репозиторий в единый LLM‑промпт с учётом структуры файлов, шаблонов и подсчёта токенов, что упрощает добавление AI‑функций без построения полной модели. Типичный сценарий — генерация промптов для прототипирования AI‑фич, построения RAG‑агентов или оценки инструментов модели, интегрируя её в пайплайны через простой CLI/SDK. Проект демонстрирует высокий уровень готовности к production: активные коммиты, более 7 тыс. звёзд, широкое принятие в сообществе и надёжную экосистему, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
mufeedvh/code2prompt 是一款基于 Rust 实现的 CLI 工具，能够将整个代码库转化为单个 LLM Prompt，支持源码树展示、模板化生成以及 token 计数，帮助开发者快速为模型提供结构化的代码上下文。

**价值**  
- **快速赋能 AI**：无需自行搭建复杂的模型栈，只需一条命令即可生成适配 LLM 的代码上下文，极大降低 AI 功能原型的开发成本。  
- **多场景适用**：适用于 AI 功能原型、RAG（检索增强生成）或智能体工作流的构建，以及模型工具链的评估与对比。  

**典型接入方式**  
1. **CLI 调用**：在 CI/CD 或本地开发环境中直接运行 `code2prompt`，输出 Prompt 文件或标准输出。  
2. **SDK/脚本集成**：通过子进程或 Rust/其他语言的包装库调用，获取生成的 Prompt 并喂入 LLM 接口。  
3. **模板化定制**：使用内置或自定义的 Prompt 模板，结合项目元数据（语言、目录结构）生成符合业务需求的 Prompt。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑22，项目拥有 7,431 星、426 Fork，最近一次提交在当日，表明社区和维护者仍在积极迭代。  
- **技术成熟**：核心实现使用 Rust，具备高性能和安全特性；提供完整的 API/CLI 文档，易于在生产环境中脚本化调用。  
- **风险可控**：暂无重大元数据或许可证风险，仍需对安全审计和维护者响应速度进行最终确认。总体而言，code2prompt 已具备在正式项目中进行试点或大规模使用的条件。

## 🧭 Practical evaluation

**Value:** mufeedvh/code2prompt helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 7431 GitHub stars
- 426 forks
- updated 2026-06-22
- primary language: Rust
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 66/100 |
| stars | 82/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 85/100 |
| recency | 80/100 |
| adoption | 78/100 |
| production | 73/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/mufeedvh/code2prompt) · [← Back to AI/ML](./README.md)</sub>
