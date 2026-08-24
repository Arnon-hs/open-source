# Kwisma/cf-SubCloud

[![Stars](https://img.shields.io/github/stars/Kwisma/cf-SubCloud?style=flat-square&color=yellow)](https://github.com/Kwisma/cf-SubCloud/stargazers) [![Forks](https://img.shields.io/github/forks/Kwisma/cf-SubCloud?style=flat-square&color=blue)](https://github.com/Kwisma/cf-SubCloud/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> 快速生成mihomo（clash  meta）配置文件,  适用于软路由 mihomo 内核，clash meta 客户端等

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 588 |
| 🍴 **Forks** | 335 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cf-workers` `clash-meta` `clashmi` `cloudflare-workers` `mihomo` `mihomo-config` `mihomo-party`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Kwisma’s **cf‑SubCloud** is a JavaScript utility that quickly generates configuration files for the *mihomo* (Clash Meta) engine, making it easy to set up the mihomo kernel on soft‑router platforms or use Clash Meta clients. It automates the creation of subscription‑based rulesets, saving users the manual editing typically required for Clash‑compatible proxies.

**Value**  
- **Speed & Consistency** – By converting raw subscription URLs into ready‑to‑use mihomo configs, it eliminates syntax errors and reduces the time spent on repetitive copy‑paste tasks.  
- **Cross‑Platform Fit** – Works both for soft‑router deployments (e.g., OpenWrt, pfSense) and desktop/mobile Clash Meta clients, covering a broad user base.  
- **Open‑Source Transparency** – With ~588 stars and an active fork count, the community can audit, extend, or tailor the generator to specific routing policies.

**Practical Adoption Path**  
1. **Read the README** – Verify the required Node.js version and any environment variables (e.g., subscription URLs, output paths).  
2. **Prototype** – Clone the repo, run the sample script on a test machine, and generate a config for a single subscription to confirm the output matches your router/client expectations.  
3. **Integrate** – Wrap the CLI call or import the core module into your existing provisioning pipeline (e.g., a Docker container that rebuilds the router’s config nightly).  
4. **Validate** – Load the generated file into your mihomo instance, check for parsing errors, and perform a functional test of proxy routing.  

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑07‑10) and has a healthy star/fork ratio, indicating community interest.  
- **Stability**: The core functionality is straightforward (JSON/YAML generation), but the integration surface (how you feed subscriptions and where you store the output) is not fully documented, so a small proof‑of‑concept is advisable.  
- **Risks**: Dependency on Node.js packages may introduce version‑drift; ensure you pin versions and monitor upstream updates. Also, confirm that the generated config aligns with any custom rules your environment requires.  

Overall, cf‑SubCloud is a solid candidate for internal or prototype deployments that need automated Clash Meta configuration, provided you perform an initial validation step and lock down its runtime dependencies before scaling to production.

### Русский

Резюме проекта Kwisma/cf-SubCloud:

Квизма/Суб-Клауд - это open-source проект, позволяющий быстро генерировать конфигурационные файлы для mihomo (clash meta) и используемый в сочетании с внутренними решениями, такими как мягкие роутеры с михомо-ядрами и клиенты clash meta. Этот проект может быть полезен в сценариях, когда README и активность проекта соответствуют конкретной рабочей процессу. Готовность проекта к производственному использованию оценивается как средняя, поэтому он может быть использован для прототипирования или внутренних рабочих процессов после проверки зависимостей и поддержки.

### 中文

**Kwisma/cf-SubCloud 简介**

Kwisma/cf-SubCloud 是一个开源项目，用于快速生成 mihomo (clash meta) 配置文件，适用于软路由 mihomo 内核、clash meta 客户端等。该项目可以帮助用户快速生成配置文件，提高工作效率。

**价值**

Kwisma/cf-SubCloud 的价值在于它可以帮助用户快速生成 mihomo 配置文件，适用于软路由 mihomo 内核、clash meta 客户端等。它可以节省用户的时间和精力，提高工作效率。

**典型接入方式**

Kwisma/cf-SubCloud 可以通过以下方式接入：

1. 克隆项目：通过 GitHub 克隆 Kwisma/cf-SubCloud 项目。
2. 安装依赖：安装必要的依赖包，包括 JavaScript 等。
3. 配置文件生成：使用 Kwisma/cf-SubCloud 生成 mihomo 配置文件。

**生产可用性**

Kwisma/cf-SubCloud 的生产可用性为中等（Medium）。它适用于内部工作流或原型开发，但

## 🧭 Practical evaluation

**Value:** Kwisma/cf-SubCloud may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 588 GitHub stars
- 335 forks
- updated 2026-07-10
- primary language: JavaScript
- 7 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 63/100 |
| stars | 59/100 |
| topics | 88/100 |
| outlook | 56/100 |
| quality | 65/100 |
| recency | 40/100 |
| adoption | 60/100 |
| production | 54/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-10 · [View on GitHub](https://github.com/Kwisma/cf-SubCloud) · [← Back to Misc](./README.md)</sub>
