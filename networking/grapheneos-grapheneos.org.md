# GrapheneOS/grapheneos.org

[![Stars](https://img.shields.io/github/stars/GrapheneOS/grapheneos.org?style=flat-square&color=yellow)](https://github.com/GrapheneOS/grapheneos.org/stargazers) [![Forks](https://img.shields.io/github/forks/GrapheneOS/grapheneos.org?style=flat-square&color=blue)](https://github.com/GrapheneOS/grapheneos.org/network) [![Language](https://img.shields.io/badge/lang-HTML-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> Servers for our website, HTTP/HTTPS connectivity checks, HTTPS network time, NTP (for Qualcomm XTRA), Broadcom PSDS cache, Samsung PSDS cache, Qualcomm PSDS (XTRA) cache, SUPL proxy, attestation key provisioning proxy, Vanadium component update check/download proxy, network location proxy and geocoding proxy. Also app and OS updates via an include.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 684 |
| 🍴 **Forks** | 197 |
| 💻 **Language** | HTML |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `grapheneos` `privacy` `security`

## 🎯 Categories

Networking · Mobile · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
GrapheneOS/grapheneos.org hosts the backend services that power the GrapheneOS website and its ecosystem, providing HTTP/HTTPS connectivity checks, time synchronization, NTP for Qualcomm XTRA, various PSDS caches (Broadcom, Samsung, Qualcomm), SUPL and attestation proxies, as well as update‑distribution proxies for Vanadium components and geolocation services. The repository also bundles scripts for app and OS updates via an include, making it a one‑stop shop for the infrastructure needed to keep GrapheneOS devices securely connected and up‑to‑date.

**Value**  
The project eliminates the need to build and maintain a custom suite of networking, time‑keeping, and update‑distribution services from scratch. By reusing GrapheneOS’s hardened, privacy‑focused proxies and caches, developers can focus on their own application logic while inheriting proven security controls, accurate time sources, and reliable OTA update pipelines.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Docker/compose files, and verify that the health‑check endpoints respond.  
2. **Proof‑of‑Concept Integration** – Replace any existing proxy or NTP service in a test environment with the GrapheneOS components, using the README’s example configuration for SUPL, attestation, and Vanadium updates.  
3. **Incremental Rollout** – Gradually point production devices or services to the new proxies, monitoring logs and performance metrics.  
4. **Full Deployment** – Harden the deployment (TLS, firewall rules, secrets management) and integrate the update‑include scripts into your CI/CD pipeline for automated OS/app rollouts.

**Production Readiness**  
- **Maturity**: Medium – the codebase is actively maintained (last commit 2026‑06‑24) and has a respectable community signal (≈ 684 ★, 197 forks).  
- **Stability**: The services are battle‑tested in the GrapheneOS ecosystem, but they are tightly coupled to GrapheneOS‑specific components (e.g., Qualcomm XTRA).  
- **Considerations**: Verify compatibility with your hardware stack, audit the proxy configurations for your threat model, and plan for ongoing maintenance of the underlying dependencies (Docker images, NTP servers, etc.).  
- **Readiness Verdict**: Suitable for internal prototypes, pilot deployments, or organizations already aligned with GrapheneOS security goals; production use is feasible after a limited integration pilot and a security review.

### Русский

GrapheneOS/grapheneos.org — набор серверных сервисов, обеспечивающих работу инфраструктуры GrapheneOS: проверка HTTP/HTTPS‑соединений, синхронизация времени (NTP), кэширование PSDS‑данных Qualcomm, Broadcom и Samsung, прокси‑службы SUPL, attestation‑key, обновлений Vanadium и геокодинга, а также дистрибуцию обновлений приложений и ОС. Типичный сценарий внедрения — подключение к этим сервисам в качестве backend‑слоя для собственных мобильных или IoT‑устройств, позволяющего быстро добавить безопасные сетевые функции и автоматическое обновление без разработки собственного стека. Готовность к production — средняя: проект стабилен и активно поддерживается (обновления до 2026‑06‑24, 684 звёзд), но требует предварительной проверки интеграции и настройки зависимостей перед запуском в продакшн.

### 中文

**项目价值**  
GrapheneOS/grapheneos.org 提供了 GrapheneOS 官方网站所需的全套后端服务，包括 HTTP/HTTPS 连通性检测、网络时间同步、NTP（Qualcomm XTRA）、多厂商 PSDS 缓存、SUPL 代理、认证密钥代理、Vanadium 组件更新代理、网络定位与逆地理编码等功能。通过这些服务，开发者可以快速获取可靠的网络、定位和安全基础设施，而无需自行搭建和维护复杂的服务器体系，从而把更多精力放在应用层的安全与隐私特性上。

**典型接入方式**  
1. **部署方式**：克隆仓库后，依据 `README` 中的 Docker‑Compose 示例启动相应的服务容器（HTTPS、NTP、SUPL、PSDS 缓存等）。  
2. **网络配置**：在 GrapheneOS 设备或自建的 Vanadium/Chromium 客户端中，将对应的 URL（如 `https://time.grapheneos.org`、`https://supl.grapheneos.org`）配置为系统的时间、位置、更新等服务端点。  
3. **API 调用**：大多数服务遵循标准的 REST/HTTPS 接口（例如 NTP 使用 UDP 123 端口，SUPL 使用 HTTPS POST），可直接在移动端或后端代码中使用现成的库进行调用。  
4. **证书与密钥**：若需要自签证书或自定义 attestation key，按照 `provisioning/` 目录提供的脚本生成并在设备上注册即可。

**生产可用性**  
- **成熟度**：项目已有 684 颗星、197 次 fork，最近一次提交在 2026‑06‑24，表明仍在活跃维护。  
- **稳定性**：核心服务（时间、HTTPS、SUPL）在 GrapheneOS 正式发布版中已实际使用，具备实战验证。  
- **集成成本**：依赖 Docker、systemd、以及几项外部库（如 `chrony`、`nginx`），对已有 CI/CD 流程有一定改动成本；建议先在测试环境做一个最小化的 PoC（仅启动 NTP 与 HTTPS 检查），确认网络、证书链和防火墙配置无误后再扩展。  
- **风险**：文档中对完整的生产部署流程描述较少，尤其是高可用与监控方案需要自行设计；另外，服务主要以 HTML 为主，若需要深度定制或二次开发，可能需要额外的后端实现工作。  

**结论**：GrapheneOS/grapheneos.org 适合作为安全/隐私导向的移动系统后端基础设施，能够显著降低自行搭建时间同步、定位和更新服务的门槛。对内部原型或对安全合规要求高的产品可直接采用；在生产环境使用前，请完成完整的容错、监控与安全审计，确保依赖的容器镜像和证书管理符合组织的运维标准。

## 🧭 Practical evaluation

**Value:** GrapheneOS/grapheneos.org helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 684 GitHub stars
- 197 forks
- updated 2026-06-24
- primary language: HTML
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 57/100 |
| stars | 60/100 |
| topics | 50/100 |
| outlook | 66/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 60/100 |
| production | 66/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/GrapheneOS/grapheneos.org) · [← Back to Networking](./README.md)</sub>
