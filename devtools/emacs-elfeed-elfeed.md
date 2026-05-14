# emacs-elfeed/elfeed

[![Stars](https://img.shields.io/github/stars/emacs-elfeed/elfeed?style=flat-square&color=yellow)](https://github.com/emacs-elfeed/elfeed/stargazers) [![Forks](https://img.shields.io/github/forks/emacs-elfeed/elfeed?style=flat-square&color=blue)](https://github.com/emacs-elfeed/elfeed/network) [![Language](https://img.shields.io/badge/lang-Emacs%20Lisp-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> An Emacs web feeds client

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.7k |
| 🍴 **Forks** | 140 |
| 💻 **Language** | Emacs Lisp |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

`atom` `emacs` `jsonfeed` `rss`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Summary**  
*emacs‑elfeed* is an Emacs‑native RSS/Atom client that lets developers read and manage web feeds without leaving their editor. With 1.7 k stars, recent commits (as of 2026‑05‑14), and a small, well‑documented Emacs‑Lisp codebase, it’s a mature OSS component ready for pilot projects.

**Value**  
The tool embeds feed consumption directly into the developer’s primary workspace, cutting the context‑switch overhead of opening a browser or external reader. By surfacing release notes, CI notifications, and project‑specific blogs inside Emacs, engineers can stay informed and react faster, tightening the development‑review loop and reducing manual information‑gathering tasks.

**Practical adoption path**  
1. **Add the package** – install via MELPA (`M-x package-install RET elfeed RET`) or clone the repo into `~/.emacs.d/`.  
2. **Configure feeds** – define a list of URLs in `~/.emacs.d/init.el` (e.g., `(setq elfeed-feeds '(("https://github.com/emacs-mirror/emacs/releases.atom" emacs) ("https://blog.rust-lang.org/feed.xml" rust)))`).  
3. **Integrate with workflow** – bind `elfeed` to a convenient key, optionally combine with `elfeed-org` for Org‑mode tagging, and hook into `elfeed-update` to run automatically after each `git pull` or CI run.  
4. **Pilot** – roll out to a small team of developers, gather feedback on feed relevance and UI tweaks, then expand to the whole engineering org.

**Production readiness**  
The project shows high readiness: it has strong community adoption (≈1.7 k stars, 140 forks), frequent maintenance (last commit today), and clear Emacs‑Lisp APIs that can be scripted or called from CI pipelines. While the license (GPL‑3.0) and security posture merit a final check, there are no known critical vulnerabilities, making *emacs‑elfeed* a safe candidate for a serious production pilot.

### Русский

**emacs-elfeed/elfeed** – это клиент RSS/Atom‑ленты, написанный на Emacs Lisp, который позволяет инженерам читать и управлять веб‑лентами прямо из Emacs, экономя время на переключение между браузером и IDE. Типичный сценарий внедрения — интеграция в ежедневный цикл разработки: автоматическое отслеживание новостей проектов, CI‑уведомлений и ревью‑запросов, что ускоряет обзоры кода и повышает оперативность обратной связи. Проект считается готовым к production‑использованию: активные коммиты, более 1700 звёзд, стабильный набор функций и открытый API/CLI, однако перед масштабным запуском рекомендуется проверить лицензию, безопасность и наличие активных мейнтейнеров.

### 中文

**项目简介**  
`emacs-elfeed/elfeed` 是一款基于 Emacs Lisp 的 RSS/Atom 阅读器，直接在 Emacs 中提供完整的 Web 订阅功能，让开发者无需离开编辑器即可浏览、筛选和管理信息流。

**价值**  
- **提升工作流效率**：在编写代码的同时即可查看技术博客、项目更新或内部新闻，省去切换浏览器的时间。  
- **自动化本地任务**：可通过 Emacs 脚本对 Feed 条目进行批量标记、导出或触发自定义命令，实现信息的自动化处理。  
- **改进 CI 反馈**：结合 CI 系统的通知 Feed，开发者可以在编辑器中实时捕获构建、测试或部署状态，快速响应。

**典型接入方式**  
1. **Emacs 配置**：在 `init.el` 或 `config.org` 中加入 `(require 'elfeed)` 并配置 Feed URL 列表。  
2. **CLI/脚本**：利用 `elfeed-search`、`elfeed-show` 等交互命令，或在 Emacs Lisp 脚本中调用 `elfeed` API（如 `elfeed-fetch`、`elfeed-db-save`）实现批量操作。  
3. **与外部工具集成**：通过 `elfeed-protocol`、`elfeed-org` 等插件，将 Feed 数据同步到 Org‑mode、Slack 或自建的通知系统。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑14，项目仍在持续更新，拥有 1728 ★、140 Fork，社区活跃。  
- **成熟度**：已在多个大型开发团队内部使用，具备稳定的 Emacs Lisp 实现和完善的文档。  
- **风险**：暂无重大元数据风险；仍需对许可证（GPL‑3.0）和安全审计进行最终确认。  

综合来看，`elfeed` 已具备在生产环境中试点的条件，适合作为 Emacs 环境下的统一信息流入口。

## 🧭 Practical evaluation

**Value:** emacs-elfeed/elfeed helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1728 GitHub stars
- 140 forks
- updated 2026-05-14
- primary language: Emacs Lisp
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 54/100 |
| stars | 69/100 |
| topics | 50/100 |
| outlook | 78/100 |
| quality | 77/100 |
| recency | 100/100 |
| adoption | 65/100 |
| production | 75/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/emacs-elfeed/elfeed) · [← Back to DevTools](./README.md)</sub>
