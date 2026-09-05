# lnbits/lnbits

[![Stars](https://img.shields.io/github/stars/lnbits/lnbits?style=flat-square&color=yellow)](https://github.com/lnbits/lnbits/stargazers) [![Forks](https://img.shields.io/github/forks/lnbits/lnbits?style=flat-square&color=blue)](https://github.com/lnbits/lnbits/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> LNbits, free and open-source Lightning wallet and accounts system.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.2k |
| 🍴 **Forks** | 409 |
| 💻 **Language** | Python |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bitcoin` `lightning-network` `lightning-network-wallet` `lnurl` `lnurl-atm`

## 🎯 Categories

Crypto

## 📝 Summary

### English

Here's a brief summary of the open-source project:

LNbits is a free and open-source Lightning wallet and accounts system that enables developers to prototype and inspect blockchain workflows with transparent implementation details. With its high production readiness and strong ecosystem signals, LNbits offers a practical adoption path for building Web3 workflows, inspecting blockchain integrations, and prototyping wallet or DeFi features. Its recent activity, adoption, and GitHub metrics (1215 stars and 409 forks) indicate a strong foundation for a serious pilot or production deployment.

### Русский

Резюме проекта lnbits/lnbits:

Lnbits - это бесплатный и открытый проект Lightning-карты и системы учетных записей. Его можно использовать для прототипирования или проверки потоков работы блокчейна с открытыми подробностями реализации.Lnbits готов к внедрению в производственный режим (Production readiness: High) и может быть использован для построения Web3-потоков, проверки интеграций блокчейна и прототипирования функций кошелька или DeFi.

### 中文

**简短介绍**  
LNbits 是一款免费且开源的 Lightning 网络钱包与多账户系统，提供完整的 API 与插件机制，帮助开发者快速原型化、测试和部署 Web3、DeFi 或其他区块链工作流。  

**价值**  
- **快速实验**：开放的实现细节让团队能够直接查看、修改并扩展 Lightning 相关功能，省去自行搭建底层节点的成本。  
- **模块化插件**：内置多种插件（如 LNURL、Paywalls、Custodial wallets 等），可即插即用地构建复杂的支付场景。  
- **社区与生态**：拥有超过 1200 颗星、400+ Fork，活跃的维护者和丰富的第三方集成案例，降低技术风险。  

**典型接入方式**  
1. **部署实例**：使用 Docker 或直接在 Python 环境中 `docker compose up -d` 部署 LNbits 实例。  
2. **创建 API Key**：在后台创建用户或子账户，获取对应的 `API‑KEY`。  
3. **调用 REST API**：通过 HTTPS 请求（如 `/api/v1/payments`、`/api/v1/withdrawals`）完成收付款、生成发票、查询余额等操作。  
4. **插件扩展**：如需自定义功能，可在 `extensions/` 目录编写插件并在 UI 中启用，或直接调用插件提供的专属端点。  

**生产可用性**  
- **活跃维护**：截至 2026‑07‑02 最近一次提交，代码库更新频繁，社区响应及时。  
- **成熟度**：已在多个商业项目和公开演示中使用，具备完整的文档、示例代码和 Docker 镜像，适合作为正式环境的支付后端。  
- **安全与合规**：采用 MIT 许可证，核心功能经过社区审计；但在生产部署前仍建议进行内部安全评估、启用 HTTPS、限制 API‑KEY 权限并定期更新依赖。  

总体而言，LNbits 具备高可用性和灵活的扩展能力，是构建 Lightning 支付或 Web3 原型的可靠 OSS 选型。

## 🧭 Practical evaluation

**Value:** lnbits/lnbits helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1215 GitHub stars
- 409 forks
- updated 2026-07-02
- primary language: Python
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 65/100 |
| stars | 66/100 |
| topics | 63/100 |
| outlook | 69/100 |
| quality | 74/100 |
| recency | 80/100 |
| adoption | 66/100 |
| production | 69/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/lnbits/lnbits) · [← Back to Crypto](./README.md)</sub>
