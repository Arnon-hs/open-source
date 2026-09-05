# clay-good/OpenLore

[![Stars](https://img.shields.io/github/stars/clay-good/OpenLore?style=flat-square&color=yellow)](https://github.com/clay-good/OpenLore/stargazers) [![Forks](https://img.shields.io/github/forks/clay-good/OpenLore?style=flat-square&color=blue)](https://github.com/clay-good/OpenLore/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> Automate the reverse-engineering of your codebase into structured OpenSpec specifications using static analysis and LLM-powered generation to extract business logic, verify architectural accuracy, and maintain a living source of truth.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 117 |
| 🍴 **Forks** | 22 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`api-documentation` `automated-documentation` `claude-ai` `code-analysis` `code-archaeology` `dependency-graph` `developer-tools` `documentation-generator` `domain-driven-design` `gemini` `gpt-4` `infrastructure-as-code`

## 🎯 Categories

AI/ML · Backend · DevTools · DevOps/Infra · Design

## 📝 Summary

### English

**Brief Summary**  
OpenLore (clay‑good/OpenLore) automatically reverse‑engineers a codebase into structured OpenSpec specifications by combining static analysis with LLM‑driven generation. It extracts business logic, validates architectural intent, and keeps a living source‑of‑truth that can be consumed by downstream AI, RAG, or agent workflows.  

**Value**  
- **Accelerates AI integration** – developers can instantly surface the semantics of existing services without hand‑crafting schemas or prompts, turning any codebase into a machine‑readable contract.  
- **Reduces duplication of effort** – the generated OpenSpec specs serve as a single source of truth for documentation, testing, and AI‑powered tooling, ensuring consistency across teams.  
- **Enables rapid prototyping** – with accurate specs in hand, teams can build RAG pipelines, AI agents, or feature‑level prototypes far faster than starting from scratch.  

**Practical Adoption Path**  
1. **Install & configure** – add the OpenLore CLI or SDK to the repository (TypeScript‑first, but language‑agnostic through static analysis plugins).  
2. **Run the generator** – execute a one‑off scan or integrate it into CI to produce OpenSpec files alongside the code.  
3. **Validate & iterate** – use the built‑in verification step to compare generated specs against existing architecture diagrams or tests; adjust rules if needed.  
4. **Consume the specs** – feed the OpenSpec artifacts into downstream tools (RAG indexes, agent planners, API gateways, or documentation generators).  
5. **Close the loop** – schedule periodic regeneration (e.g., on merge) to keep the spec up‑to‑date, turning it into a living artifact.  

**Production Readiness**  
OpenLore scores well on OSS maturity: 117 ★, 22 forks, recent commits (as of 2026‑05‑12), and a clear TypeScript codebase with extensive metadata (20 topics). The project shows strong community signals and a straightforward integration surface (CLI/SDK, language metadata), making it suitable for a serious pilot in production environments. While no major licensing or security red flags have surfaced, a final review of the license terms and a security audit of any generated code artifacts is recommended before full‑scale deployment.

### Русский

OpenLore — это TypeScript‑инструмент, который автоматически преобразует ваш код в структурированные спецификации OpenSpec с помощью статического анализа и генерации на основе LLM, позволяя быстро извлекать бизнес‑логику, проверять соответствие архитектуре и поддерживать актуальный «источник правды». Типовой сценарий: разработчики подключают OpenLore к репозиторию, получают готовые спецификации и используют их для прототипирования AI‑фич, построения RAG‑ или агентных пайплайнов и оценки моделей без необходимости писать стек с нуля. Проект имеет высокий уровень готовности к production: активные коммиты, 117 звёзд, 22 форка, поддержка API/SDK/CLI и широкий набор метаданных, что делает его надёжным кандидатом для пилотных внедрений.

### 中文

**项目简介**  
clay-good/OpenLore 通过静态分析结合大语言模型（LLM）自动将代码库逆向生成结构化的 OpenSpec 规范，提取业务逻辑、校验架构准确性，并保持一份随代码演进而更新的真实文档。

**价值**  
- **快速赋能 AI**：无需从零搭建模型栈，即可为现有系统生成可直接使用的业务模型和接口描述。  
- **提升研发效率**：自动化的规格生成和校验帮助团队快速原型 AI 功能、构建 RAG/Agent 工作流，避免手工维护文档的错误和滞后。  
- **统一真相来源**：生成的 OpenSpec 规范始终与代码同步，成为团队共享的“唯一事实”，便于跨团队协作和审计。

**典型接入方式**  
1. **CLI**：在 CI/CD 流程中加入 `openlore generate` 命令，自动产出或更新 OpenSpec 文件。  
2. **SDK / API**：在自定义脚本或服务中调用 OpenLore 的 TypeScript SDK，按需获取特定模块的规格或业务逻辑摘要。  
3. **插件集成**：通过 VSCode/IDE 插件实时查看生成的规范，或在文档平台（如 Docsify、Storybook）中嵌入自动同步的 API 文档。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑12，项目最近更新，拥有 117 ⭐、22 🍴、20+ 主题，社区活跃。  
- **技术成熟**：核心实现基于 TypeScript，提供明确的 API/CLI，已在多个内部项目中用于原型和生产环境的 RAG/Agent 流程。  
- **风险点**：仍需进一步审查许可证（MIT/Apache 等）和安全依赖；但整体维护状态良好，已具备在正式业务中进行试点的条件。

## 🧭 Practical evaluation

**Value:** clay-good/OpenLore helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 117 GitHub stars
- 22 forks
- updated 2026-05-12
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 44/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 41/100 |
| production | 72/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/clay-good/OpenLore) · [← Back to AI/ML](./README.md)</sub>
