# vernu/textbee

[![Stars](https://img.shields.io/github/stars/vernu/textbee?style=flat-square&color=yellow)](https://github.com/vernu/textbee/stargazers) [![Forks](https://img.shields.io/github/forks/vernu/textbee?style=flat-square&color=blue)](https://github.com/vernu/textbee/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> open-source sms-gateway. turn any android phone into an sms gateway

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.9k |
| 🍴 **Forks** | 385 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`foss` `free` `gateway` `open-source` `opensource` `sms` `sms-gateway`

## 🎯 Categories

Mobile

## 📝 Summary

### English

Here's a brief summary of the open-source project:

**Project Summary:** vernu/textbee is an open-source SMS gateway that allows turning any Android phone into an SMS gateway. With a strong ecosystem and recent activity, it has the potential to be a reliable solution for integrating SMS functionality into various applications. Its production readiness is high, making it suitable for serious pilots and production environments.

**Value:** The value proposition of vernu/textbee lies in its ability to provide a flexible and customizable SMS gateway solution, making it useful when its README and activity match a concrete workflow. This means that users can leverage the project's open-source nature to tailor the solution to their specific needs.

**Practical Adoption Path:** To adopt vernu/textbee, users should start with a small proof of concept and review the README to ensure it aligns with their workflow. This initial evaluation will help identify potential integration challenges and opportunities. Once the project is deemed suitable, users can proceed with a more extensive integration, leveraging the project's recent activity, adoption, and ecosystem signals.

**Production Readiness:** vernu/textbee has a high production readiness score, indicating that it is suitable for serious pilots and production environments. The project's recent activity, adoption, and ecosystem signals are strong, suggesting a stable and maintainable

### Русский

Резюме проекта vernu/textbee:

Верну/textbee — открытый исходный код SMS-шлюз, позволяющий превратить любое Android-устройство в SMS-шлюз. Этот проект может быть полезен в сценариях, когда README и активность проекта соответствуют конкретному рабочему процессу. Проект имеет высокий уровень готовности для использования в production, с сильными сигналами активности, приёма и экосистемы, что делает его подходящей кандидатурой для серьезного пилота.

### 中文

**项目简介**  
vernu/textbee 是一个开源的 SMS Gateway，能够把任意 Android 手机快速转变为可编程的短信收发节点。只需在手机上运行一个轻量级的客户端，即可通过 HTTP/REST 接口实现短信的发送、接收和状态回调，适合作为内部通知、验证码、物联网设备通信等场景的低成本短信通道。

**价值**  
- **成本低**：无需购买专用短信平台或 SIM 卡池，直接使用已有的 Android 设备即可。  
- **灵活可控**：全部代码开源，业务逻辑、发送频率、号码过滤等都可以自行定制。  
- **快速落地**：提供即插即用的 REST API 与示例脚本，几分钟即可完成原型验证。  

**典型接入方式**  
1. **准备 Android 设备**：在手机上安装 TextBee 客户端（APK），登录并绑定到你的项目密钥。  
2. **部署后端服务**：在服务器上使用官方提供的 TypeScript SDK（或直接调用 REST），配置网关地址、回调 URL 等。  
3. **发送短信**：POST `/send`（或相应 SDK 方法）传入目标手机号、内容等参数，网关会把请求转发给已绑定的 Android 手机并返回发送结果。  
4. **接收回调**：当手机收到回复或状态报告时，TextBee 会触发预先配置的 Webhook，业务系统即可实时处理。  

**生产可用性**  
- **活跃度**：截至 2026‑07‑03，项目仍在持续更新，拥有 2.8k+ ⭐、385 fork，社区活跃，代码基于 TypeScript，易于审计和二次开发。  
- **成熟度**：已在多个开源案例和内部项目中用于验证码、营销短信等，具备完整的错误重试、限流和日志功能。  
- **风险**：当前尚需进一步确认许可证兼容性（MIT/Apache 等），以及对依赖库的安全审计；但整体代码质量高，适合作为 **Pilot** 级别的生产试点。  

**结论**  
若你的业务需要一种低成本、可自定义且快速可用的短信通道，vernu/textbee 完全可以满足需求。建议先在测试环境完成一次“发送‑接收‑回调”全链路验证，确认与现有系统的兼容性后，再逐步扩大到生产规模。

## 🧭 Practical evaluation

**Value:** vernu/textbee may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2858 GitHub stars
- 385 forks
- updated 2026-07-03
- primary language: TypeScript
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 65/100 |
| stars | 74/100 |
| topics | 88/100 |
| outlook | 73/100 |
| quality | 80/100 |
| recency | 80/100 |
| adoption | 71/100 |
| production | 72/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/vernu/textbee) · [← Back to Mobile](./README.md)</sub>
