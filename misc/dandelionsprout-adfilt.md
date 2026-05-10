# DandelionSprout/adfilt

[![Stars](https://img.shields.io/github/stars/DandelionSprout/adfilt?style=flat-square&color=yellow)](https://github.com/DandelionSprout/adfilt/stargazers) [![Forks](https://img.shields.io/github/forks/DandelionSprout/adfilt?style=flat-square&color=blue)](https://github.com/DandelionSprout/adfilt/network) [![Language](https://img.shields.io/badge/lang-Adblock%20Filter%20List-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> The place where I, DandelionSprout, store my web filter lists for countless topics, including my Nordic adblock list. As simple as that, really.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.1k |
| 🍴 **Forks** | 179 |
| 💻 **Language** | Adblock Filter List |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-05-10 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ad-blocker` `adblock` `adblock-plus` `adblocking` `adguard` `brave-browser` `filterlist` `firefox` `hosts` `hosts-file` `hostsfile` `json`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
DandelionSprout/adfilt is a public repository that houses a collection of web‑filter lists authored by DandelionSprout, most notably a Nordic‑focused ad‑blocking list. The project is essentially a curated set of plain‑text filter rules that can be dropped into any ad‑blocking or content‑filtering solution that supports the Adblock Filter List format.

**Value**  
- **Ready‑made, high‑quality filter rules** for a wide range of topics (including region‑specific ad‑blocking) that save you the effort of building and maintaining your own lists.  
- **Broad community adoption** – the repo has >2 k stars and dozens of forks, indicating that many users already rely on it for privacy and performance gains.  
- **Simple integration** – the lists are plain text files, so they can be consumed by any compatible blocker (uBlock Origin, AdGuard, Pi‑hole, etc.) without code changes.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – clone the repo and point a test instance of your blocker (e.g., a local uBlock Origin profile or a Pi‑hole container) at the desired list URL. Verify that the expected requests are being blocked and that there are no false positives.  
2. **Readme review** – the repository’s README contains usage instructions and a list of topics; confirm that the list format and update cadence match your operational requirements.  
3. **Automation** – add the list URL to your production blocker configuration and set up a scheduled fetch (most blockers already support auto‑updates).  
4. **Monitoring** – enable logging or use the blocker’s dashboard to track hit rates and any breakages; adjust or whitelist as needed.

**Production Readiness**  
- **Activity**: Last commit on 2026‑05‑10, indicating active maintenance.  
- **Community signals**: 2 126 stars, 179 forks, and usage across multiple ad‑blocking ecosystems demonstrate real‑world validation.  
- **Stability**: The lists are static text files; integration risk is low, and updates are incremental and backward‑compatible.  
- **Risk mitigation**: The only uncertainty is the integration path (e.g., how to fetch the lists in your CI/CD pipeline); a small pilot can quantify any setup overhead before full rollout.

Overall, DandelionSprout/adfilt is a production‑ready, low‑cost asset for any organization or individual looking to enhance web filtering with community‑vetted rules. A short pilot followed by standard blocker configuration should be sufficient to bring it into a stable production environment.

### Русский

**DandelionSprout/adfilt** — открытый репозиторий с готовыми списками фильтрации (Adblock‑style), включая обширный нордический ad‑block лист, который можно сразу подключить к браузеру, DNS‑блокировщику или прокси‑фильтру. Типичный сценарий внедрения — добавить нужный список в конфигурацию вашего блокирующего решения (например, uBlock Origin, Pi‑hole или AdGuard) после быстрой проверки README и тестового запуска на небольшом наборе запросов. Проект обладает высокой готовностью к production: активные коммиты, более 2000 звёзд, регулярные обновления и широкое использование в сообществе, что делает его надёжным кандидатом для пилотного внедрения.

### 中文

**项目价值**  
DandelionSprout/adfilt 是 DandelionSprout 维护的多主题网页过滤规则仓库，核心包括一套针对北欧地区的广告拦截列表。它提供了即插即用的 Adblock‑compatible 过滤规则，可直接用于常见的浏览器扩展（如 uBlock Origin、AdGuard）或企业级代理/网关，实现对广告、追踪脚本以及特定内容的精准拦截。

**典型接入方式**  

| 场景 | 步骤 | 关键点 |
|------|------|--------|
| **个人浏览器** | 1. 在浏览器扩展（uBlock Origin / AdGuard 等）中打开“过滤列表”设置。<br>2. 添加自定义列表 URL：`https://raw.githubusercontent.com/DandelionSprout/adfilt/master/<list‑name>.txt`。<br>3. 启用并刷新页面。 | 列表是标准的 Adblock 语法，无需额外转换。 |
| **企业代理（Squid / Nginx）** | 1. 下载所需列表（`curl -O …`）。<br>2. 配置代理的 URL 重写或响应过滤模块（如 `squidGuard`、`ngx_http_sub_module`），使用正则/规则匹配列表条目。<br>3. 定时任务（cron）自动同步更新（`git pull` 或 `curl -s … > list.txt`）。 | 需要将 Adblock 规则转换为代理支持的匹配语法，常见工具有 `adblock2squid`、`adblock2nginx`。 |
| **CI/CD 自动化** | 1. 在项目的 `Dockerfile` 或 CI 脚本中 `ADD` 或 `COPY` 过滤列表。<br>2. 构建镜像时将列表合并到容器内的拦截模块（如 `pihole` 的 `gravity.list`）。 | 适合微服务或容器化部署的统一拦截策略。 |

**生产可用性**  
- **活跃度**：最近一次提交为 2026‑05‑10，星标 2126、fork 179，社区关注度高。  
- **成熟度**：列表遵循标准 Adblock 语法，已在多数主流拦截插件中直接使用，兼容性好。  
- **风险**：元数据未提供统一的接入文档，首次集成时需要自行确认列表名称与业务需求匹配；建议先在测试环境做小规模验证（例如只启用北欧广告列表），确认误杀率后再推广。  
- **结论**：在明确过滤需求且能够接受少量初始调试成本的场景下，adfilt 完全具备生产级别的可用性，适合作为 OSS 过滤规则的首选来源之一。

## 🧭 Practical evaluation

**Value:** DandelionSprout/adfilt may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2126 GitHub stars
- 179 forks
- updated 2026-05-10
- primary language: Adblock Filter List
- 18 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 71/100 |
| topics | 100/100 |
| outlook | 80/100 |
| quality | 85/100 |
| recency | 100/100 |
| adoption | 67/100 |
| production | 76/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-10 · [View on GitHub](https://github.com/DandelionSprout/adfilt) · [← Back to Misc](./README.md)</sub>
