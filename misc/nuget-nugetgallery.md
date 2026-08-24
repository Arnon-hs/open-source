# NuGet/NuGetGallery

[![Stars](https://img.shields.io/github/stars/NuGet/NuGetGallery?style=flat-square&color=yellow)](https://github.com/NuGet/NuGetGallery/stargazers) [![Forks](https://img.shields.io/github/forks/NuGet/NuGetGallery?style=flat-square&color=blue)](https://github.com/NuGet/NuGetGallery/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-49%2F100-brightgreen?style=flat-square)](#)

> NuGet Gallery is a package repository that powers https://www.nuget.org. Use this repo for reporting NuGet.org issues.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.6k |
| 🍴 **Forks** | 656 |
| 💻 **Language** | C# |
| 📈 **Score** | 49/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`dotnet` `hacktoberfest` `nuget`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
NuGet Gallery is the open‑source web application that powers the official https://www.nuget.org package repository. It provides the full stack for hosting, searching, and managing .NET packages, and serves as the primary venue for reporting issues that affect the public NuGet.org service.

**Value**  
- **Official source of truth** – Because it runs the production NuGet.org site, the code reflects the exact features, policies, and security controls used by the .NET ecosystem.  
- **Extensible package portal** – Organizations can fork or self‑host the gallery to create private, on‑premises NuGet feeds that share the same UI and API surface as the public service.  
- **Issue‑driven roadmap** – Bugs and feature requests filed against this repo are directly visible to the NuGet team, making it a reliable channel for influencing future platform behavior.

**Practical Adoption Path**  
1. **Evaluate the repository** – Clone the repo and run the provided Docker compose setup (or the Visual Studio solution) to confirm the UI and API meet your internal requirements.  
2. **Customize authentication/authorization** – Integrate with your corporate identity provider (Azure AD, OAuth, etc.) by editing the `Startup.Auth.cs` and related configuration files.  
3. **Deploy** – Deploy the containerized service to a staging environment (Kubernetes, Azure App Service, or on‑prem VM) and point your internal NuGet clients (`nuget.config`) to the new endpoint.  
4. **Test package lifecycle** – Publish, list, restore, and delete packages in the staging instance to verify that CI/CD pipelines and build agents work as expected.  
5. **Production rollout** – Once the customizations and monitoring (health checks, logging, backups) are in place, promote the instance to production and switch internal developers to the new feed.

**Production Readiness**  
- **Maturity**: With ~1.6 k stars, ~650 forks, and active maintenance (last commit 2026‑07‑01), the project is mature and widely used.  
- **Stability**: The core gallery code is battle‑tested in the public NuGet.org service, but the open‑source version does not include all internal Microsoft tooling (e.g., advanced telemetry).  
- **Risk**: The integration path is not fully documented; you’ll need to spend time configuring authentication, storage, and CI pipelines.  
- **Recommendation**: Suitable for prototypes, internal private feeds, or as a base for a custom NuGet portal. For mission‑critical production use, perform a thorough security review, establish automated testing, and plan for ongoing maintenance of the forked codebase.

### Русский

**NuGet Gallery** — открытая реализация репозитория пакетов, который стоит за https://www.nuget.org; проект позволяет отслеживать и фиксировать баги, а также разворачивать собственный приватный или публичный NuGet‑сервер. Типичный сценарий — интеграция в CI/CD для публикации и потребления .NET‑пакетов внутри компании (например, при построении внутреннего пакета‑менеджера или при тестировании новых функций NuGet.org). Готовность к production — средняя: репозиторий активно поддерживается (1635 ★, последние коммиты 2026‑07‑01), но требуется ручная проверка интеграционных точек и настройка инфраструктуры перед внедрением в продуктив.

### 中文

**简短介绍**

NuGet Gallery 是一个包仓库，用于托管 NuGet.org。该项目用于报告 NuGet.org 问题。

**价值**

NuGet Gallery 的价值在于它可以满足特定的工作流程需求，并且可以作为一个可靠的包仓库使用。

**典型接入方式**

由于 NuGet Gallery 的 README 和活动信息不够丰富，需要手动检查其 README 和活动信息以确保它符合您的需求后再进行接入。

**生产可用性**

NuGet Gallery 的生产可用性为中等，适合用于原型开发或内部工作流程。然而，需要在生产环境中进行依赖检查和维护检查以确保其稳定性。

## 🧭 Practical evaluation

**Value:** NuGet/NuGetGallery may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1635 GitHub stars
- 656 forks
- updated 2026-07-01
- primary language: C#
- 3 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 70/100 |
| stars | 68/100 |
| topics | 38/100 |
| outlook | 53/100 |
| quality | 62/100 |
| recency | 40/100 |
| adoption | 69/100 |
| production | 53/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/NuGet/NuGetGallery) · [← Back to Misc](./README.md)</sub>
