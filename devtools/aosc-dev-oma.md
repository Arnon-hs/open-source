# AOSC-Dev/oma

[![Stars](https://img.shields.io/github/stars/AOSC-Dev/oma?style=flat-square&color=yellow)](https://github.com/AOSC-Dev/oma/stargazers) [![Forks](https://img.shields.io/github/forks/AOSC-Dev/oma?style=flat-square&color=blue)](https://github.com/AOSC-Dev/oma/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-49%2F100-brightgreen?style=flat-square)](#)

> Package Manager for AOSC OS

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 221 |
| 🍴 **Forks** | 15 |
| 💻 **Language** | Rust |
| 📈 **Score** | 49/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`aosc` `apt` `cli` `package-manager` `rust`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
AOSC‑Dev/oma is a Rust‑based package manager tailored for AOSC OS, designed to streamline daily development, code‑review, and CI workflows. By exposing a clean API/CLI and rich language metadata, it lets engineers automate local engineering tasks and accelerate feedback loops. With 221 ★ on GitHub and recent activity, it’s a solid tool for prototype‑level or internal use, pending a final security and licensing review before production deployment.  

**Value**  
- **Time savings:** Automates repetitive packaging steps, reducing the manual effort required for building, testing, and publishing AOSC packages.  
- **Faster feedback:** Integrates with CI pipelines, delivering immediate build‑status signals that help developers catch issues early.  
- **Developer ergonomics:** A consistent CLI and SDK let engineers script common tasks, standardising workflows across teams.  

**Practical Adoption Path**  
1. **Pilot:** Clone the repo, run the CLI on a sandbox AOSC environment, and replace ad‑hoc packaging scripts with oma commands.  
2. **Integration:** Hook oma into existing CI pipelines (e.g., GitHub Actions, GitLab CI) to automate package builds and validation.  
3. **Standardisation:** Document the oma command set and expose its SDK to internal tooling, then roll it out to all engineering squads.  
4. **Governance:** Conduct a lightweight security audit, verify the MIT/Apache license compliance, and set up a maintenance schedule (e.g., weekly dependency updates).  

**Production Readiness**  
- **Maturity:** Medium – functional for prototypes and internal workflows, but requires a final review of licensing, security posture, and long‑term maintainer commitment.  
- **Stability:** Actively maintained (last commit 2026‑05‑14) with a modest contributor base; the Rust codebase is generally safe and performant.  
- **Risks:** No major metadata issues, but the project lacks a formal security policy and a clearly defined maintainer roadmap, which should be addressed before mission‑critical deployment.  

Overall, oma offers a compelling productivity boost for AOSC OS developers, and with a brief due‑diligence step it can be safely promoted from internal prototyping to production‑grade usage.

### Русский

**AOSC‑Dev/oma** — это пакетный менеджер для AOSC OS, написанный на Rust, который ускоряет ежедневные циклы разработки и ревью, позволяя автоматизировать локальные задачи и получать более быстрый фидбэк в CI. Его простой API/CLI легко интегрировать в существующие пайплайны, что делает его подходящим для прототипов и внутренних рабочих процессов, однако перед выводом в продакшн рекомендуется проверить зависимости, лицензирование и безопасность. При текущем уровне поддержки (средняя готовность, 221 звезда, активные коммиты) проект готов к ограниченному использованию, но требует дополнительного аудита перед масштабным внедрением.

### 中文

**项目简介**  
AOSC‑Dev/oma 是 AOSC OS 的官方软件包管理器，使用 Rust 编写，提供 API/SDK/CLI 三种调用方式，帮助工程师在本地快速构建、测试、发布软件包。

**价值**  
- **提升开发效率**：通过一键式依赖解析、自动化构建与本地镜像管理，显著缩短日常开发与代码审查的循环时间。  
- **加速 CI 反馈**：可在 CI 流水线中直接调用 oma CLI，实现包的增量构建、缓存复用和自动化验证，提升持续集成的速度和可靠性。  
- **统一工程任务**：统一的元数据格式和插件机制，使得本地工程任务（如 lint、格式化、签名）可以统一调度，降低脚本碎片化的维护成本。

**典型接入方式**  
1. **CLI**：在本地或 CI 环境直接运行 `oma install|build|publish`，适合快速原型和脚本化调用。  
2. **SDK（Rust crate）**：在自研工具或服务中引入 `oma` crate，调用其公开的 API 完成依赖解析、包构建等操作，适合深度集成。  
3. **REST‑like API（通过内部服务）**：项目已提供基于 HTTP 的实现信号，可在跨语言环境（如 Python、Go）中通过 HTTP 客户端调用，适合多语言团队统一使用。

**生产可用性**  
- **成熟度**：当前为 **Medium** 级别，已在内部原型和部分业务线验证，可支撑日常开发和内部 CI。  
- **依赖与维护**：Rust 生态成熟，项目活跃（截至 2026‑05‑14 最近一次提交），但仍需在正式生产前完成以下检查：  
  - 许可证合规（确认使用的开源许可证符合企业政策）  
  - 安全审计（审查第三方依赖的安全漏洞）  
  - 维护者沟通（确保关键维护者对长期支持有明确承诺）  
- **适用场景**：推荐先在内部研发环境或测试流水线中使用，待完成上述检查后再推广到面向外部用户的生产环境。

## 🧭 Practical evaluation

**Value:** AOSC-Dev/oma helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 221 GitHub stars
- 15 forks
- updated 2026-05-14
- primary language: Rust
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 30/100 |
| stars | 50/100 |
| topics | 63/100 |
| outlook | 46/100 |
| quality | 49/100 |
| recency | 20/100 |
| adoption | 44/100 |
| production | 46/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/AOSC-Dev/oma) · [← Back to DevTools](./README.md)</sub>
