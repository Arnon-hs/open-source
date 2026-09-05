# asdf-vm/asdf

[![Stars](https://img.shields.io/github/stars/asdf-vm/asdf?style=flat-square&color=yellow)](https://github.com/asdf-vm/asdf/stargazers) [![Forks](https://img.shields.io/github/forks/asdf-vm/asdf?style=flat-square&color=blue)](https://github.com/asdf-vm/asdf/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-77%2F100-brightgreen?style=flat-square)](#)

> Extendable version manager with support for Ruby, Node.js, Elixir, Erlang & more

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 25.4k |
| 🍴 **Forks** | 926 |
| 💻 **Language** | Go |
| 📈 **Score** | 77/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`asdf-vm` `bash` `cli` `elixir` `elvish` `erlang` `fish` `golang` `multiple-languages` `node` `nushell` `powershell`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
asdf‑vm/asdf is an extensible, language‑agnostic version manager that lets engineers install, switch, and isolate runtimes for Ruby, Node.js, Elixir, Erlang, and dozens of other tools with a single CLI. Its plug‑in architecture and declarative `.tool‑versions` files streamline local development, CI pipelines, and team onboarding, cutting down the “it works on my machine” friction. With >25 k stars, active maintenance, and a Go‑based core, it’s a mature OSS candidate for production use.  

**Value**  
- **Time savings** – developers can declare required runtime versions once and have the tool automatically provision them on workstations and CI agents, eliminating manual install steps.  
- **Consistency** – the same `.tool‑versions` file guarantees identical environments across developers, CI, and staging, reducing bugs caused by version drift.  
- **Extensibility** – new languages or tools are added via community‑maintained plugins, so teams can expand coverage without changing the core.  

**Practical Adoption Path**  
1. **Pilot** – Add `asdf` to a few developer workstations and a CI job; use the existing plugins for the languages you already use.  
2. **Standardize** – Commit a repository‑wide `.tool‑versions` file and update onboarding docs to make `asdf install` the first step for new contributors.  
3. **Automate** – Integrate `asdf install` into container build scripts or CI pipelines to guarantee the exact runtime versions are present before builds or tests run.  
4. **Extend** – If a needed tool lacks a plugin, create a small custom plugin (the API is well‑documented) and publish it internally or upstream.  

**Production Readiness**  
- **Activity & Adoption**: 25 429 GitHub stars, 926 forks, recent commits (as of 2026‑07‑02), and a growing ecosystem of 17 topics indicate strong community support.  
- **Stability**: The core is written in Go, a compiled language with a low runtime overhead, and the CLI is version‑stable across releases.  
- **Risk Assessment**: No major metadata or licensing concerns have been identified, though a final security audit and maintainer verification are recommended before a full‑scale rollout.  

Overall, asdf‑vm/asdf offers a high‑impact, low‑friction way to unify runtime management across development and CI environments, making it a solid candidate for production deployment after a short pilot and security review.

### Русский

**asdf‑vm/asdf** — расширяемый менеджер версий, поддерживающий Ruby, Node.js, Elixir, Erlang и многие другие инструменты, что позволяет инженерам быстро переключаться между окружениями и автоматизировать локальные задачи и CI‑потоки. Типичный сценарий внедрения — добавление в репозиторий проекта файл `.tool-versions` и настройка CI, после чего все участники получают одинаковые версии зависимостей без ручных установок. Проект считается готовым к production: активные коммиты, более 25 тыс. звёзд, широкое принятие в сообществе и стабильный набор API/CLI, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

asdf-vm/asdf 是一个可扩展的版本管理工具，支持 Ruby、Node.js、Elixir、Erlang 等多种语言，帮助开发者一键切换和管理不同项目的运行环境，显著提升本地开发与 CI/CD 流程效率。它通过简洁的 CLI 接口与插件机制轻松集成到现有工作流，无需复杂配置，即可实现环境自动化。作为拥有近 2.5 万 GitHub 星标、活跃维护且生态完善的开源项目，asdf 在生产环境中具备高可用性，已被大量团队用于稳定开发与部署场景。

## 🧭 Practical evaluation

**Value:** asdf-vm/asdf helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 25429 GitHub stars
- 926 forks
- updated 2026-07-02
- primary language: Go
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 74/100 |
| stars | 94/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 90/100 |
| recency | 80/100 |
| adoption | 88/100 |
| production | 80/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/asdf-vm/asdf) · [← Back to DevTools](./README.md)</sub>
