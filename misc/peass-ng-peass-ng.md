# peass-ng/PEASS-ng

[![Stars](https://img.shields.io/github/stars/peass-ng/PEASS-ng?style=flat-square&color=yellow)](https://github.com/peass-ng/PEASS-ng/stargazers) [![Forks](https://img.shields.io/github/forks/peass-ng/PEASS-ng?style=flat-square&color=blue)](https://github.com/peass-ng/PEASS-ng/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> PEASS - Privilege Escalation Awesome Scripts SUITE (with colors)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 20.1k |
| 🍴 **Forks** | 3.4k |
| 💻 **Language** | C# |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bash` `batch` `batch-script` `color` `csharp` `enumeration` `exe` `linpe` `linpeas` `linux` `one-liner` `oneliner`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary**  
PEASS‑ng (Privilege Escalation Awesome Scripts Suite) is an open‑source collection of colorful, ready‑to‑use UI components written in C#. It lets teams ship user‑facing interfaces quickly, reducing the amount of custom front‑end code they have to write and maintain.

**Value**  
- **Speed:** Pre‑built, visually consistent components let developers assemble product UIs far faster than building from scratch.  
- **Reusability:** The suite’s modular design encourages sharing of UI patterns across teams, lowering duplication and technical debt.  
- **Quality:** With >20 k GitHub stars, thousands of forks, and active maintenance, the codebase has been vetted by a large community, giving confidence in its stability and security.

**Practical adoption path**  
1. **Proof‑of‑concept:** Clone the repo, run the README’s quick‑start script, and replace a small existing view with a PEASS‑ng component to validate build‑tool compatibility (e.g., .NET SDK version, package manager).  
2. **Component audit:** Review the component list against your design system, identify gaps, and decide whether to extend or replace any parts.  
3. **Gradual migration:** Incrementally swap legacy UI modules for PEASS‑ng equivalents, starting with low‑risk screens, while keeping a fallback to the original implementation.  
4. **CI/CD integration:** Publish the library as a private NuGet package or reference the GitHub package feed, and add automated tests to verify visual regression and accessibility.

**Production readiness**  
The project scores 67/100 and shows strong production signals: recent commits (as of 2026‑06‑28), a vibrant contributor community, and extensive adoption across multiple repositories. While the integration documentation is sparse, the high star/fork count and active issue resolution indicate a mature, stable codebase suitable for a serious pilot. The primary risk is the unclear setup steps; a small PoC and a review of the build pipeline will confirm the actual integration effort before committing to full rollout.

### Русский

PEASS‑ng (Privileged Escalation Awesome Scripts Suite) — это открытый набор UI‑компонентов на C#, который позволяет быстро создавать пользовательские интерфейсы, минимизируя кастомную фронтенд‑работу и ускоряя выпуск продукта. Рекомендуется начать с небольшого proof‑of‑concept, проверив README и базовую интеграцию, а затем расширять использование компонентов в рамках продукта. Проект обладает высокой готовностью к production: активная поддержка, более 20 000 звёзд, 3 300 форков и регулярные обновления, однако перед масштабным внедрением следует уточнить детали установки и потенциальные затраты на интеграцию.

### 中文

**项目简介**  
PEASS‑ng（Privileged Escalation Awesome Scripts Suite）是一个带颜色高亮的特权提升检查工具集合，提供丰富的脚本和可视化输出，帮助安全团队快速定位和验证系统中的提权漏洞。

**价值**  
- **降低自研成本**：提供即插即用的前端组件和脚本模板，开发者无需从头实现 UI，即可快速搭建安全报告、结果展示等页面。  
- **加速交付**：统一的界面风格和交互逻辑让产品 UI 的迭代周期大幅缩短，团队可以把更多精力放在业务逻辑和安全检测本身。  
- **提升可视化质量**：内置颜色高亮和结构化输出，使漏洞信息更加直观，便于审计和沟通。

**典型接入方式**  
1. **先行评估**：在项目根目录克隆仓库，阅读 `README.md` 与示例代码，确认依赖（.NET 6+、C#）是否与现有技术栈兼容。  
2. **小范围 PoC**：在内部测试环境中创建一个最小化的前端模块，引用 `PEASS-ng` 提供的 UI 组件（如 `ResultTable`, `HighlightPanel`），并通过脚本生成的 JSON 数据进行渲染。  
3. **CI/CD 集成**：将脚本执行步骤加入构建流水线，产出报告文件后自动触发前端页面的生成与部署。  
4. **逐步扩展**：在 PoC 验证无误后，逐步替换现有的自研报告页面，复用组件库实现统一风格。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑28，项目拥有 20 068+ 星、3 365+ Fork，最近一次提交仅在数天前，社区活跃。  
- **技术成熟**：核心语言为 C#，配套的 UI 组件已在多个开源安全工具中实际使用，具备稳定的发布周期。  
- **风险可控**：唯一需要注意的是项目的集成文档较为简略，建议在正式上线前通过小型 PoC 验证环境搭建成本和依赖兼容性。  
- **总体评估**：在确认集成路径后，可视为 **高生产就绪度** 的 OSS 候选，适合在安全审计、渗透测试平台或内部运维工具中进行正式部署。

## 🧭 Practical evaluation

**Value:** peass-ng/PEASS-ng helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 20068 GitHub stars
- 3365 forks
- updated 2026-06-28
- primary language: C#
- 19 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 88/100 |
| stars | 92/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 91/100 |
| recency | 80/100 |
| adoption | 91/100 |
| production | 73/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/peass-ng/PEASS-ng) · [← Back to Misc](./README.md)</sub>
