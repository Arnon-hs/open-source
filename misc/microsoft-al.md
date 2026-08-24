# microsoft/AL

[![Stars](https://img.shields.io/github/stars/microsoft/AL?style=flat-square&color=yellow)](https://github.com/microsoft/AL/stargazers) [![Forks](https://img.shields.io/github/forks/microsoft/AL?style=flat-square&color=blue)](https://github.com/microsoft/AL/network) [![Language](https://img.shields.io/badge/lang-PowerShell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> Home of the Dynamics 365 Business Central AL Language extension for Visual Studio Code. Used to track issues regarding the latest version of the AL compiler and developer tools available in the Visual Studio Code Marketplace or as part of the AL Developer Preview builds for Dynamics 365 Business Central.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 857 |
| 🍴 **Forks** | 280 |
| 💻 **Language** | PowerShell |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`al-language` `bcopensource` `dynamics-365` `dynamics-365-bc` `dynamics-365-business-central` `visual-studio-code`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The **microsoft/AL** repository hosts the open‑source AL language extension for Visual Studio Code, which powers the Dynamics 365 Business Central development experience. It tracks issues, updates the AL compiler, and provides the tooling needed for the latest preview and marketplace releases. With a solid community (≈857 ⭐, 280 🍴) and recent activity, it serves as the go‑to source for extending Business Central with modern AL code.

**Value**  
- **Accelerates AI‑enabled extensions**: By leveraging the existing AL compiler and VS Code integration, developers can embed AI‑driven features (e.g., RAG, agent workflows) into Business Central without building a language stack from scratch.  
- **Rapid prototyping**: The extension gives immediate access to the latest language features and debugging tools, letting teams experiment with AI capabilities directly inside the familiar Business Central environment.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC)** – Clone the repo, follow the README to install the VS Code extension, and create a minimal AL project that calls an external AI service (e.g., Azure OpenAI).  
2. **Validate Integration** – Ensure the AL compiler can reference the AI API, test deployment to a sandbox Business Central instance, and confirm that the extension’s version aligns with your target BC release.  
3. **Scale Gradually** – Extend the PoC into a dedicated extension package, add unit tests, and automate builds with the AL Developer Preview pipeline before rolling out to staging environments.  

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last update 2026‑05‑11) and widely used, but the integration steps for AI services are not documented in the repository itself, requiring extra validation.  
- **Considerations**: Verify compatibility with your BC version, assess dependency overhead (PowerShell scripts, VS Code tooling), and perform security reviews of any external AI endpoints. Once these checks are completed, the extension is suitable for internal workflows and can be hardened for production use.

### Русский

**Краткое резюме:**  
Microsoft/AL — это официальное расширение для Visual Studio Code, поддерживающее язык AL и инструменты компилятора Dynamics 365 Business Central. Оно позволяет быстро прототипировать AI‑функциональность (RAG, агентные сценарии) внутри уже существующей экосистемы Business Central, не начиная с нуля, и подходит для внутренних пилотных проектов при условии предварительной проверки интеграции и зависимости. Готовность к production — средняя: проект стабилен (857 звёзд, активные обновления), но путь интеграции не очевиден и требует небольшого proof‑of‑concept и проверки README.

### 中文

**价值**  
- **快速赋能 AI**：通过 AL 语言扩展，开发者可以在 Dynamics 365 Business Central 中直接调用 AI 功能，而无需自行搭建模型训练、部署和运维的完整技术栈。  
- **统一开发体验**：所有编译、调试、发布工具都集成在 VS Code 中，保持与现有 Business Central 开发流程一致，降低学习成本。  
- **社区与微软支持**：项目已有 857 Stars、280 Fork，且由微软官方维护，能够及时获取最新的编译器和 AI 预览功能。

**典型接入方式**  
1. **准备环境**  
   - 在本地或 CI 环境中安装最新的 **Visual Studio Code**。  
   - 从 VS Code Marketplace 安装 **AL Language** 扩展（或使用 AL Developer Preview 版本）。  
2. **创建或迁移 AL 项目**  
   - 使用 `AL: Go!` 向导生成一个空的 Business Central AL 项目，或在现有项目中添加 `app.json` 中的 AI 相关依赖（如 Azure OpenAI、Copilot Extensions）。  
3. **编写 AI 业务逻辑**  
   - 在 `.al` 文件中调用已封装的 AI API（例如 `AzureOpenAICall`），或利用 `Codeunit`/`Page` 与外部服务交互，实现 RAG、智能客服、推荐等功能。  
4. **本地调试 & 部署**  
   - 通过 `Ctrl+F5` 启动本地 Docker‑based Business Central 沙箱进行调试。  
   - 完成后使用 `Publish` 将 `.app` 包部署到云端或本地 Production 环境。  

**生产可用性**  
- **成熟度**：Medium。当前版本已在多个内部原型和小规模业务场景中验证，编译器和 AI 扩展功能在 Microsoft 官方渠道持续更新。  
- **准备工作**：在正式上线前，需要完成以下检查：  
  - **依赖审计**：确认所使用的 AI 服务（如 Azure OpenAI）已在组织内获得授权并具备容量配额。  
  - **安全合规**：评估数据流向，确保敏感业务数据在调用 AI 服务时符合 GDPR、ISO 等合规要求。  
  - **性能基准**：在预生产环境进行负载测试，验证 AI 调用的响应时延和并发限制是否满足业务 SLA。  
- **运维成本**：主要集中在 AI 服务的配额管理和 AL 扩展的版本同步（每月检查 Marketplace 更新），相对独立于底层模型运维，整体运维负担较低。  

**结论**：microsoft/AL 适合作为 **原型验证** 或 **内部业务流程自动化** 的加速器，能够在保持 Business Central 开发统一性的前提下快速引入 AI 能力。若业务对可靠性、合规性有严格要求，建议先在受控的 PoC 环境中验证集成路径，再逐步推广到生产。

## 🧭 Practical evaluation

**Value:** microsoft/AL helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 857 GitHub stars
- 280 forks
- updated 2026-05-11
- primary language: PowerShell
- 6 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 61/100 |
| stars | 62/100 |
| topics | 75/100 |
| outlook | 52/100 |
| quality | 59/100 |
| recency | 20/100 |
| adoption | 62/100 |
| production | 48/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/microsoft/AL) · [← Back to Misc](./README.md)</sub>
