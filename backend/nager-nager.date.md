# nager/Nager.Date

[![Stars](https://img.shields.io/github/stars/nager/Nager.Date?style=flat-square&color=yellow)](https://github.com/nager/Nager.Date/stargazers) [![Forks](https://img.shields.io/github/forks/nager/Nager.Date?style=flat-square&color=blue)](https://github.com/nager/Nager.Date/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> Easily access public holidays for 150+ countries via .NET, REST API, Docker, or NuGet for online and offline use.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.4k |
| 🍴 **Forks** | 216 |
| 💻 **Language** | C# |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-07-06 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bank-holidays` `calculate-holidays` `calendar` `calendar-api` `holiday` `holiday-api` `holiday-calculation` `holiday-software` `holidayapi` `holidays` `holidays-api` `public-apis`

## 🎯 Categories

Backend · DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
nager/Nager.Date is a .NET‑based library and REST service that provides up‑to‑date public‑holiday calendars for more than 150 countries. It can be consumed via a NuGet package, a Docker‑hosted API, or a simple CLI, making it easy to add holiday awareness to any backend without building the data source yourself.  

**Value**  
- **Reuse‑first infrastructure** – eliminates the need for teams to scrape, maintain, or license holiday datasets, letting them focus on core business logic.  
- **Standardized API** – a single, well‑documented endpoint and SDK deliver consistent holiday data across services, reducing integration friction and bugs.  
- **Multi‑environment flexibility** – works offline as a library, online as a hosted API, or in a container for on‑premises deployments, fitting any DevOps strategy.  

**Practical Adoption Path**  
1. **Evaluation** – spin up the official Docker image locally and call the REST endpoints (e.g., `/api/v3/PublicHolidays/{year}/{countryCode}`) to verify data accuracy for the target regions.  
2. **Integration** – add the `Nager.Date` NuGet package to existing .NET services or generate a client from the OpenAPI spec for non‑C# stacks.  
3. **Production rollout** – choose one of three deployment models:  
   - *Self‑hosted Docker* behind your API gateway for full control and offline capability.  
   - *Managed SaaS* by running the public Docker image in a cloud container service (Azure Container Instances, AWS Fargate, etc.).  
   - *Embedded library* for low‑latency scenarios where the holiday list is compiled into the service binary.  

**Production Readiness**  
- **Activity & Community** – 1,384 GitHub stars, 216 forks, recent commits (last updated 2026‑07‑06), and 16 relevant topics signal a healthy, actively maintained project.  
- **Reliability** – the service is versioned, provides a stable OpenAPI contract, and can be deployed in Docker for deterministic environments.  
- **Risk considerations** – licensing (MIT) is permissive, but a final security audit and confirmation of an active maintainer are advisable before mission‑critical use.  

Overall, Nager.Date offers a mature, low‑effort solution for holiday data that can be integrated quickly and scaled reliably in production environments.

### Русский

Резюме проекта nager/Nager.Date:

nager/Nager.Date - это открытый проект, предоставляющий доступ к праздникам в более чем 150 странах через .NET, REST API, Docker или NuGet для онлайн- и офлайн-использования. Этот проект позволяет командам использовать готовую инфраструктуру вместо того, чтобы воссоздавать общую часть backend. Проект готов к использованию в production, с сильными сигналами активности, приёма и экосистемы, что делает его подходящей кандидатурой для serious пилота.

### 中文

**项目简介**  
Nager.Date 是一个开源库，提供 150+ 国家/地区的公共假期数据。它既可以通过 .NET SDK、RESTful API、Docker 镜像，也可以直接通过 NuGet 包离线使用，帮助开发团队快速获取可靠的假期信息，而无需自行采集和维护日历数据。

**价值点**  
- **复用基础设施**：统一的假期服务可在多个微服务、业务系统之间共享，避免各团队重复实现假期计算逻辑。  
- **加速交付**：只需调用现成的 API/SDK，即可在几行代码内完成假期查询，显著缩短 API 开发和上线时间。  
- **标准化**：统一的假期数据源和接口规范，有助于公司内部服务遵循统一的时间业务规则，降低因假期误差导致的业务错误。

**典型接入方式**  

| 场景 | 接入方式 | 关键步骤 |
|------|----------|----------|
| .NET 应用 | **NuGet 包** (`Nager.Date`) | 1. 在项目中 `dotnet add package Nager.Date` <br>2. 使用 `DateSystem`、`PublicHoliday` 等类调用 `GetPublicHolidayAsync(countryCode, year)` |
| 跨语言微服务 | **REST API** | 1. 部署官方 Docker 镜像 `docker run -p 80:80 nagerdate/api` <br>2. 调用 `GET /api/v2/PublicHoliday/{countryCode}/{year}` <br>3. 解析返回的 JSON |
| CI/CD 或脚本 | **CLI**（通过 Docker） | `docker run --rm nagerdate/api curl http://localhost/api/v2/PublicHoliday/US/2025` |
| 离线/内部网络 | **自托管 Docker** | 在内部私有仓库拉取镜像，内部网络直接访问 API，避免外网依赖。 |

**生产可用性**  
- **活跃度**：截至 2026‑07‑06，项目最近一次提交，星标 1384，Fork 216，说明社区活跃且维护及时。  
- **技术成熟度**：提供完整的 .NET SDK、REST API、Docker 镜像，支持在线与离线两种使用模式，兼容主流部署环境。  
- **安全与合规**：采用 MIT 许可证，代码公开，可自行审计；官方 Docker 镜像基于官方构建，安全基线明确。  
- **可扩展性**：支持自定义假期源（通过实现 `ICountryHolidayProvider`），满足特定业务需求。  

综合以上因素，Nager.Date 在后端/DevOps 场景下具备较高的生产就绪度，适合作为企业内部统一的公共假期服务进行试点或直接上线使用。

## 🧭 Practical evaluation

**Value:** nager/Nager.Date helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1384 GitHub stars
- 216 forks
- updated 2026-07-06
- primary language: C#
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 58/100 |
| stars | 67/100 |
| topics | 100/100 |
| outlook | 83/100 |
| quality | 84/100 |
| recency | 100/100 |
| adoption | 64/100 |
| production | 80/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/nager/Nager.Date) · [← Back to Backend](./README.md)</sub>
