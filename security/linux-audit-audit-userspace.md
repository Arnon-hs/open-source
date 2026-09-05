# linux-audit/audit-userspace

[![Stars](https://img.shields.io/github/stars/linux-audit/audit-userspace?style=flat-square&color=yellow)](https://github.com/linux-audit/audit-userspace/stargazers) [![Forks](https://img.shields.io/github/forks/linux-audit/audit-userspace?style=flat-square&color=blue)](https://github.com/linux-audit/audit-userspace/network) [![Language](https://img.shields.io/badge/lang-C-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> Linux audit userspace repository

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 714 |
| 🍴 **Forks** | 237 |
| 💻 **Language** | C |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`linux` `logging` `security`

## 🎯 Categories

Security

## 📝 Summary

### English

Here's a brief summary of the linux-audit/audit-userspace project:

The linux-audit/audit-userspace project is an open-source repository that helps developers catch security and privacy issues earlier in the workflow by providing a robust auditing system. This project strengthens security checks, adds authentication or privacy controls, and audits potential risks earlier, making it a valuable tool for developers looking to enhance their application's security. However, its adoption requires manual inspection and validation of setup costs due to sparse integration signals.

**Value:** The project's value lies in its ability to catch security and privacy issues earlier, making it easier to strengthen security checks and add authentication or privacy controls. This can lead to a more secure and reliable application.

**Practical Adoption Path:**

1. **Manual Inspection**: Before adopting the project, it's essential to manually inspect the code and understand how it integrates with your application.
2. **Dependency and Maintenance Checks**: Perform thorough dependency and maintenance checks to ensure that the project is compatible with your existing infrastructure.
3. **Prototype or Internal Workflow**: Start by using the project in a prototype or internal workflow to test its functionality and identify potential issues.
4. **Production Readiness**: Once you're satisfied with the project's performance, you can move it to production, but be prepared

### Русский

**linux-audit/audit-userspace** — это открытый репозиторий пользовательского пространства для подсистемы аудита Linux, позволяющий обнаруживать потенциальные уязвимости и нарушения конфиденциальности уже на ранних этапах разработки. Его обычно подключают в прототипы или внутренние CI‑pipeline для автоматических проверок безопасности и контроля доступа, однако перед внедрением требуется ручная оценка интеграции из‑за ограниченной документированности сигналов. Проект имеет умеренную готовность к production: достаточно стабилен для экспериментов, но требует проверки зависимостей и обслуживания перед использованием в продакшене.

### 中文

**项目简介**  
linux-audit/audit‑userspace 是 Linux 审计子系统的用户空间实现，提供一套 C 语言库和工具，用于在应用层捕获、解析和处理内核审计事件。它帮助开发者在代码提交、CI/CD 或运行时阶段提前发现安全与隐私风险。

**价值**  
- **提前发现风险**：通过实时读取内核审计日志，可在业务流程的早期阶段检测异常行为、未授权访问和隐私泄露。  
- **可定制的安全控制**：提供 API 供业务系统自行添加审计规则、权限校验或合规报告，降低后期整改成本。  
- **开源且活跃**：拥有 714 星、237 Fork，社区持续维护，代码基于 C 语言，易于嵌入已有的 Linux 服务。

**典型接入方式**  
1. **依赖安装**：在目标机器上编译或通过发行版的 `audit-userspace` 包安装库和二进制（如 `ausearch`, `aureport`）。  
2. **审计规则配置**：使用 `auditctl`（或 `augenrules`）在内核层定义要捕获的系统调用、文件、网络等事件。  
3. **集成 SDK**：在业务代码中链接 `libaudit`，调用 `audit_open()`, `audit_get_reply()` 等函数读取审计记录并进行自定义过滤或上报。  
4. **CI/CD 插件**：在构建流水线中加入审计检查脚本，自动生成合规报告或触发安全警报。  

**生产可用性**  
- **成熟度**：中等（Medium）。项目已在多个内部项目和原型中验证，可支撑业务原型或内部安全平台。  
- **准备工作**：在正式投产前需完成以下检查：  
  - 确认内核审计子系统已启用并与业务系统兼容。  
  - 评估审计规则的覆盖范围与性能影响（审计大量系统调用会增加 I/O）。  
  - 编写或审阅集成代码的错误处理与日志轮转机制。  
- **运维要求**：需要定期审计日志的归档、压缩和权限管理，防止审计数据本身成为泄露点。  

总体而言，audit‑userspace 适合作为安全审计的底层组件，在原型验证或内部合规平台中快速落地；在生产环境使用时，只要做好规则调优和运维流程，即可达到稳定可靠的水平。

## 🧭 Practical evaluation

**Value:** linux-audit/audit-userspace helps catch security and privacy issues earlier in the workflow.

**Best use cases**

- strengthen security checks
- add auth or privacy controls
- audit risk earlier

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 714 GitHub stars
- 237 forks
- updated 2026-06-30
- primary language: C
- 3 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 59/100 |
| stars | 61/100 |
| topics | 38/100 |
| outlook | 65/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 60/100 |
| production | 65/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/linux-audit/audit-userspace) · [← Back to Security](./README.md)</sub>
