# feder-cr/invisible_playwright

[![Stars](https://img.shields.io/github/stars/feder-cr/invisible_playwright?style=flat-square&color=yellow)](https://github.com/feder-cr/invisible_playwright/stargazers) [![Forks](https://img.shields.io/github/forks/feder-cr/invisible_playwright?style=flat-square&color=blue)](https://github.com/feder-cr/invisible_playwright/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> Anti-Detect Browser that passes every bot detection test. Drop-in Playwright replacement.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.6k |
| 🍴 **Forks** | 168 |
| 💻 **Language** | Python |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anti-bot` `anti-detect-browser` `automation` `bot-evasion` `browser-automation` `browser-fingerprinting` `captcha` `captcha-bypass` `fingerprint` `fingerprint-spoofing` `fingerprintjs` `firefox`

## 🎯 Categories

Automation

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
feder‑cr/invisible_playwright is an open‑source, anti‑detect browser that works as a drop‑in replacement for Playwright, reliably bypassing bot‑detection mechanisms. Written in Python and backed by a vibrant community (1,563 ★, 168 forks, recent commits), it lets you automate repetitive web‑tasks, stitch together tools, and schedule workflows without the usual fingerprinting hurdles.

**Value**  
- **Bot‑resistant automation** – By masking typical automation fingerprints, it lets you scrape, test, or interact with sites that block conventional headless browsers.  
- **Workflow acceleration** – Replace manual, click‑through steps with reliable scriptable actions, enabling repeatable pipelines and scheduled jobs.  
- **Seamless integration** – Its API/SDK/CLI mirrors Playwright’s interface, so existing Playwright scripts can be switched with minimal code changes.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, install the Python package, and run the provided demo scripts to verify that your target sites are passed by the anti‑detect layer.  
2. **Replace Playwright** – Update your `import` statements (`from invisible_playwright import sync_playwright` etc.) and run your existing Playwright test suite; adjust any custom launch options if needed.  
3. **Integrate** – Hook the library into CI/CD pipelines, orchestration tools (e.g., Airflow, Prefect) or scheduling services (cron, GitHub Actions) to automate recurring tasks.  
4. **Validate & Harden** – Add monitoring for detection failures, and pin the library version to guard against upstream changes.

**Production Readiness**  
- **Activity & Adoption** – Recent commits (as of 2026‑06‑30), strong star/fork count, and a broad set of topics indicate an active ecosystem.  
- **Stability** – The API is stable and mirrors Playwright, reducing migration risk; the project follows semantic versioning.  
- **Risk Considerations** – While no glaring metadata issues appear, a final review of the license (MIT/Apache‑style) and a security audit of the anti‑detect components is advisable before a full‑scale rollout.  

Overall, invisible_playwright is a mature, high‑confidence candidate for pilots and production use where reliable, undetectable browser automation is required.

### Русский

**feder-cr/invisible_playwright** — это open‑source anti‑detect браузер‑обёртка над Playwright, способный пройти любые проверки на ботов, тем самым устраняя необходимость ручного взаимодействия с веб‑интерфейсами. Его типичное применение — автоматизация повторяющихся задач (скрейпинг, тестирование, интеграция сервисов) и планирование операций в рамках CI/CD‑конвейеров, используя простой API/CLI на Python. Проект считается почти готовым к production: активные коммиты, 1563 звезды, 168 форков, широкая экосистема тем и недавнее обновление (30 июня 2026 г.), однако перед масштабным внедрением следует проверить лицензию, безопасность и наличие поддерживающих мейнтейнеров.

### 中文

**项目简介**

feder-cr/invisible_playwright 是一个开源项目，提供了一个可替换的 Playwright 实现，能够通过各种 bot 检测测试。它可以帮助自动化流程，减少重复的手动操作。

**价值**

该项目的价值在于，它可以帮助开发者移除重复的手动操作，从而提高工作效率和自动化流程的可靠性。它还可以帮助开发者连接工具，建立可重复的流程，并且可以定时执行操作任务。

**典型接入方式**

该项目提供了 API、SDK 和 CLI 等接口，开发者可以根据需要选择适合自己的接入方式。其语言元数据为 Python，支持 20 个主题。

**生产可用性**

该项目的生产可用性非常高，最近有活跃的更新，已有 1563 个 GitHub 星和 168 个 fork。它的安全性和许可证都需要进一步检查，但总体来说，它是一个值得信赖的开源项目。

## 🧭 Practical evaluation

**Value:** feder-cr/invisible_playwright helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1563 GitHub stars
- 168 forks
- updated 2026-06-30
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 68/100 |
| topics | 100/100 |
| outlook | 65/100 |
| quality | 69/100 |
| recency | 40/100 |
| adoption | 65/100 |
| production | 60/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/feder-cr/invisible_playwright) · [← Back to Automation](./README.md)</sub>
