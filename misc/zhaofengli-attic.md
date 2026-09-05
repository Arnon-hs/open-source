# zhaofengli/attic

[![Stars](https://img.shields.io/github/stars/zhaofengli/attic?style=flat-square&color=yellow)](https://github.com/zhaofengli/attic/stargazers) [![Forks](https://img.shields.io/github/forks/zhaofengli/attic?style=flat-square&color=blue)](https://github.com/zhaofengli/attic/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Multi-tenant Nix Binary Cache

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.9k |
| 🍴 **Forks** | 176 |
| 💻 **Language** | Rust |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`binary-cache` `nix` `nixos`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
Attic is a multi‑tenant binary cache for Nix, written in Rust, that lets multiple users or teams share pre‑built Nix store objects via a single, permission‑aware service. With a growing community (≈2 k stars) and recent activity, it can speed up reproducible builds and reduce CI load for projects that already use Nix.

**Value**  
- **Speed & cost savings** – cached artifacts are served over HTTP/HTTPS, eliminating repeated builds across CI runners or developer machines.  
- **Isolation** – tenant support means each team or project can have its own namespace and access controls, avoiding the “one‑cache‑fits‑all” security issues of a public cache.  
- **Rust implementation** – fast, low‑memory footprint and easy to embed in existing Rust‑centric infrastructure.

**Practical adoption path**  
1. **Prototype**: Deploy Attic in a sandbox (Docker or a small VM) and point a test Nix client to it using `nix.binaryCaches`. Verify that builds are correctly uploaded and retrieved.  
2. **Security review**: Examine the provided authentication mechanisms (e.g., token‑based or TLS client‑certs) and map them to your organization’s identity provider.  
3. **CI integration**: Add the cache URL to your CI configuration (GitHub Actions, GitLab CI, etc.) and monitor hit‑rate metrics exposed by Attic’s Prometheus endpoint.  
4. **Scale**: If the prototype succeeds, provision a highly‑available instance (e.g., behind a load balancer with persistent storage such as S3 or a local blob store) and migrate existing build artefacts.

**Production readiness**  
Attic sits at a medium readiness level: it is mature enough for internal prototypes and low‑risk production workloads, but the integration surface is thin—documentation on multi‑tenant setup and operational tooling is limited. Before committing to a production deployment, perform dependency audits (Rust crates, underlying storage back‑ends), establish monitoring/alerting for cache health, and run a small‑scale reliability test to confirm that cache misses and eviction policies meet your SLAs. With those checks in place, Attic can be a reliable component of a Nix‑centric CI/CD pipeline.

### Русский

**zhaofengli/attic** — это open‑source кэш бинарных пакетов Nix с поддержкой мульти‑тенантности, написанный на Rust. Он подходит для прототипов и внутренних CI/CD, где требуется изолировать кэши разных проектов/команд, но перед вводом в продакшн следует проверить совместимость с вашей инфраструктурой (например, Nix‑daemon, S3/MinIO) и оценить нагрузку на обслуживание, так как путь интеграции из метаданных неочевиден. При достаточном тестировании проект считается готовым к production‑использованию со средним уровнем надёжности.

### 中文

**项目简介**  
`zhaofengli/attic` 是一个基于 Rust 实现的多租户 Nix 二进制缓存（Binary Cache），旨在为多个团队或 CI/CD 流水线提供安全、隔离且高效的 Nix 包分发服务。

**价值**  
- **多租户隔离**：每个租户拥有独立的命名空间和访问控制，避免不同项目之间的缓存冲突。  
- **高性能**：使用 Rust 编写，具备低延迟和高并发处理能力，适配大规模构建场景。  
- **易于自托管**：提供简洁的二进制发布和 Docker 镜像，可在内部网络或云环境快速部署，降低对外部缓存服务的依赖。

**典型接入方式**  
1. **部署**：  
   - 直接运行发布的二进制或使用官方 Docker 镜像 `zhaofengli/attic:latest`。  
   - 在 `config.toml` 中配置租户、TLS 证书、存储后端（本地文件系统、S3、GCS 等）。  
2. **Nix 客户端配置**：在每个使用者机器的 `~/.config/nix/nix.conf` 中添加  
   ```conf
   substituters = https://attic.example.com/<tenant>
   trusted-public-keys = <tenant>-attic-key
   ```  
   并在对应租户的机器上分发对应的公钥。  
3. **CI/CD 集成**：在 CI 脚本（GitHub Actions、GitLab CI、Jenkins 等）里同样配置 `substituters`，并在构建前登录（若启用 JWT/OAuth）以获取临时访问令牌。

**生产可用性**  
- **成熟度**：项目已有 1900+ 星、176 次 fork，近期（2026‑06‑26）仍在活跃维护，代码质量和社区活跃度良好。  
- **适用场景**：适合内部原型、团队内部缓存或中等规模的生产环境。  
- **风险与准备**：  
  - 元数据中未提供完整的集成指南，需要自行检查租户鉴权、持久化存储（如 S3）和备份策略。  
  - 在正式投产前建议进行一次完整的灾备演练，验证缓存失效、节点扩容以及升级流程。  
- **总体评估**：在做好安全审计和运维准备后，可作为生产级 Nix 缓存服务使用；若对高可用性有严格 SLA 要求，需自行构建多节点 HA 或配合外部负载均衡器。

## 🧭 Practical evaluation

**Value:** zhaofengli/attic may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1946 GitHub stars
- 176 forks
- updated 2026-06-26
- primary language: Rust
- 3 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 70/100 |
| topics | 38/100 |
| outlook | 67/100 |
| quality | 70/100 |
| recency | 80/100 |
| adoption | 66/100 |
| production | 66/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/zhaofengli/attic) · [← Back to Misc](./README.md)</sub>
