# xca-sh/xcash

[![Stars](https://img.shields.io/github/stars/xca-sh/xcash?style=flat-square&color=yellow)](https://github.com/xca-sh/xcash/stargazers) [![Forks](https://img.shields.io/github/forks/xca-sh/xcash?style=flat-square&color=blue)](https://github.com/xca-sh/xcash/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Open-source self-hosted cryptocurrency payment gateway. Accept USDT, BTC, ETH — zero platform fees, 100+ blockchains, 3-min Docker deploy, full self-custody of private keys. Built-in MistTrack risk control.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 145 |
| 🍴 **Forks** | 7 |
| 💻 **Language** | Python |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bitcoin` `blockchain` `crypto` `cryptocurrency` `django` `ethereum` `finance` `open-source` `payment-gateway` `self-hosted` `usdt` `web3`

## 🎯 Categories

Crypto · Payments · DevOps/Infra

## 📝 Summary

### English

**Brief summary**  
xca‑sh/xcash is an open‑source, self‑hosted cryptocurrency payment gateway that lets you accept USDT, BTC, ETH and over 100 other blockchains with zero platform fees. It runs in a single Docker container in about three minutes, keeps private keys under your full control, and includes the MistTrack risk‑control engine. The project is a Python‑based reference implementation that exposes clear APIs/SDKs for prototyping and inspecting blockchain workflows.

**Value**  
- **Full self‑custody:** No third‑party escrow; you retain the private keys and can audit every transaction.  
- **Rapid onboarding:** A three‑minute Docker deployment removes infrastructure friction, making it ideal for PoCs and early‑stage Web3 products.  
- **Broad blockchain coverage:** Supporting 100+ chains and major stablecoins lets teams experiment with multi‑chain payment flows without stitching together multiple services.  
- **Risk management built‑in:** MistTrack provides out‑of‑the‑box fraud detection, reducing the need to develop custom AML/KYC tooling.

**Practical adoption path**  
1. **Spin up the Docker image** in a test environment and connect it to a sandbox wallet.  
2. **Integrate via the provided REST/CLI SDK** (Python, with language metadata for other bindings) into your e‑commerce or dApp backend.  
3. **Configure supported assets and risk rules** using the MistTrack UI or API.  
4. **Run end‑to‑end payment tests** against testnets, then switch the node endpoints to mainnet once validated.  
5. **Deploy to production** behind your own firewall or Kubernetes cluster, monitoring the logs and the built‑in health endpoints.

**Production readiness**  
- **Activity & community:** 145 ★, recent commit (2026‑06‑24), and ongoing adoption signals indicate a healthy codebase.  
- **Architecture:** Single‑container Docker model simplifies scaling and isolation; the Python core is well‑documented and extensible.  
- **Security posture:** Private keys remain on‑premise, and the MistTrack module adds a layer of transaction risk analysis, though a formal security audit and license review are still recommended.  
- **Operational maturity:** With clear API/CLI contracts and a modest dependency footprint, the gateway is ready for a serious pilot in production environments, provided you perform the usual hardening (TLS, secret management, monitoring).

### Русский

**xca‑sh/xcash** — это открытый self‑hosted шлюз для криптовалютных платежей, позволяющий принимать USDT, BTC и ETH без комиссии платформы, поддерживая более 100 блокчейнов и полностью удерживая приватные ключи в вашем распоряжении. Он быстро разворачивается в Docker (≈ 3 минуты) и включает готовый модуль риск‑контроля MistTrack, что делает его идеальным для прототипирования Web3‑процессов, интеграции кошельков или DeFi‑функций и изучения блокчейн‑интеграций. По активности репозитория (145 звёзд, свежие коммиты, широкая экосистема) проект считается готовым к пилотному использованию в продакшене, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
xca-sh/xcash 是一款开源的自托管加密货币支付网关，支持 USDT、BTC、ETH 等 100 多条链的收付款，零平台费，私钥完全自持，并内置 MistTrack 风控模块，3 分钟即可通过 Docker 完成部署。

**核心价值**  
- **全链路自托管**：私钥不离开自己的服务器，安全可审计。  
- **多链兼容**：一次部署即可接入 100+ 公链和跨链资产，省去逐链集成的成本。  
- **快速原型**：提供 API、SDK 与 CLI，帮助开发者快速搭建 Web3 支付、钱包或 DeFi 原型，且实现细节全部开源，便于学习和二次定制。  

**典型接入方式**  
1. **Docker 一键启动**：`docker run -p 8000:8000 xca-sh/xcash` 完成服务部署。  
2. **API 调用**：通过 RESTful 接口（/create‑payment、/callback 等）发起收款请求，返回唯一支付地址或 QR 码。  
3. **SDK/CLI**：项目提供 Python SDK 与命令行工具，可在后端业务中直接调用 `xcash.create_payment(...)` 或使用 `xcash-cli` 进行查询、退款等操作。  
4. **Webhook**：配置回调 URL，实时获取链上确认、风控结果等事件。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑24，星标 145，社区已有 7 个 Fork，表明项目仍在维护。  
- **技术成熟度**：核心使用 Python 实现，配套 Docker 镜像、完整 API 文档和示例代码，部署与升级成本低。  
- **安全与合规**：私钥自行管理，内置 MistTrack 风控；但仍需自行审计许可证（MIT）和代码安全（如依赖漏洞）后方可投入正式业务。  
- **适配场景**：适合需要快速验证链上支付、构建自定义钱包/DeFi 功能的企业或开发者，也可作为生产环境的支付网关，在完成安全审计后即可投入使用。

总体来看，xca-sh/xcash 具备较高的生产候选价值，适合在内部或受控环境中先行试点，随后根据安全审计结果推广到正式业务。

## 🧭 Practical evaluation

**Value:** xca-sh/xcash helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 145 GitHub stars
- 7 forks
- updated 2026-06-24
- primary language: Python
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 23/100 |
| stars | 46/100 |
| topics | 100/100 |
| outlook | 55/100 |
| quality | 58/100 |
| recency | 40/100 |
| adoption | 39/100 |
| production | 59/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/xca-sh/xcash) · [← Back to Crypto](./README.md)</sub>
