# infection/infection

[![Stars](https://img.shields.io/github/stars/infection/infection?style=flat-square&color=yellow)](https://github.com/infection/infection/stargazers) [![Forks](https://img.shields.io/github/forks/infection/infection?style=flat-square&color=blue)](https://github.com/infection/infection/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> PHP Mutation Testing library

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.2k |
| 🍴 **Forks** | 185 |
| 💻 **Language** | PHP |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ast` `coverage` `infection` `mutant` `mutation` `mutation-analysis` `mutation-testing` `php` `test-framework` `testing`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary**  
infection/infection is a PHP‑based mutation‑testing framework that automatically creates and runs code mutants to assess the effectiveness of your test suite. With over 2 200 stars, active maintenance, and a growing PHP community, it is a mature open‑source tool for improving code quality and confidence in automated tests.

**Value**  
By injecting small, systematic changes (mutations) into your source code and checking whether your existing tests detect them, Infection reveals gaps in test coverage that traditional metrics miss. This makes internal knowledge about code reliability searchable and actionable for AI assistants, enabling more accurate, evidence‑based answers when developers query the codebase.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, run `composer require infection/infection --dev`, and execute `infection` on a small, well‑tested component to see mutation scores.  
2. **README validation** – Follow the quick‑start guide to ensure your CI pipeline can install PHP, Composer, and the required extensions.  
3. **Pilot integration** – Add Infection to your CI (GitHub Actions, GitLab CI, etc.) as a separate stage that fails the build if the mutation score drops below a defined threshold.  
4. **Knowledge‑base indexing** – Export the mutation reports (JSON/HTML) and feed them into your document‑search or LLM‑grounding pipeline so assistants can cite concrete test‑coverage gaps when answering developer questions.

**Production Readiness**  
The project scores high on production readiness: recent commits (as of 2026‑06‑27), a vibrant community (2213 stars, 185 forks), and solid PHP ecosystem support. While the integration steps are not fully documented in the metadata, the straightforward Composer installation and existing CI examples make it feasible to start with a small pilot and expand once the setup cost is validated.

### Русский

**infection/infection** — это библиотека для PHP‑тестирования с помощью мутационного анализа, позволяющая автоматически проверять, насколько качественно покрыты тесты и выявлять «мёртвый» код. Типичный сценарий внедрения: в небольшом proof‑of‑concept подключить библиотеку к существующему CI, проиндексировать результаты мутаций и использовать их для улучшения поиска по внутренним знаниям и уточнения ответов ассистентов. Проект считается готовым к production‑использованию: активные коммиты, более 2200 звёзд, широкая адаптация в сообществе PHP и достаточная документация для быстрого начала.

### 中文

**项目简介（2‑3 句）**  
infection/infection 是一个用于 PHP 的变异测试（Mutation Testing）库，能够在运行单元测试时自动生成代码的细微变体并检测测试套件是否能够捕获这些变异，从而帮助开发者评估测试覆盖率的真实性和质量。

**价值**  
- **提升测试质量**：通过变异测试揭示隐藏的测试盲点，确保测试用例不仅覆盖代码路径，还能检测逻辑错误。  
- **降低回归风险**：在代码改动后快速发现测试失效的细微情形，提升发布的可靠性。  
- **促进代码健康**：提供变异分数等可量化指标，帮助团队制定更有效的测试改进策略。  

**典型接入方式**  
1. **在项目中安装**：使用 Composer 将 Infection 添加为开发依赖  
   ```bash
   composer require --dev infection/infection
   ```  
2. **初始化配置**：运行 `vendor/bin/infection init`，交互式生成 `infection.json5` 配置文件，指定要变异的目录、测试套件（PHPUnit、Pest 等）以及变异算子。  
3. **在 CI/CD 中集成**：在构建脚本或 GitHub Actions 中加入一步执行命令，例如  
   ```bash
   vendor/bin/infection --threads=4 --min-msi=80
   ```  
   生成的报告（HTML、XML、GitHub Summary）可直接作为质量门禁的检查点。  
4. **与现有工具链结合**：支持 PHPUnit、Pest、PHPStan、Psalm 等，可在同一流水线中共享覆盖率数据，进一步统一质量度量。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑27，项目拥有 2213 ⭐、185 🍴，最近一次提交在同一天，表明维护持续且社区活跃。  
- **生态兼容**：基于 Composer 的标准发布，兼容 PHP 8.0+，并提供对多种测试框架的原生支持。  
- **成熟度**：已在多个开源项目和企业内部使用，具备完整的文档、示例以及 CI 集成指南，适合作为正式生产环境的测试质量门槛。  
- **风险提示**：虽然核心功能易于上手，但变异测试对 CPU 与内存有一定消耗，建议在 CI 中通过并行执行和阈值控制（如 `--min-msi`）来平衡成本。  

综上，infection/infection 在提升 PHP 项目测试质量方面具备明确价值，接入方式简洁，且因社区活跃、文档完善而具备较高的生产可用性，适合作为正式的质量保障工具在项目中推广。

## 🧭 Practical evaluation

**Value:** infection/infection helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2213 GitHub stars
- 185 forks
- updated 2026-06-27
- primary language: PHP
- 10 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 57/100 |
| stars | 71/100 |
| topics | 100/100 |
| outlook | 66/100 |
| quality | 70/100 |
| recency | 40/100 |
| adoption | 67/100 |
| production | 56/100 |
| usefulness | 74/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/infection/infection) · [← Back to DevTools](./README.md)</sub>
