# nightscout/Trio

[![Stars](https://img.shields.io/github/stars/nightscout/Trio?style=flat-square&color=yellow)](https://github.com/nightscout/Trio/stargazers) [![Forks](https://img.shields.io/github/forks/nightscout/Trio?style=flat-square&color=blue)](https://github.com/nightscout/Trio/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> Trio - an automated insulin delivery system for iOS based on the OpenAPS algorithm with adaptations.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 332 |
| 🍴 **Forks** | 1.8k |
| 💻 **Language** | Swift |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`closed-loop` `diabetes` `opensource` `oref` `t1d`

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Brief Summary**  
Trio is an iOS‑only automated insulin‑delivery app that implements the OpenAPS algorithm with custom adaptations for Apple devices. Backed by the Nightscout community, it is actively maintained (last commit 2026‑06‑23), written in Swift, and already has a sizable user base (332 ★, 1.7 k forks).  

**Value**  
- **Open‑source, algorithmic transparency:** By re‑using the proven OpenAPS control logic, Trio gives clinicians and developers full visibility into how insulin dosing decisions are made, facilitating audit, customization, and regulatory compliance.  
- **iOS‑native experience:** Leveraging Swift and Apple’s health‑kit ecosystem, the app can integrate tightly with iPhone, Apple Watch, and compatible CGM/insulin‑pump hardware, delivering a smooth user experience that many commercial solutions lack.  
- **Community ecosystem:** The Nightscout ecosystem provides dashboards, data‑sharing APIs, and a large pool of contributors, making it easier to extend Trio with remote monitoring, tele‑health, or research‑grade data pipelines.  

**Practical Adoption Path**  
1. **Proof‑of‑concept (PoC):** Clone the repo, run the README‑guided build on a test iOS device, and verify basic OpenAPS loop functionality with a sandbox CGM/pump simulator.  
2. **Safety & compliance review:** Conduct a code‑audit (license, third‑party dependencies, security), add unit/integration tests for any custom adaptations, and document the risk‑mitigation plan.  
3. **Pilot integration:** Deploy the PoC in a controlled clinical pilot (e.g., a single diabetes clinic) using a limited patient cohort, integrate with existing Nightscout servers for data storage, and collect usability and safety metrics.  
4. **Scale‑up:** Incorporate feedback, harden the CI/CD pipeline, and formalize support/maintenance agreements before broader roll‑out.  

**Production Readiness**  
- **Recent activity & community support:** Frequent commits, many forks, and a strong star count indicate an active developer base and ongoing bug‑fixes.  
- **Maturity of core algorithm:** The OpenAPS algorithm is battle‑tested in real‑world closed‑loop therapy, reducing algorithmic risk.  
- **Platform stability:** Swift and iOS provide a stable, well‑documented runtime, and Apple’s health‑kit APIs simplify sensor integration.  
- **Remaining checks:** A final review of the licensing terms, a security audit of third‑party libraries, and confirmation of active maintainers are required before committing to a production deployment.  

Overall, Trio is a high‑potential OSS candidate for an automated insulin‑delivery pilot, provided the organization completes the standard safety, compliance, and security due‑diligence steps.

### Русский

Trio — это iOS‑приложение для автоматической подачи инсулина, реализующее алгоритм OpenAPS с адаптациями, что позволяет пациентам с диабетом получать более точный и своевременный контроль глюкозы. Типичный сценарий внедрения — интеграция в существующую систему Nightscout/CGM через небольшое proof‑of‑concept, проверка README и базовых API, после чего можно масштабировать до полноценного пилотного проекта. По активности репозитория (обновления в 2026 г., 332 звёзд, 1753 форка) и поддержке сообщества уровень готовности к production высокий, однако требуется окончательная проверка лицензии, безопасности и наличия активных мейнтейнеров.

### 中文

**项目简介**  
Trio 是一款基于 OpenAPS 算法并针对 iOS 进行二次适配的自动胰岛素输送系统，采用 Swift 开发，旨在为糖尿病患者提供开源、可定制的闭环血糖管理方案。

**价值**  
- **开源透明**：代码公开、可审计，帮助医疗团队和开发者快速了解并改进算法。  
- **跨平台生态**：与 Nightscout、OpenAPS 等成熟生态兼容，便于在已有的糖尿病管理工作流中直接集成。  
- **高活跃度**：截至 2026‑06‑23，项目拥有 332 星、1753 次 Fork，近期仍在维护，表明社区活跃、功能迭代快速。

**典型接入方式**  
1. **阅读并验证 README**：确认项目的依赖、硬件要求（如兼容的胰岛素泵、CGM）以及 iOS 版本。  
2. **小规模 PoC**：在测试设备上克隆仓库，使用 Xcode 编译运行，先实现最基本的血糖读取 → 计算 → 输注指令闭环。  
3. **与 Nightscout/OpenAPS 集成**：通过已有的 API（REST、WebSocket）将 CGM 数据、泵状态同步到 Nightscout，或直接使用 OpenAPS 的配置文件进行算法参数调优。  
4. **安全审计**：在正式部署前进行代码审计、依赖漏洞扫描，并确保符合当地医疗器械法规。  

**生产可用性**  
- **成熟度**：项目近期活跃，代码库结构清晰，Swift 语言天然适配 iOS，具备在真实患者环境中进行试点的技术基础。  
- **准备度**：在完成上述 PoC、完成安全合规检查并得到临床专家批准后，可进入受控的生产环境进行更大规模的 Pilot。  
- **风险**：仍需确认许可证兼容性、持续维护者的响应速度以及安全补丁的及时性，建议在正式上线前与核心维护者保持沟通。  

综上，nightscout/Trio 具备较高的生产候选价值，适合作为 iOS 平台的自动胰岛素输送解决方案进行小范围验证后，逐步推广至更大规模的临床使用。

## 🧭 Practical evaluation

**Value:** nightscout/Trio may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 332 GitHub stars
- 1753 forks
- updated 2026-06-23
- primary language: Swift
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 81/100 |
| stars | 54/100 |
| topics | 63/100 |
| outlook | 54/100 |
| quality | 62/100 |
| recency | 40/100 |
| adoption | 61/100 |
| production | 56/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/nightscout/Trio) · [← Back to Mobile](./README.md)</sub>
