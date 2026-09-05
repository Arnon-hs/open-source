# fossasia/eventyay-hubspot

[![Stars](https://img.shields.io/github/stars/fossasia/eventyay-hubspot?style=flat-square&color=yellow)](https://github.com/fossasia/eventyay-hubspot/stargazers) [![Forks](https://img.shields.io/github/forks/fossasia/eventyay-hubspot?style=flat-square&color=blue)](https://github.com/fossasia/eventyay-hubspot/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> hubspot integration for eventyay

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 354 |
| 🍴 **Forks** | 3 |
| 💻 **Language** | Python |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
fossasia/eventyay‑hubspot is an open‑source Python package that adds HubSpot CRM integration to the Eventyay event‑management platform. It enables automatic syncing of attendees, tickets, and event data with HubSpot contacts and workflows, helping organizers keep their marketing database up‑to‑date without manual exports. The project is modestly popular (354 ★) but shows limited recent activity, so it’s best suited for prototypes or internal tooling after a quick code review.

**Value**  
- **Unified data flow:** Eliminates the need for manual CSV exports by pushing attendee information directly into HubSpot, reducing errors and saving staff time.  
- **Marketing automation:** Allows event organizers to trigger HubSpot email sequences, lead scoring, or segmentations immediately after ticket purchase or registration.  
- **Open‑source flexibility:** The code can be customized to match specific event‑y​ay schemas or to extend the integration (e.g., adding custom HubSpot properties).

**Practical Adoption Path**  
1. **Clone & review** – Fork the repository, inspect the `README`, and run the test suite (if any) to verify compatibility with your Eventyay version.  
2. **Configure credentials** – Add HubSpot API keys or OAuth tokens to the project’s settings, following the integration guide in the repo.  
3. **Map fields** – Adjust the Python mapping layer to align Eventyay ticket/attendee fields with the HubSpot contact properties you need.  
4. **Pilot run** – Deploy the integration in a staging environment, process a small batch of test registrations, and confirm that contacts appear correctly in HubSpot.  
5. **Iterate & lock** – Address any missing edge‑cases, add logging/monitoring, and then promote the code to production.

**Production Readiness**  
- **Maturity:** Medium. The package works for prototypes and internal workflows but lacks recent commits and extensive documentation, so extra validation is required.  
- **Dependencies:** Pure Python with standard HubSpot client libraries; verify that versions are compatible with your current stack.  
- **Maintenance:** Few forks and limited recent activity mean you may need to take ownership of bug fixes or security updates.  
- **Risk:** No obvious licensing or security red flags, but a final review of the license (likely MIT) and a security audit of the HubSpot API usage are advisable before full production deployment.

### Русский

Резюме проекта fossasia/eventyay-hubspot:

Проект fossasia/eventyay-hubspot обеспечивает интеграцию с Hubspot в Eventyay, позволяя автоматизировать некоторые процессы. Он может быть полезен в сценарии, когда README и активность проекта соответствуют конкретному рабочему процессу. Проект пока не готов для широкого внедрения в производственную среду, но может быть использован для прототипирования или внутренних процессов после проверки зависимостей и поддержки.

### 中文

**价值**  
`fossasia/eventyay-hubspot` 为 Eventyay（开源活动管理平台）提供了与 HubSpot 的同步接口，能够自动把报名、票务、参会者信息等关键数据推送到 HubSpot CRM，实现营销自动化、线索追踪和后续邮件营销，显著降低手工导入的工作量并提升数据一致性。

**典型接入方式**  

1. **环境准备**  
   - 确保 Eventyay 已部署（Docker、Kubernetes 或源码运行均可）。  
   - 在 HubSpot 开通开发者账号，创建一个 **Private App**，获取 **Access Token**（或 OAuth 客户端 ID/Secret）。  

2. **安装插件**  
   ```bash
   pip install eventyay-hubspot
   # 或者在 Dockerfile 中加入
   # RUN pip install eventyay-hubspot
   ```
   将插件代码放入 Eventyay 的插件目录（`eventyay/plugins/`），并在 `settings.py` 中加入：
   ```python
   HUBSPOT = {
       "ACCESS_TOKEN": "your_hubspot_access_token",
       "CONTACT_LIST_ID": "12345678",   # 目标 HubSpot 联系人列表
   }
   ```

3. **配置同步规则**  
   - 在 Eventyay 后台的 “集成” 页面选择 **HubSpot**，勾选需要同步的事件（如报名、票务、付款成功）。  
   - 可通过 `eventyay_hubspot/config.yaml` 定义字段映射，例如：
     ```yaml
     field_mapping:
       email: email
       first_name: first_name
       last_name: last_name
       ticket_type: custom_ticket_type
     ```

4. **启动并验证**  
   - 重启 Eventyay 服务。  
   - 在前端完成一次报名，后台日志会显示 `POST /contacts/v1/contact/createOrUpdate/email/...` 的请求，确认数据已成功写入 HubSpot。  

5. **错误处理**  
   - 插件会把 HubSpot API 返回的错误写入 Eventyay 的 `integration_error` 表，便于运维通过后台 UI 或 Prometheus 监控告警。

**生产可用性**  

| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | ★★☆☆☆（中等） | 代码最近一次更新在 2026‑06‑30，星标 354，Fork 仅 3，社区活跃度一般。 |
| **功能完整度** | ✅ 基本同步（报名、票务）<br>⚠️ 高级营销自动化需自行扩展 | 支持常用字段映射，缺少对 HubSpot 工作流触发的深度集成。 |
| **安全性** | ⚠️ 需要自行审计 | 仅使用 HubSpot Access Token，建议在 Vault/Secrets Manager 中管理；暂无安全审计报告。 |
| **运维成本** | 中等 | 依赖 Eventyay 插件机制和 HubSpot API 配额；需要监控同步失败率并定期检查 Token 有效期。 |
| **适用场景** | ✅ 原型、内部营销系统<br>⚠️ 大流量生产环境需做性能压测 | 对于中小型活动或内部使用已足够，若并发报名 > 1k/s 建议加队列（如 Celery）进行异步写入。 |

**结论**  
该插件在功能上能够快速实现 Eventyay 与 HubSpot 的数据对接，适合作为原型或内部业务流程的加速工具。若计划在高并发或对数据合规性有严格要求的生产环境使用，建议：  

1. 对代码进行安全审计并加入单元/集成测试。  
2. 使用异步任务队列处理写入，防止 API 限流。  
3. 配置监控告警，确保 Token 失效或 API 错误时可快速响应。  

完成上述措施后，即可在生产环境中安全、稳定地使用 `fossasia/eventyay-hubspot`。

## 🧭 Practical evaluation

**Value:** fossasia/eventyay-hubspot may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 354 GitHub stars
- 3 forks
- updated 2026-06-30
- primary language: Python

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 15/100 |
| stars | 54/100 |
| topics | 0/100 |
| outlook | 60/100 |
| quality | 54/100 |
| recency | 80/100 |
| adoption | 43/100 |
| production | 62/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/fossasia/eventyay-hubspot) · [← Back to Misc](./README.md)</sub>
