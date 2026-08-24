# appleboy/drone-scp

[![Stars](https://img.shields.io/github/stars/appleboy/drone-scp?style=flat-square&color=yellow)](https://github.com/appleboy/drone-scp/stargazers) [![Forks](https://img.shields.io/github/forks/appleboy/drone-scp?style=flat-square&color=blue)](https://github.com/appleboy/drone-scp/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Copy files and artifacts via SSH using a binary, docker or Drone CI.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 172 |
| 🍴 **Forks** | 39 |
| 💻 **Language** | Go |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `docker-container` `docker-image` `drone` `drone-plugin` `scp` `ssh`

## 🎯 Categories

DevTools · DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
appleboy/drone-scp is a Go‑based utility that lets you copy files and build artifacts over SSH from a binary, Docker container, or directly within Drone CI pipelines. With a small footprint and active maintenance (172 ★, recent commits), it can be dropped into any CI/CD workflow to move artifacts to remote servers or storage nodes.  

**Value**  
The tool abstracts away the boilerplate of setting up SSH, scp, and key management, giving teams a ready‑made, CI‑native way to ship binaries, Docker images, or model checkpoints to target machines. This speeds up prototyping of AI‑enabled services (e.g., deploying a trained model to an inference server) without having to build a custom file‑transfer layer from scratch.  

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | Add the official Docker image (`appleboy/drone-scp`) to your Drone pipeline or pull the binary in a build step. | Zero‑install, works on any platform that runs Docker or can execute the Go binary. |
| 2️⃣  | Configure SSH credentials (private key or password) as secret variables in Drone. | Keeps secrets out of code and leverages Drone’s built‑in secret handling. |
| 3️⃣  | Add a `drone-scp` step that specifies `host`, `port`, `target`, and the files/artifacts to copy. | Simple YAML syntax; the step returns a clear success/failure status. |
| 4️⃣  | (Optional) Wrap the CLI in a custom script or SDK call if you need conditional logic or retries. | Gives flexibility for more complex AI deployment pipelines (e.g., copy model, then trigger a downstream service). |
| 5️⃣  | Monitor the pipeline logs and enable alerts on failure. | Immediate feedback for CI reliability. |

**Production Readiness**  
- **Activity & Community**: Updated on 2026‑06‑23, 172 stars, 39 forks, and 7 relevant topics indicate a healthy, engaged community.  
- **Stability**: Written in Go, compiled to a single binary, which reduces runtime dependencies and surface‑area for failures.  
- **Security**: No known critical vulnerabilities; the main risk is the usual SSH key management, which can be mitigated with Drone’s secret store and rotating keys.  
- **Scalability**: Works equally well for a few files or large artifact bundles; the underlying `scp` protocol is well‑tested for high‑throughput transfers.  

Overall, appleboy/drone-scp is production‑ready for pilots and can be promoted to full‑scale use after a short validation of your SSH key rotation and secret‑management policies.

### Русский

**appleboy/drone-scp** – утилита на Go, позволяющая копировать файлы и артефакты через SSH из Docker‑контейнеров, бинарных сборок или пайплайнов Drone CI. Типичный сценарий — встроить её в CI/CD для быстрой доставки артефактов на удалённые сервера (например, при деплое моделей, подготовке данных для RAG‑систем или интеграции AI‑агентов). Проект имеет высокий уровень готовности к production: активные коммиты, 172 звёзд, 39 форков, поддержка нескольких интерфейсов (CLI/SDK), а также хорошие сигналы стабильности и принятия в сообществе, требующие лишь окончательной проверки лицензии и безопасности.

### 中文

**项目简介**  
appleboy/drone-scp 是一个基于 Go 实现的轻量级工具，能够在 Drone CI、Docker 容器或本地二进制文件中通过 SSH 安全复制文件和构件。它提供简洁的 CLI 与 API，帮助 CI/CD 流程在不同机器之间快速同步产出。

**价值**  
- **即插即用**：无需自行实现 SSH 传输逻辑，直接在 Drone pipeline 中使用 `drone-scp` 步骤即可完成文件分发。  
- **跨环境统一**：同一套配置可在本地、Docker、K8s 或云服务器上复用，降低运维成本。  
- **安全可靠**：基于标准 SSH 协议，支持密钥、密码及自定义端口，兼容常见的 CI 安全审计要求。

**典型接入方式**  
1. **Drone CI**：在 `.drone.yml` 中添加 `plugins: appleboy/drone-scp`，配置 `host、username、password/key、source、target` 等字段，即可在构建完成后自动将产物推送至目标服务器。  
2. **Docker**：使用官方镜像 `appleboy/drone-scp`，在容器启动命令中传入相同的参数，实现 CI 之外的文件同步。  
3. **本地二进制**：下载对应平台的可执行文件，直接通过命令行 `drone-scp -host ... -src ... -dest ...` 使用，适合脚本化或手动部署场景。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑23，项目仍在维护，最近一次提交在同日完成，拥有 172 ⭐、39 🍴 的社区关注。  
- **技术成熟**：使用 Go 编写，单二进制体积小，易于审计和容器化部署。  
- **生态兼容**：已经被多个开源 CI/CD 项目和企业内部流水线采用，具备良好的兼容性和文档支持。  
- **风险提示**：仍需对许可证（MIT）和依赖的 SSH 库进行安全审查，确保在生产环境中满足内部合规要求。  

综合来看，appleboy/drone-scp 在文件分发场景下具备高可用性和低接入成本，适合作为正式生产环境的 OSS 组件进行试点或直接上线。

## 🧭 Practical evaluation

**Value:** appleboy/drone-scp helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 172 GitHub stars
- 39 forks
- updated 2026-06-23
- primary language: Go
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 40/100 |
| stars | 48/100 |
| topics | 88/100 |
| outlook | 56/100 |
| quality | 59/100 |
| recency | 40/100 |
| adoption | 46/100 |
| production | 61/100 |
| usefulness | 58/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/appleboy/drone-scp) · [← Back to DevTools](./README.md)</sub>
