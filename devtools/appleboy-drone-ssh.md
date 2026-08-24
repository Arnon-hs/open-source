# appleboy/drone-ssh

[![Stars](https://img.shields.io/github/stars/appleboy/drone-ssh?style=flat-square&color=yellow)](https://github.com/appleboy/drone-ssh/stargazers) [![Forks](https://img.shields.io/github/forks/appleboy/drone-ssh?style=flat-square&color=blue)](https://github.com/appleboy/drone-ssh/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Drone plugin for executing remote ssh commands

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 308 |
| 🍴 **Forks** | 79 |
| 💻 **Language** | Go |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `docker-container` `docker-image` `drone` `drone-plugin` `ssh`

## 🎯 Categories

DevTools · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`appleboy/drone-ssh` is a lightweight Drone CI/CD plugin written in Go that lets pipelines run arbitrary SSH commands on remote hosts. With over 300 stars, recent commits, and active community forks, it offers a ready‑to‑use bridge between Drone and any SSH‑accessible infrastructure, making it easy to automate deployments, configuration tasks, or remote script execution.

**Value**  
- **Fast AI‑in‑the‑loop workflows** – By exposing a simple CLI/SDK, the plugin can be called from AI‑driven pipelines (e.g., a model that decides which servers to update) without building a custom SSH client from scratch.  
- **Unified tooling** – Keeps all CI steps inside Drone, avoiding context switches to separate orchestration tools and reducing operational overhead.  
- **Extensible** – Because it’s a Go library with clear API hooks, developers can embed it in custom agents or RAG/agent pipelines that need to trigger remote actions as part of a larger AI workflow.

**Practical Adoption Path**  
1. **Add the plugin to your `.drone.yml`** – reference the Docker image (`appleboy/drone-ssh`) and configure host, user, key, and command parameters.  
2. **Test in a staging pipeline** – run a non‑critical command (e.g., `echo test`) against a staging server to verify connectivity and secret handling.  
3. **Integrate with AI components** – have your model or orchestration service generate the command string, pass it to the plugin via environment variables, and let Drone execute it.  
4. **Scale** – reuse the same plugin across multiple pipelines or repos; version‑pin the Docker image to guarantee reproducibility.

**Production Readiness**  
- **Activity & Community** – Updated as of 2026‑06‑23, 308 stars, 79 forks, and active issue discussions indicate healthy maintenance.  
- **Stability** – The Go codebase is small and well‑documented, with clear error handling and built‑in support for known SSH options (port, timeout, strict host key checking).  
- **Security** – No major metadata risks identified, but a final review of the repository’s license (MIT) and the handling of SSH keys/secrets is recommended.  
- **Ecosystem Fit** – Works out‑of‑the‑box with Drone’s plugin architecture and can be combined with other DevOps tools (Kubernetes, Helm, Terraform) for end‑to‑end CI/CD pipelines.

Overall, `appleboy/drone-ssh` is production‑ready for pilots and can be promoted to full‑scale use after a short validation phase and a security audit of secret management.

### Русский

**appleboy/drone-ssh** — это плагин для CI‑системы Drone, позволяющий выполнять произвольные команды SSH на удалённых серверах прямо из пайплайна. Он часто используется для автоматизации деплоймента, конфигурации инфраструктуры и интеграции AI‑моделей в существующие воркфлоу (например, запуск RAG‑агентов или проверка моделей после сборки). По состоянию на 2026‑06‑23 проект считается готовым к production: активные коммиты, 308 звёзд, 79 форков, написан на Go и имеет хорошую экосистемную поддержку, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介（2‑3 句）**  
appleboy/drone-ssh 是一款基于 Go 实现的 Drone CI 插件，能够在构建流水线中安全、便捷地执行远程 SSH 命令。它通过简洁的 YAML 配置，将服务器上的脚本、部署或运维操作直接嵌入 CI/CD 流程，帮助团队实现自动化交付。

**价值**  
- **提升效率**：无需手动登录服务器，CI 步骤即可完成代码部署、服务重启、数据库迁移等常见运维任务。  
- **统一审计**：所有 SSH 操作均记录在 Drone 的构建日志中，便于追踪和审计。  
- **易于扩展**：基于 Go 编写，插件本身可二次开发或结合其他 Drone 插件，实现更复杂的 AI/ML 部署或 RAG/Agent 工作流。

**典型接入方式**  
1. 在 Drone 仓库的 `.drone.yml` 中添加 `appleboy/drone-ssh` 步骤。  
2. 配置 SSH 私钥（通过 secret 注入）以及目标主机、执行的命令或脚本路径。  
3. 可选地使用 `environment`、`when` 等条件控制执行时机，实现分支或标签的差异化部署。  

```yaml
steps:
- name: deploy
  image: appleboy/drone-ssh
  settings:
    host: your.server.com
    username: root
    password:
      from_secret: ssh_password
    script:
      - cd /var/www/app
      - git pull origin main
      - systemctl restart app
```

**生产可用性**  
- **活跃度**：截至 2026‑06‑23，项目最近一次提交，拥有 308 星、79 Fork，且社区持续贡献。  
- **成熟度**：插件已在多个公开项目中使用，文档完整，支持 Go 语言的跨平台构建。  
- **风险**：暂无重大安全或许可证问题，但仍建议在正式生产环境前审查 SSH 密钥管理策略并确认维护者的响应速度。  

综合来看，appleboy/drone-ssh 具备高可用性，适合作为 CI/CD 自动化部署的核心组件，能够快速帮助团队实现 AI/ML 或其他业务的持续交付。

## 🧭 Practical evaluation

**Value:** appleboy/drone-ssh helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 308 GitHub stars
- 79 forks
- updated 2026-06-23
- primary language: Go
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 48/100 |
| stars | 53/100 |
| topics | 75/100 |
| outlook | 56/100 |
| quality | 59/100 |
| recency | 40/100 |
| adoption | 51/100 |
| production | 61/100 |
| usefulness | 58/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/appleboy/drone-ssh) · [← Back to DevTools](./README.md)</sub>
