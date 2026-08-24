# GoogleCloudPlatform/magic-modules

[![Stars](https://img.shields.io/github/stars/GoogleCloudPlatform/magic-modules?style=flat-square&color=yellow)](https://github.com/GoogleCloudPlatform/magic-modules/stargazers) [![Forks](https://img.shields.io/github/forks/GoogleCloudPlatform/magic-modules?style=flat-square&color=blue)](https://github.com/GoogleCloudPlatform/magic-modules/network) [![Language](https://img.shields.io/badge/lang-Go%20Template-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Add Google Cloud Platform support to Terraform

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 951 |
| 🍴 **Forks** | 2.3k |
| 💻 **Language** | Go Template |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`gcp` `go` `golang` `google-cloud` `googlecloud` `googlecloudplatform` `magic-modules` `terraform`

## 🎯 Categories

Templates · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
GoogleCloudPlatform / magic‑modules is an open‑source code‑generation framework that builds Terraform providers for Google Cloud services, letting teams provision, query, and migrate data on GCP with minimal hand‑written plumbing. With over 950 ★ on GitHub, active commits, and broad adoption across the Terraform ecosystem, it is a production‑ready candidate for any organization looking to automate GCP infrastructure as code.

**Value**  
- **Unified data‑infrastructure automation** – By generating Terraform resources directly from Google’s APIs, magic‑modules eliminates the need for custom scripts or SDK wrappers, reducing operational overhead and the risk of drift.  
- **Speed and consistency** – Teams can provision databases, storage buckets, and other services in a single, declarative workflow, accelerating prototyping and ensuring that environments are reproducible across development, staging, and production.  
- **Extensibility** – The framework exposes API/SDK metadata and language‑specific templates, making it easy to extend or customize providers for niche GCP services without reinventing the wheel.

**Practical Adoption Path**  
1. **Evaluate the generated provider** – Clone the repository, run the generator for the GCP services you need, and inspect the resulting Terraform modules.  
2. **Pilot in a sandbox** – Deploy a small, non‑critical workload (e.g., a CloudSQL instance) using the generated modules to verify resource mapping, state handling, and any required provider configuration.  
3. **Integrate into CI/CD** – Add the generated modules to your existing Terraform pipeline, leveraging Terraform Cloud or your preferred backend for state management.  
4. **Iterate and extend** – If you need additional services or custom tweaks, modify the generator templates or add overlay modules, then re‑run the generation step.  

**Production Readiness**  
- **Activity & Community** – The repo shows recent commits (last updated 2026‑05‑11), 951 stars, 2,286 forks, and a vibrant contributor base, indicating strong maintenance.  
- **Ecosystem Fit** – It is already used by several high‑profile Terraform providers, and the generated code follows Terraform’s stability guarantees.  
- **Risk Profile** – No immediate licensing or security red flags have been identified, though a final review of the Apache‑2.0 license compliance and a security audit of any custom extensions is advisable.  

Overall, magic‑modules offers a mature, well‑supported path to bring Google Cloud infrastructure under Terraform control, making it suitable for production pilots and full‑scale deployments.

### Русский

**GoogleCloudPlatform/magic-modules** — это набор шаблонов и генераторов, позволяющий автоматически создавать Terraform‑провайдеры для сервисов Google Cloud Platform, что упрощает управление инфраструктурой и ускоряет вывод в продакшн новых облачных ресурсов. Типичный сценарий: команда DevOps интегрирует модуль в CI/CD, получает готовые Terraform‑конфигурации и быстро развёртывает/модифицирует базы данных, хранилища и другие сервисы без написания собственного кода. Проект имеет высокий уровень готовности к production: активная поддержка, более 900 звёзд на GitHub, частые обновления и широкое принятие в сообществе.

### 中文

**简短介绍**  
GoogleCloudPlatform/magic-modules 为 Terraform 提供完整的 Google Cloud Platform 支持，自动生成 Terraform Provider 的代码，使用户能够以声明式方式管理 GCP 上的几乎所有资源。项目基于 Go Template，社区活跃，星标 951、Fork 2286，近期仍在持续更新。

**价值**  
- **统一管理**：一次编写、一次生成，即可在 Terraform 中使用原生的 GCP 资源，省去手动编写 Provider 的繁琐工作。  
- **加速交付**：通过自动化生成的模块，团队可以更快地完成基础设施即代码（IaC）的编写、测试与发布。  
- **降低风险**：生成的代码遵循 GCP 官方 API 规范，保持与云服务同步更新，减少因 API 变更导致的维护成本。

**典型接入方式**  
1. **克隆仓库**并切换到对应的 GCP 版本分支。  
2. 使用 `make generate`（或对应的 CI 脚本）基于最新的 GCP Discovery 文档生成 Terraform Provider 代码。  
3. 将生成的 provider 编译为二进制或直接在本地 `terraform init` 时引用本地路径。  
4. 在 Terraform 配置文件中使用 `provider "google"` 或自定义的 `magic-modules` 提供的资源块，即可管理 GCP 资源。

**生产可用性**  
- **活跃度**：截至 2026‑05‑11，项目仍在频繁提交，社区贡献者众多，具备持续维护的能力。  
- **生态兼容**：生成的 Provider 与官方 Terraform 生态完全兼容，可直接在现有 Terraform 工作流中使用。  
- **成熟度**：拥有大量实际使用案例，且通过 CI/CD 完成自动化测试，整体风险低。  
- **注意事项**：在正式投产前仍建议审查许可证（Apache 2.0）和安全审计报告，确保符合企业合规要求。  

综上，magic-modules 是一套成熟、易集成且适合在生产环境中使用的 GCP Terraform 自动化解决方案。

## 🧭 Practical evaluation

**Value:** GoogleCloudPlatform/magic-modules helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 951 GitHub stars
- 2286 forks
- updated 2026-05-11
- primary language: Go Template
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 84/100 |
| stars | 63/100 |
| topics | 100/100 |
| outlook | 56/100 |
| quality | 66/100 |
| recency | 20/100 |
| adoption | 69/100 |
| production | 54/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/GoogleCloudPlatform/magic-modules) · [← Back to Templates](./README.md)</sub>
