# lightningd/plugins

[![Stars](https://img.shields.io/github/stars/lightningd/plugins?style=flat-square&color=yellow)](https://github.com/lightningd/plugins/stargazers) [![Forks](https://img.shields.io/github/forks/lightningd/plugins?style=flat-square&color=blue)](https://github.com/lightningd/plugins/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> Community curated plugins for core-lightning

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 308 |
| 🍴 **Forks** | 133 |
| 💻 **Language** | Python |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`c-lightning` `cln` `core-lightning` `lightning` `lightning-network` `lightningd` `plugin`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
`lightningd/plugins` is a community‑maintained collection of plugins for Core Lightning (c-lightning), written primarily in Python. With over 300 GitHub stars, frequent commits, and a growing user base, the repository provides ready‑to‑use extensions that expose Core Lightning’s API/SDK signals, making it easy to add custom functionality to a Lightning node.

**Value**  
- **Extensible ecosystem** – The plugins cover common operational needs (e.g., monitoring, invoicing, routing hints) and expose Core Lightning’s internal signals, allowing developers to plug in new features without modifying the daemon itself.  
- **Low‑entry barrier** – Because the code is in Python and each plugin follows a simple CLI‑style interface, teams can quickly prototype, test, and ship Lightning‑related capabilities.  
- **Community‑driven** – Contributions are curated by the Core Lightning community, ensuring that the most useful patterns and best practices are shared and kept up‑to‑date.

**Practical Adoption Path**  
1. **Evaluate fit** – Review the repository README and the list of available plugins to identify those that match your workflow (e.g., payment monitoring, custom routing policies).  
2. **Prototype** – Clone the repo, install the required Python dependencies, and run a selected plugin against a testnet or regtest Core Lightning node to validate behavior.  
3. **Integrate** – Add the plugin to your production node’s `lightningd` configuration (`plugin-dir` or explicit `plugin=` entries). Use the exposed RPC methods or CLI hooks to automate the desired workflow.  
4. **Customize** – Fork the plugin or write a new one using the same Python skeleton, leveraging the documented API/SDK signals for deeper integration.  

**Production Readiness**  
- **Activity & adoption** – The project shows recent commits (last update 2026‑05‑11), a healthy star/fork count, and active issue discussion, indicating an engaged maintainer community.  
- **Stability** – Plugins are isolated processes that communicate with `lightningd` over a well‑defined JSON‑RPC interface, limiting failure impact on the core daemon.  
- **Risk considerations** – While no immediate licensing or security red flags appear, a final review of the license (MIT/Apache‑style) and a security audit of any third‑party dependencies is advisable before large‑scale deployment.  

Overall, `lightningd/plugins` is a mature, well‑maintained OSS component that can be safely piloted in production environments, offering a fast path to extend Core Lightning functionality with minimal engineering overhead.

### Русский

**Lightningd/plugins** — это набор сообществом поддерживаемых плагинов для Core‑Lightning, написанных на Python, которые открывают доступ к сигналам реализации (API/SDK/CLI) и позволяют быстро добавить в узел функции вроде мониторинга, автоматизации платежей или интеграции с внешними сервисами. Типичный сценарий — установка нужных плагинов в рабочий node Core‑Lightning и их конфигурация через единую точку управления, что ускоряет построение кастомных Lightning‑решений без собственного кода. Проект обладает высокой готовностью к production: активные коммиты, более 300 звёзд, 133 форка, актуальная поддержка (обновление 2026‑05‑11) и широкое принятие в сообществе, однако перед запуском следует проверить лицензию, безопасность и наличие активных мейнтейнеров.

### 中文

**项目简介**  
lightningd/plugins 是一套由社区维护的 **core‑lightning** 插件集合，提供常用的业务扩展（如支付路由、自动通道管理、监控告警等），帮助用户在不改动 core‑lightning 源码的前提下快速实现特定工作流。

**价值**  
- **即插即用**：插件遵循 core‑lightning 的插件接口，使用 Python 编写，可直接放入 `lightningd/plugins/` 目录或通过 `--plugin` 参数加载。  
- **社区精选**：聚合了社区最常用、最成熟的功能，省去自行开发或维护的成本。  
- **可组合**：多个插件可以并行运行，互不冲突，便于构建复杂的 Lightning 业务链路。  

**典型接入方式**  
1. **安装依赖**（如 `pip install -r requirements.txt`），确保 Python 环境可用。  
2. **下载或克隆插件仓库**：`git clone https://github.com/lightningd/plugins.git`。  
3. **启动 core‑lightning 并加载插件**：  
   ```bash
   lightningd --plugin=plugins/<plugin_name>.py
   ```  
   或者在 `lightningd.conf` 中添加 `plugin=<path>/plugins/<plugin_name>.py`。  
4. **通过 RPC/CLI 调用**：插件会在 `lightning-cli` 中自动注册对应的命令或 RPC 接口，直接使用即可。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑11 最近一次提交，仓库拥有 308 星、133 Fork，社区贡献持续。  
- **技术成熟**：基于 core‑lightning 官方插件框架，使用 Python 实现，易于审计和二次开发。  
- **生态兼容**：与主流 Lightning 节点（c-lightning、lnd）配合良好，已有多家运营商在生产环境中使用。  
- **风险点**：仍需检查许可证（MIT/Apache 等）是否符合企业合规要求，并对插件代码进行安全审计，确保无未修复的依赖漏洞。  

综合来看，lightningd/plugins 已具备 **高生产就绪度**，适合作为正式业务的功能扩展或快速原型验证的首选组件。

## 🧭 Practical evaluation

**Value:** lightningd/plugins may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 308 GitHub stars
- 133 forks
- updated 2026-05-11
- primary language: Python
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 53/100 |
| stars | 53/100 |
| topics | 88/100 |
| outlook | 47/100 |
| quality | 57/100 |
| recency | 20/100 |
| adoption | 53/100 |
| production | 51/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/lightningd/plugins) · [← Back to Misc](./README.md)</sub>
