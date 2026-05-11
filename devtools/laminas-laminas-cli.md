# laminas/laminas-cli

[![Stars](https://img.shields.io/github/stars/laminas/laminas-cli?style=flat-square&color=yellow)](https://github.com/laminas/laminas-cli/stargazers) [![Forks](https://img.shields.io/github/forks/laminas/laminas-cli?style=flat-square&color=blue)](https://github.com/laminas/laminas-cli/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Console command runner, exposing commands written in Laminas MVC and Mezzio components and applications

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 56 |
| 🍴 **Forks** | 23 |
| 💻 **Language** | PHP |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `command-line` `command-line-tool` `laminas` `mezzio`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Summary**  
Laminas‑CLI is a lightweight console command runner that lets you expose and execute commands written for Laminas MVC or Mezzio applications. By providing a unified CLI entry point, it streamlines local development tasks, CI automation, and routine engineering workflows.  

**Value**  
- **Time‑saving**: Developers can invoke framework‑specific actions (e.g., migrations, cache warm‑ups, code generators) without writing custom scripts, reducing repetitive boiler‑plate.  
- **Consistent tooling**: Because the commands live inside the same codebase as the application, the CLI stays in sync with application logic, improving reliability of CI feedback and local testing.  
- **Low friction**: The package ships with sensible defaults and integrates directly with existing Laminas MVC/Mezzio projects, so teams can adopt it without major architectural changes.  

**Practical adoption path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣ | Add the package via Composer (`composer require laminas/laminas-cli`) | Pulls in the CLI core and registers the console entry point. |
| 2️⃣ | Register the CLI module in your application config (`'modules' => ['Laminas\Cli']`) | Enables the framework to discover commands. |
| 3️⃣ | Create command classes that implement `Laminas\Cli\Command\AbstractCommand` (or use existing Laminas/Mezzio commands). | Leverages the same dependency‑injection container used by the app. |
| 4️⃣ | Wire the commands in `module.config.php` under the `laminas-cli` key. | Makes the commands discoverable by the `laminas` executable. |
| 5️⃣ | Run `vendor/bin/laminas <command>` locally, add scripts to `composer.json` for convenience, and integrate the same invocations into CI pipelines. | Provides a single source of truth for both developers and CI. |
| 6️⃣ | (Optional) Extend with custom middleware or integrate with other tooling (e.g., Docker entrypoints, Git hooks). | Tailors the CLI to specific workflow needs. |

**Production readiness**  
- **Maturity**: Medium. The project is actively maintained (last update 2026‑05‑11) and has modest community adoption (≈56 ★, 23 forks).  
- **Suitability**: Ideal for prototypes, internal tools, and as a backbone for shared engineering scripts. For mission‑critical production environments, perform a dependency audit (check for transitive security advisories) and verify that the command set is version‑locked.  
- **Risks**: No major licensing or metadata concerns identified, but you should confirm the current license compatibility with your stack and review any open security issues on the repository before promoting to production.  

Overall, laminas‑cli offers a pragmatic way to unify command‑line tasks across Laminas MVC and Mezzio projects, delivering measurable developer‑efficiency gains while requiring only a modest integration effort.

### Русский

**laminas/laminas-cli** — это инструмент командной строки, позволяющий запускать и управлять командами, написанными в компонентах Laminas MVC и Mezzio, что ускоряет локальные задачи разработки и автоматизирует проверки в CI. Его типичное внедрение — добавление в проект как dev‑зависимость и использование готовых CLI‑команд для генерации кода, миграций и скриптов сборки, тем самым сокращая время цикла разработки и ревью. Готовность к production — средняя: проект стабилен и активно обновляется (56 звёзд, 23 форка, последний коммит 2026‑05‑11), но перед выпуском в продакшн стоит проверить лицензирование, безопасность зависимостей и наличие активных мейнтейнеров.

### 中文

**项目简介**  
laminas/laminas-cli 是一个基于 Laminas MVC 与 Mezzio 的控制台命令运行器，能够把框架内的业务逻辑直接包装为 CLI 命令，供本地开发、自动化脚本和 CI 环境使用。

**价值**  
- **提升开发效率**：将已有的 MVC/Mezzio 代码复用为命令行工具，避免重复实现相同功能。  
- **自动化日常任务**：可在本地或 CI 中统一执行数据库迁移、缓存清理、代码生成等工程任务，缩短反馈循环。  
- **统一入口**：通过统一的 CLI 接口管理项目所有脚本，降低团队成员之间的认知成本。

**典型接入方式**  
1. 在项目的 `composer.json` 中添加依赖 `laminas/laminas-cli`。  
2. 在 `config/autoload/cli.global.php`（或 Mezzio 的 `config/pipeline.php`）中注册命令类，命令类实现 `Laminas\Cli\Command\AbstractCommand`。  
3. 运行 `vendor/bin/laminas` 即可列出并执行已注册的命令，亦可在 CI 脚本中直接调用，例如 `vendor/bin/laminas db:migrate`。

**生产可用性**  
- **成熟度**：中等（Medium）。代码已在多个内部原型和内部工作流中验证，可用于生产环境的非关键任务。  
- **依赖与维护**：依赖 Laminas MVC / Mezzio，需确认这些组件的安全更新和兼容性；项目最近更新于 2026‑05‑11，GitHub 星标 56、Fork 23，活跃度一般。  
- **风险**：许可证、长期维护者状态以及安全审计仍需进一步确认后方可在高风险生产环境使用。  

总体而言，laminas-cli 适合作为内部工具链或原型项目的命令行入口，若在生产环境使用，建议做好依赖审计并安排专人维护。

## 🧭 Practical evaluation

**Value:** laminas/laminas-cli helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 56 GitHub stars
- 23 forks
- updated 2026-05-11
- primary language: PHP
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 37/100 |
| topics | 63/100 |
| outlook | 75/100 |
| quality | 66/100 |
| recency | 100/100 |
| adoption | 37/100 |
| production | 71/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/laminas/laminas-cli) · [← Back to DevTools](./README.md)</sub>
