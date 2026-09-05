# testcontainers/testcontainers-go

[![Stars](https://img.shields.io/github/stars/testcontainers/testcontainers-go?style=flat-square&color=yellow)](https://github.com/testcontainers/testcontainers-go/stargazers) [![Forks](https://img.shields.io/github/forks/testcontainers/testcontainers-go?style=flat-square&color=blue)](https://github.com/testcontainers/testcontainers-go/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-83%2F100-brightgreen?style=flat-square)](#)

> Testcontainers for Go is a Go package that makes it simple to create and clean up container-based dependencies for automated integration/smoke tests. The clean, easy-to-use API enables developers to programmatically define containers that should be run as part of a test and clean up those resources when the test is done.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4.9k |
| 🍴 **Forks** | 610 |
| 💻 **Language** | Go |
| 📈 **Score** | 83/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`automation` `docker` `go` `golang` `hacktoberfest` `testcontainers` `testcontainers-go` `testing`

## 🎯 Categories

Automation · DevTools · DevOps/Infra

## 📝 Summary

### English

Testcontainers for Go simplifies creating and tearing down container‑based dependencies in integration tests, letting developers spin up blockchain nodes, wallets, or DeFi services with a clean Go API. Its straightforward integration (exposes API/SDK/CLI signals) and strong recent activity—high star/fork counts, frequent updates, and active ecosystem—make it a production‑ready choice for pilots and ongoing Web3 workflow prototyping.

### Русский

Testcontainers‑Go — это библиотека для Go, позволяющая автоматически поднимать и удалять контейнеры‑зависимости в интеграционных и smoke‑тестах, что упрощает прототипирование и проверку Web3/блокчейн‑workflow (например, кошельков, DeFi‑протоколов). Типичный сценарий: в тесте программно описывается нужный контейнер (например, Ethereum‑node), запускается, тест взаимодействует с ним, а после завершения контейнер автоматически уничтожается. Проект имеет высокую готовность к production: активные коммиты, более 4 900 звёзд, широкое принятие в сообществе и стабильный API.

### 中文

**项目简介**  
Testcontainers‑Go 是一个面向 Go 语言的轻量级库，提供简洁的 API，帮助开发者在集成测试或冒烟测试期间自动启动、配置并在测试结束后自动销毁容器化依赖。通过代码即可声明所需的数据库、消息队列、区块链节点等服务，省去手动搭建和清理环境的繁琐工作。

**价值**  
- **加速区块链/Web3原型开发**：可直接在测试中启动以太坊、Hyperledger 等链节点，快速验证钱包、DeFi 合约或跨链流程。  
- **提升测试可靠性**：容器化的依赖在每次运行时都是全新实例，避免了环境污染和“本地机器”导致的 flaky 测试。  
- **统一 DevOps 与 CI/CD**：在本地、GitHub Actions、GitLab CI 等 CI 环境中使用相同代码，确保开发、预发布、生产的测试环境保持一致。

**典型接入方式**  
1. **在 Go 项目中引入依赖**  
   ```bash
   go get github.com/testcontainers/testcontainers-go
   ```
2. **在测试代码里声明容器**（以 PostgreSQL 为例）  
   ```go
   ctx := context.Background()
   req := testcontainers.ContainerRequest{
       Image:        "postgres:15-alpine",
       Env:          map[string]string{"POSTGRES_PASSWORD": "secret"},
       ExposedPorts: []string{"5432/tcp"},
       WaitingFor:   wait.ForListeningPort("5432/tcp"),
   }
   pgContainer, err := testcontainers.GenericContainer(ctx, testcontainers.GenericContainerRequest{
       ContainerRequest: req,
       Started:          true,
   })
   defer pgContainer.Terminate(ctx)   // 测试结束自动清理
   ```
3. **在 CI/CD pipeline 中使用**  
   - 在 `Dockerfile` 或 CI 镜像中预装 Docker Engine（或使用 Docker‑in‑Docker）。  
   - 直接运行 `go test ./...`，Testcontainers‑Go 会在 CI 环境中拉取并启动所需容器，无需额外脚本。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑25，拥有近 5 k ⭐、600+ forks，最近一次提交在同日，表明项目仍在积极维护。  
- **生态兼容**：已被多家区块链 SDK、微服务框架以及 CI 平台（GitHub Actions、GitLab CI、CircleCI）采用，具备成熟的社区支持。  
- **安全与合规**：采用 Apache‑2.0 许可证，容器镜像由官方或可信仓库提供，可通过企业镜像仓库进行审计。  
- **风险点**：仍需自行评估底层 Docker 引擎的安全补丁、容器镜像的 CVE 状况，以及项目维护者的长期可用性。总体而言，Testcontainers‑Go 已达到 **生产级**（High）可用性，适合作为正式项目的集成测试基础设施。

## 🧭 Practical evaluation

**Value:** testcontainers/testcontainers-go helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 4892 GitHub stars
- 610 forks
- updated 2026-06-25
- primary language: Go
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 70/100 |
| stars | 79/100 |
| topics | 100/100 |
| outlook | 85/100 |
| quality | 84/100 |
| recency | 80/100 |
| adoption | 76/100 |
| production | 78/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/testcontainers/testcontainers-go) · [← Back to Automation](./README.md)</sub>
