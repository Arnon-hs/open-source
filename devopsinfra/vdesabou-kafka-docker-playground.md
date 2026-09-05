# vdesabou/kafka-docker-playground

[![Stars](https://img.shields.io/github/stars/vdesabou/kafka-docker-playground?style=flat-square&color=yellow)](https://github.com/vdesabou/kafka-docker-playground/stargazers) [![Forks](https://img.shields.io/github/forks/vdesabou/kafka-docker-playground?style=flat-square&color=blue)](https://github.com/vdesabou/kafka-docker-playground/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> 🐳✨ Fully automated Apache Kafka® and Confluent Docker based examples // 👷‍♂️ Easily build examples or reproduction models

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 779 |
| 🍴 **Forks** | 239 |
| 💻 **Language** | Shell |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`confluent` `confluent-cloud` `confluent-kafka` `confluent-platform` `kafka` `kafka-connect` `kafka-connectors`

## 🎯 Categories

DevOps/Infra

## 📝 Summary

### English

**Summary**  
vdesabou/kafka‑docker‑playground is a fully automated, Docker‑compose‑based suite that spins up Apache Kafka® and Confluent components together with ready‑to‑run example applications. It lets developers quickly prototype, reproduce bugs, or build end‑to‑end demos without writing any Kafka plumbing code, and the examples are packaged as reusable shell scripts and CLI commands.

**Value**  
The project eliminates the heavy lifting of provisioning a Kafka cluster and wiring producers/consumers, so UI teams can focus on building the front‑end experience while still testing against a realistic streaming backend. By reusing the provided Docker images and example scripts, teams accelerate UI development cycles, reduce duplicated setup effort, and gain a consistent, version‑controlled environment for integration testing.

**Practical adoption path**  
1. Clone the repo and run `docker-compose up` – a complete Kafka/Confluent stack starts in minutes.  
2. Pick an example (e.g., a REST proxy producer, a KSQL query, or a simple console consumer) and run the corresponding shell script to generate test data.  
3. Point your front‑end code to the locally exposed endpoints (REST proxy, Schema Registry, etc.) and iterate.  
4. For CI/CD, embed the same `docker-compose` commands in pipeline jobs to spin up a disposable Kafka environment for every test run.

**Production readiness**  
The repository shows strong OSS health signals: 779 ★, 239 forks, recent commits (last update 2026‑05‑14), active issue discussion, and a well‑documented Docker‑compose configuration. While the core is a development‑focused playground, the underlying Kafka images are the official Confluent containers, making the stack itself production‑grade. The main remaining checks are a formal license audit, a security scan of the Docker images, and confirmation of long‑term maintainer commitment—once those are cleared, the project is suitable for pilot deployments and can be hardened for production use.

### Русский

**Краткое резюме:**  
`vdesabou/kafka-docker-playground` — это набор полностью автоматизированных Docker‑примеров для Apache Kafka® и Confluent, позволяющий быстро развернуть тестовые кластеры и воспроизводить сценарии без написания собственного инфраструктурного кода. Он идеален для разработки и демонстрации пользовательских UI‑компонентов, где требуется мгновенный доступ к Kafka‑топикам и API/SDK, ускоряя построение прототипов и ускоряя поставку фронтенда. Проект считается готовым к пилотному использованию в продакшене: активные коммиты, более 700 звёзд, регулярные обновления и широкая поддержка сообщества подтверждают его надёжность.

### 中文

**项目简介**  
vdesabou/kafka-docker-playground 是一个基于 Docker 的 Apache Kafka® 与 Confluent 完全自动化示例库，提供即开即用的演示、复现和学习环境，帮助开发者快速搭建和验证 Kafka 场景。

**价值**  
- **降低门槛**：通过一键启动的 Docker‑Compose 配置，省去手动安装、配置 ZooKeeper、Kafka、Schema Registry 等繁琐步骤。  
- **加速研发**：提供丰富的生产者/消费者、Kafka Streams、KSQL、Connect 等示例，团队可以直接复用或改写，缩短 UI/业务层的集成时间。  
- **提升可靠性**：所有示例均在容器化环境中运行，保证在本地、CI/CD 或微服务集群中行为一致，便于快速定位问题。

**典型接入方式**  
1. **克隆仓库**：`git clone https://github.com/vdesabou/kafka-docker-playground.git`  
2. **启动环境**：在项目根目录执行 `docker-compose up -d`，即可得到完整的 Kafka + Confluent Stack（包括 Schema Registry、KSQL、Kafka Connect 等）。  
3. **使用示例**：通过提供的 Shell 脚本或 REST API（如 Confluent CLI、kafka‑cat）运行生产者/消费者示例，或在自己的代码中引用对应的 Docker 镜像/网络地址。  
4. **自定义**：修改 `docker-compose.yml` 或 `scripts/` 目录下的脚本，加入自定义主题、ACL、Connector 等，轻松构建专属的复现模型。

**生产可用性**  
- **活跃度**：截至 2026‑05‑14，项目拥有 779 ★、239 Fork，最近一次提交在同一天，表明仍在积极维护。  
- **技术成熟度**：使用官方 Confluent 镜像，遵循 Kafka 最佳实践，示例覆盖常见生产场景（事务、Exactly‑once、Schema Registry、KSQLDB 等），可直接迁移到生产集群。  
- **风险**：暂无重大许可证或安全漏洞报告，但建议在正式上线前进行一次依赖审计（Docker 镜像安全扫描、许可证合规检查）并确认维护者的响应速度。  

综上，vdesabou/kafka-docker-playground 适合作为内部培训、功能验证或快速原型开发的底层平台，在经过简单的安全审查后即可在生产环境中作为可靠的 Kafka 环境搭建工具使用。

## 🧭 Practical evaluation

**Value:** vdesabou/kafka-docker-playground helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 779 GitHub stars
- 239 forks
- updated 2026-05-14
- primary language: Shell
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 60/100 |
| stars | 62/100 |
| topics | 88/100 |
| outlook | 70/100 |
| quality | 76/100 |
| recency | 80/100 |
| adoption | 61/100 |
| production | 70/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/vdesabou/kafka-docker-playground) · [← Back to DevOps & Infra](./README.md)</sub>
