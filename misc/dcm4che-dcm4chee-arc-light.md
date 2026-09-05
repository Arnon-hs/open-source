# dcm4che/dcm4chee-arc-light

[![Stars](https://img.shields.io/github/stars/dcm4che/dcm4chee-arc-light?style=flat-square&color=yellow)](https://github.com/dcm4che/dcm4chee-arc-light/stargazers) [![Forks](https://img.shields.io/github/forks/dcm4che/dcm4chee-arc-light?style=flat-square&color=blue)](https://github.com/dcm4che/dcm4chee-arc-light/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> DICOM Archive J2EE application

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 491 |
| 🍴 **Forks** | 283 |
| 💻 **Language** | Java |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
dcm4che/dcm4chee‑arc‑light is an open‑source, J2EE‑based DICOM archive that provides storage, retrieval, query/retrieve (C‑GET/C‑MOVE), and basic work‑list services for medical imaging workflows. With a mature Java codebase (≈ 500 ★, 300 forks) and recent activity, it can serve as a foundation for internal PACS prototypes or niche integration projects, provided the team is prepared to invest time in configuration and validation.

**Value**  
- **Comprehensive DICOM support** – Implements the full set of DICOM networking and storage SOP classes, letting you build a standards‑compliant archive without writing low‑level protocol code.  
- **Java/J2EE ecosystem** – Fits naturally into existing Java EE stacks, enabling reuse of familiar tools (e.g., Spring, JPA, application servers) and simplifying custom extensions such as metadata enrichment or study‑level indexing.  
- **Active community & extensibility** – The project’s fork/star count and recent commits indicate ongoing maintenance; the modular architecture allows plug‑ins for HL7, DICOMweb, or custom authentication mechanisms.

**Practical Adoption Path**  
1. **Initial assessment** – Clone the repository, run the provided Docker compose or Maven‑based setup, and verify basic C‑STORE/C‑FIND operations against a test modality.  
2. **Environment alignment** – Deploy to an application server matching your organization’s standards (e.g., WildFly, Tomcat) and configure the database (PostgreSQL/MySQL) and TLS certificates.  
3. **Workflow mapping** – Map your existing imaging workflow to the archive’s services (e.g., define AE titles, storage policies, and study retention rules).  
4. **Customization & integration** – Add any required adapters (HL7 order integration, DICOMweb REST, or PACS UI) using the documented extension points.  
5. **Testing & validation** – Run conformance tests (DCMTK, IHE profiles) and perform load testing to gauge performance under expected study volumes.  

**Production Readiness**  
- **Maturity:** Medium. The codebase is stable and actively maintained, but documentation around deployment best‑practices and scaling guidelines is limited.  
- **Risk:** Integration effort is non‑trivial; the lack of detailed “quick‑start” guides means you’ll need to allocate time for manual configuration, security hardening, and performance tuning.  
- **Recommendation:** Suitable for prototypes, research environments, or internal departmental PACS where you can afford a modest setup cost and ongoing maintenance. For large‑scale, mission‑critical production, conduct a thorough pilot, verify compliance with IHE/HL7 standards, and consider a commercial support contract or a more turnkey solution.

### Русский

dcm4che/dcm4chee-arc-light — это open‑source J2EE‑приложение для архивации DICOM‑изображений, позволяющее развернуть PACS‑сервер с поддержкой стандартных DICOM‑операций (C‑STORE, C‑FIND, C‑MOVE и т.п.) и интеграции в существующие клинические системы. Оно подходит для прототипов и внутренних рабочих процессов, где требуется гибкая настройка и расширяемость, но перед вводом в продакшн необходимо провести детальный аудит установки, зависимостей и поддержки, так как путь интеграции из метаданных не очевиден. При должной проверке проекта он обеспечивает средний уровень готовности к production и может стать надёжным ядром DICOM‑инфраструктуры.

### 中文

**dcm4che/dcm4chee-arc-light 简介**

dcm4che/dcm4chee-arc-light 是一个开源 DICOM 框架，提供 DICOM 档案 J2EE 应用。它可以用于 DICOM 文件的存储和管理。

**价值**

dcm4che/dcm4chee-arc-light 的价值在于，它可以帮助开发人员快速构建 DICOM 应用，提高工作效率。它的使用场景包括 DICOM 文件的存储、检索和管理。

**典型接入方式**

由于 dcm4che/dcm4chee-arc-light 的 README 和活动信息较少，因此需要手动检查和测试才能确定其接入方式。一般来说，开发人员需要按照 README 中的指示进行配置和部署。

**生产可用性**

dcm4che/dcm4chee-arc-light 的生产可用性为中等水平。它可以用于内部工作流和原型开发，但在生产环境中需要进行依赖检查和维护检查，以确保其稳定性和安全性。

## 🧭 Practical evaluation

**Value:** dcm4che/dcm4chee-arc-light may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 491 GitHub stars
- 283 forks
- updated 2026-07-03
- primary language: Java

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 61/100 |
| stars | 57/100 |
| topics | 0/100 |
| outlook | 61/100 |
| quality | 61/100 |
| recency | 80/100 |
| adoption | 58/100 |
| production | 63/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/dcm4che/dcm4chee-arc-light) · [← Back to Misc](./README.md)</sub>
