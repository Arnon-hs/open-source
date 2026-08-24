# symfony/recipes-contrib

[![Stars](https://img.shields.io/github/stars/symfony/recipes-contrib?style=flat-square&color=yellow)](https://github.com/symfony/recipes-contrib/stargazers) [![Forks](https://img.shields.io/github/forks/symfony/recipes-contrib?style=flat-square&color=blue)](https://github.com/symfony/recipes-contrib/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-44%2F100-brightgreen?style=flat-square)](#)

> Symfony Contrib Recipes Repositories

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 557 |
| 🍴 **Forks** | 699 |
| 💻 **Language** | PHP |
| 📈 **Score** | 44/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`recipes` `symfony`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`symfony/recipes-contrib` is the community‑maintained collection of Symfony “recipes” that automate the installation and configuration of third‑party bundles and libraries. It provides ready‑made Composer scripts and configuration snippets, helping developers bootstrap Symfony projects faster while keeping the setup reproducible.

**Value**  
The repository supplies curated, version‑locked configuration files (Docker, environment variables, Symfony Flex recipes, etc.) for a wide range of popular PHP packages. By leveraging these recipes you avoid manual copy‑paste of boilerplate code, reduce the risk of mis‑configuration, and benefit from community‑tested defaults that evolve with Symfony releases.

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | Add the Symfony Flex plugin (if not already present) and enable the contrib recipes channel: `composer config extra.symfony.allow-contrib-recipe true` | Allows Composer to pull recipes from this repo automatically. |
| 2️⃣  | Install the desired third‑party bundle via Composer, e.g., `composer require doctrine/doctrine-bundle`. | Flex will detect the package and fetch the matching recipe from `recipes-contrib`. |
| 3️⃣  | Review the generated files (config/packages/*.yaml, .env, Dockerfiles, etc.) and adjust them to your project’s conventions. | The repo provides sensible defaults, but you must verify they fit your environment and security policies. |
| 4️⃣  | Run the usual Symfony checks (`php bin/console doctrine:schema:validate`, `symfony check:security`, etc.) to confirm the integration works. | Guarantees that the recipe’s configuration is compatible with your codebase. |
| 5️⃣  | Commit the generated configuration and keep the recipe version locked in `composer.lock` for reproducibility. | Ensures future builds use the same setup. |

**Production Readiness**  
- **Maturity:** The project is actively maintained (last update 2026‑05‑14) and has a healthy community footprint (≈ 557 ★, 699 forks).  
- **Risk Level:** Medium. The recipes are reliable for prototyping and internal tooling, but because the integration signals are sparse, you should manually verify each recipe’s impact on security, performance, and compatibility with your existing stack.  
- **Recommended Use:** Adopt for non‑critical services, proof‑of‑concepts, or internal applications after a short validation sprint. For customer‑facing production systems, perform a thorough code‑review, run integration tests, and consider pinning the recipe version to avoid unexpected changes during upgrades.  

In short, `symfony/recipes-contrib` can accelerate Symfony project setup, but it requires a brief manual audit before being promoted to production environments.

### Русский

**symfony/recipes-contrib** — набор вспомогательных рецептов для Symfony, позволяющих быстро подключать сторонние пакеты и стандартизировать их конфигурацию. Он удобен в прототипах и внутренних проектах, где требуется автоматизировать настройку зависимостей без написания собственного кода, однако перед выводом в продакшн требуется ручная проверка интеграции и оценка поддержки конкретных пакетов. Готовность к production — средняя: проект активно поддерживается (обновления до 2026‑05‑14, 557 звёзд, 699 форков), но пути интеграции не всегда очевидны и требуют дополнительного тестирования.

### 中文

**项目简介**  
`symfony/recipes-contrib` 是 Symfony 官方社区维护的 **Contrib Recipes** 仓库，收录了大量第三方 PHP 包的 Symfony 配置（Recipe），帮助开发者在使用这些包时能够“一键”获得最佳的 bundle、config、services 等集成文件。

**价值**  
- **快速集成**：通过 Composer 的 Symfony Flex 插件，自动把对应的 Recipe 应用到项目中，省去手动编写或复制配置的时间。  
- **统一规范**：所有配方遵循 Symfony 官方的最佳实践，保证配置风格一致、可维护性高。  
- **社区维护**：拥有 557+ stars、699+ forks，活跃的贡献者会持续更新配方，使其兼容最新的 Symfony 版本和第三方库。

**典型接入方式**  
1. 确保项目已启用 Symfony Flex（`composer require symfony/flex`）。  
2. 在 `composer.json` 中添加 Contrib 仓库（通常不需要手动添加，Flex 会自动从 Packagist 拉取）。  
3. 安装目标第三方库，例如 `composer require doctrine/orm`，Flex 会检测到对应的 recipe 在 `symfony/recipes-contrib` 中并自动执行 `symfony-scripts`，生成 `config/packages/doctrine.yaml`、`services.yaml` 等文件。  
4. 如需手动查看或覆盖配方，可在项目根目录运行 `composer recipes:show doctrine/orm`，或在 `symfony.lock` 中锁定特定版本的 recipe。

**生产可用性**  
- **成熟度**：Medium。配方在社区广泛使用，适合原型、内部工具以及正式项目的快速启动。  
- **使用前检查**：因为配方仅提供默认配置，生产环境仍需根据业务需求审查并可能自定义（如安全、缓存、日志等）。  
- **维护成本**：定期运行 `composer recipes:update` 以获取最新配方；关注项目的 Issue 与 Pull Request，确保关键依赖的配方保持更新。  

综上，`symfony/recipes-contrib` 是加速 Symfony 项目集成第三方库的实用工具，只要在引入前进行一次配置审查，即可安全用于生产环境。

## 🧭 Practical evaluation

**Value:** symfony/recipes-contrib may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 557 GitHub stars
- 699 forks
- updated 2026-05-14
- primary language: PHP
- 2 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 71/100 |
| stars | 58/100 |
| topics | 25/100 |
| outlook | 43/100 |
| quality | 52/100 |
| recency | 20/100 |
| adoption | 62/100 |
| production | 45/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/symfony/recipes-contrib) · [← Back to Misc](./README.md)</sub>
