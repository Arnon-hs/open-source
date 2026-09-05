# zowe/zowe-explorer-vscode

[![Stars](https://img.shields.io/github/stars/zowe/zowe-explorer-vscode?style=flat-square&color=yellow)](https://github.com/zowe/zowe-explorer-vscode/stargazers) [![Forks](https://img.shields.io/github/forks/zowe/zowe-explorer-vscode?style=flat-square&color=blue)](https://github.com/zowe/zowe-explorer-vscode/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Visual Studio Code Extension for Zowe, which lets users interact with z/OS Data Sets, Unix System Services, and Jobs on a remote mainframe instance. Powered by Zowe SDKs.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 188 |
| 🍴 **Forks** | 112 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary (2‑3 sentences)**  
The *zowe/zowe‑explorer‑vscode* extension brings Zowe’s mainframe APIs into Visual Studio Code, letting developers browse, edit, and submit z/OS data sets, USS files, and jobs from a remote mainframe. Built on the Zowe SDKs and written in TypeScript, it provides a ready‑made UI layer that can be extended with AI/ML capabilities such as RAG or agent‑driven workflows without starting from scratch. With ~190 stars, active recent commits, and a modest dependency footprint, it is a practical starting point for prototyping AI‑enhanced mainframe tooling.

**Value**  
- **Accelerates AI integration** – the extension already abstracts the low‑level Zowe APIs, so you can focus on adding AI features (e.g., code‑completion, intelligent job‑status prediction, or RAG over data‑set contents) rather than building a mainframe connector.  
- **Unified developer experience** – developers stay inside VS Code, reducing context‑switching and enabling rapid iteration on AI‑driven prototypes.  
- **Open‑source and extensible** – the TypeScript codebase is easy to fork or contribute to, and the Zowe SDKs are well‑documented, lowering the barrier to custom model deployment.

**Practical adoption path**  
1. **Proof‑of‑concept** – clone the repo, run the extension locally (follow the README), and verify connectivity to a test mainframe instance.  
2. **Add AI layer** – integrate your preferred model (e.g., OpenAI, Hugging Face) behind the existing command handlers or create new VS Code commands that call the model for suggestions, RAG, etc.  
3. **Iterate & test** – use the built‑in VS Code debugging tools to validate AI responses against real data‑sets and jobs.  
4. **Package & distribute** – once stable, publish a custom VS Code marketplace entry or bundle the extension with your internal tooling.

**Production readiness**  
- **Maturity** – medium. The extension is actively maintained (last update 2026‑05‑12) and has a modest user base, making it suitable for internal prototypes or limited‑scope production use.  
- **Dependencies** – relies on Zowe SDKs and standard VS Code APIs; a review of version compatibility and security advisories is recommended before wider rollout.  
- **Operational considerations** – ensure mainframe credentials are managed securely (e.g., via VS Code secret storage or external vaults) and perform a brief security audit of any added AI services.  
- **Scalability** – for high‑volume or mission‑critical workloads, you’ll likely need to harden the extension (logging, error handling) and possibly host the AI inference layer behind a controlled service.  

Overall, *zowe‑explorer‑vscode* offers a solid, low‑friction foundation for adding AI capabilities to mainframe development workflows, with a clear path from prototype to production after the usual dependency and security vetting.

### Русский

**zowe/zowe-explorer-vscode** — это расширение VS Code, позволяющее разработчикам напрямую работать с наборами данных, UNIX‑службами и заданиями z/OS через Zowe SDK. Оно удобно для быстрого прототипирования AI‑фич, создания RAG‑ и агентных воркфлоу, а также оценки инструментов моделей, при этом первый шаг внедрения рекомендуется оформить как небольшой proof‑of‑concept с проверкой README и зависимостей. Проект находится на среднем уровне готовности к production: достаточно стабилен для внутренних прототипов, но требует дополнительного аудита лицензий, безопасности и поддержки перед масштабным использованием.

### 中文

**项目价值**  
zowe‑explorer‑vscode 为 VS Code 提供了与远程 z/OS 主机交互的统一入口，开发者可以在编辑器中直接浏览、编辑、上传/下载 Data Sets、USS 文件以及提交、监控 Job。借助 Zowe SDK，它把传统的 mainframe 操作流程搬到现代 IDE，极大降低了运维和开发人员的学习成本，并为在主机上快速原型化 AI/ML 功能（如 RAG、Agent）提供了现成的 API 与 UI 支持。

**典型接入方式**  
1. **插件安装**：在 VS Code 市场搜索 “Zowe Explorer” 或直接执行 `code --install-extension zowe.zowe-explorer-vscode`。  
2. **配置连接**：在插件侧栏点击 “Add Connection”，填写主机地址、端口、用户名/密码（或使用 SSH Key），保存后即可看到远程 Data Sets、USS、Jobs。  
3. **调用 SDK**：插件内部基于 Zowe SDK（Node/TS），如果需要在自定义脚本或扩展中复用，只需在项目中 `npm install @zowe/cli`、`@zowe/sdk`，使用与插件相同的连接配置即可调用 `List`, `Get`, `Put`, `Submit` 等 API。  
4. **原型 AI 功能**：在 VS Code 中打开 Data Set/USS 文件，结合本地 LLM（如 OpenAI、Claude）或自建模型，实现“从文件直接生成查询/分析代码”或“基于 Job 输出进行 RAG 检索”，无需额外搭建主机侧服务。

**生产可用性**  
- **成熟度**：GitHub ★188、Fork ★112，2026‑05‑12 最近一次提交，活跃度尚可。  
- **适用场景**：适合内部工具、原型开发、CI/CD 流水线中对主机资源的自动化操作；对外部面向客户的生产系统仍需进行安全审计（许可证、依赖漏洞）和运维监控。  
- **风险与准备**：目前未发现重大元数据泄露风险，但仍需检查 OSS 许可证兼容性、依赖的安全报告以及维护者响应速度。建议先在小范围 PoC（例如单机测试环境）验证功能、性能与安全后，再推广至生产环境。  

总体而言，zowe‑explorer‑vscode 能快速把 mainframe 资源引入现代开发流程，尤其在需要结合 AI/ML 的场景下，可作为低成本的原型平台；在完成安全与运维评估后，可进入生产级别使用。

## 🧭 Practical evaluation

**Value:** zowe/zowe-explorer-vscode helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 188 GitHub stars
- 112 forks
- updated 2026-05-12
- primary language: TypeScript

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 48/100 |
| topics | 0/100 |
| outlook | 62/100 |
| quality | 57/100 |
| recency | 80/100 |
| adoption | 49/100 |
| production | 66/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/zowe/zowe-explorer-vscode) · [← Back to Misc](./README.md)</sub>
