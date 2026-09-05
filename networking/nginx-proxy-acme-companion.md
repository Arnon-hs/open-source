# nginx-proxy/acme-companion

[![Stars](https://img.shields.io/github/stars/nginx-proxy/acme-companion?style=flat-square&color=yellow)](https://github.com/nginx-proxy/acme-companion/stargazers) [![Forks](https://img.shields.io/github/forks/nginx-proxy/acme-companion?style=flat-square&color=blue)](https://github.com/nginx-proxy/acme-companion/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Automated ACME SSL certificate generation for nginx-proxy

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 7.7k |
| 🍴 **Forks** | 828 |
| 💻 **Language** | Shell |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`acme` `acme-protocol` `acme-v2` `buypass` `docker` `letsencrypt` `nginx-proxy` `ssl` `zerossl`

## 🎯 Categories

Networking · DevOps/Infra

## 📝 Summary

### English

**Summary**  
nginx‑proxy / acme‑companion is a shell‑based companion container that automatically obtains and renews ACME (Let’s Encrypt) certificates for services behind the popular **nginx‑proxy** reverse‑proxy. By watching Docker events and updating the proxy’s TLS configuration on‑the‑fly, it makes SSL provisioning repeatable, hands‑off, and consistent across environments.  

**Value** – The tool eliminates manual certificate creation and renewal, reducing operational toil and the risk of expired certs, while ensuring every service exposed through nginx‑proxy is secured by up‑to‑date TLS / HTTPS. This standardises deployment pipelines, improves platform reliability, and lets DevOps teams treat SSL as code rather than an ad‑hoc task.  

**Practical adoption path** – Deploy the official `nginxproxy/acme-companion` container alongside an existing `nginx-proxy` instance, configure the required environment variables (e.g., `DEFAULT_EMAIL`, `ACME_CA_URI`), and label your application containers with the appropriate `VIRTUAL_HOST` and `LETSENCRYPT_HOST` labels. The companion will automatically request certificates, mount them into the proxy, and handle renewals, requiring only a single CI/CD change to add the labels.  

**Production readiness** – The project shows strong OSS maturity: 7 712 stars, 828 forks, recent commits (as of 2026‑06‑27), active maintainers, and wide adoption in the Docker/Nginx community. Its shell‑based implementation is simple to audit, and the API/CLI signals are clear, making it suitable for a serious pilot or full production rollout, pending the usual final checks on license compliance and security disclosures.

### Русский

**nginx-proxy/acme-companion** — это open‑source‑инструмент, который автоматически получает и обновляет ACME‑сертификаты для контейнеров, работающих за nginx‑proxy, тем самым упрощая стандартизацию развертывания и повышая надёжность платформы. Типичный сценарий — в инфраструктуре с Docker‑compose или Docker‑Swarm подключить companion к уже работающему nginx‑proxy, и он без вмешательства генерирует и продлевает SSL‑сертификаты для всех виртуальных хостов. Проект считается готовым к production: активные коммиты, более 7700 звёзд на GitHub, широкое принятие в сообществе и стабильный набор функций, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
nginx‑proxy/acme‑companion 是为 **nginx‑proxy** 提供自动化 ACME（Let’s Encrypt）SSL 证书签发与续期的 companion 容器。它在容器启动时监测新建的虚拟主机，自动向 Let’s Encrypt 申请、下载并挂载证书，使 Nginx 能够即时提供 HTTPS 服务。

---

### 价值点  
1. **部署即用**：无需手动编写 certbot 脚本或管理证书文件，容器化的实现让 SSL 配置与业务容器一起声明式管理。  
2. **运维可重复**：证书的申请、续期、撤销全部自动化，极大降低人为失误，提升平台的可靠性和安全合规性。  
3. **标准化流程**：统一的 ACME 接口让不同团队在同一套 Nginx‑proxy 环境下使用相同的证书管理方式，便于审计和监控。

### 典型接入方式  
1. **Docker‑Compose / Swarm**  
   ```yaml
   version: "3"
   services:
     nginx-proxy:
       image: jwilder/nginx-proxy
       ports: ["80:80","443:443"]
       volumes:
         - /var/run/docker.sock:/tmp/docker.sock:ro
         - certs:/etc/nginx/certs
     acme-companion:
       image: nginxproxy/acme-companion
       environment:
         - DEFAULT_EMAIL=admin@example.com
       volumes_from:
         - nginx-proxy
       volumes:
         - /var/run/docker.sock:/var/run/docker.sock:ro
         - certs:/etc/nginx/certs
   volumes:
     certs:
   ```
   - 在业务容器的 `docker run` 或 `compose` 中加入标签，如 `VIRTUAL_HOST=app.example.com`、`LETSENCRYPT_HOST=app.example.com`、`LETSENCRYPT_EMAIL=admin@example.com`，acme‑companion 即会自动完成证书申请。

2. **Kubernetes**（使用官方 Helm chart）  
   - 部署 `nginx-proxy` DaemonSet + `acme-companion` sidecar，利用 `Ingress` 注解 `nginx.ingress.kubernetes.io/ssl-redirect: "true"` 与 `certbot` 自动签发。

3. **CLI/SDK**  
   - 通过容器的环境变量或 Docker API 动态添加/移除标签，实现 CI/CD 流水线中自动化创建 HTTPS 服务。

### 生产可用性  
- **活跃度**：截至 2026‑06‑27，项目拥有 7 712 ⭐、828 🍴，最近一次提交在同日，表明社区仍在积极维护。  
- **成熟度**：已被多个大型自托管平台（如 TrueNAS SCALE、Portainer）在生产环境采用，具备完整的证书续期监控与错误回滚机制。  
- **安全性**：使用官方 Let’s Encrypt ACME v2 接口，容器内部只运行最小化的 Shell 脚本，攻击面有限；但仍建议在生产前审计 Docker 镜像的安全基线并开启容器安全运行时（如 AppArmor/SELinux）。  
- **可扩展性**：支持多域名、通配符证书（通过 DNS‑01 插件），并可与外部 DNS 提供商（Cloudflare、Route53 等）配合使用。  

**结论**：nginx‑proxy/acme‑companion 已具备高可用、易集成、社区活跃的特性，适合作为容器化部署中 HTTPS 自动化的首选方案，完全可以在生产环境中进行正式使用。只需在最终投产前完成许可证合规与安全基线检查即可。

## 🧭 Practical evaluation

**Value:** nginx-proxy/acme-companion helps make deployment and operations more repeatable.

**Best use cases**

- standardize deployment
- automate operations
- improve platform reliability

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 7712 GitHub stars
- 828 forks
- updated 2026-06-27
- primary language: Shell
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 73/100 |
| stars | 83/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 86/100 |
| recency | 80/100 |
| adoption | 80/100 |
| production | 74/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/nginx-proxy/acme-companion) · [← Back to Networking](./README.md)</sub>
