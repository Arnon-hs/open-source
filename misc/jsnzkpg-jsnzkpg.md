# Jsnzkpg/Jsnzkpg

[![Stars](https://img.shields.io/github/stars/Jsnzkpg/Jsnzkpg?style=flat-square&color=yellow)](https://github.com/Jsnzkpg/Jsnzkpg/stargazers) [![Forks](https://img.shields.io/github/forks/Jsnzkpg/Jsnzkpg?style=flat-square&color=blue)](https://github.com/Jsnzkpg/Jsnzkpg/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> 已持续维护5年多，每天都会检测可用性，全网质量最高的免费节点订阅，魔鬼式筛选出高质量的免费节点，shadowrocket丨stash丨singbox丨clash丨karing丨hiddify丨mihomo丨clashmi丨ClashMeta丨FIClash丨Surfboard

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.7k |
| 🍴 **Forks** | 359 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
Jsnzkpg/Jsnzkpg is a five‑year‑old, actively maintained JavaScript project that scrapes the Internet for free proxy/VPN nodes, filters them with strict quality criteria, and republishes the best‑performing subscriptions for clients such as Shadowrocket, Clash, Sing‑Box, and many others. With over 3,700 GitHub stars and recent updates, it claims to deliver the “highest‑quality free node list” across a wide range of proxy platforms.  

**Value**  
- **Free, high‑quality proxy lists** – the tool continuously checks node availability and discards unreliable or slow entries, saving users the effort of manual testing.  
- **Multi‑client compatibility** – output formats are ready for popular iOS/Android and desktop clients (Shadowrocket, Stash, Sing‑Box, Clash, Hiddify, Mihomo, etc.), making it a one‑stop source for diverse environments.  
- **Open‑source transparency** – the filtering logic is visible and can be audited or customized to suit specific security or performance policies.  

**Practical Adoption Path**  
1. **Review the repository** – clone the repo, read the README and inspect the `config`/filter scripts to understand how nodes are fetched and scored.  
2. **Run a local test** – execute the provided script (usually `npm install && npm start` or similar) and generate a subscription file.  
3. **Validate the output** – import the generated URL into a client (e.g., Clash) and run a quick connectivity test on a handful of nodes.  
4. **Customize if needed** – adjust filtering thresholds, add or remove source URLs, or integrate the script into your CI pipeline for periodic updates.  
5. **Deploy** – host the generated subscription on a reliable static site or a small serverless function, and distribute the URL to your users or internal services.  

**Production Readiness**  
- **Maturity**: The project shows a healthy star count (≈3.7 k) and regular commits, indicating a stable codebase.  
- **Risk**: Integration points are not explicitly documented; you’ll need to verify the build process and ensure the generated subscription format matches your client versions.  
- **Readiness Level**: **Medium** – suitable for prototypes, internal tooling, or environments where a free proxy list is acceptable, but it requires a validation step and possibly a wrapper to handle updates and error handling before being used in a production‑critical service.  

**Bottom Line**  
If you need a continuously refreshed, free proxy subscription and are comfortable performing a brief integration test, Jsnzkpg/Jsnzkpg can be a cost‑effective component of your network tooling. For mission‑critical deployments, treat it as a supplemental source and add monitoring/fallback mechanisms to mitigate the inherent volatility of free proxy nodes.

### Русский

Jsnzkpg/Jsnzkpg — это открытый проект, который уже более пяти лет ежедневно собирает и тщательно отбирает бесплатные прокси‑узлы‑подписки (Shadowrocket, Stash, Sing‑Box, Clash, Karing, Hiddify, Mihomo, ClashMeta, FIClash, Surfboard и др.), обеспечивая самым высоким в сети качеством доступа. Подходит для быстрого прототипирования или внутреннего использования в системах, где требуется динамический набор надёжных бесплатных узлов, но перед выводом в продакшн необходимо вручную проверить конфигурацию и убедиться в совместимости с вашими инструментами. Готовность к production — средняя: проект активно поддерживается (обновление 2026‑06‑27), имеет большую пользовательскую базу (3712 ★), однако путь интеграции не документирован и требует дополнительного тестирования.

### 中文

**项目简介（2‑3 句）**  
Jsnzkpg 是一个已连续维护 5 年以上的免费节点订阅库，项目每日自动检测节点可用性并进行“魔鬼式”筛选，提供全网质量最高的免费节点列表，兼容 Shadowrocket、Stash、Sing‑Box、Clash、Karing、Hiddify、MiHoMo、ClashMeta、FIClash、Surfboard 等多种客户端。

**价值**  
- **高质量、实时可用**：每日自动探测并剔除失效节点，确保订阅中的节点始终保持在线率和速度。  
- **多平台兼容**：一次订阅即可在主流 iOS、Android、Windows、Linux 客户端上直接使用，省去手动搜集和测试节点的时间成本。  
- **社区活跃、开源透明**：拥有 3700+ 星、350+ Fork，代码公开，便于自行审计或二次定制。

**典型接入方式**  
1. **获取订阅链接**：在项目 README 或 Releases 页面复制 `https://raw.githubusercontent.com/Jsnzkpg/Jsnzkpg/main/subscription.txt`（示例），也可通过 API 拉取 JSON。  
2. **在客户端中添加**：在 Shadowrocket、Clash‑Meta、Sing‑Box 等客户端的「订阅」或「配置」页面粘贴链接，保存并手动或设置定时刷新。  
3. **可选自定义**：如需过滤特定协议或地区，可在本地使用 `jq`、`sed` 等工具对原始订阅进行二次处理后再导入。  

**生产可用性**  
- **成熟度**：项目已连续更新 5 年，活跃度高，代码质量和测试覆盖尚未完整公开，建议在正式环境前进行一次完整的功能验证（节点连通性、延迟、带宽等）。  
- **适用场景**：适合内部研发、原型验证或对成本敏感的业务场景；若对 SLA 有严格要求，建议在生产环境中配合自建节点或商业 CDN 进行冗余备份。  
- **风险与注意事项**：  
  - 订阅路径和节点协议可能随时变动，需定期监控更新。  
  - 项目未提供官方的容错或热备方案，部署时应自行实现节点健康检查和自动切换。  
  - 受限于免费资源，流量和速率可能不稳定，务必做好流量监控和限速策略。  

综上，Jsnzkpg 可作为快速获取高质量免费节点的便捷入口，适合原型和内部工具使用；在生产环境使用时，请做好额外的监控、容错和备份措施，以确保服务的可靠性。

## 🧭 Practical evaluation

**Value:** Jsnzkpg/Jsnzkpg may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 3712 GitHub stars
- 359 forks
- updated 2026-06-27
- primary language: JavaScript

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 64/100 |
| stars | 76/100 |
| topics | 0/100 |
| outlook | 65/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 73/100 |
| production | 65/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/Jsnzkpg/Jsnzkpg) · [← Back to Misc](./README.md)</sub>
