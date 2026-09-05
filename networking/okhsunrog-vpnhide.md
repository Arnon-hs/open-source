# okhsunrog/vpnhide

[![Stars](https://img.shields.io/github/stars/okhsunrog/vpnhide?style=flat-square&color=yellow)](https://github.com/okhsunrog/vpnhide/stargazers) [![Forks](https://img.shields.io/github/forks/okhsunrog/vpnhide?style=flat-square&color=blue)](https://github.com/okhsunrog/vpnhide/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> Hide active VPN from selected Android apps (kernel module + LSPosed + Zygisk)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 422 |
| 🍴 **Forks** | 21 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `gki` `kernel-module` `kernelsu` `kotlin` `kprobes` `lsposed` `magisk` `privacy` `root` `rust` `vpn`

## 🎯 Categories

Networking · Mobile

## 📝 Summary

### English

**Project Summary:**

okhsunrog/vpnhide is an open-source project that allows Android users to hide their active VPN from selected apps, leveraging kernel modules, LSPosed, and Zygisk technologies. This tool is particularly useful for users who require a secure workflow, such as journalists or individuals working with sensitive information. With its Kotlin-based implementation and medium production readiness, it's suitable for prototype development or internal workflows, but requires careful dependency and maintenance checks before production deployment.

**Value:**

The value proposition of vpnhide lies in its ability to provide a secure workflow by hiding active VPN connections from selected apps. This can be particularly useful for individuals working with sensitive information or those who require an extra layer of security.

**Practical Adoption Path:**

To adopt vpnhide, start by evaluating its feasibility through a small proof of concept. This involves checking the README documentation to understand the setup process and potential challenges. Once you've validated the setup cost, you can proceed with integrating the project into your workflow.

**Production Readiness:**

vpnhide has a medium production readiness score, indicating that it's suitable for prototype development or internal workflows. However, before deploying it in a production environment, it's essential to perform dependency and maintenance checks to ensure its stability and reliability. This includes

### Русский

**okhsunrog/vpnhide** – open‑source модуль ядра + LSPosed/Zygisk, позволяющий скрывать активное VPN‑соединение от выбранных приложений Android (например, банковских или стриминговых сервисов). Типовой сценарий: в тестовой среде подключаем модуль, через Zygisk указываем список пакетов, которым VPN будет скрыт, и проверяем работу приложения; при положительном результате можно масштабировать решение для внутренних прототипов или ограниченных продакшн‑сред. Готовность к production — средняя: проект активно поддерживается (обновлён 27 июня 2026, 422★), но требует предварительной проверки интеграции, настройки ядра и оценки затрат на поддержку.

### 中文

**okhsunrog/vpnhide 简介**

okhsunrog/vpnhide 是一个开源项目，用于在 Android 设备上隐藏 VPN 活动，防止特定应用程序检测到 VPN。它通过 kernel 模块、LSPosed 和 Zygisk 技术实现。

**价值**

okhsunrog/vpnhide 对于那些需要隐私保护的用户或开发者来说非常有价值。它可以帮助用户在使用 VPN 时避免被特定应用程序检测到，从而保护用户的隐私。

**典型接入方式**

okhsunrog/vpnhide 的接入方式如下：

1. 安装 LSPosed 和 Zygisk
2. 编译和加载 kernel 模块
3. 配置 VPN 和 LSPosed/Zygisk

**生产可用性**

okhsunrog/vpnhide 的生产可用性为 中等。虽然它可以用于内部工作流或原型测试，但在生产环境中使用之前，需要进行依赖性检查和维护检查。

## 🧭 Practical evaluation

**Value:** okhsunrog/vpnhide may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 422 GitHub stars
- 21 forks
- updated 2026-06-27
- primary language: Kotlin
- 15 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 69/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 50/100 |
| production | 67/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/okhsunrog/vpnhide) · [← Back to Networking](./README.md)</sub>
