# obra/superpowers-marketplace

[![Stars](https://img.shields.io/github/stars/obra/superpowers-marketplace?style=flat-square&color=yellow)](https://github.com/obra/superpowers-marketplace/stargazers) [![Forks](https://img.shields.io/github/forks/obra/superpowers-marketplace?style=flat-square&color=blue)](https://github.com/obra/superpowers-marketplace/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-49%2F100-brightgreen?style=flat-square)](#)

> Curated Claude Code plugin marketplace

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.1k |
| 🍴 **Forks** | 222 |
| 💻 **Language** | Unknown |
| 📈 **Score** | 49/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
Obra’s *superpowers‑marketplace* is an open‑source, curated catalog of Claude Code plugins that lets developers discover, browse, and install ready‑made AI‑powered extensions. With over a thousand GitHub stars and recent activity (last updated 2026‑06‑30), the project offers a convenient entry point for teams looking to experiment with Claude‑based tooling without building plugins from scratch.

**Value**  
- **Centralized discovery** – All vetted Claude Code plugins are listed in one place, reducing the time spent searching disparate repositories.  
- **Curated quality** – The marketplace applies basic vetting (e.g., basic metadata checks, usage examples), giving a higher baseline confidence than random GitHub searches.  
- **Accelerated prototyping** – Teams can quickly plug in pre‑built capabilities (e.g., code generation, data extraction) into their Claude‑enabled applications, shortening proof‑of‑concept cycles.

**Practical Adoption Path**  
1. **Review the README & plugin list** – Identify plugins that match your workflow (e.g., language‑specific code assistants, test‑generation tools).  
2. **Clone or add the plugin as a dependency** – Follow the installation instructions provided for each plugin (typically a `pip`/`npm` install or a direct Git submodule).  
3. **Run a sandbox test** – Execute the plugin in an isolated environment (Docker container or virtualenv) to verify compatibility with your Claude version and internal security policies.  
4. **Integrate into CI/CD** – Once validated, add the plugin to your build pipeline, configure any required API keys, and write a thin wrapper to expose the plugin’s functionality to your application.  
5. **Monitor & maintain** – Pin the plugin version, track upstream updates (via GitHub releases), and schedule periodic security scans.

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last commit 2026‑06‑30) and has a solid community signal (1,123 stars, 222 forks), but the marketplace metadata is sparse, so each plugin must be manually vetted for licensing, security, and compatibility.  
- **Risk Management:** Before production use, perform a license audit, run static‑analysis/security scans on the plugin code, and confirm that the maintainers respond to issues.  
- **Suitability:** Ideal for prototypes, internal tools, or early‑stage products where rapid integration outweighs the overhead of a full security review. With proper validation and version pinning, the marketplace can be hardened for production, but it is not a turnkey, enterprise‑grade solution out of the box.

### Русский

**obra/superpowers-marketplace** — это открытый каталог плагинов Claude Code, который позволяет быстро находить и подключать готовые расширения для автоматизации разработки. Типичный сценарий — команда интегрирует нужный плагин в свой CI/CD‑pipeline после ручного просмотра репозитория, тем самым ускоряя прототипирование и внутренние рабочие процессы. Проект находится на среднем уровне готовности: подходит для прототипов и внутренних сервисов, но перед выводом в продакшн требуется проверка лицензий, безопасности и активности поддерживающих разработчиков.

### 中文

**项目简介**  
obra/superpowers‑marketplace 是一个面向 Claude 大模型的代码插件聚合平台，提供经过筛选的插件列表，帮助开发者快速发现并集成可直接在 Claude 中调用的功能模块。

**价值**  
- **即插即用**：统一的插件入口，让团队无需自行搜索、评估即可在 Claude 工作流中使用成熟的代码工具。  
- **质量保障**：仓库已有 1,123+ 星、222+ Fork，且持续更新（截至 2026‑06‑30），提供一定的社区信任度。  
- **加速原型**：在内部原型或实验性项目中，可快速组装所需功能，显著缩短开发周期。

**典型接入方式**  
1. **阅读 README**：确认插件的功能、调用方式以及所需的 Claude 版本。  
2. **手动审查**：检查插件的许可证、依赖列表及安全声明，确保符合内部合规要求。  
3. **在 Claude 中注册**：按照文档将插件的入口 URL 或代码包添加到 Claude 的插件配置里。  
4. **测试调用**：在本地或沙盒环境执行一次完整的插件调用，验证输入/输出符合预期。  
5. **CI/CD 集成**（可选）：将插件的安装脚本或 Docker 镜像写入项目的部署流水线，实现自动化部署。

**生产可用性**  
- **成熟度**：中等（Medium）。适合作为原型、内部工具或低风险业务的功能组件。  
- **风险点**：需自行确认许可证兼容性、潜在安全漏洞以及维护者活跃度后再用于生产环境。  
- **建议**：在正式上线前进行依赖审计、性能基准测试，并设定监控与回滚机制；对关键业务场景可考虑在内部镜像仓库中托管已审查的插件版本。

## 🧭 Practical evaluation

**Value:** obra/superpowers-marketplace may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1123 GitHub stars
- 222 forks
- updated 2026-06-30

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 59/100 |
| stars | 65/100 |
| topics | 0/100 |
| outlook | 48/100 |
| quality | 53/100 |
| recency | 40/100 |
| adoption | 63/100 |
| production | 52/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/obra/superpowers-marketplace) · [← Back to Misc](./README.md)</sub>
