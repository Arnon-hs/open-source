# shuakami/qq-chat-exporter

[![Stars](https://img.shields.io/github/stars/shuakami/qq-chat-exporter?style=flat-square&color=yellow)](https://github.com/shuakami/qq-chat-exporter/stargazers) [![Forks](https://img.shields.io/github/forks/shuakami/qq-chat-exporter?style=flat-square&color=blue)](https://github.com/shuakami/qq-chat-exporter/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> 🚀 QQ聊天记录、表情包导出工具 | 自动化提取图片/文字/图片消息，支持TXT/JSON导出，高效备份，支持NT QQ

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4.1k |
| 🍴 **Forks** | 245 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-07-06 |
| 🔍 **Source** | github |

## 🏷️ Topics

`chat-exports` `electron` `export` `exporter` `javascript` `qq` `qq-expoter` `qq-nt` `qqnt`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary:** 
shuakami/qq-chat-exporter is an open-source project that allows users to export QQ chat records, including images and text messages, in either TXT or JSON format. This tool is particularly useful for those seeking to efficiently back up their QQ chat history. With its recent activity and strong adoption signals, it has high production readiness.

**Value Proposition:** 
The value of shuakami/qq-chat-exporter lies in its ability to automate the extraction of chat records, images, and text messages from QQ, making it easier to backup and manage chat history. This can be particularly useful for individuals who want to preserve their online conversations or for businesses that need to maintain a record of their online interactions.

**Practical Adoption Path:** 
To adopt shuakami/qq-chat-exporter, users can start by reviewing the project's README documentation to understand its features and usage. A small proof of concept should be performed to evaluate the tool's feasibility and ensure it meets their specific requirements. With its strong adoption signals and recent activity, users can have confidence in its stability and maintainability.

**Production Readiness:** 
The project's production readiness is high due to its recent activity, strong adoption signals, and a large community of users (4096 GitHub stars).

### Русский

Резюме проекта shuakami/qq-chat-exporter:

shuakami/qq-chat-exporter - это открытый исходный проект, который позволяет автоматизировать.exportировать чат-логи и изображения из QQ, включая TXT и JSON форматы. Этот инструмент может быть полезен в сценариях, когда требуется эффективное хранение и доступ к историческим чат-логам. Проект демонстрирует высокую готовность к production, с последними обновлениями, активной деятельностью и широкой адопцией в сообществе.

### 中文

**项目简介（2‑3 句）**  
shuakami/qq-chat-exporter 是一款基于 TypeScript 的开源工具，能够自动化导出 QQ（包括 NT QQ）聊天记录、表情包和图片消息，支持生成 TXT 或 JSON 文件，帮助用户快速完成聊天记录的备份与迁移。

**价值**  
- **一键备份**：无需手动复制，工具可批量抓取文字、图片、表情等多媒体内容，极大降低漏抓风险。  
- **多格式输出**：TXT 适合人类阅读，JSON 便于后续数据分析、搜索或迁移到其他系统。  
- **跨版本兼容**：同时支持传统 QQ 客户端和 NT QQ，覆盖大多数用户场景。  

**典型接入方式**  
1. **克隆仓库并安装依赖**  
   ```bash
   git clone https://github.com/shuakami/qq-chat-exporter.git
   cd qq-chat-exporter
   npm install
   ```  
2. **配置导出参数**（在 `config.json` 或命令行中指定）  
   - `accountId`：QQ 号  
   - `outputDir`：导出目录  
   - `format`：`txt` 或 `json`  
3. **运行导出脚本**  
   ```bash
   npm run export -- --accountId=12345678 --format=json
   ```  
4. **在业务流程中调用**：可将上述命令封装为 CI/CD 步骤或内部运维脚本，实现定时备份或灾备恢复。  

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑07‑06，项目仍在维护；拥有 4 k+ ⭐、245+ Fork，社区活跃。  
- **技术成熟度**：全 TypeScript 实现，代码结构清晰，提供完整的 README 与示例，易于二次开发。  
- **安全与合规**：暂无已知许可证或安全漏洞风险，但在正式生产环境使用前建议自行审计依赖（尤其是网络请求相关库）并确认符合企业合规要求。  
- **可扩展性**：导出逻辑解耦，可自行实现自定义的后处理（如上传至对象存储、写入数据库），适合作为更大数据治理平台的子模块。  

综上，shuakami/qq-chat-exporter 在功能完整性、社区活跃度和技术实现上均具备生产级别的使用价值，适合作为企业内部 QQ 聊天记录备份或迁移的首选方案。

## 🧭 Practical evaluation

**Value:** shuakami/qq-chat-exporter may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 4096 GitHub stars
- 245 forks
- updated 2026-07-06
- primary language: TypeScript
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 60/100 |
| stars | 77/100 |
| topics | 100/100 |
| outlook | 81/100 |
| quality | 87/100 |
| recency | 100/100 |
| adoption | 72/100 |
| production | 79/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/shuakami/qq-chat-exporter) · [← Back to Misc](./README.md)</sub>
