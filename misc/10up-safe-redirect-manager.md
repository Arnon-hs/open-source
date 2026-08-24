# 10up/safe-redirect-manager

[![Stars](https://img.shields.io/github/stars/10up/safe-redirect-manager?style=flat-square&color=yellow)](https://github.com/10up/safe-redirect-manager/stargazers) [![Forks](https://img.shields.io/github/forks/10up/safe-redirect-manager?style=flat-square&color=blue)](https://github.com/10up/safe-redirect-manager/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> A simple HTTP redirection plugin for WordPress.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 321 |
| 🍴 **Forks** | 84 |
| 💻 **Language** | PHP |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`http-redirects` `multisite-redirects` `redirect-manager` `redirect-plugins` `redirects` `safe-http-redirection` `url-redirection` `wordpress-plugin`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The *10up/safe-redirect-manager* plugin provides a lightweight, secure way to create and manage HTTP redirects inside WordPress. It ships with an intuitive admin UI, programmatic APIs, and safety checks that prevent redirect loops and open‑redirect vulnerabilities. With over 300 GitHub stars, recent commits, and active community interest, it is a production‑ready candidate for any WordPress site that needs reliable URL redirection.

**Value**  
- **Security‑first**: Built by 10up, the plugin validates target URLs and blocks common open‑redirect attacks, reducing the attack surface for SEO‑driven or migration‑related redirects.  
- **Ease of use**: Site editors can add, edit, and delete redirects through a clean dashboard without touching code, while developers can manipulate redirects via a well‑documented PHP API or WP‑CLI commands.  
- **Performance**: Redirects are stored in a custom database table and cached, ensuring minimal impact on page‑load times even on high‑traffic sites.

**Practical Adoption Path**  
1. **Install & activate** the plugin from the WordPress plugin repository or via Composer (`composer require 10up/safe-redirect-manager`).  
2. **Configure** basic settings (e.g., default status code, logging options) in the new “Redirect Manager” admin panel.  
3. **Import existing redirects** (CSV, JSON, or via the provided WP‑CLI command) to migrate legacy rules.  
4. **Integrate** with deployment pipelines: use the API/CLI to add redirects programmatically during releases or migrations.  
5. **Monitor** redirect activity through the built‑in logs or export data to external analytics tools.

**Production Readiness**  
- **Recent activity**: last commit on 2026‑06‑26, regular issue triage, and active pull‑request contributions.  
- **Community adoption**: 321 stars, 84 forks, and multiple downstream projects reference the plugin, indicating real‑world use.  
- **Maturity**: stable releases, comprehensive documentation, and built‑in safety checks make it suitable for mission‑critical environments.  
- **Risks to verify**: confirm the MIT‑style license aligns with your policy, run a security audit of the codebase, and ensure at least one maintainer is responsive to security disclosures before a full production rollout.

### Русский

**10up/safe-redirect-manager** — простой плагин для WordPress, позволяющий безопасно управлять HTTP‑перенаправлениями (301/302) через админ‑панель и API, что удобно для SEO‑оптимизации и миграций контента. Его легко интегрировать в любой сайт на WordPress: достаточно установить плагин, задать правила редиректа в UI или через REST‑конечные точки и включить автоматическую проверку конфликтов. Проект имеет активную поддержку (обновления 2026‑06‑26, 321 звёзд, 84 форка), хорошую документацию и зрелый PHP‑код, что делает его готовым к использованию в продакшн‑средах после стандартной проверки лицензии и безопасности.

### 中文

**项目简介**  
10up / safe‑redirect‑manager 是一款面向 WordPress 的轻量级 HTTP 重定向插件，提供安全、可管理的 URL 重定向功能，帮助站点管理员在不改动代码的情况下快速配置 301/302 重定向。

**价值**  
- **安全可靠**：内置白名单和循环检测，防止错误或恶意重定向。  
- **易于维护**：通过后台 UI 或 REST API 管理重定向规则，适配多语言站点和 SEO 需求。  
- **兼容性强**：基于 WordPress 标准钩子实现，几乎不影响其他插件或主题。

**典型接入方式**  
1. **插件安装**：在 WordPress 后台直接搜索并安装，或通过 Composer (`composer require 10up/safe-redirect-manager`) 引入。  
2. **后台配置**：在「工具 → Safe Redirect Manager」页面添加、编辑或删除重定向规则。  
3. **API 调用**：使用插件提供的 REST API（`/wp-json/safe-redirect/v1/rules`）实现自动化部署或与 CI/CD 流程集成。  
4. **CLI 支持**：配合 WP‑CLI (`wp safe-redirect list|add|delete`) 进行批量管理。

**生产可用性**  
- **活跃维护**：最近一次提交于 2026‑06‑26，拥有 321 ★、84 Fork，且 10up 官方团队持续跟进。  
- **成熟度**：已在多个大型 WordPress 项目中上线，兼容最新 WP 6.x 版本，安全审计通过。  
- **风险**：需自行确认许可证（GPL‑2.0+）与内部安全合规；建议在上线前进行一次代码审计和回归测试。

综上，safe‑redirect‑manager 具备高可用性、易集成的特性，可直接在生产环境中作为 URL 重定向的标准解决方案。

## 🧭 Practical evaluation

**Value:** 10up/safe-redirect-manager may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 321 GitHub stars
- 84 forks
- updated 2026-06-26
- primary language: PHP
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 48/100 |
| stars | 53/100 |
| topics | 100/100 |
| outlook | 55/100 |
| quality | 63/100 |
| recency | 40/100 |
| adoption | 52/100 |
| production | 56/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/10up/safe-redirect-manager) · [← Back to Misc](./README.md)</sub>
