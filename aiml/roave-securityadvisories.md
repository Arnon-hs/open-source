# Roave/SecurityAdvisories

[![Stars](https://img.shields.io/github/stars/Roave/SecurityAdvisories?style=flat-square&color=yellow)](https://github.com/Roave/SecurityAdvisories/stargazers) [![Forks](https://img.shields.io/github/forks/Roave/SecurityAdvisories?style=flat-square&color=blue)](https://github.com/Roave/SecurityAdvisories/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> :closed_lock_with_key: Security advisories as a simple composer exclusion list, updated daily

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.9k |
| 🍴 **Forks** | 111 |
| 💻 **Language** | Unknown |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-07-15 |
| 🔍 **Source** | github |

## 🏷️ Topics

`composer` `infosec` `php` `security-advisories` `security-vulnerabilities` `security-vulnerability`

## 🎯 Categories

AI/ML · Security

## 📝 Summary

### English

Here's a brief summary of the Roave/SecurityAdvisories project:

Roave/SecurityAdvisories is an open-source project that provides a daily-updated composer exclusion list for security advisories, allowing developers to add AI capabilities without starting from scratch. This project can be used in prototype development, building RAG (Red, Amber, Green) or agent workflows, and evaluating model tooling, making it suitable for internal workflows and proof-of-concepts. However, its adoption in production requires manual inspection and validation of setup costs due to sparse integration signals and potential dependency and maintenance checks.

### Русский

Резюме проекта Roave/SecurityAdvisories:

Roave/SecurityAdvisories - это открытый проект, который предоставляет список исключений Composer для обновления безопасности daily. Этот проект особенно полезен для прототипирования функций AI и построения RAG или агентных потоков. Проект имеет среднюю готовность к production (Medium), что означает, что он может быть полезен для прототипирования или внутренних потоков, но требует тщательного проверки зависимостей и обслуживания перед выпуском в production.

### 中文

**项目简介**

Roave/SecurityAdvisories 是一个开源项目，提供每日更新的安全建议列表，帮助开发者避免使用已知安全漏洞的依赖项。这个项目通过 Composer 依赖管理工具提供一个简单的排除列表，帮助开发者提高项目的安全性。

**价值**

Roave/SecurityAdvisories 的价值在于它为开发者提供了一个快速的安全建议列表，帮助避免使用已知安全漏洞的依赖项。这个项目特别适合用于 AI/ML 和安全领域的开发。

**典型接入方式**

典型的接入方式是通过 Composer 依赖管理工具，添加以下依赖项：

```json
{
    "require": {
        "roave/securityadvisories": "^2023.4"
    }
}
```

然后，开发者可以使用 Composer 的排除列表功能，排除已知安全漏洞的依赖项。

**生产可用性**

Roave/SecurityAdvisories 的生产可用性为中等（Medium）。这个项目适合用于内部开发、原型开发和测试环境，需要在生产环境中进行额外的依赖项检查和

## 🧭 Practical evaluation

**Value:** Roave/SecurityAdvisories helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 2912 GitHub stars
- 111 forks
- updated 2026-07-15
- 6 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 74/100 |
| topics | 75/100 |
| outlook | 78/100 |
| quality | 82/100 |
| recency | 100/100 |
| adoption | 67/100 |
| production | 75/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-15 · [View on GitHub](https://github.com/Roave/SecurityAdvisories) · [← Back to AI/ML](./README.md)</sub>
