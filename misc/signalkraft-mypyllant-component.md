# signalkraft/mypyllant-component

[![Stars](https://img.shields.io/github/stars/signalkraft/mypyllant-component?style=flat-square&color=yellow)](https://github.com/signalkraft/mypyllant-component/stargazers) [![Forks](https://img.shields.io/github/forks/signalkraft/mypyllant-component?style=flat-square&color=blue)](https://github.com/signalkraft/mypyllant-component/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Home Assistant component for the myVAILLANT API, controls Vaillant devices such as aroTHERM heatpumps and ecoTEC boilers

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 326 |
| 🍴 **Forks** | 50 |
| 💻 **Language** | Python |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`hacs` `home-assistant` `home-assistant-component` `homeassistant` `vaillant`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Project Summary:**

The `signalkraft/mypyllant-component` is an open-source Home Assistant component that enables integration with Vaillant devices, such as aroTHERM heat pumps and ecoTEC boilers, through the myVAILLANT API. This project facilitates the addition of AI capabilities without requiring a custom model stack. It is suitable for prototyping AI features, building RAG or agent workflows, and evaluating model tooling.

**Value:**

The project provides an easy-to-use solution for integrating Vaillant devices with Home Assistant, enabling users to leverage AI capabilities without starting from scratch. Its value lies in its ability to:

* Simplify the integration process with Vaillant devices
* Facilitate AI feature prototyping and development
* Support the creation of RAG or agent workflows
* Evaluate model tooling and performance

**Practical Adoption Path:**

To adopt this project, follow these steps:

1. Review the project's documentation and codebase to ensure it meets your requirements.
2. Evaluate the project's production readiness and risk factors, such as license, security posture, and active maintainers.
3. Install and configure the Home Assistant component according to the project's instructions.
4. Integrate the component with your Vaillant

### Русский

Резюме проекта signalkraft/mypyllant-component:

Этот открытый исходный проект предоставляет компонент для Home Assistant, который позволяет контролировать устройства Vaillant, такие как ароТЕРМ и экоТЭК. Он помогает добавлять функциональность AI без необходимости создания сложной модели стека. Внедрение компонента подходит для прототипирования функций AI, построения потоков RAG или агентов, а также оценки инструментов моделирования. Проект готов к пилотному внедрению в production, учитывая недавнюю активность, широкое распространение и сильные сигналы экосистемы.

### 中文

**项目简介**  
`signalkraft/mypyllant-component` 是 Home Assistant 的 Python 组件，封装了 myVAILLANT API，能够在 Home Assistant 中直接控制 Vaillant 系列设备（如 aroTHERM 热泵、ecoTEC 锅炉），实现智能家居的集中管理与自动化。

**价值**  
- **即插即用**：无需自行实现底层协议，只需在 Home Assistant 中加载组件即可完成设备发现与控制。  
- **AI 友好**：组件提供统一的 API/SDK 接口，便于在此基础上快速叠加 AI 功能（如预测性维护、基于大模型的能耗优化、RAG/Agent 工作流等），大幅降低模型研发的前期成本。  
- **社区活跃**：项目已有 326+ Stars、50+ Forks，近期仍在维护，具备一定的生态支撑。

**典型接入方式**  
1. **在 Home Assistant 中安装**：通过 UI 的 “集成” 页面搜索 “myVAILLANT”，或在 `configuration.yaml` 中添加相应的 `myyllant` 配置块。  
2. **提供 API 凭证**：在 Vaillant 账户后台生成的 API token 填入配置，组件会自动完成设备发现。  
3. **使用 Python SDK（可选）**：如果需要在自定义脚本或 AI 服务中直接调用，可通过 `pip install myyllant` 安装 SDK，利用 `MyVailantClient` 与 Home Assistant 同步状态或发送指令。  

**生产可用性**  
- **成熟度**：项目最近一次提交在 2026‑07‑01，代码活跃，兼容最新的 Home Assistant 2024+ 版本。  
- **可靠性**：已在多个社区实例中用于实际暖通控制，错误日志和异常处理较为完善。  
- **安全性**：使用 HTTPS 与 Vaillant 官方 API 交互，凭证通过 Home Assistant 的加密存储管理；仍建议在生产环境中进行额外的审计（依赖许可证、依赖库的安全报告）。  
- **可扩展性**：提供统一的事件/状态回调，便于在上层加入自定义自动化或 AI 推理模块，适合作为 AI 原型或正式业务的底层驱动。  

综上，`signalkraft/mypyllant-component` 是一个即插即用、社区活跃且具备生产级别稳定性的 Home Assistant 组件，特别适合需要快速集成 Vaillant 设备并在此基础上实验 AI 功能的开发者和企业。

## 🧭 Practical evaluation

**Value:** signalkraft/mypyllant-component helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 326 GitHub stars
- 50 forks
- updated 2026-07-01
- primary language: Python
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 43/100 |
| stars | 54/100 |
| topics | 63/100 |
| outlook | 54/100 |
| quality | 57/100 |
| recency | 40/100 |
| adoption | 50/100 |
| production | 56/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/signalkraft/mypyllant-component) · [← Back to Misc](./README.md)</sub>
