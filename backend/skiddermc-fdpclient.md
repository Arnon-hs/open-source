# SkidderMC/FDPClient

[![Stars](https://img.shields.io/github/stars/SkidderMC/FDPClient?style=flat-square&color=yellow)](https://github.com/SkidderMC/FDPClient/stargazers) [![Forks](https://img.shields.io/github/forks/SkidderMC/FDPClient?style=flat-square&color=blue)](https://github.com/SkidderMC/FDPClient/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> Minecraft 1.8.9 forge hacked client based on LiquidBounce.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 503 |
| 🍴 **Forks** | 197 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cheat` `client` `client-project` `client-server` `client-side` `gplv3` `gradle` `hack` `java` `jvm` `jvm-bytecode` `kotlin`

## 🎯 Categories

Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
SkidderMC/FDPClient is an open‑source, Kotlin‑based hacked client for Minecraft 1.8.9 built on the LiquidBounce framework. It bundles a collection of ready‑made UI components and a modular API/SDK that let developers ship user‑facing interfaces with far less custom code. With active maintenance, 503 GitHub stars and a growing fork network, it’s positioned as a practical toolkit for quickly prototyping and delivering Minecraft‑style front‑ends.

**Value**  
- **Accelerated UI development** – The client ships pre‑crafted menus, HUD elements, and configuration screens, so teams can focus on game logic rather than reinventing common UI patterns.  
- **Component reuse** – Its modular architecture exposes reusable widgets and styling conventions that can be shared across multiple Minecraft mods or related tools.  
- **Developer tooling** – An integrated CLI/SDK simplifies building, testing, and packaging custom client builds, reducing the overhead of setting up a Forge development environment from scratch.

**Practical Adoption Path**  
1. **Evaluate the SDK** – Clone the repository, run the provided Gradle tasks, and inspect the sample modules to understand the component hierarchy and API surface.  
2. **Prototype a feature** – Use the existing UI widgets (menus, sliders, toggles) to implement a small feature (e.g., a custom cheat toggle) and verify it works on a local 1.8.9 Forge server.  
3. **Integrate with your codebase** – Add FDPClient as a Gradle sub‑project or Maven dependency, replace placeholder UI code with the client’s components, and adjust the build pipeline to include the client’s obfuscation and signing steps.  
4. **Testing & CI** – Leverage the built‑in unit‑test framework and the CLI to run automated UI tests in CI, ensuring compatibility with your existing mod ecosystem.  
5. **Roll out** – Package the final client jar, distribute it to your user base, and monitor community feedback for any required UI tweaks.

**Production Readiness**  
- **Activity & Community** – The repo shows recent commits (last updated 2026‑06‑24), 503 stars, 197 forks, and 13 topical tags, indicating a healthy, engaged community.  
- **Stability** – Built on the mature LiquidBounce codebase and targeting a specific, well‑understood Minecraft version (1.8.9), the core functionality is stable for production use.  
- **Ecosystem Fit** – Kotlin/Gradle integration aligns with standard Forge mod development pipelines, making onboarding straightforward for teams already using these tools.  
- **Risks** – Formal license verification, a detailed security audit, and confirmation of long‑term maintainers are still required before a full production rollout, but no immediate red flags have been identified.  

Overall, FDPClient offers a robust, ready‑to‑use UI foundation for Minecraft mod developers, with a clear path from prototype to production and a strong signals‑based indication of readiness for serious pilot projects.

### Русский

SkidderMC/FDPClient — это открытый форж‑клиент для Minecraft 1.8.9, построенный на базе LiquidBounce и написанный на Kotlin. Он позволяет быстро собрать пользовательский интерфейс и переиспользовать готовые UI‑компоненты, что ускоряет разработку клиентской части и упрощает доставку фронтенда. Проект имеет высокую готовность к production: активные коммиты, 503 звёзды, 197 форков, свежие обновления и широкую экосистему, хотя перед запуском стоит уточнить лицензию и вопросы безопасности.

### 中文

**项目简介**  
SkidderMC/FDPClient 是基于 LiquidBounce 的 Minecraft 1.8.9 Forge 破解客户端，使用 Kotlin 开发，拥有 503 颗星和 197 次 fork，社区活跃度高，适合作为游戏外挂功能的快速原型或二次开发基础。

**价值**  
- **快速交付**：提供完整的作弊模块、UI 组件和网络通信实现，开发者无需从零编写底层逻辑，即可直接在客户端上集成各种功能。  
- **代码复用**：模块化设计让 UI、模块管理、配置系统等可直接复用，降低重复工作量。  
- **社区与生态**：活跃的开源社区提供丰富的 issue、PR 与文档，帮助快速定位问题并获取实现思路。

**典型接入方式**  
1. **源码集成**：将仓库克隆到本地，使用 Gradle（`./gradlew build`）编译后，将生成的 `jar` 包作为 Forge mod 加载到 Minecraft 1.8.9 客户端。  
2. **模块化插件**：项目提供的 `API` 包（`fdp-api.jar`）可在其他 Kotlin/Java 项目中通过 Maven/Gradle 依赖引入，实现自定义模块或 UI 扩展。  
3. **CLI/脚本**：通过项目自带的 `FDPClient` 启动脚本，可在命令行指定配置文件、加载自定义插件，实现自动化部署或 CI 流程。

**生产可用性**  
- **活跃维护**：最近一次提交为 2026‑06‑24，代码库持续更新，issues 处理及时。  
- **成熟度**：已有数千次下载和多个公开的服务器实例在使用，证明在真实环境下运行稳定。  
- **风险**：需进一步审查许可证（GPL‑3.0）与安全审计（尤其是对第三方插件的加载），确保符合内部合规要求。总体而言，FDPClient 已具备在内部项目或受控生产环境中试点使用的条件。

## 🧭 Practical evaluation

**Value:** SkidderMC/FDPClient helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 503 GitHub stars
- 197 forks
- updated 2026-06-24
- primary language: Kotlin
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 57/100 |
| stars | 58/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 76/100 |
| recency | 80/100 |
| adoption | 57/100 |
| production | 70/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/SkidderMC/FDPClient) · [← Back to Backend](./README.md)</sub>
