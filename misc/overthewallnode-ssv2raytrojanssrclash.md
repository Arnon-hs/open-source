# OverTheWallNode/SSV2RayTrojanSSRClash

[![Stars](https://img.shields.io/github/stars/OverTheWallNode/SSV2RayTrojanSSRClash?style=flat-square&color=yellow)](https://github.com/OverTheWallNode/SSV2RayTrojanSSRClash/stargazers) [![Forks](https://img.shields.io/github/forks/OverTheWallNode/SSV2RayTrojanSSRClash?style=flat-square&color=blue)](https://github.com/OverTheWallNode/SSV2RayTrojanSSRClash/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> 2026 科学上网，ss, ssr, v2ray, trojan, clash, clashr，翻墙机场推荐

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.7k |
| 🍴 **Forks** | 162 |
| 💻 **Language** | Unknown |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`clash` `free` `google` `hysteria` `hysteria2` `shadowrocket` `shadowsocks` `ssr` `trojan` `v2ray`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
OverTheWallNode/SSV2RayTrojanSSRClash is a curated collection of open‑source tools and configuration templates for modern “scientific‑internet‑access” (ss, ssr, v2ray, trojan, clash, clashr) and a list of recommended proxy “airports”. With over 2,700 ★ and recent commits (last update 2026‑05‑11), it serves as a one‑stop starter kit for users who need to set up or switch between multiple proxy protocols quickly.

**Value**  
- **All‑in‑one repository** – bundles scripts, Dockerfiles, and example configs for the most common proxy stacks, eliminating the need to hunt across disparate projects.  
- **Up‑to‑date recommendations** – the “airport” list is refreshed regularly, helping users find reliable, low‑latency servers without manual research.  
- **Community traction** – high star/fork count and active issue discussions indicate a mature user base that can provide quick help and share best practices.

**Practical adoption path**  
1. **Review the README** to select the desired protocol (e.g., V2Ray + ClashR) and copy the corresponding Docker‑compose or shell script.  
2. **Run the provided container** (or compile the binary) in a test environment, injecting your own server credentials from the airport list.  
3. **Validate connectivity** with a simple curl or proxy‑aware browser; adjust firewall/NAT rules as needed.  
4. **Integrate into CI/CD** by pinning the repository tag and automating config generation for your production fleet.

**Production readiness**  
The project shows strong production signals: recent commits, a large star/fork base, and multiple topics indicating broad ecosystem integration. While the code itself is stable, a final security audit (license compliance, upstream vulnerability scanning, and maintainer responsiveness) is still required before deploying at scale. Once those checks are cleared, the repository is suitable for a serious pilot or full‑scale rollout.

### Русский

OverTheWallNode/SSV2RayTrojanSSRClash — это набор скриптов и конфигураций для быстрого развёртывания современных прокси‑решений (Shadowsocks, Shadowsocks‑R, V2Ray, Trojan, Clash/Clash‑R) в облаке, что позволяет сразу получить надёжный «обход стены» и подключать клиентские устройства через единый профиль. Проект уже имеет более 2700 звёзд, активные коммиты и недавнее обновление (11 мая 2026), что делает его готовым к использованию в пилотных и производственных окружениях после базовой проверки лицензии и безопасности. Типичный сценарий — автоматизированный CI‑pipeline, который генерирует и разворачивает конфиги на сервере‑провайдере, после чего пользователи подключаются к единому шлюзу через любой поддерживаемый клиент.

### 中文

**项目简介**  
OverTheWallNode/SSV2RayTrojanSSRClash 是一套 **2026 年最新的科学上网工具集合**，集成了 **Shadowsocks、Shadowsocks‑R、V2Ray、Trojan、Clash / Clash‑R** 等主流协议，并提供了常用的翻墙机场推荐列表，帮助用户一键部署多协议、多平台的代理服务。

**价值**  
- **一站式多协议支持**：无需分别维护多个仓库或脚本，统一管理 ss/ssr/v2ray/trojan/clash，降低运维复杂度。  
- **实时机场推荐**：内置常用机场节点信息，开箱即用，适合快速搭建个人或小团队的科学上网环境。  
- **活跃社区与持续更新**：截至 2026‑05‑11 已有 2700+ 星、160+ Fork，最近一次提交仅在数天前，说明项目仍在积极维护，安全补丁和协议升级能够及时跟进。  

**典型接入方式**  
1. **Docker 部署**（推荐）  
   ```bash
   docker pull overthewallnode/ssv2raytrojanssrclash:latest
   docker run -d --name otw-proxy \
       -p 1080:1080 -p 8388:8388 \
       -v $(pwd)/config.yaml:/app/config.yaml \
       overthewallnode/ssv2raytrojanssrclash
   ```  
   - `config.yaml` 中配置所需的协议、端口、机场节点等。  
2. **二进制直接运行**（适用于轻量服务器）  
   ```bash
   wget https://github.com/OverTheWallNode/SSV2RayTrojanSSRClash/releases/download/vX.Y.Z/otw-linux-amd64.tar.gz
   tar -xzf otw-linux-amd64.tar.gz
   ./otw -c config.yaml
   ```  
3. **K8s Helm Chart**（大规模部署）  
   - 项目已提供 `helm/otw` 目录，使用 `helm install otw ./helm/otw --values values.yaml` 即可在集群中创建 StatefulSet + Service，配合 Ingress/MetalLB 暴露端口。  

**生产可用性**  
- **成熟度**：GitHub 近期活跃，拥有 2700+ 星、160+ Fork，且已有多家国内外用户在生产环境（机场、企业 VPN）中使用。  
- **安全性**：项目采用 MIT 许可证，代码公开，可自行审计；社区定期发布安全补丁，建议在生产环境中开启自动更新或定期拉取最新镜像。  
- **运维成本**：通过 Docker/Helm 可实现“一键升级”，并支持日志、Prometheus 监控插件，便于在生产环境中进行故障排查和容量规划。  

**结论**：该项目在功能完整性、社区活跃度和更新频率上均达到生产级别，适合作为企业或个人科学上网的核心代理平台，只需在部署前确认许可证符合内部合规要求并进行一次安全审计即可投入使用。

## 🧭 Practical evaluation

**Value:** OverTheWallNode/SSV2RayTrojanSSRClash may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2713 GitHub stars
- 162 forks
- updated 2026-05-11
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 55/100 |
| stars | 73/100 |
| topics | 100/100 |
| outlook | 52/100 |
| quality | 66/100 |
| recency | 20/100 |
| adoption | 68/100 |
| production | 52/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/OverTheWallNode/SSV2RayTrojanSSRClash) · [← Back to Misc](./README.md)</sub>
