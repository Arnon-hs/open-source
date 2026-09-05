# wp-cli/i18n-command

[![Stars](https://img.shields.io/github/stars/wp-cli/i18n-command?style=flat-square&color=yellow)](https://github.com/wp-cli/i18n-command/stargazers) [![Forks](https://img.shields.io/github/forks/wp-cli/i18n-command?style=flat-square&color=blue)](https://github.com/wp-cli/i18n-command/network) [![Language](https://img.shields.io/badge/lang-Gherkin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Provides internationalization tools for WordPress projects.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 116 |
| 🍴 **Forks** | 60 |
| 💻 **Language** | Gherkin |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `hacktoberfest` `i18n` `localization` `pot` `translation` `wordpress` `wp-cli` `wp-cli-package`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary**  
The **wp‑cli/i18n‑command** package adds a set of WordPress‑CLI commands that automate common internationalisation tasks (e.g., extracting strings, generating POT files, checking text‑domains). With 116 ★ and recent activity (last updated 2026‑05‑14), it offers a lightweight, CLI‑first way for developers to keep their plugins and themes translation‑ready.

**Value**  
- **Time‑saving:** One‑line commands replace manual grep/awk scripts, cutting hours of repetitive work during development and code review.  
- **Workflow acceleration:** The tool can be scripted into local dev setups and CI pipelines, providing instant feedback on missing or malformed translation strings.  
- **Consistency:** Enforces WordPress i18n best practices across a team, reducing human error and improving the quality of localisation assets.

**Practical Adoption Path**  
1. **Install via WP‑CLI** (`wp package install wp-cli/i18n-command`).  
2. **Add to project docs** – expose the most useful commands (e.g., `wp i18n make-pot`, `wp i18n check`) and wire them into npm/yarn scripts or Makefiles.  
3. **Integrate into CI** – run `wp i18n check` as a lint step; fail builds on missing text‑domains or outdated POT files.  
4. **Iterate** – monitor the generated reports, adjust the command options for your codebase, and optionally contribute back custom wrappers.

**Production Readiness**  
- **Maturity:** Medium. The package is actively maintained (last commit 2026‑05‑14) and has a modest but healthy community (116 ★, 60 forks).  
- **Dependencies:** Relies on WP‑CLI and standard PHP extensions; no heavyweight runtime requirements.  
- **Risks:** Licensing and security posture need a final check, and the primary language is listed as Gherkin (likely for test specs), so ensure the core PHP code aligns with your security policies. After a quick audit of the repository and a test run in a staging environment, it can be safely promoted to production for internal or prototype workflows.

### Русский

**wp-cli/i18n-command** — набор CLI‑утилит для интернационализации WordPress‑проектов, позволяющий быстро генерировать и проверять переводные файлы, что значительно ускоряет цикл разработки и ревью. Типичный сценарий: интеграция в локальный workflow и CI, где команда автоматически обновляет POT‑файлы, проверяет отсутствие «мёртвых» строк и генерирует PO/MO для разных языков. Проект находится на среднем уровне готовности к продакшену — подходит для прототипов и внутренних процессов, но перед масштабным внедрением стоит проверить лицензию, безопасность зависимостей и наличие активных мейнтейнеров.

### 中文

**项目简介（2‑3 句话）**  
wp‑cli/i18n‑command 为 WordPress 项目提供一套完整的国际化（i18n）工具，能够在命令行下快速抽取、检查和生成翻译文件。它基于 WP‑CLI 扩展实现，使用 Gherkin 编写测试，社区已有 116 星、60 Fork，最近一次更新在 2026‑05‑14。

**价值**  
- **提升开发效率**：一键完成 POT、PO、MO 文件的生成与同步，省去手动编辑和重复校对的时间。  
- **加速审查与 CI**：在 CI 流程中自动校验翻译键的完整性和格式，及时反馈缺失或冲突，避免代码合并后出现国际化回归。  
- **统一工程任务**：将本地化工作纳入日常脚本或 Makefile，降低团队成员之间的工具差异。

**典型接入方式**  
1. **WP‑CLI 插件安装**  
   ```bash
   wp package install wp-cli/i18n-command
   ```
2. **在项目根目录添加配置（可选）**  
   ```bash
   # wp-i18n-config.json 示例
   {
     "slug": "my-plugin",
     "domain": "my-plugin",
     "pot_path": "languages/my-plugin.pot"
   }
   ```
3. **在本地或 CI 中调用**  
   ```bash
   # 生成 POT 文件
   wp i18n make-pot . languages/my-plugin.pot

   # 检查翻译一致性
   wp i18n check-pot languages/my-plugin.pot
   ```
   可把上述命令写入 `composer.json` 的 `scripts`、GitHub Actions、GitLab CI 等自动化流程中。

**生产可用性评估**  
- **成熟度**：社区活跃度一般（116 ★、60 Fork），最近更新在 2026‑05‑14，代码基于 Gherkin 的行为测试，质量相对可靠。  
- **依赖与维护**：依赖 WP‑CLI 与 PHP，兼容 WordPress 5.0+；但仍需确认维护者的响应速度以及是否有安全审计。  
- **适用场景**：非常适合原型、内部工具或中小型插件/主题的本地化流程；在大规模生产环境使用前，建议进行一次安全审查并锁定版本号，以防止上游更新引入不兼容或安全风险。  

综上，wp‑cli/i18n‑command 能显著缩短 WordPress 项目的国际化开发周期，接入方式简单，经过适当的依赖锁定和安全评估后即可在生产环境中稳定使用。

## 🧭 Practical evaluation

**Value:** wp-cli/i18n-command helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 116 GitHub stars
- 60 forks
- updated 2026-05-14
- primary language: Gherkin
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 44/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 70/100 |
| recency | 80/100 |
| adoption | 44/100 |
| production | 68/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/wp-cli/i18n-command) · [← Back to DevTools](./README.md)</sub>
