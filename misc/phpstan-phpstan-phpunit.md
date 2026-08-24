# phpstan/phpstan-phpunit

[![Stars](https://img.shields.io/github/stars/phpstan/phpstan-phpunit?style=flat-square&color=yellow)](https://github.com/phpstan/phpstan-phpunit/stargazers) [![Forks](https://img.shields.io/github/forks/phpstan/phpstan-phpunit?style=flat-square&color=blue)](https://github.com/phpstan/phpstan-phpunit/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-48%2F100-brightgreen?style=flat-square)](#)

> PHPUnit extensions and rules for PHPStan

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 533 |
| 🍴 **Forks** | 57 |
| 💻 **Language** | PHP |
| 📈 **Score** | 48/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`php` `php7` `phpstan` `phpunit` `static-analysis` `static-code-analysis` `testing`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
phpstan/phpstan-phpunit provides a collection of PHPUnit‑specific extensions and static‑analysis rules for PHPStan, letting developers catch test‑related bugs early and keep test suites consistent. With over 500 stars and recent maintenance, it can accelerate daily development and review cycles by surfacing issues before code reaches CI.  

**Value**  
- **Time savings** – By flagging mis‑configured tests, missing assertions, or misuse of PHPUnit APIs at edit‑time, engineers spend less time debugging failing tests and reviewing pull‑requests.  
- **Better CI feedback** – Static analysis runs faster than executing the full test suite, giving early, deterministic signals that complement runtime test results.  
- **Consistency** – Enforces best‑practice patterns (e.g., proper use of data providers, correct mock expectations) across the codebase, reducing flaky tests.  

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Add the package to a sandbox branch, run `composer require --dev phpstan/phpstan-phpunit`, and enable the provided rules in the project’s `phpstan.neon` file.  
2. **README validation** – Verify the installation steps, required PHPStan version, and any optional extensions (e.g., integration with phpunit‑bridge).  
3. **Pilot** – Enable the rules on a subset of modules or a single micro‑service and monitor false‑positive rates.  
4. **Gradual rollout** – Once confidence is built, expand the configuration to the whole monorepo and add the PHPStan command to the pre‑commit hook or CI pipeline.  

**Production Readiness**  
- **Maturity**: Medium. The library is actively maintained (last update 2026‑06‑25) and has a healthy community signal (533 ★, 57 forks).  
- **Suitability**: Ideal for prototypes, internal tools, and teams that already use PHPStan; production use is feasible after a short validation phase.  
- **Risks**: The integration steps are not fully documented in the metadata, so initial setup may require digging into the README or source code. Dependency compatibility (PHPStan version, PHPUnit version) should be verified, and ongoing maintenance must be accounted for in the project’s tooling budget.  

Overall, phpstan/phpstan-phpunit offers a low‑to‑moderate effort way to boost test quality and developer velocity, provided the team allocates a brief proof‑of‑concept window to confirm the integration cost.

### Русский

**phpstan/phpstan-phpunit** — набор расширений и правил для PHPStan, позволяющий автоматически проверять тесты PHPUnit, тем самым ускоряя локальную разработку и повышая качество CI‑обратной связи. Для начала рекомендуется внедрить небольшую proof‑of‑concept в репозиторий и проверить README, после чего оценить зависимости и стоимость поддержки; при положительных результатах проект готов к использованию в прототипах и внутренних workflow, а при дополнительной проверке стабильности может стать частью production‑pipeline.

### 中文

**价值**  
phpstan/phpstan-phpunit 为 PHPUnit 提供专门的 PHPStan 扩展和规则，能够在静态分析阶段捕获测试代码中的常见错误（如错误的断言、未使用的测试方法、错误的 mock 配置等）。这让开发者在本地编辑时就能得到即时反馈，显著缩短调试和代码审查的周期，提升 CI 的质量报告准确度，从而整体加快日常开发与发布流程。

**典型接入方式**  

1. **在项目根目录添加依赖**（推荐使用 Composer）  
   ```bash
   composer require --dev phpstan/phpstan-phpunit
   ```
2. **在 `phpstan.neon`（或 `phpstan.neon.dist`）中启用扩展**  
   ```neon
   includes:
       - vendor/phpstan/phpstan-phpunit/extension.neon
   ```
3. **可选：自定义规则或排除路径**  
   ```neon
   parameters:
       level: max
       paths:
           - src
           - tests
       ignoreErrors:
           - '#Some specific warning you want to silence#'
   ```
4. **在 CI 中运行**（以 GitHub Actions 为例）  
   ```yaml
   steps:
     - uses: actions/checkout@v3
     - uses: shivammathur/setup-php@v2
       with:
         php-version: '8.2'
         extensions: mbstring, intl
     - run: composer install --prefer-dist --no-progress --no-suggest
     - run: vendor/bin/phpstan analyse
   ```

**生产可用性**  

| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | 中等 | 已有 533 ⭐、57 🍴，活跃维护（截至 2026‑06‑25），适合作为内部或原型项目的质量门槛。 |
| **依赖风险** | 需要评估 | 依赖 PHPStan 与 PHPUnit 版本匹配，建议在升级前跑一次完整的 `composer update` 并在本地验证。 |
| **维护成本** | 低‑中 | 规则大多是“开箱即用”，仅在项目特有的测试约定下需要少量自定义。 |
| **上线门槛** | 低 | 只需在 CI 中加入一次 `phpstan analyse` 步骤，配合现有的 PHPUnit 测试即可。 |
| **适用场景** | 原型、内部工具、渐进式提升 CI 质量 | 对于已经使用 PHPStan 的项目，接入成本极低；对尚未使用的项目，可先在小范围（如 `tests/Unit`）做 PoC，确认规则覆盖率后再全局推广。 |

**结论**：phpstan/phpstan-phpunit 是提升 PHP 项目测试质量的轻量级工具，接入简单、维护成本低，适合作为内部工作流或原型阶段的质量保障手段。若在生产环境使用，建议先在预发布分支完成一次完整的兼容性验证，再正式推广到主分支的 CI 中。

## 🧭 Practical evaluation

**Value:** phpstan/phpstan-phpunit helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 533 GitHub stars
- 57 forks
- updated 2026-06-25
- primary language: PHP
- 7 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 58/100 |
| topics | 88/100 |
| outlook | 55/100 |
| quality | 62/100 |
| recency | 40/100 |
| adoption | 54/100 |
| production | 53/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/phpstan/phpstan-phpunit) · [← Back to Misc](./README.md)</sub>
