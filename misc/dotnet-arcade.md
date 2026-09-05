# dotnet/arcade

[![Stars](https://img.shields.io/github/stars/dotnet/arcade?style=flat-square&color=yellow)](https://github.com/dotnet/arcade/stargazers) [![Forks](https://img.shields.io/github/forks/dotnet/arcade?style=flat-square&color=blue)](https://github.com/dotnet/arcade/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> Tools that provide common build infrastructure for multiple .NET Foundation projects.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 720 |
| 🍴 **Forks** | 386 |
| 💻 **Language** | C# |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
dotnet/arcade is an open‑source collection of build‑automation tools and common infrastructure that many .NET Foundation projects use to compile, test, package, and publish their code. By centralising common build logic in C#, it lets teams ship user‑facing interfaces faster with far less custom UI scaffolding and configuration. The project is actively maintained (720 ★, 386 forks, last update 2026‑05‑12) and serves as a solid foundation for internal prototypes or larger‑scale .NET front‑end pipelines.

**Value**  
- **Accelerated UI delivery** – Re‑use proven build scripts, versioning, signing, and publishing conventions instead of reinventing them for each product.  
- **Consistency & quality** – Shared conventions enforce the same standards across multiple .NET applications, reducing bugs and simplifying onboarding.  
- **Reduced maintenance overhead** – Updates to the core Arcade tooling propagate automatically to all consuming projects, keeping them aligned with the latest .NET tooling improvements.

**Practical Adoption Path**  
1. **Explore the repository** – Clone the repo and review the `README.md` and the `src/Arcade` folder to understand the provided MSBuild targets and NuGet packages.  
2. **Run the sample builds** – Execute the included CI scripts (e.g., `build.cmd` or `build.sh`) on a small test project to verify that your environment (Windows, Linux, .NET SDK version) is compatible.  
3. **Add Arcade as a submodule or NuGet** – Most projects reference Arcade via a `Directory.Build.props` file that imports the central `Microsoft.DotNet.Arcade.Sdk`. Add this import to your solution’s root.  
4. **Gradual migration** – Start by adopting a single target (e.g., `Pack`, `Publish`, or `Sign`) and validate the output. Incrementally enable additional Arcade features (code‑coverage, signing, version stamping) as confidence grows.  
5. **Manual inspection & customization** – Because the metadata does not expose a turnkey integration guide, review the build logs and adjust any project‑specific MSBuild properties (e.g., `PackageVersion`, `SignAssembly`) to fit your workflow.

**Production Readiness**  
- **Maturity**: Medium. Arcade is battle‑tested across many high‑profile .NET Foundation projects, but it is primarily a build‑infrastructure layer rather than a runtime component.  
- **Suitability**: Ideal for internal prototypes, CI/CD pipelines, or any .NET UI product that can adopt a shared build process. Production use is feasible after a short validation phase to ensure compatibility with your existing tooling and to lock down dependency versions.  
- **Risks**: The integration path is not fully documented in the discovered metadata, so you’ll need to allocate time for a proof‑of‑concept and to verify that the required MSBuild targets align with your custom UI build steps. Once those checks pass, Arcade can be considered production‑ready for most .NET front‑end workloads.

### Русский

dotnet/arcade — набор инструментов на C#, который стандартизирует процесс сборки и CI/CD для множества проектов фонда .NET, позволяя быстрее выводить пользовательские интерфейсы, переиспользовать готовые компоненты и упростить доставку фронтенда. При внедрении рекомендуется сначала провести ручную проверку интеграции, так как автоматические сигналы о совместимости скудны, а затем оценить затраты на настройку и поддержку. Проект находится на среднем уровне готовности к продакшн: подходит для прототипов и внутренних пайплайнов, но требует проверки зависимостей и возможных рисков перед масштабным использованием.

### 中文

**项目简介**  
dotnet/arcade 是一套面向 .NET Foundation 项目的通用构建工具，提供统一的 MSBuild、NuGet、CI/CD 流水线等基础设施，让多个仓库能够共享同一套可靠的构建脚本和约定。

**价值**  
- **降低 UI 开发成本**：通过统一的构建与发布流程，团队无需为每个项目重复搭建 CI、打包、版本管理等环节，从而把更多精力放在用户界面本身的实现上。  
- **提升交付一致性**：所有使用 arcade 的项目遵循相同的版本号策略、依赖解析和发布规范，减少因环境差异导致的构建失败。  
- **加速原型与内部工具**：快速复制已有的构建模板，即可为新 UI 项目或内部工具搭建完整的 CI/CD 流水线。

**典型接入方式**  
1. **引用共享 SDK**：在项目根目录的 `global.json` 中添加对 `Microsoft.DotNet.Arcade.Sdk` 的引用（或在 `Directory.Build.props` 中导入）。  
2. **继承默认目标**：在项目的 `.csproj` 中使用 `<Import Project="$(MSBuildExtensionsPath)\Microsoft\DotNet\Arcade\Sdk\Sdk.props" />` 并在需要的地方覆盖或追加自定义任务。  
3. **CI 配置**：在 Azure Pipelines、GitHub Actions 等 CI 平台上使用官方提供的 `arcade.yml` 模板，直接复用预定义的构建、测试、打包、发布步骤。  
4. **本地验证**：运行 `dotnet build` / `dotnet test` 即可验证集成是否成功，必要时通过 `arcade` 提供的诊断脚本检查依赖冲突。

**生产可用性**  
- **成熟度**：GitHub 720 ★、386 Fork，活跃维护至 2026‑05‑12，代码基于 C#，社区和 .NET Foundation 对其有长期支持。  
- **适用场景**：适合内部原型、部门内部工具以及需要统一构建流程的中小规模服务；在生产环境使用前建议进行依赖审计和维护成本评估。  
- **风险**：元数据中缺乏明确的接入指引，实际集成时可能需要手动检查和调试；因此在大规模生产部署前，最好在单独的实验环境中验证完整的构建‑发布链路。  

总体而言，dotnet/arcade 为 .NET 前端/UI 项目提供了可靠、可复用的构建基础设施，能够显著缩短交付周期，只要做好前期的集成验证和依赖管理，即可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** dotnet/arcade helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 720 GitHub stars
- 386 forks
- updated 2026-05-12
- primary language: C#

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 65/100 |
| stars | 61/100 |
| topics | 0/100 |
| outlook | 65/100 |
| quality | 63/100 |
| recency | 80/100 |
| adoption | 62/100 |
| production | 63/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/dotnet/arcade) · [← Back to Misc](./README.md)</sub>
