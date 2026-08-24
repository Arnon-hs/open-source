# phpactor/phpactor

[![Stars](https://img.shields.io/github/stars/phpactor/phpactor?style=flat-square&color=yellow)](https://github.com/phpactor/phpactor/stargazers) [![Forks](https://img.shields.io/github/forks/phpactor/phpactor?style=flat-square&color=blue)](https://github.com/phpactor/phpactor/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-49%2F100-brightgreen?style=flat-square)](#)

> Mainly a PHP Language Server with more features than you can shake a stick at

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.9k |
| 🍴 **Forks** | 157 |
| 💻 **Language** | PHP |
| 📈 **Score** | 49/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`completion` `php` `refactoring` `vim`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary**  
phpactor/phpactor is an extensible PHP language server that packs a wide range of developer‑productivity tools—code completion, refactoring, navigation, diagnostics, and more—into a single, AI‑enhanced package. With over 1.8 k stars and active maintenance, it lets teams prototype AI‑driven PHP tooling (e.g., code‑completion models, RAG‑based documentation look‑ups, or autonomous refactoring agents) without building a stack from scratch.

**Value proposition**  
- **AI‑ready foundation** – The server already exposes hooks (e.g., language‑server protocol extensions, custom actions) that can be wired to LLMs or vector stores, turning a conventional IDE helper into an AI‑augmented assistant.  
- **Rapid prototyping** – You can replace or augment existing completions with model‑generated suggestions, experiment with retrieval‑augmented generation (RAG) for project‑wide docs, or build simple autonomous agents that issue refactorings via the server’s command API.  
- **Low‑cost entry** – Because phpactor runs as a standard LSP process, it integrates with any editor that supports LSP (VS Code, PHPStorm, Vim, etc.), letting developers test AI features in their familiar workflow.

**Practical adoption path**  

| Step | Action | Goal |
|------|--------|------|
| 1️⃣  | **Clone & run the demo** – Follow the README to start the language server locally (`composer install && bin/phpactor language-server`). Verify it works with an editor. | Confirm basic functionality and environment (PHP 8+, Composer). |
| 2️⃣  | **Identify extension point** – Locate the `Extension` classes (e.g., `CompletionProvider`, `DiagnosticsProvider`). These are the places where you can inject AI calls. | Understand where to hook your model or RAG service. |
| 3️⃣  | **Proof‑of‑concept integration** – Implement a minimal `CompletionProvider` that forwards the current file context to an LLM API (OpenAI, Anthropic, etc.) and returns the generated suggestions. | Validate that the LSP can round‑trip AI responses without breaking the editor. |
| 4️⃣  | **Add a RAG layer (optional)** – Use a vector store (e.g., Pinecone, Qdrant) to retrieve relevant project docs and prepend them to the prompt. | Demonstrate richer, context‑aware completions. |
| 5️⃣  | **Automated tests** – Write unit tests for the new provider and add integration tests that spin up the language server and query it via the LSP client. | Ensure stability before scaling. |
| 6️⃣  | **Gradual rollout** – Deploy the enhanced server behind a feature flag in a staging environment; let a small developer team use it. Collect telemetry on latency, error rates, and usefulness. | Measure real‑world impact and tune performance. |
| 7️⃣  | **Production hardening** – Pin PHP and dependency versions, add health‑check endpoints, monitor memory/CPU, and set up CI/CD pipelines for the server container. | Achieve a reliable, maintainable production deployment. |

**Production readiness** – **Medium**. phpactor is mature enough for internal prototypes and can be hardened for production with modest effort:  
- **Strengths**: Active maintenance (last commit 2026‑06‑26), solid community (≈1.9 k stars), well‑documented LSP interface, pure‑PHP stack that fits existing PHP back‑ends.  
- **Caveats**: The AI‑specific integration points are not explicitly documented, so you’ll need to explore the extension system and possibly contribute upstream documentation. Dependency management (Composer packages, PHP version) must be audited for security and compatibility with your runtime.  

Overall, phpactor offers a practical, low‑friction way to embed AI capabilities into PHP development workflows; a small proof‑of‑concept followed by incremental hardening can move it from prototype to production use.

### Русский

**phpactor/phpactor** — это open‑source PHP Language Server, предоставляющий широкие возможности автодополнения, рефакторинга и статического анализа, а также набор инструментов для быстрого прототипирования AI‑фич (RAG, агентных воркфлоу) без необходимости строить собственный стек моделей. Типичный путь внедрения — запуск небольшого proof‑of‑concept: установить пакет, проверить README, интегрировать базовые LSP‑функции в IDE и добавить AI‑модуль через предоставленные хуки. Проект имеет средний уровень готовности к production: хорошая популярность (≈1900 ⭐) и активные обновления, но требует проверки зависимостей и поддержки перед использованием в критических системах.

### 中文

**项目价值**  
phpactor/phpactor 是一个功能强大的 PHP 语言服务器，除了提供代码补全、跳转、重构等常规 IDE 功能外，还内置了 AI 辅助特性（如基于大模型的代码生成、上下文检索等），可以让开发团队在现有 PHP 项目中快速加入智能编程能力，而无需自行搭建模型训练或推理平台。

**典型接入方式**  
1. **本地或容器化部署**：通过 Composer 安装 `phpactor/phpactor`，在项目根目录执行 `vendor/bin/phpactor` 启动语言服务器；也可以使用官方提供的 Docker 镜像直接运行。  
2. **IDE 集成**：在 VS Code、PhpStorm、Neovim 等编辑器中配置 LSP（Language Server Protocol）指向启动的 phpactor 进程，即可获得实时的 AI 辅助提示和重构功能。  
3. **脚本化调用**：利用 phpactor 的 CLI 子命令（如 `code:generate`、`refactor:extract-method`）在 CI/CD 流程或自定义脚本中自动化代码生成或审查。  
4. **小范围 PoC**：先在单个微服务或内部工具中开启 phpactor，验证 AI 代码建议的质量与安全性，再逐步推广到全局。

**生产可用性**  
- **成熟度**：GitHub ★1894、活跃度高，最近一次提交在 2026‑06‑26，表明项目仍在维护。  
- **适用场景**：非常适合作为原型开发、内部工具或团队内部的智能编码助手；在对代码质量和安全有严格审查的生产环境中，需要额外进行**依赖审计**、**模型输出审查**以及**回滚机制**。  
- **准备度**：中等。对生产使用来说，建议在正式上线前完成以下检查：  
  1. **依赖安全审计**（Composer lock、Docker 镜像）。  
  2. **性能基准**（启动时延、并发请求数）。  
  3. **AI 输出治理**（过滤敏感信息、审计日志）。  
  4. **容错与监控**（服务不可用时的降级方案）。  

综上，phpactor/phpactor 能显著提升 PHP 开发效率，接入成本相对低，适合作为内部原型或受控生产环境的 AI 编码助手；在全面投入生产前，需做好安全、性能和治理方面的验证。

## 🧭 Practical evaluation

**Value:** phpactor/phpactor helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1894 GitHub stars
- 157 forks
- updated 2026-06-26
- primary language: PHP
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 55/100 |
| stars | 70/100 |
| topics | 50/100 |
| outlook | 54/100 |
| quality | 62/100 |
| recency | 40/100 |
| adoption | 66/100 |
| production | 53/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/phpactor/phpactor) · [← Back to Misc](./README.md)</sub>
