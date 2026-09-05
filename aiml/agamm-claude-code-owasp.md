# agamm/claude-code-owasp

[![Stars](https://img.shields.io/github/stars/agamm/claude-code-owasp?style=flat-square&color=yellow)](https://github.com/agamm/claude-code-owasp/stargazers) [![Forks](https://img.shields.io/github/forks/agamm/claude-code-owasp?style=flat-square&color=blue)](https://github.com/agamm/claude-code-owasp/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Claude Code skill for OWASP security best practices (2025-2026). Includes Top 10:2025, ASVS 5.0, Agentic AI security, and 20+ language-specific security quirks.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 263 |
| 🍴 **Forks** | 25 |
| 💻 **Language** | Unknown |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-security` `appsec` `asvs` `claude` `claude-code` `claude-skills` `owasp` `secure-coding` `security` `vulnerability`

## 🎯 Categories

AI/ML · Security

## 📝 Summary

### English

Here's a brief summary of the agamm/claude-code-owasp project:

The agamm/claude-code-owasp project is an open-source AI skill that integrates OWASP security best practices, including the Top 10:2025, ASVS 5.0, Agentic AI security, and 20+ language-specific security quirks. This skill helps developers add AI capabilities without building from scratch, making it suitable for prototyping AI features, building RAG or agent workflows, and evaluating model tooling. While it's useful for prototypes or internal workflows, its production readiness is medium due to the need for manual inspection and dependency checks.

The value of agamm/claude-code-owasp lies in its ability to simplify the integration of AI capabilities with OWASP security best practices, making it easier for developers to build secure and intelligent applications. The practical adoption path involves:

1. Manual inspection: Developers need to inspect the integration signals in the discovered metadata to ensure a smooth adoption.
2. Dependency checks: Before committing to production, developers should validate the setup cost and perform necessary dependency checks.
3. Prototyping and testing: The skill is best suited for prototyping AI features, building RAG or agent workflows, and evaluating model tooling.

In terms of

### Русский

**agamm/claude-code-owasp** — это набор навыков Claude Code, реализующий лучшие практики OWASP (Top 10 2025, ASVS 5.0, агентную безопасность ИИ и более 20 языковых особенностей). Он позволяет быстро добавить AI‑функциональность в прототипы, RAG‑системы или агентные воркфлоу без необходимости строить собственную модельную стеку, однако перед внедрением требуется ручная проверка и оценка затрат на интеграцию, поскольку метаданные проекта не дают полного представления о пути подключения. Готовность к production — средняя: подходит для внутренних прототипов и экспериментов после проверки зависимостей и поддержки.

### 中文

**项目简介**  
agamm/claude-code-owasp 为 Claude Code 提供了 2025‑2026 年最新的 OWASP 安全最佳实践库，覆盖 Top 10 2025、ASVS 5.0、Agentic AI 安全以及 20 多种语言的安全细节。它让开发者在已有代码生成模型上快速叠加安全检查能力，而无需自行构建完整的安全知识图谱。

**价值**  
- **快速赋能**：直接在 Claude Code 或其他 LLM 工作流中调用 OWASP 规则，省去自行收集、整理安全标准的时间。  
- **覆盖面广**：既有通用的 Top 10 与 ASVS，又包含语言特有的安全陷阱，适用于多语言项目。  
- **原型友好**：提供可直接用于 RAG（检索增强生成）或 Agent 工作流的提示库，帮助团队在原型阶段就能评估安全风险。

**典型接入方式**  
1. **提示库引入**：将仓库中的 `prompts/`、`rules/` 文件复制到项目的 Prompt 目录或通过 Git 子模块引用。  
2. **RAG/Agent 集成**：在 LangChain、LlamaIndex 等框架的工具链中注册一个 “OWASP 检查器”工具，使用仓库提供的 JSON/YAML 规则文件作为检索或工具调用的知识源。  
3. **CI/CD 检查**：在 GitHub Actions 或 GitLab CI 中加入一步调用 Claude Code（或兼容的 OpenAI/Anthropic API），将代码片段与 OWASP 规则对比，自动生成安全审计报告。  

**生产可用性**  
- **成熟度**：GitHub ★263、Fork 25，最近一次更新为 2026‑06‑28，属于中等成熟度。  
- **适用场景**：非常适合内部原型、研发实验或安全审计辅助工具；在正式生产环境使用前，需要：  
  - **手动审查**：确认规则与组织内部合规要求匹配，避免误报/漏报。  
  - **依赖管理**：检查提示库与所使用的 LLM 版本兼容性，并锁定依赖。  
  - **监控与回滚**：在 CI/CD 中加入失败阈值和回滚策略，以防规则误判导致部署阻塞。  

综上，agamm/claude-code-owasp 能显著降低在 AI 代码生成项目中引入 OWASP 安全检查的门槛，适合作为原型或内部工具的安全层；在投入生产前建议完成一次完整的安全验证和运维准备。

## 🧭 Practical evaluation

**Value:** agamm/claude-code-owasp helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 263 GitHub stars
- 25 forks
- updated 2026-06-28
- 10 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 52/100 |
| topics | 100/100 |
| outlook | 71/100 |
| quality | 71/100 |
| recency | 80/100 |
| adoption | 47/100 |
| production | 66/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/agamm/claude-code-owasp) · [← Back to AI/ML](./README.md)</sub>
