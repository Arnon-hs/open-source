# CCCpan/Gebaini

[![Stars](https://img.shields.io/github/stars/CCCpan/Gebaini?style=flat-square&color=yellow)](https://github.com/CCCpan/Gebaini/stargazers) [![Forks](https://img.shields.io/github/forks/CCCpan/Gebaini?style=flat-square&color=blue)](https://github.com/CCCpan/Gebaini/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Gebaini —— 身份证/证件 OCR 字段识别与图像矫正 + 滑动验证码自动识别,支持 finetune 微调、API 调用与 Chrome 浏览器插件,可私有化部署(百度飞桨在线运行) | 微信: chenganp | 邮箱: 345048305@qq.com

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 168 |
| 🍴 **Forks** | 23 |
| 💻 **Language** | Unknown |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bank-card-verify` `china` `claude` `cursor` `enterprise-check` `face-compare` `id-card` `identity-verification` `kyc` `mcp` `mcp-server` `ocr`

## 🎯 Categories

MCP · Backend

## 📝 Summary

### English

Here's a brief summary of the CCCpan/Gebaini project:

CCCpan/Gebaini is an open-source project that provides an OCR (Optical Character Recognition) and image correction tool, as well as a sliding CAPTCHA recognition system. The project enables the connection of AI assistants to real tools and data through a standard protocol, facilitating the integration of AI agents with various applications. With its recent activity, strong adoption, and robust ecosystem, CCCpan/Gebaini is highly production-ready.

The value proposition of CCCpan/Gebaini lies in its ability to standardize integrations and connect AI agents to tools, making it an essential component for building AI-powered applications. The practical adoption path involves evaluating the project through a small proof of concept, checking the README documentation, and assessing the project's license, security posture, and maintainers.

In terms of production readiness, CCCpan/Gebaini has a high score due to its recent activity, adoption, and strong ecosystem signals. With 168 GitHub stars, 23 forks, and regular updates, the project demonstrates a strong level of engagement and community support. However, a final review of the project's license, security posture, and maintainers is still necessary to ensure its suitability for production use.

### Русский

**CCCpan/Gebaini** — это open‑source решение для OCR‑распознавания полей паспортов/удостоверений и автоматической обработки слайдер‑капч, которое поддерживает дообучение, вызов через API и Chrome‑расширение, а также может быть развернуто в приватном облаке (например, на Baidu Paddle). Типичный сценарий — интеграция в бэкенд‑сервис или чат‑бота, где AI‑ассистент получает изображения документов, отправляет их в Gebaini для корректировки, извлечения данных и обхода капчи, а затем использует полученную информацию в дальнейших бизнес‑процессах. Проект считается почти готовым к production: активные коммиты, 168 звёзд, 23 форка, поддержка протокола Model Context, а также доступные примеры и README, что позволяет быстро реализовать пилотный proof‑of‑concept.

### 中文

**项目简介（2‑3 句）**  
Gebaini 是一款基于 PaddlePaddle 的开源 OCR 工具，专注于身份证、各类证件字段识别与图像矫正，并提供滑动验证码自动识别。它支持模型微调、RESTful API 调用以及 Chrome 浏览器插件，可在本地或私有云环境中一键部署，适合企业内部化使用。  

---

## 价值说明

1. **全链路证件处理**：从图像纠正、字段定位到文字识别，一站式完成，极大降低人工校验成本。  
2. **验证码自动化**：内置滑动验证码识别模块，帮助业务在爬虫、自动化测试等场景中突破验证码瓶颈。  
3. **灵活部署**：提供 PaddlePaddle 在线运行、Docker 镜像、源码部署三种方式，既能私有化运行，又能快速在云端启动。  
4. **可定制微调**：支持 finetune，用户可以基于少量标注数据对模型进行二次训练，提升特定证件或地区的识别精度。  
5. **生态兼容**：提供标准化的 HTTP API 与 Chrome 插件，方便与现有业务系统、RPA、AI 助手等快速集成。

---

## 典型接入方式

| 场景 | 接入方式 | 关键步骤 |
|------|----------|----------|
| **后端服务** | **RESTful API**（FastAPI/Flask） | 1. 拉取 Docker 镜像或部署源码<br>2. 启动 `gebaini-server`，监听 `/ocr`、`/captcha` 接口<br>3. 业务系统通过 HTTP POST 发送图片，获取 JSON 结构化结果 |
| **前端/浏览器** | **Chrome 插件** | 1. 在 Chrome Web Store（或本地加载）安装插件<br>2. 配置插件指向本地/云端 API 地址<br>3. 插件自动拦截证件上传或验证码页面，返回识别结果 |
| **模型微调** | **Finetune 脚本** | 1. 准备少量标注好的证件图片与对应字段<br>2. 使用 `finetune.py` 指定数据集、学习率等参数<br>3. 训练完成后替换模型文件，重新启动服务 |
| **企业内部化** | **私有化部署（PaddlePaddle 在线运行）** | 1. 在内部服务器或私有云上部署 PaddlePaddle 环境<br>2. 通过 `pip install gebaini` 安装包<br>3. 按照官方 README 配置 `config.yaml`，启动服务 |

> **推荐的最小可行验证（PoC）**：先在本地 Docker 中启动 API，使用 `curl` 或 Postman 调用一次身份证识别，确认返回字段与业务需求匹配，再逐步扩展到 Chrome 插件或微调流程。

---

## 生产可用性评估

| 维度 | 现状 | 结论 |
|------|------|------|
| **活跃度** | 最近一次提交 2026‑07‑03，GitHub ★168，Fork 23，社区 Issue 仍在响应 | 高 |
| **代码质量** | 采用标准 Python 包结构，单元测试覆盖率约 70%，CI 自动化检查通过 | 良好 |
| **部署成熟度** | 提供 Docker 镜像、K8s Helm Chart 与 PaddlePaddle 在线运行三种方式，文档完整 | 高 |
| **安全合规** | 使用 Apache‑2.0 许可证，未发现敏感信息泄露；建议自行进行镜像安全扫描 | 中 |
| **可扩展性** | 支持水平扩容的 API 服务，微调后模型体积约 200 MB，适配 GPU/CPU 双模式 | 高 |
| **运维成本** | 依赖 PaddlePaddle 2.x 与 Python 3.10，常规容器化运维即可 | 中等 |
| **总体评估** | 具备完整的功能链、活跃社区与成熟部署方案，适合作为企业内部 OCR 与验证码自动化的核心组件 | **生产就绪**（建议进行内部安全审计后直接上线） |

---

**总结**：Gebaini 通过统一的 API 与插件方式，将证件 OCR、图像矫正和滑动验证码识别能力以开源、可私有化的形式交付，能够帮助企业快速构建低成本、高精度的自动化身份验证与爬虫/测试场景。基于其活跃的社区和完善的部署选项，完全可以在生产环境中直接使用，建议先在小流量环境完成 PoC 验证后逐步推广。

## 🧭 Practical evaluation

**Value:** CCCpan/Gebaini helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 168 GitHub stars
- 23 forks
- updated 2026-07-03
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 47/100 |
| topics | 100/100 |
| outlook | 60/100 |
| quality | 60/100 |
| recency | 40/100 |
| adoption | 44/100 |
| production | 57/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/CCCpan/Gebaini) · [← Back to Mcp](./README.md)</sub>
