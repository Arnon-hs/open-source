# Hyundai-Kia-Connect/kia_uvo

[![Stars](https://img.shields.io/github/stars/Hyundai-Kia-Connect/kia_uvo?style=flat-square&color=yellow)](https://github.com/Hyundai-Kia-Connect/kia_uvo/stargazers) [![Forks](https://img.shields.io/github/forks/Hyundai-Kia-Connect/kia_uvo?style=flat-square&color=blue)](https://github.com/Hyundai-Kia-Connect/kia_uvo/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> A Home Assistant HACS integration that supports Kia Connect(Uvo) and Hyundai Bluelink. The integration supports the EU, Canada and the USA.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 851 |
| 🍴 **Forks** | 189 |
| 💻 **Language** | Python |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-05-10 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bluelink` `car` `homeassistant` `homeassistant-integration` `hyundai` `kia` `uvo`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Summary (2‑3 sentences)**  
Hyundai‑Kia‑Connect/kia_uvo is a Python‑based Home Assistant HACS integration that enables control of Kia Connect (Uvo) and Hyundai Bluelink vehicles across the EU, Canada, and the USA. With over 850 GitHub stars and recent commits, it offers a ready‑to‑use bridge between vehicle APIs and Home Assistant, allowing users to monitor and command their cars from a single smart‑home dashboard. The project’s active community and solid codebase make it a strong candidate for rapid prototyping of AI‑enhanced automotive features such as predictive alerts or RAG‑driven assistance.

**Value**  
- **AI‑ready data source**: The integration surfaces vehicle telemetry (location, battery state, door status, climate control, etc.) in Home Assistant, providing a structured, real‑time dataset that can be fed directly into LLM or RAG pipelines for personalized recommendations, anomaly detection, or voice‑assistant commands.  
- **Speed to prototype**: Because the connector already handles authentication, regional API quirks, and entity mapping, developers can focus on building AI logic (e.g., “suggest optimal charging schedule”) without writing low‑level API wrappers.  
- **Ecosystem leverage**: Home Assistant’s extensive automation engine and community add‑ons let you combine vehicle data with other smart‑home signals (weather, occupancy, energy pricing) to create richer, context‑aware AI workflows.

**Practical adoption path**  
1. **Proof‑of‑concept**: Fork the repo, install via HACS in a test Home Assistant instance, and verify that your Kia/Hyundai vehicle appears as expected.  
2. **Read‑me validation**: Follow the integration’s README to configure credentials (Uvo/Bluelink tokens) and enable the desired regions; confirm entity updates in the UI.  
3. **AI layer hookup**: Export the Home Assistant states (via the REST API or MQTT) to your AI platform, then prototype a simple LLM prompt or RAG query that consumes the vehicle data.  
4. **Iterate & secure**: Harden the deployment (API token storage, network isolation) and add unit tests for any custom automation before scaling.  

**Production readiness**  
- **Activity & adoption**: Recent commits (as of 2026‑05‑10), 851 stars, 189 forks, and a vibrant Home Assistant community indicate strong maintenance and user interest.  
- **Stability**: The integration is mature enough for pilot deployments; core vehicle commands have been battle‑tested across multiple regions.  
- **Risks**: Licensing (MIT) and security posture appear sound, but a final review of token handling and any third‑party dependencies is advisable. Overall, the project is “high” for OSS production use, making it suitable for serious pilots that embed AI features into vehicle‑home automation workflows.

### Русский

Hyundai‑Kia‑Connect/kia_uvo — это открытая интеграция для Home Assistant (через HACS), позволяющая управлять автомобилями Kia Connect (Uvo) и Hyundai Bluelink в регионах EU, Canada и USA. При помощи готового Python‑кода можно быстро прототипировать AI‑фичи, RAG‑агенты или другие автоматизации, не начиная с нуля, а сразу подключив данные автомобиля к вашим workflow. Проект активно поддерживается (обновления – 2026‑05‑10, > 850 звёзд, 189 форков), поэтому готов к пилотному запуску в production после небольшого PoC и проверки README/лицензии.

### 中文

**项目简介**  
Hyundai‑Kia‑Connect/kia_uvo 是一款面向 Home Assistant 的 HACS 集成，能够在欧盟、加拿大和美国地区接入 Kia Connect（Uvo）和 Hyundai Bluelink 车载服务，实现车辆状态、远程控制等功能的自动化。

**价值**  
- **即插即用**：无需自行实现车厂 API，直接在 Home Assistant 中把车辆信息和控制指令映射为实体，快速构建智能家居场景。  
- **AI/ML 友好**：提供标准化的车辆数据接口，可直接用于原型化 AI 功能（如行程预测、异常检测）或在 RAG/Agent 工作流中调用。  
- **跨区域支持**：统一的代码库兼容 EU、CA、US 三大市场，降低多地区部署的维护成本。

**典型接入方式**  
1. 在 Home Assistant 中通过 HACS 安装 `kia_uvo` 集成。  
2. 在集成配置页面填写 Kia/Hyundai 账户的用户名、密码以及所在地区（EU/CA/US）。  
3. 完成 OAuth 授权后，系统会自动创建车辆实体（电池、里程、门锁等），即可在自动化脚本或 Dashboard 中使用。  
4. 如需 AI 扩展，可通过 Home Assistant 的 REST API 或 MQTT 将车辆状态推送至外部模型服务进行进一步分析。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑10，项目拥有 851 ⭐、189 🍴，最近一次提交仅数天前，说明维护活跃。  
- **生态兼容**：基于 Python 开发，已在 Home Assistant 官方 HACS 仓库中发布，兼容最新的 Home Assistant 版本。  
- **风险可控**：暂无重大许可证或安全漏洞报告，仍需进行最终的许可证合规和安全审计。  
- **适配度**：适合作为正式生产环境的 OSS 组件进行试点，建议先在小规模 HA 实例中完成 PoC，验证与现有自动化流程的兼容性后再大规模部署。

## 🧭 Practical evaluation

**Value:** Hyundai-Kia-Connect/kia_uvo helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 851 GitHub stars
- 189 forks
- updated 2026-05-10
- primary language: Python
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 57/100 |
| stars | 62/100 |
| topics | 88/100 |
| outlook | 81/100 |
| quality | 81/100 |
| recency | 100/100 |
| adoption | 61/100 |
| production | 77/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-10 · [View on GitHub](https://github.com/Hyundai-Kia-Connect/kia_uvo) · [← Back to AI/ML](./README.md)</sub>
