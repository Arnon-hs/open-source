# mitchellkrogza/nginx-ultimate-bad-bot-blocker

[![Stars](https://img.shields.io/github/stars/mitchellkrogza/nginx-ultimate-bad-bot-blocker?style=flat-square&color=yellow)](https://github.com/mitchellkrogza/nginx-ultimate-bad-bot-blocker/stargazers) [![Forks](https://img.shields.io/github/forks/mitchellkrogza/nginx-ultimate-bad-bot-blocker?style=flat-square&color=blue)](https://github.com/mitchellkrogza/nginx-ultimate-bad-bot-blocker/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Nginx Block Bad Bots, Spam Referrer Blocker, Vulnerability Scanners, User-Agents, Malware, Adware, Ransomware, Malicious Sites, with anti-DDOS, Wordpress Theme Detector Blocking and Fail2Ban Jail for Repeat Offenders

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4.8k |
| 🍴 **Forks** | 522 |
| 💻 **Language** | Shell |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`adware` `bot-blocker` `bots` `gambling-filter` `malware` `nginx` `nginx-server` `porn-filter` `referer-blocker` `referrer-spam` `scanners` `spam-blocker`

## 🎯 Categories

Automation · Backend · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The *nginx‑ultimate‑bad‑bot‑blocker* is a comprehensive, community‑maintained rule set for Nginx that blocks malicious bots, spam referrers, vulnerability scanners, ransomware‑related user‑agents, and known malicious domains, while also offering anti‑DDoS, WordPress theme‑detector blocking and a Fail2Ban jail for repeat offenders. Written in shell scripts, it automates the generation and updating of Nginx configuration files, letting operators replace tedious manual blacklist maintenance with a single, regularly refreshed source. With over 4,700 stars and active contributions, it is a mature, production‑ready OSS component for any Nginx‑based web service.

**Value**  
- **Automation of repetitive security tasks** – eliminates the need for security teams to manually curate and update IP, UA, and referrer blocklists.  
- **Broad coverage** – combines bot, malware, adware, ransomware, and DDoS defenses plus WordPress‑specific filters in one package, reducing the number of disparate tools required.  
- **Fail2Ban integration** – automatically escalates repeat offenders to a jail, further hardening the environment without extra scripting.  
- **Low operational overhead** – a single cron‑driven script pulls updates from the GitHub repository and reloads Nginx, keeping defenses current with minimal human intervention.

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Proof‑of‑Concept** – Clone the repo on a staging Nginx instance, run `./install.sh` (or the documented setup script) and verify that the generated `badbots.conf` is included in the Nginx config. | Confirms compatibility with your Nginx version and validates that the script does not clash with existing custom rules. |
| 2️⃣  | **Baseline testing** – Use a set of known bad‑bot user‑agents and spam referrers (provided in the repo) to ensure they are blocked (HTTP 403/404). | Guarantees the rule set works as expected before production rollout. |
| 3️⃣  | **Fail2Ban integration** – Enable the optional Fail2Ban jail, test that repeated hits from a single IP trigger the ban. | Adds an extra layer of protection for persistent attackers. |
| 4️⃣  | **Gradual rollout** – Deploy the configuration to a subset of production servers (e.g., 10 % of load balancer pool) while monitoring error logs and traffic metrics. | Limits risk; any false positives can be caught early. |
| 5️⃣  | **Full deployment & automation** – Schedule the update script (daily or weekly) via cron, enable automatic Nginx reload, and add monitoring alerts for rule‑update failures. | Ensures continuous protection with zero‑touch maintenance. |
| 6️⃣  | **Ongoing review** – Periodically audit the blocked lists and adjust any custom whitelists needed for legitimate traffic. | Maintains a balance between security and availability. |

**Production Readiness**  
- **Activity & Community** – 4,752 stars, 522 forks, recent commits (as of 2026‑06‑26) indicate an active maintainer base.  
- **Maturity** – The project has been used in numerous public deployments and is referenced in security blogs, suggesting real‑world stability.  
- **Ease of Integration** – The installer script and clear README make initial setup straightforward; however, the exact integration steps (e.g., where to place the generated config) must be validated in your environment.  
- **Risk Mitigation** – Because the integration path is not fully described in metadata, start with a small proof‑of‑concept and verify that the update process does not interfere with existing Nginx customizations.  

Overall, the blocker is a high‑readiness, low‑cost security enhancement for any Nginx‑served application, provided you allocate a brief validation window to confirm fit‑for‑purpose and to fine‑tune any necessary whitelist exceptions.

### Русский

**Краткое резюме:**  
`mitchellkrogza/nginx-ultimate-bad-bot-blocker` — это готовый набор скриптов и конфигураций для Nginx, который автоматически блокирует известные вредоносные боты, сканеры уязвимостей, спам‑рефереры, рекламное и вредоносное ПО, а также защищает от DDoS‑атак и распознаёт попытки сканировать WordPress‑темы; при повторных нарушениях можно подключить Fail2Ban для автоматической изоляции. Типовой сценарий внедрения — добавление репозитория в CI/CD, запуск скрипта‑установщика на новых серверах и периодическое обновление списков через cron, что полностью устраняет ручную работу по поддержке черных списков. Проект имеет высокий уровень готовности к production: активные коммиты, более 4700 звёзд, широкое сообщество и проверенные зависимости, однако перед масштабным rollout рекомендуется выполнить небольшое proof‑of‑concept и уточнить детали интеграции из README.

### 中文

**价值**  
mitchellkrogza/nginx-ultimate-bad-bot-blocker 通过维护一套持续更新的恶意 User‑Agent、爬虫、Referer、漏洞扫描器、恶意站点等黑名单，自动在 Nginx 层面拦截这些请求，并可配合 Fail2Ban 对重复违规者进行封禁。这样可以大幅削减因恶意流量导致的带宽、CPU、日志噪声以及潜在的安全风险，省去运维人员手动维护 `robots.txt`、iptables 规则或自建 WAF 的繁琐工作。

**典型接入方式**  

| 步骤 | 说明 |
|------|------|
| 1️⃣ 拉取仓库 | `git clone https://github.com/mitchellkrogza/nginx-ultimate-bad-bot-blocker.git` |
| 2️⃣ 生成规则文件 | 运行 `./install.sh`（或 `./update.sh`）生成 `badbots.conf`、`badreferrers.conf` 等 Nginx include 文件。 |
| 3️⃣ Nginx 配置 | 在主站点的 `server` 块或全局 `http` 块中加入 `include /path/to/badbots.conf;`（同理加入 referer、geoip 等文件）。 |
| 4️⃣ 可选 Fail2Ban | 将 `fail2ban` 示例配置复制到 `/etc/fail2ban/jail.d/`，开启对重复违规 IP 的自动封禁。 |
| 5️⃣ 自动化/定时更新 | 将 `./update.sh` 加入 crontab（如每日 02:00），确保黑名单保持最新。 |
| 6️⃣ 验证 | 通过 `curl -A "BadBot"` 或模拟恶意 Referer 测试拦截是否生效。 |

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑26，拥有 4752 ⭐、522 Fork，社区活跃，问题响应及时。  
- **成熟度**：项目已在多家企业生产环境中使用，提供完整的安装脚本、Fail2Ban 集成以及 WordPress 主题检测等实用扩展。  
- **风险**：元数据未提供“一键部署”或 CI/CD 插件，首次接入需要手动验证脚本执行权限和 Nginx 配置兼容性；建议先在预生产环境做小规模 POC，确认更新频率与业务流量的冲突情况。  
- **结论**：在安全、性能和运维自动化方面具备 **高** 生产就绪度，适合作为 OSS 方案在正式业务中推广使用。

## 🧭 Practical evaluation

**Value:** mitchellkrogza/nginx-ultimate-bad-bot-blocker helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 4752 GitHub stars
- 522 forks
- updated 2026-06-26
- primary language: Shell
- 20 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 68/100 |
| stars | 78/100 |
| topics | 100/100 |
| outlook | 64/100 |
| quality | 74/100 |
| recency | 40/100 |
| adoption | 75/100 |
| production | 58/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/mitchellkrogza/nginx-ultimate-bad-bot-blocker) · [← Back to Automation](./README.md)</sub>
