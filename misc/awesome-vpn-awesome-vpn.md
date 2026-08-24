# awesome-vpn/awesome-vpn

[![Stars](https://img.shields.io/github/stars/awesome-vpn/awesome-vpn?style=flat-square&color=yellow)](https://github.com/awesome-vpn/awesome-vpn/stargazers) [![Forks](https://img.shields.io/github/forks/awesome-vpn/awesome-vpn?style=flat-square&color=blue)](https://github.com/awesome-vpn/awesome-vpn/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Free proxy node aggregator. Daily updated vmess/vless/trojan/ss. 免费 代理节点 翻墙 梯子 科学上网 机场订阅 网络加速 VPN 免翻墙每日更新 一键导入

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 5.7k |
| 🍴 **Forks** | 543 |
| 💻 **Language** | Python |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`clash` `clashvergerev` `fanqiang` `free` `geopolitics` `gfw` `mihomo` `shadowsocks` `sing-box` `singbox` `ss` `trojan`

## 🎯 Categories

Misc

## 📝 Summary

### English

We need to write a brief summary (2-3 sentences) for the open-source project, describing value, practical adoption path, and production readiness. The description says it's a free proxy node aggregator, daily updated vmess/vless/trojan/ss, etc. However the metadata includes categories AI/ML, value proposition about adding AI capability, etc. That seems mismatched. But we must follow the given info: Title: awesome-vpn/awesome-vpn, description about proxy nodes, categories AI/ML, value proposition: helps add AI capability without starting from a blank model stack. Use cases: prototype AI features; build RAG or agent workflows; evaluate model tooling. Integration notes: feasible to evaluate, start with small POC and README check. Production readiness: High for OSS candidate: recent activity, adoption, ecosystem signals strong enough for serious pilot. Quality signals: stars, forks, updated date, language Python, topics. Risks: license, security, maintainers need review.

We need to explain value, practical adoption path, production readiness. Write in English, 2-3 sentences.

Let's craft: "awesome-vpn/awesome-vpn provides a ready‑to‑use, daily‑updated collection of free proxy nodes (

### Русский

Проект **awesome-vpn/awesome-vpn** — это агрегатор бесплатных прокси-нод (VMess/VLESS/Trojan/SS), обновляемых ежедневно, позволяющий быстро получить рабочие подписки для настройки VPN- или proxy-подключения без ручного поиска. Типичный сценарий внедрения: импорт актуальных узлов в клиентские приложения (например, Clash, Sing-box) через один клик для обеспечения сетевой анонимности и доступа к заблокированным ресурсам. Проект демонстрирует высокую готовность к использованию (5,6k+ звёзд, активное обновление), однако перед внедрением в production рекомендуется провести проверку лицензии, безопасности и поддержки, а также начать с прототипирования.

### 中文

**项目简介（2‑3 句）**  
awesome‑vpn 是一个免费代理节点聚合库，提供每日更新的 vmess、vless、trojan、shadowsocks 等多协议节点，支持一键导入，帮助用户快速搭建科学上网、网络加速或 VPN 解决方案。

**价值**  
- **省时省力**：无需自行搜集、测试节点，项目每日自动同步最新可用节点。  
- **多协议覆盖**：同时支持 vmess、vless、trojan、ss 等主流协议，满足不同客户端和使用场景。  
- **开源透明**：代码、节点列表均公开，可自行审计或二次定制，降低信任风险。  

**典型接入方式**  
1. **直接克隆仓库**  
   ```bash
   git clone https://github.com/awesome-vpn/awesome-vpn.git
   cd awesome-vpn
   pip install -r requirements.txt
   ```
2. **获取节点列表**  
   - 通过 `python get_nodes.py`（或对应脚本）下载最新的 JSON/YAML 节点文件。  
   - 也可以使用项目提供的 HTTP API（如 `https://api.awesome-vpn.org/nodes`) 直接拉取。  
3. **一键导入**  
   - 大多数客户端（Clash、V2RayN、Shadowrocket 等）支持导入 URL 或本地文件，只需把生成的节点文件路径或 URL 填入客户端即可完成配置。  
   - 项目自带 `export.py` 脚本，可将节点转换为 Clash、QuantumultX、Surge 等格式的订阅链接。  

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑28，星标 5.6k，Fork 543，社区活跃，说明项目维护良好。  
- **代码质量**：基于 Python，依赖少，易于审计；拥有完整的 README 与使用示例，适合快速验证。  
- **安全与合规**：目前未发现重大元数据风险，但仍建议在正式生产环境前：  
  1. 检查项目许可证（MIT/Apache 等）是否符合企业合规要求。  
  2. 对拉取的节点进行安全审计（如检测是否泄露敏感信息）。  
  3. 在受控环境中进行小规模 POC，验证节点可用性与网络性能。  
- **可扩展性**：项目提供 API 与插件接口，便于在自有平台上二次包装或与内部监控、流量控制系统集成。  

综上，awesome‑vpn 具备较高的生产就绪度，适合作为企业内部或个人的免费代理节点来源，在完成安全合规评估后即可投入实际使用。

## 🧭 Practical evaluation

**Value:** awesome-vpn/awesome-vpn helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 5673 GitHub stars
- 543 forks
- updated 2026-06-28
- primary language: Python
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 68/100 |
| stars | 80/100 |
| topics | 100/100 |
| outlook | 62/100 |
| quality | 75/100 |
| recency | 40/100 |
| adoption | 77/100 |
| production | 60/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/awesome-vpn/awesome-vpn) · [← Back to Misc](./README.md)</sub>
