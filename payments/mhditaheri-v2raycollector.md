# MhdiTaheri/V2rayCollector

[![Stars](https://img.shields.io/github/stars/MhdiTaheri/V2rayCollector?style=flat-square&color=yellow)](https://github.com/MhdiTaheri/V2rayCollector/stargazers) [![Forks](https://img.shields.io/github/forks/MhdiTaheri/V2rayCollector?style=flat-square&color=blue)](https://github.com/MhdiTaheri/V2rayCollector/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-48%2F100-brightgreen?style=flat-square)](#)

> This script is designed to retrieve configuration details for various VPN protocols (VLESS, VMess, Shadowsocks, and Trojan) from a list of Telegram channel URLs provided within the script. It uses cURL to fetch content and regular expressions to extract the configurations.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 301 |
| 🍴 **Forks** | 23 |
| 💻 **Language** | PHP |
| 📈 **Score** | 48/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`config` `hysteria` `php` `server` `subscription` `tuic` `v2ray` `vless` `vmess`

## 🎯 Categories

Payments · Backend

## 📝 Summary

### English

**Project Summary:**

MhdiTaheri/V2rayCollector is an open-source script that automates the retrieval of VPN configuration details from Telegram channels, utilizing cURL and regular expressions for extraction. This script can be used to integrate billing, checkout, or payment flows faster. It supports various VPN protocols such as VLESS, VMess, Shadowsocks, and Trojan.

**Value Proposition:**

The script's primary value proposition lies in its ability to streamline the integration of payment flows, allowing developers to automate payment operations and evaluate PSP (Payment Service Provider) flows more efficiently. This can save time and resources in the development process.

**Practical Adoption Path:**

To adopt this script, follow these steps:

1. **Evaluate the script**: Assess the script's functionality and performance to ensure it meets your project's requirements.
2. **Develop a proof of concept**: Create a small-scale implementation to test the script's integration with your existing system.
3. **Review the README documentation**: Understand the script's dependencies, maintenance requirements, and any potential issues.
4. **Validate setup costs**: Estimate the time and resources needed to set up and maintain the script in your production environment.

**Production Readiness:**

The script has a medium production readiness score, indicating that it can

### Русский

Резюме проекта MhdiTaheri/V2rayCollector:

MhdiTaheri/V2rayCollector - это скрипт, который позволяет интегрировать монетизацию, оплаты и потоки PSP (Payment Service Provider) быстрее. Этот скрипт предназначен для автоматизации процесса настройки VPN-протоколов (VLESS, VMess, Shadowsocks и Trojan) из списка URL-адресов Telegram-каналов. Проект имеет средний уровень готовности к production, что позволяет использовать его в прототипах или внутренних процессах после проверки зависимостей и обслуживания.

### 中文

**价值**  
MhdiTaheri/V2rayCollector 能自动从 Telegram 频道中抓取 VLESS、VMess、Shadowsocks、Trojan 等 VPN 协议的配置信息，帮助业务快速获取、统一管理和分发节点数据。对于需要在计费、结算或 PSP（支付服务提供商）流程中嵌入 VPN 资源的产品，它可以显著缩短手工收集、解析节点的时间成本，提升原型开发和内部测试的效率。

**典型接入方式**  

1. **克隆仓库并安装依赖**  
   ```bash
   git clone https://github.com/MhdiTaheri/V2rayCollector.git
   cd V2rayCollector
   composer install   # 如有 PHP 依赖
   ```
2. **在 `config.php`（或脚本内）填入待抓取的 Telegram 频道 URL 列表**。  
3. **调用主脚本**（如 `collector.php`），它会使用 cURL 拉取页面并通过正则提取出符合协议的链接。  
   ```php
   php collector.php > configs.txt
   ```
4. **将输出的配置文件（或 JSON）交给后端计费系统**，在用户购买或开通服务时直接返回对应的节点信息。  
5. **可选**：把脚本封装为 Docker 镜像或内部 API（例如 `GET /v2ray/configs`），让其他微服务通过 HTTP 调用，实现“即插即用”。

**生产可用性**  

| 维度 | 评估 | 说明 |
|------|------|------|
| **代码成熟度** | 中等 | 301 星、23 Fork，最近一次提交在 2026‑07‑08，活跃度一般。 |
| **依赖管理** | 需要检查 | 仅依赖 PHP 与 cURL，需确认运行环境的 PHP 版本与扩展兼容性。 |
| **可扩展性** | 良好 | 通过修改正则或添加新协议即可支持更多节点格式。 |
| **安全性** | 待评估 | 脚本会直接请求外部 Telegram 链接，需防止 SSRF、恶意内容注入等风险。 |
| **运维成本** | 低‑中 | 只要保证 PHP 与网络通畅即可，建议加入日志与监控。 |
| **适用场景** | 原型、内部工具、自动化脚本 | 对外生产使用前建议做一次 POC，验证抓取准确率、异常处理和与计费系统的对接方式。 |

**结论**  
V2rayCollector 适合作为内部原型或自动化运维工具，帮助快速获取 VPN 配置并与计费/结算流程对接。若要在正式生产环境使用，建议在以下方面做进一步工作：  

1. 编写完整的 README/API 文档，明确输入/输出格式。  
2. 增加异常捕获、重试机制以及抓取频率限制，防止被 Telegram 封禁。  
3. 对输出进行安全校验（如 URL 白名单、协议合法性），避免把恶意节点交付给用户。  

完成上述改进后，即可在支付/订阅系统中以低成本实现 VPN 节点的自动化供应。

## 🧭 Practical evaluation

**Value:** MhdiTaheri/V2rayCollector helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 301 GitHub stars
- 23 forks
- updated 2026-07-08
- primary language: PHP
- 9 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 53/100 |
| topics | 100/100 |
| outlook | 54/100 |
| quality | 61/100 |
| recency | 40/100 |
| adoption | 48/100 |
| production | 53/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-08 · [View on GitHub](https://github.com/MhdiTaheri/V2rayCollector) · [← Back to Payments](./README.md)</sub>
