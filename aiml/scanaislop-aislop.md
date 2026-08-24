# scanaislop/aislop

[![Stars](https://img.shields.io/github/stars/scanaislop/aislop?style=flat-square&color=yellow)](https://github.com/scanaislop/aislop/stargazers) [![Forks](https://img.shields.io/github/forks/scanaislop/aislop?style=flat-square&color=blue)](https://github.com/scanaislop/aislop/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> Catch the slop AI coding agents leave in your code: narrative comments, swallowed exceptions, as-any casts, dead code, oversized functions. 50+ rules across 8 languages (TypeScript, JavaScript, Python, Go, Rust, Ruby, PHP). Sub-second, deterministic, no LLM at runtime. MIT-licensed.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 451 |
| 🍴 **Forks** | 19 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-slop` `ai-slop-detection` `cli` `code-quality` `code-review` `developer-tools` `github-actions` `go` `javascript` `linter` `php`

## 🎯 Categories

AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
scanaislop/aislop is an MIT‑licensed static‑analysis toolkit that detects “AI slop” – leftover narrative comments, swallowed exceptions, `as‑any` casts, dead code, and oversized functions – across eight popular languages. It ships with 50+ deterministic, sub‑second rules (no LLM required at runtime) and can be invoked via API, SDK, or CLI.

**Value**  
- **Immediate AI‑aware code hygiene:** Teams can surface the subtle artifacts that AI‑generated code often leaves behind, improving readability, maintainability, and security without waiting for a full‑blown AI code‑review system.  
- **Language‑wide coverage:** By supporting TypeScript, JavaScript, Python, Go, Rust, Ruby, and PHP, it fits into most polyglot codebases, letting you enforce consistent standards across the entire stack.  
- **Fast, deterministic results:** Because the analysis runs locally in under a second per file, it can be integrated into CI pipelines, pre‑commit hooks, or IDE extensions without incurring latency or cost from external LLM calls.

**Practical Adoption Path**  
1. **Prototype:** Pull the repository, run the CLI on a sample repository, and review the generated report to gauge relevance of the default rule set.  
2. **Integration:** Add the npm package (or the compiled binary for non‑Node environments) to your CI configuration (e.g., GitHub Actions, GitLab CI) and fail builds when critical “AI slop” violations are detected.  
3. **Customization:** Extend or disable rules via the provided JSON/YAML config or write custom TypeScript plugins if you need domain‑specific checks.  
4. **Scale:** Deploy the SDK in internal tooling (e.g., a code‑review bot or IDE plugin) to surface findings in real time for developers, closing the feedback loop.

**Production Readiness**  
- **Activity & Community:** 451 stars, 19 forks, recent commits (as of 2026‑06‑28) and a primary TypeScript codebase indicate an active project.  
- **Stability:** Deterministic, sub‑second analysis with no runtime dependencies on external LLM services reduces operational risk.  
- **Licensing & Security:** MIT license is permissive; a quick audit of the dependency tree and CI security scans is still advisable before enterprise rollout.  
Overall, scanaislop/aislop is mature enough for a serious pilot in production environments, especially for teams looking to add AI‑aware linting without building a custom model stack.

### Русский

**scanaislop/aislop** — это быстрый (меньше секунды), детерминированный open‑source сканер, который выявляет «слёпы» ИИ‑агентов в коде — лишние комментарии, подавленные исключения, `as‑any`‑касты, мёртвый код и слишком большие функции. Проект предоставляет более 50 правил для 8 языков (TypeScript, JavaScript, Python, Go, Rust, Ruby, PHP) и может быть подключён к прототипам AI‑фич, RAG‑ или агентным пайплайнам без необходимости строить собственный стек моделей. С активным развитием (обновления 2026‑06‑28), 451 звёздой на GitHub и MIT‑лицензией, aislop готов к серьёзным пилотам в продакшн‑окружениях, хотя окончательная проверка лицензии и безопасности всё же рекомендуется.

### 中文

**项目简介**  
scanaislop/aislop 是一款开源的代码质量检测工具，专注于捕捉 AI 编码助手留下的“脏代码”：叙事式注释、被吞掉的异常、`as‑any` 强制转换、死代码、过大的函数等。它内置 50+ 条规则，覆盖 TypeScript、JavaScript、Python、Go、Rust、Ruby、PHP 等 8 种语言，运行时无需 LLM，子秒级、可确定性输出，采用 MIT 许可证。

**价值**  
- **快速赋能 AI 功能**：在已有代码库中自动发现 AI 生成代码的常见缺陷，帮助团队在不从零搭建模型栈的前提下，直接加入 AI 辅助的代码审查或自动修复能力。  
- **多语言、规则丰富**：一次部署即可在多语言项目中统一检测，避免因语言分散导致的检测盲区。  
- **高效且安全**：子秒响应、无外部模型调用，既满足 CI/CD 的性能要求，又降低了数据泄露风险。

**典型接入方式**  
1. **CLI**：在 CI 流程（GitHub Actions、GitLab CI、Jenkins 等）中直接调用 `aislop scan <path>`，获取 JSON/HTML 报告。  
2. **SDK / API**：通过 npm 包 `@scanaislop/aislop` 在自定义脚本或 IDE 插件中调用 `scanProject()`，获取结构化的规则触发信息。  
3. **语言元数据**：项目根目录放置 `aislop.config.json`，配置需要启用的规则集、排除路径以及自定义阈值，即可实现“即插即用”。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑28 最近一次提交，GitHub 统计 451 ★、19 Fork，拥有 20+ 相关话题，表明社区和维护者仍在积极迭代。  
- **成熟度**：核心实现基于 TypeScript，代码结构清晰，提供完整的单元测试与 CI，适合作为正式环境的代码审查环节。  
- **安全与合规**：MIT 许可证，无运行时依赖外部 LLM，降低了合规审查的复杂度；仍建议在正式部署前进行一次内部安全审计（依赖库的 CVE 检查）。  

综合来看，scanaislop/aislop 已具备较高的生产可用性，适合作为 AI 辅助代码质量检测的首选 OSS 方案，可在原型验证、RAG/Agent 工作流以及模型工具评估等场景中快速落地。

## 🧭 Practical evaluation

**Value:** scanaislop/aislop helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 451 GitHub stars
- 19 forks
- updated 2026-06-28
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 33/100 |
| stars | 57/100 |
| topics | 100/100 |
| outlook | 64/100 |
| quality | 62/100 |
| recency | 40/100 |
| adoption | 50/100 |
| production | 62/100 |
| usefulness | 90/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/scanaislop/aislop) · [← Back to AI/ML](./README.md)</sub>
