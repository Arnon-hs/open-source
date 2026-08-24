# hacs/default

[![Stars](https://img.shields.io/github/stars/hacs/default?style=flat-square&color=yellow)](https://github.com/hacs/default/stargazers) [![Forks](https://img.shields.io/github/forks/hacs/default?style=flat-square&color=blue)](https://github.com/hacs/default/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-48%2F100-brightgreen?style=flat-square)](#)

> The home of the default HACS repositories.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 573 |
| 🍴 **Forks** | 2.7k |
| 💻 **Language** | Python |
| 📈 **Score** | 48/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`hacktoberfest`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary**  
The `hacs/default` repository is the curated collection of default Home Assistant Community Store (HACS) add‑ons, serving as the reference point for the standard set of integrations that HACS can install out of the box. With a solid base of community interest (over 570 ★ and 2.7 k forks) and recent activity, it provides a convenient starting point for Home Assistant users who want a ready‑made catalogue of vetted plugins.

**Value**  
- **Centralized source** – All default HACS add‑ons are listed in one place, eliminating the need to hunt across multiple repos.  
- **Community‑backed** – The star and fork counts show broad adoption, indicating that many users already rely on this set for their Home Assistant setups.  
- **Up‑to‑date** – The repo is actively maintained (last commit 2026‑05‑11), helping to keep the default add‑ons compatible with the latest Home Assistant releases.

**Practical adoption path**  
1. **Review the README** to understand the selection criteria and verify that the listed add‑ons align with your project’s requirements.  
2. **Clone or add the repo as a HACS source** in your Home Assistant instance, then run HACS’s “Refresh” to import the default catalog.  
3. **Perform a manual audit** of each add‑on you plan to use—check licensing, security advisories, and the maintainers’ activity, as the repository’s metadata is sparse.  
4. **Pin versions** of the chosen add‑ons in your configuration to guard against unexpected breaking changes.  

**Production readiness**  
The project sits at a medium readiness level: it is suitable for prototypes, internal environments, or as a baseline for production deployments, provided you conduct the recommended due‑diligence checks (license compliance, security review, and maintainer responsiveness). Once those checks are completed and you have locked down the specific add‑ons you need, `hacs/default` can be safely promoted to production use.

### Русский

**hacs/default** — это репозиторий с набором «стандартных» пакетов для Home Assistant Community Store, который удобно использовать как отправную точку при построении собственного каталога интеграций. Он подходит для прототипов и внутренних workflow‑ов, однако перед выпуском в продакшн требуется ручная проверка лицензий, безопасности и активности поддерживающих разработчиков. При условии такой проверки проект считается готовым к среднему уровню эксплуатации.

### 中文

**项目价值**  
hacs/default 是 Home Assistant Community Store（HACS）官方维护的默认仓库集合，聚合了大量经过社区验证的插件、主题和自定义组件。它提供了统一的入口，帮助用户快速发现并安装常用的 Home Assistant 扩展，省去自行搜索、评估单个仓库的时间成本。

**典型接入方式**  
1. **在 Home Assistant 中启用 HACS**：通过 UI 或 CLI 安装 HACS 插件。  
2. **添加默认仓库源**：HACS 安装完成后会自动包含 `hacs/default`，也可以在 HACS 设置的 “Repositories” 页面手动添加 `https://github.com/hacs/default`。  
3. **浏览与安装**：在 HACS 的 “Frontend” 或 “Integrations” 分类下，即可看到默认仓库提供的插件列表，直接点击 “Install” 完成安装。  
4. **手动审查**：由于元数据较为简略，建议在正式采用前检查每个插件的 README、许可证、更新频率以及安全公告。

**生产可用性**  
- **成熟度**：星标 573、Fork 2732，活跃度高，最近一次更新在 2026‑05‑11，表明项目仍在维护。  
- **适用场景**：适合原型开发、内部部署或对插件来源有统一管理需求的团队。  
- **风险与注意事项**：  
  - 元数据（如依赖、兼容性）不够完整，需自行核对。  
  - 仍需对许可证、潜在安全漏洞以及维护者活跃度进行最终审查。  
- **结论**：在完成上述审查后，hacs/default 可作为生产环境的可靠插件来源，尤其适合需要快速搭建 Home Assistant 生态的项目。若对安全合规有更高要求，建议在正式上线前进行额外的依赖审计和持续监控。

## 🧭 Practical evaluation

**Value:** hacs/default may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 573 GitHub stars
- 2732 forks
- updated 2026-05-11
- primary language: Python
- 1 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 86/100 |
| stars | 59/100 |
| topics | 13/100 |
| outlook | 43/100 |
| quality | 52/100 |
| recency | 20/100 |
| adoption | 66/100 |
| production | 47/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/hacs/default) · [← Back to Misc](./README.md)</sub>
