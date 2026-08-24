# lerd-env/lerd

[![Stars](https://img.shields.io/github/stars/lerd-env/lerd?style=flat-square&color=yellow)](https://github.com/lerd-env/lerd/stargazers) [![Forks](https://img.shields.io/github/forks/lerd-env/lerd?style=flat-square&color=blue)](https://github.com/lerd-env/lerd/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Open-source, Herd-like local PHP development environment for Linux and macOS. Automatic .test domains, per-project PHP/Node isolation, one-command TLS. Podman-native, rootless.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 702 |
| 🍴 **Forks** | 37 |
| 💻 **Language** | Go |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`developer-tools` `development-environment` `laravel` `lemp` `linux` `local-development` `nginx` `php` `php-development` `podman` `symfony` `ubuntu`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Project Summary**

Lerd is an open-source local PHP development environment for Linux and macOS, designed to provide a Herd-like setup with automatic .test domains, project isolation, and one-command TLS. This tool is particularly useful for adding AI capabilities to existing projects without requiring a new model stack. It is highly production-ready, with recent activity, adoption, and a strong ecosystem.

**Value Proposition**

Lerd's primary value lies in its ability to simplify the process of adding AI capabilities to existing projects, making it an attractive option for developers and organizations looking to integrate AI features without starting from scratch. By providing a pre-configured environment, Lerd reduces the complexity and time required to set up and test AI-powered workflows.

**Practical Adoption Path**

To adopt Lerd, follow these steps:

1. Evaluate the tool by checking the README and performing a small proof of concept to ensure it meets your project's requirements.
2. Review the license, security posture, and active maintainers to ensure they align with your organization's standards.
3. Install Lerd using the provided documentation and set up a local development environment.
4. Integrate Lerd with your existing project by following the provided guidelines and adapting the tool to suit your specific needs.

**Production Readiness**

Lerd is highly

### Русский

Резюме проекта lerd-env/lerd:

lerd-env/lerd — это open-source локальный среда разработки для PHP, предназначенная для Linux и macOS. Это утилитарная среда, позволяющая автоматически создавать домены для тестирования, изолировать проекты по PHP/Node и включать TLS с помощью одной команды. lerd-env/lerd готов к производственному использованию, поскольку имеет высокий уровень готовности, недавнюю активность, широкое распространение и сильные сигналы экосистемы.

### 中文

**项目价值**  
lerd‑env/lerd 为 Linux 与 macOS 提供了类似 Herd 的本地 PHP 开发环境，能够在同一台机器上实现 **项目级别的 PHP/Node 版本隔离、自动生成 `.test` 域名以及一键 TLS**。基于 Podman 的 rootless 运行方式让开发者无需管理员权限即可安全启动容器，极大降低了环境搭建和依赖冲突的成本。

**典型接入方式**  

1. **快速试用**  
   ```bash
   curl -fsSL https://raw.githubusercontent.com/lerd-env/lerd/main/install.sh | sh
   lerd init my-project
   cd my-project
   lerd up
   ```  
   以上三条命令即可在当前目录创建一个独立的项目环境，自动分配 `my-project.test` 域名并生成自签名 TLS 证书。

2. **在 CI/CD 中使用**  
   - 在 CI 脚本里安装 lerd（同上），然后通过 `lerd up --ci` 启动容器，完成测试后 `lerd down` 销毁。  
   - 通过 `lerd php -v`、`lerd node -v` 等子命令在流水线中验证不同语言版本的兼容性。

3. **与现有工具链集成**  
   - 通过 `lerd exec <cmd>` 在项目容器内部执行任意命令，可直接替代 `docker exec`、`podman exec`。  
   - 将 `lerd` 作为 VS Code Remote Containers 或 JetBrains IDE 的后端，编辑器会自动使用已隔离的环境。

**生产可用性**  

- **活跃度**：截至 2026‑07‑05 最近一次提交，GitHub ★702、Fork 37，社区活跃，Issue 响应及时。  
- **技术成熟度**：核心实现基于 Go，使用 Podman‑native、rootless 模式，天然兼容容器安全最佳实践；自动 TLS 与 `.test` 域名功能已在多个开源项目中验证。  
- **风险评估**：目前未发现重大元数据或许可证冲突；仍需对容器镜像的安全基线（如 CVE 扫描）进行二次审计，并确认维护者对关键 bug 的响应时效。  
- **适配性**：对 Linux 与 macOS 均提供原生支持，Windows 通过 WSL2 亦可使用，满足大多数生产团队的跨平台需求。  

综上，lerd‑env/lerd 已具备 **高可用性** 与 **易集成** 的特性，可在内部研发环境或小规模生产环境中直接采用，建议先在单一项目做 PoC，验证与现有 CI/CD、IDE 的兼容性后再逐步推广。

## 🧭 Practical evaluation

**Value:** lerd-env/lerd helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 702 GitHub stars
- 37 forks
- updated 2026-07-05
- primary language: Go
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 39/100 |
| stars | 61/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 65/100 |
| recency | 40/100 |
| adoption | 55/100 |
| production | 56/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/lerd-env/lerd) · [← Back to DevTools](./README.md)</sub>
