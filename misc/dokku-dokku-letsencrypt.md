# dokku/dokku-letsencrypt

[![Stars](https://img.shields.io/github/stars/dokku/dokku-letsencrypt?style=flat-square&color=yellow)](https://github.com/dokku/dokku-letsencrypt/stargazers) [![Forks](https://img.shields.io/github/forks/dokku/dokku-letsencrypt?style=flat-square&color=blue)](https://github.com/dokku/dokku-letsencrypt/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Automatic Let's Encrypt TLS Certificate installation for dokku

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.1k |
| 🍴 **Forks** | 96 |
| 💻 **Language** | Shell |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`dokku` `dokku-letsencrypt` `letsencrypt` `nginx`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
`dokku/dokku-letsencrypt` is a shell‑based plugin that automatically obtains and renews Let’s Encrypt TLS certificates for apps deployed on Dokku. With over a thousand GitHub stars and recent activity, it streamlines HTTPS setup, making it a handy tool for developers who need quick, zero‑cost SSL on Dokku‑hosted services.

**Value**  
The plugin eliminates the manual steps of generating certificates, configuring Nginx, and handling renewals, allowing teams to secure their Dokku applications with a single command. This reduces operational overhead, speeds up onboarding of new services, and ensures compliance with modern security best‑practices without needing a separate reverse‑proxy or load‑balancer.

**Practical adoption path**  
1. **Prototype:** Clone the repo, follow the README to install the plugin on a test Dokku host, and run `dokku letsencrypt <app>` on a non‑critical app. Verify that the certificate is issued and auto‑renewed.  
2. **Integration:** Add the plugin to your infrastructure-as-code (e.g., Ansible, Terraform) so it is installed automatically on every Dokku node. Document any required environment variables (e.g., email address) in your deployment docs.  
3. **Validation:** Run a small proof‑of‑concept pipeline that deploys a sample app, triggers the plugin, and checks HTTPS connectivity and renewal logs. Adjust firewall/DNS settings if needed.  
4. **Roll‑out:** Gradually enable the plugin for production apps, monitoring the Dokku logs and Let’s Encrypt rate limits.

**Production readiness**  
The project is **medium‑ready**: it is actively maintained (last update May 2026), has a sizable community (≈1.1 k stars, 96 forks), and the core functionality is stable. However, because the integration steps are not fully detailed in the metadata, teams should perform a controlled rollout, verify compatibility with their specific Dokku version, and set up monitoring for renewal failures. Once those checks are in place, the plugin is suitable for internal services and prototypes, and with proper testing can be trusted for production workloads.

### Русский

**Краткое резюме:**  
`dokku/dokku-letsencrypt` — скрипт на Shell, автоматически получает и устанавливает бесплатные TLS‑сертификаты Let's Encrypt для приложений, развернутых в Dokku, что упрощает настройку HTTPS без ручного вмешательства. Типовой сценарий внедрения — в небольшом Proof‑of‑Concept или внутреннем окружении: добавить плагин к Dokku, включить автоматическое обновление сертификатов и проверить работу через README; при положительном результате расширить на продакшн‑кластер, учитывая зависимости и процесс обновления. Готовность к production — средняя: проект имеет более 1 000 звёзд, активные форки и недавнее обновление, но интеграционный путь не полностью описан в метаданных, поэтому требуется предварительная проверка настроек и стратегии поддержки.

### 中文

**项目简介（2‑3 句话）**  
`dokku/dokku-letsencrypt` 是为 Dokku（基于 Docker 的轻量级 PaaS）提供的插件，能够在部署应用后自动向 Let’s Encrypt 申请并安装免费 TLS 证书，实现 HTTPS 的一键化配置。

**价值**  
- **自动化**：部署后即自动完成证书申请、续期和绑定，免去手动操作的繁琐。  
- **安全性**：使用业界认可的 Let’s Encrypt 证书，为所有公开服务提供强制加密。  
- **成本**：完全免费，适合创业公司、内部平台或个人项目快速上线安全的 HTTPS 服务。

**典型接入方式**  
1. **插件安装**：在 Dokku 主机上执行 `dokku plugin:install https://github.com/dokku/dokku-letsencrypt.git`。  
2. **域名配置**：为目标应用添加自定义域（`dokku domains:add <app> example.com`），确保 DNS 已指向服务器 IP。  
3. **启用插件**：运行 `dokku letsencrypt <app>`，插件会自动向 Let’s Encrypt 发起 ACME 请求并将证书写入 Nginx 配置。  
4. **自动续期**：插件会在后台以 cron 方式定期检查并续签证书，无需额外操作。

**生产可用性**  
- **成熟度**：已有 1,115+ 星、96+ Fork，活跃维护至 2026‑05‑13，代码基于 Shell 脚本，易于审计。  
- **适用场景**：非常适合原型、内部业务系统或中小规模生产环境的快速 HTTPS 部署。  
- **注意事项**：在正式生产环境使用前，需要检查：  
  - DNS 解析是否稳定，确保 ACME 挑战能够成功。  
  - 服务器的防火墙/安全组是否允许 80/443 端口的外部访问。  
  - 与现有 Nginx/SSL 配置的兼容性（如自定义 SSL 参数）。  
  - 定期监控证书状态，防止因 API 限额或网络异常导致续期失败。  

综上，`dokku-letsencrypt` 提供了“一键 HTTPS” 的低成本解决方案，接入简单，适合作为 Dokku 部署流水线的标准组件；在完成上述环境验证后，可投入生产使用。

## 🧭 Practical evaluation

**Value:** dokku/dokku-letsencrypt may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1115 GitHub stars
- 96 forks
- updated 2026-05-13
- primary language: Shell
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 50/100 |
| stars | 65/100 |
| topics | 50/100 |
| outlook | 74/100 |
| quality | 75/100 |
| recency | 100/100 |
| adoption | 61/100 |
| production | 72/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/dokku/dokku-letsencrypt) · [← Back to Misc](./README.md)</sub>
