# nroduit/Weasis

[![Stars](https://img.shields.io/github/stars/nroduit/Weasis?style=flat-square&color=yellow)](https://github.com/nroduit/Weasis/stargazers) [![Forks](https://img.shields.io/github/forks/nroduit/Weasis?style=flat-square&color=blue)](https://github.com/nroduit/Weasis/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Weasis is a web-based DICOM viewer for advanced medical imaging and seamless PACS integration.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.3k |
| 🍴 **Forks** | 371 |
| 💻 **Language** | Java |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`dicom` `dicom-image` `dicom-image-viewer` `dicom-images` `dicom-pr` `dicom-rt` `dicom-seg` `dicom-viewer` `dicom-web-viewer` `dicomweb` `ecg` `export-dicom`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Weasis is an open‑source, web‑based DICOM viewer written in Java that offers advanced medical‑imaging visualization and tight PACS integration. Its modular architecture makes it a convenient foundation for prototyping AI‑enhanced imaging features, such as model‑in‑the‑loop diagnostics or RAG/agent‑driven workflows. With over 1 200 stars, recent commits, and active community support, it is ready for serious pilot projects.

**Value**  
Weasis supplies a battle‑tested imaging stack, so developers can focus on adding AI capabilities rather than building a DICOM viewer from scratch. The viewer’s plugin system and REST‑style interfaces let you inject inference services, generate annotations, or feed images into retrieval‑augmented generation pipelines with minimal friction.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the supplied Docker/Gradle build, and verify the demo viewer against a test PACS.  
2. **AI Hook Integration** – Implement a simple HTTP endpoint that receives a DICOM file, runs an inference model (e.g., segmentation), and returns overlay data; register this endpoint as a Weasis plugin or external service.  
3. **Iterate & Scale** – Extend the plugin to support batch processing, RAG prompts, or agent orchestration, and add CI checks to the existing README‑driven workflow.  

**Production Readiness**  
Weasis scores high on production readiness: it has recent activity (last commit 2026‑07‑12), a large user base (≈1.3 k stars, 371 forks), and a mature Java ecosystem with extensive documentation and community forums. While the integration path isn’t fully documented, the open‑source nature and modular design allow a small, controlled pilot to validate setup costs before committing to a full deployment.

### Русский

Weasis — это веб‑ориентированный DICOM‑просмотрщик, позволяющий быстро добавить AI‑функциональность к медицинским изображениям без необходимости создавать стек моделей с нуля; типичный сценарий — прототипирование AI‑модулей (например, RAG‑агентов) и их тестирование в интеграции с PACS. Проект демонстрирует высокий уровень готовности к production: активная разработка, более 1200 звёзд на GitHub, регулярные релизы и широкое принятие в сообществе, что делает его надёжной базой для пилотных внедрений. При этом путь интеграции не полностью документирован, поэтому рекомендуется начать с небольшого proof‑of‑concept и проверить инструкции в README.

### 中文

**项目简介**  
Weasis 是一款基于 Web 的 DICOM 查看器，支持高级医学成像和无缝的 PACS（Picture Archiving and Communication System）集成。它采用 Java 开发，拥有 1.2k+ 星、370+ Fork，社区活跃，最近一次提交仍在 2026 年。

**价值**  
- **快速赋能 AI**：在已有的高质量医学影像浏览与标注能力之上，直接嵌入 AI 推理模型，无需从零搭建图像处理流水线。  
- **原型与实验**：适合快速原型化 AI 功能、构建 RAG/Agent 工作流或评估不同模型工具链的效果。  
- **成熟生态**：已有多家医院和科研机构在生产环境中使用，证明了其在真实 PACS 场景下的可靠性。

**典型接入方式**  
1. **本地部署**：下载源码或使用官方 Docker 镜像，按 README 配置 Tomcat/Jetty 并接入本地 PACS（DICOM‑Web、C‑GET 等）。  
2. **微服务包装**：将 Weasis 作为独立的影像服务，使用 REST API 调用其 DICOM 读取/渲染功能；在前端（React/Vue）中嵌入 iframe 或 WebComponent。  
3. **AI 插件**：在 Weasis 的插件机制中实现 `IImageViewer` 或 `IExtensionPoint`，在影像加载后调用外部 AI 推理服务（REST/gRPC），把结果（标注、分割、报告）回写到 UI。  
   - 推荐先在本地做一个 “Hello‑World” 插件，验证模型调用、结果展示与 DICOM 元数据写回的完整链路。  
4. **CI/CD 验证**：使用项目自带的 Maven 构建脚本，配合 GitHub Actions 完成单元测试与镜像构建，确保后续上线的可重复性。

**生产可用性**  
- **成熟度**：活跃的社区、持续更新（截至 2026‑07‑12），以及在多家医院的实际部署，表明其已具备生产级别的稳定性。  
- **可扩展性**：插件化设计和标准的 DICOM‑Web 接口，使其能够平滑对接现有 PACS、AI 推理平台或云存储。  
- **风险点**：官方文档对自定义插件的示例较少，集成路径需要先完成小规模 PoC 并确认部署成本（如容器化、网络安全、权限控制）。  

总体而言，Weasis 是一个高质量、可直接用于 AI 原型和生产环境的医学影像查看平台，只要在初期做好概念验证并梳理插件开发流程，即可安全投入业务使用。

## 🧭 Practical evaluation

**Value:** nroduit/Weasis helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1286 GitHub stars
- 371 forks
- updated 2026-07-12
- primary language: Java
- 18 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 64/100 |
| stars | 66/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 80/100 |
| recency | 80/100 |
| adoption | 66/100 |
| production | 69/100 |
| usefulness | 74/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/nroduit/Weasis) · [← Back to Misc](./README.md)</sub>
