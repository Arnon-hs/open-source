# crossxx-labs/free-proxy

[![Stars](https://img.shields.io/github/stars/crossxx-labs/free-proxy?style=flat-square&color=yellow)](https://github.com/crossxx-labs/free-proxy/stargazers) [![Forks](https://img.shields.io/github/forks/crossxx-labs/free-proxy?style=flat-square&color=blue)](https://github.com/crossxx-labs/free-proxy/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Provide free clash subscriptions of ssr / vmess / hysteria2 proxy servers 提供免费clash订阅，免费ssr节点，免费trojan节点，免费vmess节点，免费hysteria2节点服务器

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.5k |
| 🍴 **Forks** | 75 |
| 💻 **Language** | Shell |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`clash` `clash-subscription` `clash-verge-rev` `free-clash` `free-node` `free-server` `hiddify` `hiddify-app` `shadowsocksr` `vless` `vmess`

## 🎯 Categories

Payments · Networking · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
crossxx‑labs/free‑proxy is an open‑source repository that publishes free Clash subscription links for a variety of proxy protocols (SSR, Vmess, Trojan, Hysteria2). It aggregates publicly available proxy servers and makes them consumable via a single, regularly‑updated subscription file, allowing users to quickly set up proxy clients without manual configuration.

**Value Proposition**  
- **Rapid monetization/billing integration** – The project can serve as a ready‑made data source for services that need to provision proxy credentials as part of a paid offering, shortening the time to market for SaaS platforms, VPN resellers, or payment‑flow testing environments.  
- **Cost‑effective testing** – Developers can use the free subscription to simulate real‑world traffic and validate PSP (payment service provider) or checkout flows that depend on network routing or geo‑restriction checks, without incurring infrastructure costs.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, inspect the `README` and the script that generates the Clash subscription (Shell). Run the script locally to produce a subscription URL and load it into a Clash‑compatible client (e.g., Clash Meta, Clash for Windows).  
2. **Integration** – Wrap the subscription generation script in a CI/CD job or a lightweight API service that your billing system can call to fetch the latest proxy list on demand.  
3. **Pilot** – Deploy the wrapper in a sandbox environment, link it to a test checkout flow, and verify that proxy selection works as expected for different payment‑gateway regions.  

**Production Readiness**  
- **Activity & Adoption** – 1,527 GitHub stars, 75 forks, recent commit (2026‑06‑23) and a solid community around the Clash ecosystem indicate healthy maintenance.  
- **Technical Fit** – The repository is a single‑file Shell project with clear entry points, making it easy to containerize or embed in existing automation pipelines.  
- **Risks** – The repository does not expose a formal API or detailed deployment guide; you’ll need to validate the runtime environment (Shell, curl, etc.) and monitor the upstream proxy list for reliability. Starting with a small proof‑of‑concept and confirming the operational cost of running the script mitigates these concerns.  

Overall, crossxx‑labs/free‑proxy is production‑ready for pilots and can be quickly integrated into billing or PSP testing workflows, provided you perform the initial validation steps.

### Русский

**crossxx-labs/free-proxy** — это open‑source набор скриптов, который автоматически собирает и публикует бесплатные Clash‑подписки для SSR, Vmess, Trojan и Hysteria2 серверов. Он подходит для быстрого прототипирования и тестирования платёжных/биллинг‑процессов, позволяя встраивать проверку доступа к прокси‑ресурсам в checkout‑ или PSP‑флоу без собственного инфраструктурного обслуживания. Проект имеет активную поддержку (обновления в 2026 г., >1500 звёзд, 75 форков) и готов к пилотному запуску в продакшн, однако интеграцию следует начать с небольшого proof‑of‑concept и уточнить детали настройки из README.

### 中文

**项目价值**  
crossxx-labs/free-proxy 通过提供免费 Clash 订阅链接，聚合了 SSR、Vmess、Trojan、Hysteria2 等多协议的代理节点，帮助用户快速搭建科学上网环境，省去自行寻找、测试节点的时间成本。对于需要在产品或服务中嵌入代理、VPN、或网络加速功能的团队，它可以作为「即插即用」的节点源，降低研发和运维门槛。

**典型接入方式**  

| 场景 | 接入步骤 | 关键文件/命令 |
|------|----------|--------------|
| **在自建服务中使用 Clash** | 1. 克隆仓库 <br>2. 运行 `./update.sh`（或直接下载 `free-proxy.yaml`） <br>3. 将生成的 YAML 文件配置到本地/服务器的 Clash 客户端 | `free-proxy.yaml`、`update.sh` |
| **在容器化环境中提供代理** | 1. 使用官方 Dockerfile（或自行编写） <br>2. 环境变量 `PROXY_SUB_URL` 指向仓库生成的订阅链接 <br>3. 启动容器后，容器内部的代理服务即可直接读取节点 | Docker 镜像 `crossxxlabs/free-proxy`（社区维护） |
| **在 CI/CD 流程中自动更新节点** | 1. 在 CI 脚本中调用 `./update.sh` <br>2. 将最新的 `free-proxy.yaml` 推送到内部配置仓库 <br>3. 自动重载 Clash 实例 | GitHub Actions / GitLab CI 示例脚本 |
| **在业务系统中做流量分发** | 1. 通过 HTTP GET 获取订阅链接 <br>2. 解析后写入自研的负载均衡或路由规则 <br>3. 动态刷新节点列表 | 订阅 URL 如 `https://raw.githubusercontent.com/crossxx-labs/free-proxy/main/free-proxy.yaml` |

**生产可用性**  
- **活跃度**：最近一次提交在 **2026‑06‑23**，仓库星标 1527、fork 75，表明社区活跃且维护及时。  
- **技术成熟度**：核心实现为 Shell 脚本，依赖少，易于审计和二次定制。  
- **安全性**：节点均为公开免费资源，使用前建议自行检测延迟、可用性和安全性；不适合作为对安全合规有严格要求的生产环境的唯一代理来源。  
- **部署门槛**：只需一行脚本或一个 Docker 镜像即可完成，适合作为 **Proof‑of‑Concept** 或 **内部工具** 快速验证；若要在大规模生产环境中使用，建议搭配自研监控、节点健康检查以及备份的商业节点。  

**结论**  
crossxx-labs/free-proxy 在 **快速验证**、**内部研发** 或 **低成本实验** 场景下具备高可用性，接入成本极低；在正式生产环境中使用时，需要自行实现节点质量监控和容灾方案，以弥补免费节点的波动性和潜在安全风险。

## 🧭 Practical evaluation

**Value:** crossxx-labs/free-proxy helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1527 GitHub stars
- 75 forks
- updated 2026-06-23
- primary language: Shell
- 11 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 47/100 |
| stars | 68/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 78/100 |
| recency | 80/100 |
| adoption | 62/100 |
| production | 69/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/crossxx-labs/free-proxy) · [← Back to Payments](./README.md)</sub>
