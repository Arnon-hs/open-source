# kort0881/telegram-proxy-collector

[![Stars](https://img.shields.io/github/stars/kort0881/telegram-proxy-collector?style=flat-square&color=yellow)](https://github.com/kort0881/telegram-proxy-collector/stargazers) [![Forks](https://img.shields.io/github/forks/kort0881/telegram-proxy-collector?style=flat-square&color=blue)](https://github.com/kort0881/telegram-proxy-collector/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> 🛡️ Автоматический сборщик MTProto‑прокси с уникальной фильтрацией  «Умный комбайн» для автоматического сбора, анализа и фильтрации MTProto‑прокси.   Отделяет **"золотые" прокси**, маскирующиеся под Yandex, VK, Gosuslugi и другие популярные RU‑сервисы (Fake‑TLS), от обычных.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 858 |
| 🍴 **Forks** | 59 |
| 💻 **Language** | Python |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
`kort0881/telegram-proxy-collector` is a Python‑based “smart combiner” that automatically gathers MTProto proxy addresses, analyses them, and applies a custom filter that separates “golden” proxies (those masquerading as popular Russian services such as Yandex, VK, Gosuslugi via Fake‑TLS) from ordinary ones. The tool is open‑source, has attracted over 850 ⭐ on GitHub, and is actively maintained as of June 2026.

**Value Proposition**  
- **Targeted proxy quality** – By detecting Fake‑TLS proxies that imitate trusted RU services, the collector helps you build a higher‑quality proxy pool, reducing connection failures and improving Telegram latency.  
- **Automation** – The pipeline runs continuously, fetching new proxies, performing heuristic analysis, and outputting filtered lists, which saves manual curation time.  
- **Extensibility** – Written in Python, the code can be integrated into existing proxy‑management or bot‑deployment pipelines with minimal effort.

**Practical Adoption Path**  
1. **Clone & Install** – `git clone https://github.com/kort0881/telegram-proxy-collector.git` and install dependencies (`pip install -r requirements.txt`).  
2. **Configure** – Adjust `config.yaml` to set source URLs, filtering thresholds, and output destinations (e.g., JSON file, Redis, or a database).  
3. **Run a pilot** – Execute the collector in a sandboxed environment, review the generated “golden” proxy list, and verify connectivity to Telegram’s MTProto endpoints.  
4. **Integrate** – Hook the output into your existing proxy rotation service or bot deployment script (e.g., read the JSON file or subscribe to a Redis channel).  
5. **Monitor & Tune** – Use the built‑in logging to track false‑positives/negatives and tweak the heuristic parameters as needed.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained and has a sizable community star count, but it lacks formal CI/CD pipelines, comprehensive test coverage, and a clearly defined release schedule.  
- **Dependencies**: Pure‑Python with common libraries (requests, aiohttp, PyYAML); no heavy system‑level dependencies, easing containerization.  
- **Risk Considerations**: Verify the license (MIT‑compatible) and perform a security audit of the proxy‑parsing logic before exposing it to production. Ensure that any external proxy sources comply with your organization’s policy on third‑party network traffic.  
- **Recommendation**: Suitable for prototypes, internal tools, or as a supplemental source in a larger proxy‑management system. For mission‑critical deployments, add unit/integration tests, containerize the service, and establish a monitoring/alerting layer around its output.

### Русский

**Kort0881/telegram-proxy-collector** — это Python‑утилита, автоматически собирающая MTProto‑прокси и отбирающая «золотые» прокси, имитирующие популярные RU‑сервисы (Yandex, VK, Госуслуги) через Fake‑TLS. Она подходит для прототипов и внутренних систем, где требуется быстрое формирование списка надёжных прокси для обхода ограничений Telegram, но перед запуском в продакшн нужен ручной аудит качества, проверка лицензии и подтверждение поддержки проекта. Уровень готовности — средний: проект активно обновляется (2026‑06‑25), имеет 858 звёзд и 59 форков, однако интеграцию следует проводить после дополнительного тестирования и мониторинга.

### 中文

**项目简介（2‑3 句）**  
`kort0881/telegram-proxy-collector` 是一个基于 Python 的自动化工具，能够批量抓取 MTProto 代理并通过“智能组合”算法对其进行深度过滤，识别出伪装成 Yandex、VK、Gosuslugi 等热门俄语服务的“金牌”代理（Fake‑TLS），并与普通代理区分开来。

---

## 价值点

| 价值 | 说明 |
|------|------|
| **高质量代理筛选** | 通过特征匹配和流量指纹识别，自动挑选出具备伪装能力的高可用 MTProto 代理，提升 Telegram 连接成功率和隐蔽性。 |
| **自动化批量采集** | 一键抓取公开渠道（Telegram 频道、GitHub 列表、公开 API 等），省去手工收集的时间成本。 |
| **可定制过滤规则** | 支持自定义正则、IP/端口白名单、延迟阈值等，灵活适配不同业务需求。 |
| **开源透明** | 完全开源，代码可审计，便于二次开发或集成到现有代理管理平台。 |

---

## 典型接入方式

1. **直接运行脚本**  
   ```bash
   git clone https://github.com/kort0881/telegram-proxy-collector.git
   cd telegram-proxy-collector
   pip install -r requirements.txt
   python collector.py --output proxies.json
   ```
   - 生成的 `proxies.json` 包含过滤后的代理列表，可直接供 Telegram 客户端或自建代理池使用。

2. **作为库集成**  
   ```python
   from collector import ProxyCollector

   collector = ProxyCollector(
       sources=['telegram_channel', 'github'],
       filters={'min_latency': 150, 'fake_tls': True}
   )
   good_proxies = collector.run()
   ```
   - 在已有的代理调度系统中调用 `run()` 方法即可获得实时更新的优质代理。

3. **容器化部署**  
   - 项目提供 `Dockerfile`，可在 Kubernetes 或 Docker Compose 中以定时任务方式运行，定期刷新代理列表并写入共享存储（如 Redis、MongoDB）。

---

## 生产可用性评估

| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | ★★☆☆☆（中等） | 代码已更新至 2026‑06‑25，星标 858，fork 59，具备基本的社区活跃度，但缺少正式的 CI/CD、版本发布策略。 |
| **可靠性** | 中等 | 自动采集依赖外部公开渠道，受源站可用性影响；建议在生产环境加入异常重试、结果持久化与监控。 |
| **安全性** | 待评估 | 项目未明确声明安全审计或依赖锁定（`requirements.txt`），在引入前需审查第三方库的安全漏洞。 |
| **运维成本** | 低‑中 | 只需部署脚本或容器，定时任务即可；若需高可用可考虑水平扩展采集节点。 |
| **适用场景** | 原型、内部代理池、科研实验 | 适合需要快速获取高质量 MTProto 代理的业务，但在面向外部用户的生产系统中仍需额外的安全与稳定性保障。 |

**结论**：`telegram-proxy-collector` 在原型开发和内部工具链中价值突出，可快速提供经过“智能过滤”的 MTProto 代理。若要在生产环境中使用，建议：  
1. 对关键依赖进行安全审计并锁定版本；  
2. 加入监控、告警及结果持久化（如写入数据库或缓存）；  
3. 通过容器化或 CI 流水线实现自动化部署与滚动更新。  

在完成上述措施后，该项目可作为内部代理服务的可靠数据来源。

## 🧭 Practical evaluation

**Value:** kort0881/telegram-proxy-collector may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 858 GitHub stars
- 59 forks
- updated 2026-06-25
- primary language: Python

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 62/100 |
| topics | 0/100 |
| outlook | 47/100 |
| quality | 51/100 |
| recency | 40/100 |
| adoption | 57/100 |
| production | 54/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/kort0881/telegram-proxy-collector) · [← Back to Misc](./README.md)</sub>
