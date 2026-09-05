# rizinorg/cutter

[![Stars](https://img.shields.io/github/stars/rizinorg/cutter?style=flat-square&color=yellow)](https://github.com/rizinorg/cutter/stargazers) [![Forks](https://img.shields.io/github/forks/rizinorg/cutter?style=flat-square&color=blue)](https://github.com/rizinorg/cutter/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> Free and Open Source Reverse Engineering Platform powered by rizin

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 19.1k |
| 🍴 **Forks** | 1.4k |
| 💻 **Language** | C++ |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cutter` `debugger` `gui` `reverse-engineering` `security`

## 🎯 Categories

Security

## 📝 Summary

### English

**Brief Summary**  
Cutter is a free, open‑source reverse‑engineering platform built on top of the Rizin framework. It provides a ready‑made, modern UI for binary analysis, letting teams ship user‑facing interfaces without writing custom front‑end code. With strong community adoption (19 k+ stars, 1.4 k forks) and recent activity, it is a mature candidate for production pilots.

**Value**  
Cutter bundles a rich set of reusable UI components—graph views, disassembly panes, decompiler output, and plugin integration—so developers can focus on domain‑specific features rather than reinventing the analysis interface. This accelerates UI delivery, reduces maintenance overhead, and ensures a consistent user experience across security tools.

**Practical Adoption Path**  
1. **Proof of Concept** – Clone the repo, run the provided Docker/CI scripts, and verify the baseline UI on a small binary set.  
2. **Integration Checklist** – Follow the README to connect Cutter to your existing Rizin backend or custom analysis plugins; start with a minimal plugin that exposes your data.  
3. **Component Reuse** – Identify UI widgets (e.g., hex view, call‑graph) that match your product needs and embed them via the Cutter extension API or by forking the UI code.  
4. **Iterative Expansion** – Gradually replace bespoke UI pieces with Cutter components, measuring development time saved and user feedback.

**Production Readiness**  
Cutter scores high on production readiness: it is actively maintained (last commit 2026‑06‑23), has a large, engaged community, and is used in several commercial reverse‑engineering tools. The main risk is the lack of explicit integration documentation; a small pilot should be used to quantify setup effort and verify compatibility with your build pipeline before a full rollout. Once the proof‑of‑concept validates the integration cost, Cutter can be considered a reliable, OSS‑grade front‑end for security‑focused products.

### Русский

**rizinorg/cutter** — это бесплатная открытая платформа для реверс‑инжиниринга, построенная на базе rizin и предоставляющая готовый пользовательский интерфейс. Она позволяет быстро собрать UI продукта, переиспользовать готовые компоненты и ускорить доставку фронтенда, при этом обладает высокой готовностью к production (активная разработка, более 19 тыс. звёзд, регулярные обновления). Рекомендуется начать интеграцию с небольшого proof‑of‑concept и проверки README, чтобы уточнить затраты на настройку.

### 中文

**项目简介**  
rizinorg/cutter 是基于 rizin 的免费开源逆向工程平台，提供图形化的前端界面，让用户无需从零编写 UI 即可进行二进制分析、调试和可视化。

**价值**  
- **快速交付 UI**：内置丰富的逆向工程组件（如反汇编视图、函数图、十六进制编辑器），开发者可以直接复用，省去大量自研前端工作。  
- **提升前端效率**：统一的界面框架和交互模式帮助团队在短时间内搭建产品化的逆向分析工具或内部平台。  
- **社区与生态**：拥有近 2 万星、千余 Fork，活跃的社区提供插件、文档和案例，降低学习成本。

**典型接入方式**  
1. **先行评估**：克隆仓库，阅读 `README.md` 与 `docs/`，确认依赖（C++、Qt、rizin）。  
2. **小范围 PoC**：在本地或 CI 环境编译 `cutter`，通过命令行参数或插件机制加载自定义二进制，验证 UI 与后端 rizin 的交互是否满足需求。  
3. **集成到产品**：  
   - **嵌入式方式**：将 `cutter` 作为子模块或子进程启动，使用 IPC（如 JSON‑RPC）与主业务系统通信。  
   - **插件方式**：编写 Qt 插件或 Python 脚本，扩展现有视图或添加专属功能。  
4. **持续交付**：利用已有的 CMake 构建脚本，将编译产物打包进 Docker 镜像或内部软件仓库，实现自动化部署。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑23，社区维护频繁，issue 处理及时。  
- **成熟度**：拥有 19122 个 GitHub stars、1398 个 Fork，广泛用于学术、CTF 与商业逆向项目，证明其在真实场景下已相当稳健。  
- **风险**：元数据未直接给出标准化的 SDK 接口，集成前需评估编译环境和依赖的配置成本；建议先在测试环境完成 PoC，确认部署脚本与安全合规性后再推广至生产。  

综上，rizinorg/cutter 具备高生产可用性，适合作为逆向工程前端的即插即用解决方案，只要做好前期的环境验证和小规模概念验证即可平滑落地。

## 🧭 Practical evaluation

**Value:** rizinorg/cutter helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 19122 GitHub stars
- 1398 forks
- updated 2026-06-23
- primary language: C++
- 5 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 79/100 |
| stars | 91/100 |
| topics | 63/100 |
| outlook | 75/100 |
| quality | 84/100 |
| recency | 80/100 |
| adoption | 88/100 |
| production | 71/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/rizinorg/cutter) · [← Back to Security](./README.md)</sub>
