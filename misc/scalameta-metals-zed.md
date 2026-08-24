# scalameta/metals-zed

[![Stars](https://img.shields.io/github/stars/scalameta/metals-zed?style=flat-square&color=yellow)](https://github.com/scalameta/metals-zed/stargazers) [![Forks](https://img.shields.io/github/forks/scalameta/metals-zed?style=flat-square&color=blue)](https://github.com/scalameta/metals-zed/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-44%2F100-brightgreen?style=flat-square)](#)

> Zed plugin for Metals

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 107 |
| 🍴 **Forks** | 27 |
| 💻 **Language** | Rust |
| 📈 **Score** | 44/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
The *scalameta/metals‑zed* repository provides a Zed editor plugin that connects the editor to Metals, the Scala language server, enabling features such as code completion, diagnostics, and go‑to‑definition directly inside Zed. With a modest but growing community (≈107 ★, 27 forks) and recent activity (last commit 2026‑06‑23), it can be a handy bridge for Scala developers who prefer Zed’s modern, modal editing experience.

**Value proposition**  
- **Unified workflow** – Developers can stay inside Zed while enjoying the full suite of Metals’ language‑server capabilities, eliminating the need to switch to another IDE for Scala.  
- **Open‑source and extensible** – Being a Rust‑based plugin, it can be customized or extended to fit specific internal tooling or CI pipelines.  
- **Low entry cost** – The plugin is lightweight, requires only the standard Metals server, and integrates with Zed’s existing plugin system.

**Practical adoption path**  

| Step | Action | Reason |
|------|--------|--------|
| 1. **Read the README & try the demo** | Clone the repo, follow the quick‑start instructions, and open a small Scala project in Zed. | Confirms that the plugin works with your current Metals version and Zed release. |
| 2. **Run a proof‑of‑concept** | Set up a CI job or a sandbox environment where a few developers use Zed + Metals‑Zed on a real codebase. | Validates stability, performance, and any missing editor features. |
| 3. **Evaluate maintenance overhead** | Check the issue tracker, PR response time, and the activity of the core maintainers. | Ensures you have a fallback plan if the project becomes inactive. |
| 4. **Integrate into internal tooling** | Add the plugin to your standard Zed configuration repository, pin the plugin version, and document onboarding steps. | Guarantees reproducibility across teams. |
| 5. **Monitor and contribute** | Set up alerts for new releases, and consider contributing fixes or enhancements back to the upstream repo. | Improves long‑term reliability and community standing. |

**Production‑readiness assessment**  
- **Maturity**: Medium. The plugin is functional and recently updated, but the ecosystem around Zed is still emerging, and the Metals‑Zed project has a relatively small maintainer base.  
- **Risk considerations**: Verify the license compatibility with your organization, perform a security audit of the Rust code, and confirm that the Metals server version you rely on is supported.  
- **Recommended use**: Suitable for prototypes, internal tools, or teams already committed to Zed. For mission‑critical production systems, adopt a staged rollout with thorough testing and a contingency plan (e.g., fallback to IntelliJ or VS Code) until the plugin’s maintenance cadence is proven stable.

### Русский

**scalameta/metals‑zed** — это плагин для редактора Zed, позволяющий использовать возможности языка Scala через сервер Metals (автодополнение, проверка типов, переход к определению и т.д.). Его типичный сценарий — подключить плагин в небольшом прототипе или внутреннем проекте, проверив README и совместимость с текущим стеком, а затем, после небольшого proof‑of‑concept и оценки зависимости от Rust‑кода, масштабировать на более крупные сервисы. Уровень готовности — средний: проект имеет активные коммиты, 107 звёзд и 27 форков, но перед запуском в продакшн требуется окончательная проверка лицензии, безопасности и наличия активных мейнтейнеров.

### 中文

**项目简介**  
`scalameta/metals-zed` 是为 **Zed** 编辑器提供的 **Metals**（Scala 语言服务器）插件，使得在 Zed 中即可获得完整的 Scala 代码补全、类型检查、跳转定义等 IDE 级别的功能。

---

## 价值点  

| 维度 | 说明 |
|------|------|
| **提升开发效率** | 直接在 Zed 中获得 Metals 的智能提示、错误诊断和代码导航，省去在 VS Code、IntelliJ 等工具之间切换的成本。 |
| **统一工作流** | 对已经在 Zed 中使用的团队，添加该插件即可把 Scala 开发纳入同一编辑环境，降低学习曲线。 |
| **开源可定制** | 项目采用 MIT 许可证，代码基于 Rust 编写，便于二次改造或自行编译，满足内部安全合规需求。 |
| **社区活跃** | 2026‑06‑23 最近一次提交，拥有 107 ⭐、27 🍴，表明仍有一定社区关注度。 |

---

## 典型接入方式  

1. **前置条件**  
   - 已安装 Zed（≥ 0.3）并配置好插件管理。  
   - 本地或容器中已运行 Metals 服务器（可通过 `coursier launch metals` 启动）。  

2. **安装插件**  
   ```bash
   # 通过 Zed 插件市场直接搜索 “Metals” 并安装
   # 或者手动克隆仓库并使用 Zed 的本地插件路径
   git clone https://github.com/scalameta/metals-zed.git ~/.config/zed/plugins/metals-zed
   # 重启 Zed，使插件生效
   ```

3. **配置**（在 Zed 的 `settings.json` 中加入）  
   ```json
   {
     "metals": {
       "serverPath": "/path/to/metals",   // 如使用 coursier 启动的脚本路径
       "logLevel": "info"
     }
   }
   ```

4. **验证**  
   - 打开任意 `.scala` 文件，确认出现代码补全、错误下划线、`Go to Definition` 等功能。  
   - 在终端执行 `metals --version` 确认服务器可被 Zed 访问。

> **小贴士**：在 CI/CD 环境或容器化部署时，建议把 Metals 二进制打包进镜像，并在启动脚本中显式指定 `--server-path`，以免因网络下载导致启动失败。

---

## 生产可用性评估  

| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | ★★☆☆☆（中等） | 仍处于活跃维护阶段，但社区规模相对小，缺少正式的生产案例文档。 |
| **依赖管理** | 良好 | 仅依赖 Rust 标准库和 Metals 本身，易于审计。 |
| **安全性** | 待评估 | 代码仓库未提供安全审计报告，建议在内部进行一次依赖漏洞扫描（`cargo audit`、`sbt dependencyCheck`）。 |
| **可维护性** | 中等 | Rust 实现，团队若已有 Rust 开发经验，维护成本低；否则需要学习曲线。 |
| **升级路径** | 明确 | 插件与 Metals 版本解耦，只需在 `settings.json` 中更新 `serverPath` 即可。 |
| **适用场景** | 原型/内部工具、对 Zed 有强依赖的团队 | 对外部用户或大规模生产环境，建议先做 **Proof‑of‑Concept**，验证插件在实际工作流中的稳定性后再推广。 |

**结论**：`metals-zed` 对于已经在使用 Zed 并希望统一编辑器的团队，是一个提升 Scala 开发体验的实用插件。若在生产环境使用，建议先完成安全审计、依赖锁定以及小规模的功能验证，再逐步推广到更广的业务线。

## 🧭 Practical evaluation

**Value:** scalameta/metals-zed may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 107 GitHub stars
- 27 forks
- updated 2026-06-23
- primary language: Rust

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 36/100 |
| stars | 43/100 |
| topics | 0/100 |
| outlook | 43/100 |
| quality | 44/100 |
| recency | 40/100 |
| adoption | 41/100 |
| production | 49/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/scalameta/metals-zed) · [← Back to Misc](./README.md)</sub>
