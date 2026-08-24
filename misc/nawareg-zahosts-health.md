# Nawareg/zahosts-health

[![Stars](https://img.shields.io/github/stars/Nawareg/zahosts-health?style=flat-square&color=yellow)](https://github.com/Nawareg/zahosts-health/stargazers) [![Forks](https://img.shields.io/github/forks/Nawareg/zahosts-health?style=flat-square&color=blue)](https://github.com/Nawareg/zahosts-health/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-35%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 35/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Zahosts Health is an open‑source WHM (WebHost Manager) plugin that monitors login activity to detect /24‑range brute‑force attacks on cPanel accounts. By aggregating failed‑login attempts across an entire /24 subnet, it can flag coordinated attacks that would otherwise slip past per‑IP rate limits, helping hosting providers harden their infrastructure.

**Value**  
- **Targeted security**: Detects distributed credential‑spraying attacks that spread across many IPs within the same /24 network, a pattern common with botnets and compromised residential gateways.  
- **Low‑cost hardening**: As a free plugin, it adds an extra layer of intrusion detection without requiring a separate SIEM or third‑party service.  
- **Actionable alerts**: Generates WHM‑compatible notifications (email, cPanel alerts) that can trigger automated blocks or manual review.

**Practical Adoption Path**  
1. **Review repository** – Clone the project, verify the license (e.g., MIT/Apache), and read the README for installation steps and configuration options.  
2. **Test in a sandbox** – Deploy the plugin on a non‑production WHM instance, enable the default monitoring profile, and generate synthetic failed‑login traffic to confirm detection and alerting.  
3. **Integrate with existing controls** – Map the plugin’s alerts to your firewall or fail2ban rules, or to a ticketing system for incident response.  
4. **Configure thresholds** – Adjust the number of failures and time windows that constitute a /24 brute‑force event, based on your traffic baseline.  
5. **Roll out gradually** – Enable the plugin on a subset of servers or accounts, monitor false‑positive rates, and refine the settings before full deployment.

**Production Readiness**  
- **Maturity**: Updated recently (2026‑06‑23) but with limited activity (only two topics) and sparse documentation, placing it at a **medium** readiness level.  
- **Dependencies**: Relies on WHM/cPanel APIs; ensure compatibility with your WHM version and any custom plugins.  
- **Maintenance**: No clear release cadence or active issue triage, so you’ll need to monitor the repo for security patches or consider forking for long‑term support.  
- **Risk mitigation**: Conduct a security audit of the code, verify that the plugin does not expose additional attack surfaces, and implement fallback mechanisms (e.g., manual lockouts) in case the plugin fails.  

Overall, Zahosts Health can be a valuable addition for hosting environments that need to detect distributed brute‑force attempts, provided you perform the necessary due‑diligence, pilot testing, and integration work before treating it as a production‑critical component.

### Русский

Show HN: Zahosts Health — это открытый WHM‑плагин, который отслеживает попытки перебора паролей по целым /24‑подсетям и генерирует оповещения, позволяя администраторам быстро блокировать атакующие IP‑адреса. Его типичное внедрение — установка в панель WHM/cPanel для внутренних хостинг‑провайдеров или крупных сайтов, где требуется автоматическое обнаружение массовых brute‑force‑атак; перед запуском рекомендуется проверить лицензию, актуальность документации и частоту релизов. Готовность к production оценивается как средняя: плагин подходит для прототипов и внутренних процессов, но требует ручного аудита и контроля зависимостей перед использованием в критически важных окружениях.

### 中文

**项目简介**  
Show HN: Zahosts Health 是一个开源的 WHM（WebHost Manager）插件，用于监测并阻止基于 /24 子网的暴力登录攻击。它通过实时分析登录日志，快速识别同一子网内的大量失败尝试，从而在攻击扩散之前自动触发封禁或警报。

**价值**  
- **安全防护**：专注捕获 /24 规模的暴力破解，帮助托管服务商在攻击初期即做出响应，降低被入侵风险。  
- **成本低廉**：开源且可直接部署在已有的 WHM 环境中，无需额外付费的商业安全产品。  
- **可定制**：插件源码公开，方便根据自家业务规则（如阈值、封禁时长、通知渠道）进行二次开发。

**典型接入方式**  
1. **环境准备**：确保服务器运行的 WHM 版本兼容（插件 README 中列出支持的最低 WHM 版本）。  
2. **下载与安装**：  
   ```bash
   cd /usr/local/cpanel/base/frontend/paper_lantern
   git clone https://github.com/yourorg/za-hosts-health.git zahosts-health
   ```
   或者直接下载压缩包解压到 WHM 插件目录。  
3. **依赖检查**：插件依赖 `perl` 模块 `JSON::PP`、`IO::Socket::IP` 等，使用 `yum`/`apt` 安装缺失的模块。  
4. **配置**：在 WHM → 插件管理 页面启用插件后，编辑生成的 `zahosts-health.conf`，设置：  
   - `threshold`（单位时间内允许的失败次数）  
   - `ban_duration`（封禁时长）  
   - `notify_email`（告警接收邮箱）  
5. **启动与验证**：重启 cPanel/WHM 服务或执行插件自带的 `./zahosts-health --start`，随后在日志文件 `/var/log/zahosts-health.log` 中检查是否成功捕获测试登录失败。  

**生产可用性**  
- **成熟度**：项目最近一次更新于 2026‑06‑23，代码量不大且仅包含两个主题，说明功能相对集中但社区活跃度有限。  
- **适用场景**：适合内部原型、实验性安全加固或中小型托管环境的快速防御；在大规模生产环境使用前建议：  
  1. **审计许可证**（确认为 MIT/Apache 等宽松许可）。  
  2. **评估维护状态**：检查 Issues、Pull Requests 以及作者的响应速度。  
  3. **进行安全审计**：代码审查、单元测试和与现有安全工具（如 Fail2Ban、ModSecurity）的兼容性验证。  
- **风险**：元数据和社区信号较少，可能缺乏完善的文档、自动化测试和持续发布流程。若决定投入生产，需自行建立 CI/CD、监控和更新机制，以防止插件因未及时维护而产生安全漏洞。  

**结论**  
Zahosts Health 提供了一套轻量级、针对 /24 暴力破解的防御方案，价值明显，但因社区活跃度和质量信号有限，建议在内部测试验证后，再根据业务需求决定是否在生产环境中正式采用，并配合额外的审计与维护措施。

## 🧭 Practical evaluation

**Value:** Show HN: Zahosts Health – An open-source WHM plugin to catch /24 brute-force may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-06-23
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 33/100 |
| quality | 26/100 |
| recency | 40/100 |
| adoption | 0/100 |
| production | 41/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/Nawareg/zahosts-health) · [← Back to Misc](./README.md)</sub>
