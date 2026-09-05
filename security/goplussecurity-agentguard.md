# GoPlusSecurity/agentguard

[![Stars](https://img.shields.io/github/stars/GoPlusSecurity/agentguard?style=flat-square&color=yellow)](https://github.com/GoPlusSecurity/agentguard/stargazers) [![Forks](https://img.shields.io/github/forks/GoPlusSecurity/agentguard?style=flat-square&color=blue)](https://github.com/GoPlusSecurity/agentguard/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Security guard for AI agents — blocks malicious skills, prevents data leaks, protects secrets. 24 detection rules, runtime action evaluation, trust registry.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 403 |
| 🍴 **Forks** | 60 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Security

## 📝 Summary

### English

**Brief Summary**  
AgentGuard (GoPlusSecurity/agentguard) is a TypeScript‑based runtime guard for AI agents that blocks malicious skills, prevents data leaks, and protects secrets using 24 built‑in detection rules and a trust‑registry framework. It lets teams add safe AI capabilities—such as RAG pipelines or autonomous agents—without building a security layer from scratch.

**Value**  
- **Security‑first guardrail:** Detects and blocks unsafe actions (e.g., credential exfiltration, prompt injection) before they reach the model, reducing the attack surface of any AI‑augmented product.  
- **Speed to prototype:** Plug‑and‑play rule set and trust registry let developers focus on core functionality while AgentGuard handles compliance and data‑leak protection.  
- **Extensibility:** Rules are configurable and can be extended to match organization‑specific policies, making it suitable for both internal experiments and customer‑facing services.

**Practical Adoption Path**  
1. **Sandbox evaluation** – Clone the repo, run the provided test suite, and experiment with the default 24 rules on a small demo agent.  
2. **Policy tailoring** – Add or adjust rules to reflect your organization’s data‑handling and secret‑management policies; optionally integrate your own trust‑registry source (e.g., internal service catalog).  
3. **Integration** – Wrap your agent’s skill‑execution layer with AgentGuard’s middleware (the library exposes a simple `evaluate(action, context)` API).  
4. **Manual review** – Because metadata signals are sparse, perform a code audit and run threat‑modeling exercises to confirm that the guard covers all critical attack vectors in your stack.  
5. **Staged rollout** – Deploy the guarded agent in a non‑critical environment (e.g., internal dev or QA) and monitor logs for false positives/negatives before promoting to production.

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last commit 2026‑05‑14) and has modest community traction (403 stars, 60 forks).  
- **Dependencies:** Pure TypeScript with minimal external libraries, simplifying dependency‑management checks.  
- **Risks:** Licensing and long‑term maintainer commitment still need verification; integration signals are limited, so thorough testing and manual inspection are required before production use.  
- **Recommendation:** Suitable for prototypes, internal tooling, or controlled‑release AI features. With a dedicated security review and a small pilot rollout, it can be hardened for production, but organizations should not rely on it as a sole security control without complementary safeguards.

### Русский

GoPlusSecurity / agentguard — это открытый «охранник» для AI‑агентов, который в режиме реального времени блокирует вредоносные навыки, предотвращает утечки данных и защищает секреты с помощью 24‑х правил обнаружения и реестра доверия. Он подходит для быстрого прототипирования AI‑фич, построения RAG‑ и агентных пайплайнов, а также оценки инструментов моделирования, однако перед внедрением в продакшн требуется ручная проверка и проверка зависимости/поддержки, так как готовность проекта находится на среднем уровне (подходит для внутренних прототипов, но требует дополнительного контроля перед масштабным использованием).

### 中文

**项目简介（2‑3 句）**  
GoPlusSecurity/agentguard 是面向 AI 代理的安全守护层，能够在运行时拦截恶意技能、阻止数据泄漏并保护机密信息。它内置 24 条检测规则，支持实时动作评估和信任登记册，为 AI 应用提供细粒度的安全控制。

**价值**  
- **快速赋能**：在已有模型之上直接加入安全防护，无需从零构建安全体系。  
- **降低风险**：通过技能审计、数据泄漏检测和机密保护，防止代理被利用进行攻击或泄露敏感信息。  
- **提升可信度**：信任登记册帮助团队管理和审计可信技能，提升业务合规与审计能力。

**典型接入方式**  
1. **依赖安装**：在项目中通过 npm/yarn 安装 `@goplussecurity/agentguard`。  
2. **初始化守护**：在代理框架启动时创建 `AgentGuard` 实例并加载默认规则或自定义规则文件。  
3. **拦截点挂载**：在技能调用前后或数据流转的关键节点调用 `guard.evaluate(action)`，根据返回的评估结果决定是否放行、警告或阻断。  
4. **信任登记**：使用提供的 API 将经过审计的技能注册到信任库，后续调用将自动通过信任检查。

**生产可用性**  
- **成熟度**：当前评分 63/100，适合作为原型或内部工作流的安全层。  
- **依赖与维护**：项目活跃度一般（403 星、60 Fork），最近更新于 2026‑05‑14，使用 TypeScript 开发，需自行评估其依赖安全性和长期维护计划。  
- **上线建议**：在正式生产环境前进行手动审查和安全评估，确认规则覆盖率、许可证兼容性以及维护者响应能力后方可部署。  

总体而言，AgentGuard 能在不重构模型堆栈的前提下，为 AI 代理提供即时的安全防护，是原型开发和内部实验的实用工具，但在生产环境使用前仍需进行充分的风险评估和维护保障。

## 🧭 Practical evaluation

**Value:** GoPlusSecurity/agentguard helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 403 GitHub stars
- 60 forks
- updated 2026-05-14
- primary language: TypeScript

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 55/100 |
| topics | 0/100 |
| outlook | 63/100 |
| quality | 59/100 |
| recency | 80/100 |
| adoption | 52/100 |
| production | 66/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/GoPlusSecurity/agentguard) · [← Back to Security](./README.md)</sub>
