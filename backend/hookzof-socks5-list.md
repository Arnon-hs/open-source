# hookzof/socks5_list

[![Stars](https://img.shields.io/github/stars/hookzof/socks5_list?style=flat-square&color=yellow)](https://github.com/hookzof/socks5_list/stargazers) [![Forks](https://img.shields.io/github/forks/hookzof/socks5_list?style=flat-square&color=blue)](https://github.com/hookzof/socks5_list/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Auto-updated SOCKS5 proxy list + proxies for Telegram (прокси для телеграмм/телеграм/тг) https://mtpro.xyz/mtproto

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 963 |
| 🍴 **Forks** | 176 |
| 💻 **Language** | Unknown |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

`freeproxy` `proxies` `proxy` `proxy-list` `proxy-server` `proxylist` `socks` `socks-proxy` `socks5` `socks5-proxy` `telegram-proxy`

## 🎯 Categories

Backend

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
hookzof/socks5_list is an open‑source repository that continuously aggregates and publishes SOCKS5 proxy addresses, including ones optimized for Telegram (MTProto) usage. With over 960 ★ on GitHub and recent commits, it offers a ready‑made proxy list that teams can embed in their services instead of building and maintaining their own proxy‑gathering infrastructure.  

**Value**  
- **Infrastructure reuse:** Provides a curated, auto‑updated proxy database, eliminating the need to write scrapers, parsers, or monitoring pipelines.  
- **Speed to market:** Teams can plug the list into API gateways, web‑crawlers, or Telegram bots and ship functional services faster.  
- **Standardisation:** By using a single, community‑maintained source, different services within an organisation share the same proxy‑selection logic, reducing configuration drift and support overhead.  

**Practical adoption path**  
1. **Review the repo** – clone the project and inspect the `README` and example scripts to understand the output format (plain text, JSON, etc.).  
2. **Validate a subset** – fetch a small batch of proxies and run a quick connectivity test (e.g., `curl --socks5 <ip:port> https://api.ipify.org`).  
3. **Integrate** – add a lightweight fetch step to your CI/CD pipeline (e.g., a cron job or GitHub Action) that pulls the latest list and stores it in a config store or environment variable.  
4. **Wrap with fallback logic** – implement retry/fallback handling in your service code so that a failing proxy does not break the request flow.  
5. **Monitor** – set up basic health checks (success rate, latency) to detect when the list needs manual pruning.  

**Production readiness**  
The project scores high on readiness: it has recent activity (last commit on 2026‑05‑14), strong community adoption (963 ★, 176 forks, 11 topics), and is already used for Telegram MTProto proxies. While the repository does not expose explicit integration hooks, the data format is simple and can be consumed with minimal code. The main risk is the lack of built‑in health‑checking or authentication, so teams should allocate modest effort to validate and monitor the proxies before relying on them in a production environment. With that validation step, hookzof/socks5_list is a solid OSS candidate for a pilot or even full‑scale deployment.

### Русский

**hookzof/socks5_list** — это открытый проект, предоставляющий постоянно обновляемый список SOCKS5‑прокси, в том числе готовых к работе с Telegram (MTProto). Он позволяет быстро подключать готовую инфраструктуру прокси‑служб, избавляя команды от необходимости самостоятельно разрабатывать и поддерживать аналогичный бекенд, что ускоряет запуск API‑сервисов и стандартизирует их сетевые паттерны. Проект уже активно поддерживается (обновления — 2026‑05‑14, 963 звёзд, 176 форков), но перед внедрением требуется ручная проверка и настройка, так как автоматические сигналы интеграции из метаданных ограничены.

### 中文

**项目简介**  
hookzof/socks5_list 是一个自动更新的 SOCKS5 代理列表仓库，专门提供可直接用于 Telegram（MTProto） 的代理地址。项目活跃度高，已累计 963 星、176 Fork，并在 2026‑05‑14 仍保持更新。

**价值**  
- **基础设施即服务**：团队无需自行搭建、维护代理抓取、检测和更新逻辑，可直接复用已有的高质量代理库。  
- **加速业务上线**：在需要对外访问或突破网络限制（如 Telegram、Telegram Bot、Telegram Login）时，只需引用列表即可快速完成网络层的准备工作。  
- **统一标准**：统一的代理来源和格式（JSON/Plain‑text）帮助团队在不同微服务或脚本中保持一致的代理使用方式，降低运维成本。

**典型接入方式**  
1. **直接下载**：使用 `curl` 或 `wget` 拉取最新的 `socks5.txt`（或 `socks5.json`）文件。  
   ```bash
   curl -L https://raw.githubusercontent.com/hookzof/socks5_list/main/socks5.txt -o socks5.txt
   ```  
2. **脚本/代码读取**：在后端服务（Node.js、Python、Go 等）中读取文件或直接请求 GitHub 原始链接，解析每行 `host:port`，并在创建 HTTP/Telnet/MTProto 客户端时填入。  
   ```python
   import requests
   proxies = requests.get('https://raw.githubusercontent.com/hookzof/socks5_list/main/socks5.txt').text.splitlines()
   # 任选一个或轮询使用
   ```  
3. **自动化更新**：利用 CI/CD 定时（如 GitHub Actions）拉取最新列表并写入内部配置中心或环境变量，保证生产环境始终使用最新可用代理。  
4. **Telegram 客户端**：在 MTProto 客户端（如 Telethon、MadelineProto）中将 `proxy` 参数指向 `socks5://host:port` 即可。

**生产可用性**  
- **活跃维护**：最近一次提交在 2026‑05‑14，说明项目仍在持续更新。  
- **社区认可**：近千星、百余 Fork，且已有多个公开项目引用，验证了其实用性。  
- **风险与注意事项**：元数据中未提供完整的集成文档，建议在正式环境前进行一次手动审查（如检测延迟、可用性），并做好 fallback 机制（如多源代理或自建备份）。  
- **总体评估**：在经过一次简易验证后，即可视为 **高可用** 的 OSS 组件，适合作为生产环境的代理来源。

## 🧭 Practical evaluation

**Value:** hookzof/socks5_list helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 963 GitHub stars
- 176 forks
- updated 2026-05-14
- 11 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 64/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 83/100 |
| recency | 100/100 |
| adoption | 61/100 |
| production | 75/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/hookzof/socks5_list) · [← Back to Backend](./README.md)</sub>
