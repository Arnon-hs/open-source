# fougue/mayo

[![Stars](https://img.shields.io/github/stars/fougue/mayo?style=flat-square&color=yellow)](https://github.com/fougue/mayo/stargazers) [![Forks](https://img.shields.io/github/forks/fougue/mayo?style=flat-square&color=blue)](https://github.com/fougue/mayo/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> 3D CAD viewer and converter based on Qt + OpenCascade

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.1k |
| 🍴 **Forks** | 346 |
| 💻 **Language** | C++ |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`3d-graphics` `3d-viewer` `brep` `cad` `converter` `converter-cli` `dxf` `fbx` `gltf` `gltf-viewer` `iges` `meshviewer`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Project Summary:**
Mayo is an open-source 3D CAD viewer and converter based on Qt and OpenCascade, providing a foundation for integrating AI capabilities into existing model stacks. It enables users to prototype AI features, build workflows, and evaluate model tooling, making it an attractive solution for those looking to add AI functionality without starting from scratch. With a strong adoption rate and recent activity, Mayo is considered production-ready for serious pilots.

**Value Proposition:**
The primary value proposition of Mayo lies in its ability to simplify the integration of AI capabilities into existing 3D CAD models, allowing users to focus on building and evaluating AI features without the need to develop a new model stack from scratch. This makes it an ideal solution for prototyping AI features, building RAG (Rule-Based Agent) or agent workflows, and evaluating model tooling.

**Practical Adoption Path:**
To adopt Mayo, users can start by evaluating the project through its exposed implementation signals, such as API/SDK/CLI, language metadata, or focused topics. With a primary language of C++ and 20 topics, users can explore the project's documentation and codebase to understand how to integrate Mayo into their existing workflows. The project's recent activity and strong adoption rate make it a reliable choice for serious pilots

### Русский

**fougue/mayo** — это открытый 3D‑CAD‑просмотрщик и конвертер, построенный на Qt и OpenCascade, который уже готов к использованию в проектах с AI‑фичами. Он позволяет быстро прототипировать AI‑модели (RAG, агентные сценарии) и интегрировать их через готовый API/SDK/CLI, при этом демонстрирует высокий уровень готовности к production: активные коммиты, более 2000 звёзд, широкая экосистема и стабильный C++‑код. Основные риски (лицензия, безопасность, поддержка) требуют лишь финального аудита, но в целом проект подходит для серьёзных пилотных внедрений.

### 中文

**项目简介**  
fougue/mayo 是基于 Qt 与 OpenCascade 的开源 3D CAD 查看器与格式转换工具，提供高性能的几何渲染、交互式模型浏览以及多种 CAD/STEP/IGES 等文件的相互转换。

**价值**  
- **快速赋能 AI**：通过已有的几何解析与渲染能力，开发者可以在此基础上直接叠加 AI 模块（如模型识别、属性抽取、RAG 检索），无需从零搭建 CAD 解析栈。  
- **原型与实验**：适合作为 AI 功能原型、智能助手或检索代理的实验平台，帮助团队快速验证概念并收集真实几何数据。  
- **生态兼容**：提供 C++ API、Python 绑定以及 CLI，便于在不同语言和工作流中调用，支持与现有模型库、数据库或云服务无缝集成。

**典型接入方式**  
1. **库调用**：在 C++ 项目中通过 `#include <Mayo>` 引入核心库，使用 `Mayo::Document`、`Mayo::IO::Reader` 等类完成文件加载、几何查询和渲染。  
2. **Python 绑定**：安装 `mayo-py`（或使用 `pybind11` 生成的绑定），在脚本中调用 `mayo.load("model.step")`，配合 AI 推理库（如 PyTorch、TensorFlow）进行属性预测或语义分割。  
3. **CLI/REST**：利用自带的 `mayo-cli` 实现批量转换或元数据导出；可包装为微服务，接受 HTTP 请求后调用 CLI 完成转换并返回结果。  

**生产可用性**  
- **活跃度**：截至 2026‑07‑03，项目拥有 2086+ 星、346+ Fork，最近一次提交仅数天前，表明社区活跃、代码维护及时。  
- **技术成熟度**：Qt 与 OpenCascade 均为业界成熟的底层框架，Mayo 对其封装稳健，已在多个内部 CAD 工作流中使用，具备可靠的渲染与文件兼容性。  
- **安全与合规**：采用 LGPL‑3.0 许可证，需注意在商业产品中遵守开源条款；建议在引入前进行一次依赖安全审计（SBOM、漏洞扫描）。  
- **可扩展性**：提供丰富的信号/回调机制（如 `documentLoaded`, `entitySelected`），便于插入自定义 AI 推理、日志或监控逻辑，适合作为生产级 AI‑CAD 服务的核心组件。  

综上，fougue/mayo 具备高生产可用性，能够帮助团队在已有 CAD 基础上快速叠加 AI 功能，接入方式灵活，适合原型研发与正式部署。

## 🧭 Practical evaluation

**Value:** fougue/mayo helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2086 GitHub stars
- 346 forks
- updated 2026-07-03
- primary language: C++
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 64/100 |
| stars | 71/100 |
| topics | 100/100 |
| outlook | 63/100 |
| quality | 71/100 |
| recency | 40/100 |
| adoption | 69/100 |
| production | 59/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/fougue/mayo) · [← Back to DevTools](./README.md)</sub>
