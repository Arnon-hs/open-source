# crazywhalecc/static-php-cli

[![Stars](https://img.shields.io/github/stars/crazywhalecc/static-php-cli?style=flat-square&color=yellow)](https://github.com/crazywhalecc/static-php-cli/stargazers) [![Forks](https://img.shields.io/github/forks/crazywhalecc/static-php-cli?style=flat-square&color=blue)](https://github.com/crazywhalecc/static-php-cli/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Build standalone portable PHP binaries on Linux, macOS, Windows, with PHP project together, with popular extensions included.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.9k |
| 🍴 **Forks** | 397 |
| 💻 **Language** | PHP |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`alpine` `binary` `frankenphp` `php` `php-cli` `php-src` `php8` `static` `static-link-binary` `swoole` `workerman`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary**  
`crazywhalecc/static-php-cli` bundles a full PHP runtime—including popular extensions—into a single portable binary for Linux, macOS, and Windows. This lets developers ship PHP‑based tools or user‑facing interfaces without requiring a separate PHP installation or complex dependency management.

**Value**  
- **Zero‑install deployment** – The static binary contains everything needed to run PHP code, eliminating the “PHP not installed” hurdle on client machines.  
- **Consistent environment** – All builds use the same PHP version and compiled extensions, guaranteeing that the UI behaves identically across platforms.  
- **Faster UI delivery** – Teams can focus on building the front‑end logic while relying on the pre‑packaged runtime, reducing custom UI scaffolding and integration effort.

**Practical Adoption Path**  
1. **Evaluate the binary** – Download the appropriate platform binary from the releases page and run a simple script (e.g., `php -v`) to confirm the bundled version and extensions.  
2. **Integrate into CI/CD** – Add the binary to your build pipeline (e.g., as an artifact or Docker base image) and use it to compile or execute PHP‑based UI components, CLI tools, or micro‑services.  
3. **Replace existing PHP dependencies** – Swap out system‑wide PHP installations with the static binary in production containers, CI runners, or end‑user distribution packages.  
4. **Monitor and extend** – If you need additional extensions, fork the repo and modify the build script; the project’s Makefile‑style workflow makes adding modules straightforward.

**Production Readiness**  
- **Activity & Adoption** – 1,904 ★, 397 forks, recent commits (as of 2026‑07‑06), and a healthy issue/PR flow indicate an active community.  
- **Stability** – The binary is built from officially released PHP sources and includes widely used extensions, providing a reliable baseline for production workloads.  
- **Risk Assessment** – No glaring licensing or security red flags have been identified, though a final review of the project’s license (MIT‑style) and any disclosed CVEs for bundled extensions is advisable.  
- **Overall** – Given its strong community signals, up‑to‑date maintenance, and clear path to integration, `static-php-cli` is ready for a serious pilot or full production rollout after the standard security and compliance checks.

### Русский

**crazywhalecc/static-php-cli** — это open‑source утилита, позволяющая собрать полностью автономные PHP‑бинарники для Linux, macOS и Windows, включающие популярные расширения и ваш проект в едином пакете. Типичный сценарий — разработчики быстро упаковывают backend‑логика и UI‑компоненты в готовый к развертыванию исполняемый файл, что ускоряет доставку пользовательского интерфейса без необходимости отдельной настройки веб‑сервера. По активности репозитория (1904 ★, 397 forks, обновления до 2026‑07‑06) и наличию всех необходимых API/CLI‑интерфейсов проект считается готовым к пилотному использованию в продакшн‑среде, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**crazywhalecc/static-php-cli 简介**

crazywhalecc/static-php-cli 是一个开源项目，用于在 Linux、macOS 和 Windows 平台上构建独立的可移植 PHP 二进制文件和 PHP 项目，包括流行的扩展。它旨在帮助开发人员快速搭建用户界面并减少自定义 UI 工作量。

**价值**

crazywhalecc/static-php-cli 帮助开发人员：

* 快速搭建产品 UI
* 重用界面组件
* 改善前端交付

**典型接入方式**

开发人员可以通过以下方式接入 crazywhalecc/static-php-cli：

* 直接使用 CLI 工具构建 PHP 二进制文件和项目
* 集成到 CI/CD 流程中自动构建和部署 PHP 项目
* 使用 SDK 或 API 与 crazywhalecc/static-php-cli 进行交互

**生产可用性**

crazywhalecc/static-php-cli 具备高生产可用性：

* 最近活跃，采用广泛，生态系统信号强
* GitHub 星标 1904，分支 397，

## 🧭 Practical evaluation

**Value:** crazywhalecc/static-php-cli helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1904 GitHub stars
- 397 forks
- updated 2026-07-06
- primary language: PHP
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 65/100 |
| stars | 70/100 |
| topics | 100/100 |
| outlook | 63/100 |
| quality | 71/100 |
| recency | 40/100 |
| adoption | 68/100 |
| production | 59/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/crazywhalecc/static-php-cli) · [← Back to DevTools](./README.md)</sub>
