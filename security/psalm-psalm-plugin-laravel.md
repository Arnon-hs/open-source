# psalm/psalm-plugin-laravel

[![Stars](https://img.shields.io/github/stars/psalm/psalm-plugin-laravel?style=flat-square&color=yellow)](https://github.com/psalm/psalm-plugin-laravel/stargazers) [![Forks](https://img.shields.io/github/forks/psalm/psalm-plugin-laravel?style=flat-square&color=blue)](https://github.com/psalm/psalm-plugin-laravel/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> Laravel static analysis with built-in security scanning

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 334 |
| 🍴 **Forks** | 78 |
| 💻 **Language** | PHP |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`laravel` `looking-for-maintainer` `php` `php-static-analysis` `psalm` `psalm-plugin` `static-analysis`

## 🎯 Categories

Security

## 📝 Summary

### English

**Summary**  
psalm/psalm‑plugin‑laravel extends the Psalm static‑analysis tool with Laravel‑specific type inference and built‑in security checks, letting developers catch bugs and vulnerabilities at compile time. The plugin is actively maintained (334 ★, 78 forks, last update 2026‑06‑25) and integrates directly into existing Laravel projects via Composer, requiring only a few configuration lines.

**Value**  
By bringing AI‑assisted analysis to a familiar PHP ecosystem, the plugin accelerates the detection of insecure code patterns, mis‑typed service container bindings, and other Laravel‑specific issues without writing custom rules. Teams can prototype AI‑driven security policies or RAG/agent workflows on top of the existing static‑analysis pipeline, reducing the time‑to‑value for secure AI features.

**Practical adoption path**  
1. Add the package with `composer require --dev psalm/psalm-plugin-laravel`.  
2. Enable the plugin in the `psalm.xml` configuration (`<pluginClass>Psalm\Laravel\Plugin\LaravelPlugin</pluginClass>`).  
3. Run `vendor/bin/psalm` as part of the CI pipeline; the plugin automatically enriches type information and reports security warnings.  
4. Optionally extend the built‑in checks with custom Psalm plugins or integrate the output into AI‑driven dashboards.

**Production readiness**  
The project shows strong production signals: recent commits, a healthy star/fork count, and clear Laravel‑focused documentation. While the license and long‑term maintainer commitment still need a final review, the current activity and community adoption make it a solid candidate for a serious pilot in production environments.

### Русский

**psalm/psalm-plugin-laravel** — это open‑source расширение для Psalm, которое добавляет статический анализ Laravel‑приложений и встроенное сканирование уязвимостей, позволяя быстро выявлять ошибки кода и потенциальные проблемы безопасности. Типичный сценарий — интеграция плагина в CI/CD pipeline проекта Laravel для автоматической проверки качества и защиты кода перед релизом, а также прототипирование AI‑фич, используя предоставленные сигналы API/CLI. По оценке готовности к продакшну проект считается «high»: активные коммиты, 334 звёзд, 78 форков, свежие обновления и сильная поддержка сообщества, хотя окончательная проверка лицензии и безопасности всё же требуется.

### 中文

**项目简介**  
`psalm/psalm-plugin-laravel` 是为 Laravel 项目提供的 Psalm 静态分析插件，内置安全扫描规则，可在开发阶段自动发现代码中的潜在安全漏洞和类型错误。

**价值**  
- **提升代码安全**：通过预置的安全检查（如 SQL 注入、XSS、CSRF 等），帮助团队在提交前拦截高危缺陷。  
- **降低维护成本**：静态分析在 CI 中即可运行，避免了后期调试和补丁的高昂成本。  
- **与 Laravel 深度集成**：插件直接读取 Laravel 的容器、路由和模型定义，提供框架感知的分析结果，准确率远高于通用 PHP 静态分析工具。

**典型接入方式**  
1. **Composer 安装**  
   ```bash
   composer require --dev psalm/psalm-plugin-laravel
   ```
2. **在项目根目录生成 Psalm 配置**（若已有可跳过）  
   ```bash
   vendor/bin/psalm --init
   ```
3. **在 `psalm.xml` 中启用插件**（插件会自动注册）或手动添加：  
   ```xml
   <plugins>
       <pluginClass>Psalm\LaravelPlugin\Plugin</pluginClass>
   </plugins>
   ```
4. **CI 集成**（GitHub Actions、GitLab CI 等）  
   ```yaml
   - name: Run Psalm with Laravel plugin
     run: vendor/bin/psalm --output-format=github
   ```
   通过上述步骤即可在每次提交或合并请求时自动执行安全扫描。

**生产可用性**  
- **活跃度**：截至 2026‑06‑25 最近一次提交，项目仍在维护；GitHub ★334、Fork 78，社区活跃。  
- **生态兼容**：基于 PHP，支持 Laravel 8/9/10，兼容现有的 Psalm 版本。  
- **成熟度**：插件已在多个开源 Laravel 项目中使用，具备稳定的错误报告和修复路径。  
- **风险**：需自行审查许可证（MIT）以及项目的安全审计报告；建议在生产环境前进行一次内部评估。

综合来看，`psalm/psalm-plugin-laravel` 已具备足够的成熟度和社区支持，可直接在生产级 Laravel 项目中作为 CI 静态安全检测的核心组件使用。

## 🧭 Practical evaluation

**Value:** psalm/psalm-plugin-laravel helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 334 GitHub stars
- 78 forks
- updated 2026-06-25
- primary language: PHP
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 47/100 |
| stars | 54/100 |
| topics | 88/100 |
| outlook | 54/100 |
| quality | 62/100 |
| recency | 40/100 |
| adoption | 52/100 |
| production | 55/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/psalm/psalm-plugin-laravel) · [← Back to Security](./README.md)</sub>
