# fivetaku/fablize

[![Stars](https://img.shields.io/github/stars/fivetaku/fablize?style=flat-square&color=yellow)](https://github.com/fivetaku/fablize/stargazers) [![Forks](https://img.shields.io/github/forks/fivetaku/fablize?style=flat-square&color=blue)](https://github.com/fivetaku/fablize/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> A Claude Code plugin that makes Opus behave like Fable — completion, evidence, and verification enforced as procedure. Ships only what a Fable-vs-Opus comparison proved transferable.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 756 |
| 🍴 **Forks** | 90 |
| 💻 **Language** | Python |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic` `anthropic` `claude` `claude-code` `fable` `harness` `opus`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
fivetaku/fablize is a Claude‑Code plugin that transforms Opus into a “Fable‑style” system, enforcing a disciplined flow of completion, evidence, and verification. It only ships code that has been proven transferable through a systematic Fable‑vs‑Opus comparison, letting developers add robust AI capabilities without building a model stack from scratch.

**Value**  
- **Accelerated AI prototyping** – By reusing proven Opus components, teams can quickly prototype RAG pipelines, autonomous agents, or other AI‑driven features without the overhead of training or fine‑tuning models.  
- **Built‑in rigor** – The mandatory evidence and verification steps reduce hallucinations and improve trustworthiness, which is especially valuable for compliance‑sensitive applications.  
- **Low entry barrier** – A single Python package with clear API/CLI hooks lets developers integrate the plugin into existing workflows with minimal refactoring.

**Practical Adoption Path**  
1. **Evaluation** – Clone the repo, run the provided CLI demos, and inspect the API surface (Python SDK, REST wrapper).  
2. **Proof‑of‑Concept** – Replace a current Opus call in a sandboxed service with `fablize.complete(...)`, capture the generated evidence, and verify the output against your own test suite.  
3. **Integration** – Wrap the plugin in your RAG or agent orchestration layer (e.g., LangChain, LlamaIndex) and configure the verification policy to match production SLAs.  
4. **Monitoring & Feedback** – Use the built‑in logging of evidence artifacts to monitor performance and feed back failures for continuous improvement.

**Production Readiness**  
- **Activity & Community** – 756 stars, 90 forks, recent commits (last updated 2026‑07‑06), and a healthy set of 7 topical tags indicate an active community.  
- **Maturity** – The plugin follows a clear procedural contract (completion → evidence → verification) and ships only code that passes a documented transferability test, reducing runtime surprises.  
- **Risk Considerations** – No major metadata issues are evident, but a final review of the open‑source license, security audit of dependencies, and maintainer responsiveness is advisable before full‑scale deployment.  

Overall, fivetaku/fablize is a high‑readiness OSS component that can be piloted quickly and, after the standard security/legal vetting, promoted to production for robust AI feature development.

### Русский

**fivetaku/fablize** — это плагин для Claude Code, превращающий Opus в «Fable»: каждый вывод сопровождается завершённостью, доказательствами и проверкой, а в продакшн попадает только то, что прошёл сравнение Fable‑vs‑Opus и доказано переносимым. Он позволяет быстро добавить AI‑функциональность (прототипировать RAG‑ или агентские сценарии, оценивать инструменты моделей) без необходимости строить стек моделей с нуля, а благодаря активной поддержке, 756 звёздам и свежим обновлениям (июль 2026) готов к серьёзным пилотам в продакшн. (Лицензия и безопасность требуют окончательной проверки.)

### 中文

**项目简介（2‑3 句话）**  
fivetaku/fablize 是一个 Claude Code 插件，它把 Opus 的生成能力包装成类似 Fable 的“完成‑证据‑验证”流程，只交付经 Fable‑vs‑Opus 对比验证可迁移的结果。通过该插件，开发者可以在不从零构建模型堆栈的情况下，快速为现有系统加入 AI 能力。

**价值主张**  
- **即插即用**：提供统一的 API/SDK/CLI，直接在现有代码库中调用，无需自行训练或部署模型。  
- **可靠性保障**：内置完成‑证据‑验证三步流程，确保生成内容经过可追溯的证据支撑，降低 hallucination 风险。  
- **加速原型**：适用于 RAG、智能代理、自动化脚本等场景，帮助团队在数小时内验证 AI 功能可行性。

**典型接入方式**  
1. **API 调用**：通过 HTTP REST 接口发送 `prompt`，返回包含 `completion`、`evidence` 与 `verification` 的结构化响应。  
2. **SDK 使用**：在 Python 项目中 `pip install fablize`，然后 `from fablize import FablizeClient`，创建客户端并调用 `client.complete(prompt)`。  
3. **CLI 工具**：在终端执行 `fablize run --prompt "..."`，即可得到完整的三阶段输出，适合脚本化集成或快速调试。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑07‑06，仓库拥有 756 ★、90 Fork，说明社区活跃且代码维护及时。  
- **生态兼容**：使用纯 Python 实现，兼容主流云函数、容器和虚拟环境，易于在 CI/CD 流水线中部署。  
- **安全与合规**：目前未发现重大元数据风险，仍需对许可证（MIT/Apache 等）及依赖安全审计进行最终确认。  
- **成熟度**：在 GitHub 上已有若干实际项目引用，具备“OSS 候选”级别的生产准备度，适合作为内部试点或受控生产环境的 AI 能力入口。  

综上，fivetaku/fablize 通过标准化的“完成‑证据‑验证”流程，为团队提供低门槛、可审计的 AI 能力，接入简便且具备较高的生产可用性。

## 🧭 Practical evaluation

**Value:** fivetaku/fablize helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 756 GitHub stars
- 90 forks
- updated 2026-07-06
- primary language: Python
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 49/100 |
| stars | 61/100 |
| topics | 88/100 |
| outlook | 73/100 |
| quality | 74/100 |
| recency | 80/100 |
| adoption | 58/100 |
| production | 72/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/fivetaku/fablize) · [← Back to AI/ML](./README.md)</sub>
