# SonarSource/sonar-dotnet

[![Stars](https://img.shields.io/github/stars/SonarSource/sonar-dotnet?style=flat-square&color=yellow)](https://github.com/SonarSource/sonar-dotnet/stargazers) [![Forks](https://img.shields.io/github/forks/SonarSource/sonar-dotnet?style=flat-square&color=blue)](https://github.com/SonarSource/sonar-dotnet/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Code analyzer for C# and VB.NET projects

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 909 |
| 🍴 **Forks** | 242 |
| 💻 **Language** | C# |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`c-sharp` `code-quality` `roslyn` `sonarqube` `static-analysis` `static-analyzer` `static-code-analysis` `visual-basic`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary**  
SonarSource/sonar-dotnet is an open‑source static‑analysis engine that inspects C# and VB.NET code for bugs, security vulnerabilities, and maintainability issues. With a healthy star count, regular commits, and wide adoption in the .NET ecosystem, it is a mature candidate for a pilot integration.

**Value**  
The analyzer brings SonarQube‑compatible quality rules directly into the build pipeline, helping teams catch defects early, enforce coding standards, and improve overall code health without buying a commercial tool. Its rule set covers security hotspots, code smells, and reliability problems, delivering immediate ROI for any .NET project that already uses CI/CD.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Add the `SonarAnalyzer.CSharp` (and/or `SonarAnalyzer.VisualBasic`) NuGet packages to a small, non‑critical repository.  
2. **Configure** – Follow the README to add the SonarScanner for MSBuild step in the CI workflow (Azure Pipelines, GitHub Actions, etc.).  
3. **Validate** – Run a local scan, review the generated issues, and compare them against existing tooling.  
4. **Scale** – Once the output is satisfactory, roll the scanner out to all .NET services, optionally integrating results into SonarQube or SonarCloud dashboards for centralized reporting.

**Production Readiness**  
The project shows strong production signals: recent commits (as of 2026‑06‑23), 909 stars, 242 forks, and active community maintenance. Its integration guidelines are well‑documented, and the analyzer is already used by many enterprises, indicating a high level of stability. The main risk is that the exact setup steps may vary across CI systems, so a small pilot is advisable to gauge configuration effort before full deployment.

### Русский

SonarSource/sonar‑dotnet — это открытый статический анализатор кода для C# и VB.NET, который позволяет автоматически выявлять баги, уязвимости и проблемные места в проектах, интегрируясь в CI/CD (например, через SonarQube, Azure DevOps или GitHub Actions). Типичный сценарий внедрения — запуск небольшого proof‑of‑concept на одном репозитории, проверка README и настройка сканирования, после чего расширение на остальные проекты. По метрикам активности, количеству звёзд (909) и недавним обновлениям проект считается готовым к использованию в продакшене, однако путь интеграции следует уточнить перед масштабным rollout‑ом.

### 中文

**项目简介**  
SonarSource/sonar-dotnet 是 SonarSource 官方维护的开源代码分析器，专门用于检测 C# 与 VB.NET 项目中的代码质量、漏洞、代码异味和安全问题。它可以在本地 IDE、CI/CD 流水线以及 SonarQube/SonarCloud 中运行，为团队提供统一、可追溯的质量报告。

**价值**  
- **提升代码质量**：提供超过 400 条规则，覆盖安全（OWASP、CWE）、可靠性、可维护性和性能等维度。  
- **统一治理**：与 SonarQube/SonarCloud 深度集成，所有项目统一使用同一套质量门槛，便于在组织内部推行“质量门”。  
- **降低风险**：自动发现潜在的安全漏洞和性能瓶颈，帮助团队在提交代码前就把问题拦截下来，减少后期修复成本。  

**典型接入方式**  
| 场景 | 接入步骤 | 关键配置 |
|------|----------|----------|
| **本地开发** | 在 IDE（如 Visual Studio、VS Code）中安装 SonarLint 插件，绑定到本地 SonarQube 项目或使用默认规则集。 | `sonarlint.ruleset`（可选） |
| **CI/CD** | 在构建脚本中加入 `dotnet-sonarscanner`（.NET Core）或 `MSBuild.SonarQube.Runner`（.NET Framework）步骤，完成 **Prepare → Build → End** 三阶段。 | `sonar.projectKey`、`sonar.host.url`、`sonar.login` |
| **SonarQube/SonarCloud** | 将项目关联到 SonarQube 实例，开启质量阈值（Quality Gate），并在 Pull Request 中自动触发分析。 | Quality Gate、Quality Profile、Branch/PR 分析配置 |

**生产可用性**  
- **活跃度**：截至 2026‑06‑23 最近一次提交，拥有 909 ⭐、242 🍴，社区活跃，官方持续发布新规则和 bug 修复。  
- **成熟度**：已在大量企业级 .NET 项目中使用，配合 SonarQube 的企业版可实现完整的治理流水线。  
- **集成成本**：虽然基本步骤简单，但需要配置 SonarQube 服务器或使用 SonarCloud，并在 CI 中添加 scanner 步骤。建议先在一个小模块做 PoC，验证规则集与质量门的适配度后，再推广至全仓库。  

**结论**：凭借强大的规则库、与 Sonar 平台的深度集成以及活跃的维护社区，sonar‑dotnet 完全具备在生产环境中作为代码质量与安全检测核心工具的条件，只要做好前期的规则调优和 CI 集成工作，即可投入正式使用。

## 🧭 Practical evaluation

**Value:** SonarSource/sonar-dotnet may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 909 GitHub stars
- 242 forks
- updated 2026-06-23
- primary language: C#
- 8 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 60/100 |
| stars | 63/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 78/100 |
| recency | 80/100 |
| adoption | 62/100 |
| production | 69/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/SonarSource/sonar-dotnet) · [← Back to DevTools](./README.md)</sub>
