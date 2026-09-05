# chengaopan/AutoMergePublicNodes

[![Stars](https://img.shields.io/github/stars/chengaopan/AutoMergePublicNodes?style=flat-square&color=yellow)](https://github.com/chengaopan/AutoMergePublicNodes/stargazers) [![Forks](https://img.shields.io/github/forks/chengaopan/AutoMergePublicNodes?style=flat-square&color=blue)](https://github.com/chengaopan/AutoMergePublicNodes/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> 自动抓取合并互联网上的公开节点。 🚀 免费节点,🚀免费节点订阅,🚀v2ray免费节点,ssr免费节点订阅,clash免费节点订阅,免费梯子,免费翻墙,免费科学上网,免费ss/v2ray/trojan/clash节点,谷歌商店,翻墙梯子

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 7.7k |
| 🍴 **Forks** | 1.2k |
| 💻 **Language** | Python |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*AutoMergePublicNodes* is a Python tool that automatically crawls the web for publicly shared proxy/VPN nodes (V2Ray, SSR, Trojan, Clash, etc.) and merges them into unified subscription lists. It aims to provide users with continuously updated, free “scientific‑internet‑access” resources, packaging them in formats compatible with popular clients.

**Value**  
- **Time‑saving aggregation** – Instead of manually searching disparate forums, GitHub repos, or blogs for free node links, the script harvests and de‑duplicates them automatically.  
- **Ready‑to‑use subscriptions** – The merged output can be fed directly into Clash, V2Ray, or similar clients, giving end‑users immediate connectivity without configuration overhead.  
- **Community‑driven freshness** – Because the crawler runs on a schedule, the node list stays current, which is crucial for free services that are frequently taken down or blocked.

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Clone & review** the repository; inspect the `README` and configuration files to understand required inputs (e.g., source URLs, merge rules). | Guarantees the tool fits your environment and clarifies any required secrets or API keys. |
| 2️⃣  | **Run a sandbox test** on a non‑production server or container, using a limited set of source URLs. Verify that the generated subscription file is syntactically correct for your client (Clash, V2Ray, etc.). | Detects parsing errors, duplicate handling, or unexpected node formats before scaling. |
| 3️⃣  | **Integrate into CI/CD** – set up a scheduled GitHub Action, cron job, or Kubernetes CronJob that executes the script daily and pushes the resulting file to a secure storage bucket (e.g., S3, GCS) or a private Git repo. | Automates continuous updates while keeping the process observable and versioned. |
| 4️⃣  | **Deploy to clients** – point your fleet of proxy clients to the generated subscription URL or file path. Optionally add health‑checks that alert you if the list becomes empty or malformed. | Enables production use with minimal manual intervention. |
| 5️⃣  | **Monitor & audit** – log the sources used, node success rates, and any rate‑limit or captcha failures. Periodically audit the list for malicious or unstable nodes. | Maintains security hygiene and ensures the free‑node pool remains reliable. |

**Production Readiness**  
- **Activity & Adoption** – The project shows recent commits (as of 2026‑07‑02), a large community footprint (≈7.7 k stars, 1.2 k forks), and active forking, indicating healthy interest.  
- **Technical maturity** – Core functionality (crawling, merging, output formatting) is stable; the codebase is primarily Python, a language with mature packaging and deployment tooling.  
- **Risk considerations** – While no immediate licensing or security red flags appear, the free‑node ecosystem is inherently volatile and may contain malicious or throttled endpoints. A manual security review and runtime sandboxing are recommended before exposing the merged list to production traffic.  
- **Readiness level** – Given the strong community signals and recent maintenance, the project is **production‑ready for pilot deployments** provided you implement the above testing, monitoring, and security‑review steps.

### Русский

Резюме проекта chengaopan/AutoMergePublicNodes:

Проект предлагает автоматизированную сборку и объединение бесплатных интернет-ресурсов для обхода блокировок и доступа к заблокированным контентам. Он может быть полезен в сценариях, когда требуется быстрый и надежный доступ к интернет-ресурсам без оплаты. Проект готов к внедрению в производственную среду, поскольку имеет сильные сигналы активности, адопции и экосистемы, но требует тщательного обзора и проверки лицензии, безопасности и активных поддерживающих разработчиков.

### 中文

**项目简介**

chengaopan/AutoMergePublicNodes 是一个开源项目，旨在自动抓取和合并互联网上的公开节点，提供免费的节点订阅、V2Ray节点、SSR节点订阅、Clash节点订阅等服务。🚀

**价值**

chengaopan/AutoMergePublicNodes 的价值在于其可以帮助用户找到和使用免费的互联网节点，方便科学上网、翻墙等需求。

**典型接入方式**

由于该项目提供了 Python 语言的实现，因此用户可以根据自己的需求选择直接使用该项目的 API 或者结合其他工具和框架进行集成。具体接入方式可能需要根据项目的 README 文档进行配置和调整。

**生产可用性**

该项目具有很高的生产可用性，因为其最近的活动、采用率和生态信号都强劲，因此适合于严肃的试验或生产环境中使用。

## 🧭 Practical evaluation

**Value:** chengaopan/AutoMergePublicNodes may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 7692 GitHub stars
- 1238 forks
- updated 2026-07-02
- primary language: Python

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 77/100 |
| stars | 83/100 |
| topics | 0/100 |
| outlook | 67/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 81/100 |
| production | 69/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/chengaopan/AutoMergePublicNodes) · [← Back to Misc](./README.md)</sub>
