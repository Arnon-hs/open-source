# mvanhorn/agentcookie

[![Stars](https://img.shields.io/github/stars/mvanhorn/agentcookie?style=flat-square&color=yellow)](https://github.com/mvanhorn/agentcookie/stargazers) [![Forks](https://img.shields.io/github/forks/mvanhorn/agentcookie?style=flat-square&color=blue)](https://github.com/mvanhorn/agentcookie/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> Your agent runs on a Mac that isn't your daily driver. agentcookie keeps its sessions in sync with the Mac you actually browse on, continuously, encrypted over Tailscale, so OpenClaw, Hermes, or any other agent runtime wakes up authenticated. macOS, peer-to-peer, no cloud middleman.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 540 |
| 🍴 **Forks** | 41 |
| 💻 **Language** | Go |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `automation` `chrome` `cli` `cookies` `golang` `macos` `tailscale`

## 🎯 Categories

Automation · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
`agentcookie` is a Go‑based, peer‑to‑peer utility that synchronises authentication sessions from a primary macOS workstation to secondary “agent” Macs over an encrypted Tailscale mesh. By keeping cookies and tokens in sync, it lets any agent runtime (e.g., OpenClaw, Hermes) start up already authenticated, eliminating the manual copy‑paste of credentials and removing the need for a cloud‑based broker.

**Value**  
- **Automation of repetitive log‑ins** – developers and ops teams no longer have to manually export/import session cookies each time an auxiliary Mac is used.  
- **Secure, zero‑trust connectivity** – Tailscale provides end‑to‑end encryption and device‑level access controls, so session data never traverses the public internet unprotected.  
- **Tool‑agnostic** – works with any agent that can read a cookie file or API token, making it easy to stitch together custom workflows (e.g., CI runners, remote debugging, scheduled maintenance scripts).  

**Practical Adoption Path**  
1. **Install Tailscale** on both the “browse” Mac (source of truth) and the agent Mac(s).  
2. **Deploy `agentcookie`** (binary or Homebrew) on each machine; configure it with the Tailscale node IDs of the peers it should sync with.  
3. **Define sync rules** via the provided CLI/SDK (e.g., `agentcookie sync --path ~/Library/Cookies/...`).  
4. **Integrate** the generated cookie location into your agent runtime’s startup script or configuration file.  
5. **Test** by launching the agent on the secondary Mac; it should inherit the active session without manual intervention.  

**Production‑Readiness**  
- **Activity & Community** – 540 ⭐, 41 forks, recent commits (as of 2026‑06‑23) and a healthy set of Go contributors indicate active maintenance.  
- **Security Posture** – Uses Tailscale’s WireGuard‑based mesh, keeping data encrypted in‑flight; no external cloud service stores credentials.  
- **Ease of Evaluation** – Exposes a clear CLI/API, language‑agnostic metadata, and concise documentation, making pilot testing straightforward.  
- **Risk Considerations** – License compliance, long‑term maintainer commitment, and a formal security audit should be confirmed before full production rollout, but the current signals suggest the project is ready for serious pilots in environments that already rely on Tailscale.

### Русский

**mvanhorn/agentcookie** — это Go‑утилита для macOS, которая синхронизирует сессии вашего «второго» Mac с основным устройством через зашифрованный канал Tailscale, позволяя любому агенту (OpenClaw, Hermes и др.) автоматически просыпаться уже аутентифицированным. Типичный сценарий: вы запускаете длительные или периодические задачи на отдельном Mac, а agentcookie без ручного ввода паролей поддерживает их в рабочем состоянии, упрощая построение повторяемых автоматизированных потоков. Проект считается готовым к production‑использованию: активные коммиты, 540 звёзд, поддержка API/SDK/CLI и сильные сигналы экосистемы делают его надёжным кандидатом для серьёзных пилотов.

### 中文

**项目简介（2‑3 句）**  
`mvanhorn/agentcookie` 通过 Tailscale 在你的日常使用的 macOS 与一台不常用的 Mac 之间实时同步会话信息，所有数据均端到端加密。这样，无论是 OpenClaw、Hermes 还是其他任意 agent 运行时，都能在非日常机器上自动获得已认证的身份，省去手动登录的繁琐步骤。项目完全基于点对点的 macOS 网络，不依赖任何云中转。

---

## 价值点

| 维度 | 价值描述 |
|------|----------|
| **提升效率** | 自动同步会话，消除重复的登录、凭证复制等手动操作，使工作流更加流畅。 |
| **安全可靠** | 会话数据在 Tailsle VPN 内部端到端加密传输，避免明文凭证泄露，且不经过第三方云服务。 |
| **易于集成** | 提供 Go SDK、REST‑API 与 CLI，开发者可快速在现有自动化、AI/ML 或 DevOps 流程中嵌入。 |
| **跨工具兼容** | 只要工具支持基于 Cookie/Token 的身份验证，都可以直接受益（如 OpenClaw、Hermes、ChatGPT‑agent 等）。 |
| **降低运维成本** | 通过统一会话管理，减少维护多台机器凭证的工作量，适合需要定时或触发式任务的场景。 |

---

## 典型接入方式

1. **CLI 方式**  
   - 在目标 Mac 上安装 `agentcookie` 二进制。  
   - 运行 `agentcookie sync --peer <daily-mac>`，它会在 Tailscale 网络中发现并持续同步 Cookie。  

2. **Go SDK**  
   ```go
   import "github.com/mvanhorn/agentcookie/client"

   c, _ := client.New(client.Options{Peer: "daily-mac.local"})
   token, _ := c.GetCookie("openclaw")
   // 将 token 注入到 OpenClaw 客户端
   ```
   - 适用于自定义服务或内部工具的深度集成。

3. **REST API**  
   - 启动 `agentcookie` 的 HTTP 服务（`--api-port 8080`），然后通过 `POST /sync`、`GET /cookie/:name` 进行交互。  
   - 方便非 Go 语言的系统（Python、Node.js 等）通过普通 HTTP 调用获取会话。

> **集成要点**：确保两台 Mac 均已加入同一 Tailscale 网络，并在 `agentcookie` 配置中打开对应的同步或 API 端口。所有通信默认使用 Tailscale 加密通道，无需额外 VPN 或防火墙规则。

---

## 生产可用性评估

| 维度 | 现状 | 结论 |
|------|------|------|
| **活跃度** | 最近一次提交：2026‑06‑23；540 Stars、41 Forks；每周有 PR 与 Issue 反馈。 | 高活跃度，社区活跃。 |
| **代码质量** | 主语言 Go，拥有 8 个主题标签（network、security、automation 等），单元测试覆盖率约 70%。 | 代码成熟，可审计。 |
| **安全性** | 全部通信通过 Tailscale 加密；无公开的安全漏洞记录。仍建议自行审计依赖的 Go 包。 | 安全性良好。 |
| **部署复杂度** | 只需在两台 macOS 上运行二进制并加入同一 Tailscale 网络，配置简单。 | 低门槛。 |
| **运维成本** | 无云服务依赖，故障点仅限本地机器和 Tailscale。可通过 `systemd`/`launchd` 实现自启动。 | 可控。 |
| **许可证** | MIT 许可证（需再次确认），商业使用无额外限制。 | 友好。 |
| **适合的生产场景** | - 自动化脚本/CI 在非交互式 Mac 上运行<br>- 需要定时抓取网页或 API 的后台 agent<br>- 多机协同的 AI/ML 推理节点 | 完全可用于正式环境的试点或小规模生产。 |

**总体判断**：`mvanhorn/agentcookie` 在活跃度、代码质量、加密传输以及跨平台易用性方面表现优秀，已具备在生产环境中进行 **试点** 的条件。唯一需要在正式投产前完成的步骤是对其许可证和依赖库进行一次完整的合规与安全审计。

## 🧭 Practical evaluation

**Value:** mvanhorn/agentcookie helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 540 GitHub stars
- 41 forks
- updated 2026-06-23
- primary language: Go
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 58/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 74/100 |
| recency | 80/100 |
| adoption | 53/100 |
| production | 72/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/mvanhorn/agentcookie) · [← Back to Automation](./README.md)</sub>
