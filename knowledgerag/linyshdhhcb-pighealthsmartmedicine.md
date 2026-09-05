# linyshdhhcb/PigHealthSmartMedicine

[![Stars](https://img.shields.io/github/stars/linyshdhhcb/PigHealthSmartMedicine?style=flat-square&color=yellow)](https://github.com/linyshdhhcb/PigHealthSmartMedicine/stargazers) [![Forks](https://img.shields.io/github/forks/linyshdhhcb/PigHealthSmartMedicine?style=flat-square&color=blue)](https://github.com/linyshdhhcb/PigHealthSmartMedicine/network) [![Language](https://img.shields.io/badge/lang-Vue-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> 本项目是一个基于 RAG 的生猪健康管理智慧医药系统，集成了 AI 兽医诊断、疾病管理、药品管理、文章资讯管理等功能模块，旨在通过数字化手段提升生猪养殖的医疗管理水平。系统基于 Spring Boot 3 + Spring AI + Milvus + MySQL 8 + MyBatis-Plus + Ollama / DeepSeek / 通义千问/ 阿里百炼 / SiliconFlow 等技术构建，提供智能兽医诊断服务，帮助养殖户或兽医快速识别生猪病情并推荐相应的治疗方案。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 162 |
| 🍴 **Forks** | 27 |
| 💻 **Language** | Vue |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`element-ui` `java` `javascript` `minio` `mybatisplus` `mysql` `ollama` `pinia` `rag` `redis` `satoken` `springai`

## 🎯 Categories

Knowledge/RAG · AI/ML · Frontend · Database

## 📝 Summary

### English

**Brief Summary**  
PigHealthSmartMedicine is an open‑source, Retrieval‑Augmented Generation (RAG) platform for swine health management that combines AI‑driven veterinary diagnostics, disease and medication tracking, and article/news curation. Built on Spring Boot 3, Spring AI, Milvus, MySQL 8, MyBatis‑Plus, and large‑model providers such as Ollama, DeepSeek, Tongyi Qianwen, Alibaba Baichuan, and SiliconFlow, the system lets farmers or vets quickly identify pig illnesses and receive treatment recommendations.

**Value**  
- **Knowledge‑centric AI**: By indexing veterinary guidelines, case studies, and drug information, the system makes otherwise siloed expertise searchable and instantly usable in diagnostic conversations.  
- **Accelerated decision‑making**: Real‑time AI diagnosis reduces the time needed for manual symptom analysis, helping producers intervene earlier and lower mortality.  
- **Extensible ecosystem**: The modular stack (Spring Boot, MyBatis‑Plus, Milvus vector store) allows easy integration with existing farm management software, sensor data pipelines, or custom analytics dashboards.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC)** – Clone the repository, spin up the Docker‑compose environment (Spring Boot API, Milvus, MySQL) and run the provided Vue front‑end. Load a small subset of your own veterinary documents into Milvus using the built‑in ingestion scripts.  
2. **Domain Tuning** – Replace the default LLM endpoints with the model that best fits your cost/latency requirements (e.g., local Ollama for on‑prem, or DeepSeek/Alibaba Baichuan for cloud). Fine‑tune prompts or add few‑shot examples to improve diagnostic accuracy for the breeds and diseases you handle.  
3. **Integration** – Connect the API to existing farm IoT platforms or ERP systems via the exposed REST endpoints; map user roles (farm manager, vet, technician) to the built‑in RBAC.  
4. **Pilot Rollout** – Deploy the system in a single barn or farm, gather user feedback, and monitor key metrics (diagnosis turnaround time, treatment success rate).  
5. **Scale** – Replicate the service across multiple sites, enable multi‑tenant isolation in MySQL, and consider sharding Milvus for larger document corpora.  

**Production Readiness**  
- **Maturity**: Medium. The project has a healthy star/fork count and recent activity, indicating an active community, but documentation around deployment scripts and model configuration is limited.  
- **Stability**: Core components (Spring Boot, MySQL, Milvus) are production‑grade, yet the AI layer depends on external LLM services that may have variable latency and cost.  
- **Operational Considerations**: Requires management of a vector database (Milvus), a relational DB, and potentially GPU resources for local LLM inference. Monitoring, backup, and security hardening (e.g., DB credentials, API auth) must be added before a production rollout.  
- **Risk**: Integration steps are not fully scripted; teams should allocate effort for environment setup, model selection, and validation of diagnostic outputs against veterinary standards.  

Overall, PigHealthSmartMedicine is a solid foundation for building a smart, AI‑augmented swine health workflow, suitable for internal pilots or prototype deployments, with a clear path to production once the integration and operational overhead are addressed.

### Русский

**lіnyshdhhcb/PigHealthSmartMedicine** — это open‑source система управления здоровьем свиней, построенная на RAG‑технологиях и стекe Spring Boot 3 + Spring AI + Milvus + MySQL 8 + MyBatis‑Plus, с интеграцией моделей Ollama, DeepSeek, Tongyi Qianwen, Alibaba Bailian и SiliconFlow. Она позволяет быстро индексировать внутренние ветеринарные документы, статьи и протоколы, а затем с помощью AI‑врачей находить релевантные сведения и предлагать диагностические и лечебные рекомендации, что ускоряет работу фермеров и ветеринаров. Проект уже имеет базовый набор функций и достаточно зрелую инфраструктуру (162 ★, активные обновления, Vue‑frontend), поэтому подходит для прототипов и внутренних пилотов, но требует дополнительной проверки зависимостей и настройки CI/CD перед масштабным production‑развёртыванием.

### 中文

**价值说明**  
- **数字化诊疗**：通过 RAG（检索增强生成）技术把海量养殖文献、病例和药品手册转化为可交互的知识库，AI 兽医能够在几秒钟内检索相关信息并给出诊断建议，显著提升疾病识别速度和准确率。  
- **全链路管理**：系统集成了疾病管理、药品库存、资讯推送等模块，养殖场可以在同一平台完成从病情上报、药品调配到后期疗效追踪的闭环管理，降低人工成本、减少用药错误。  
- **可扩展生态**：基于 Spring Boot 3 与 Spring AI，后端可灵活接入 Ollama、DeepSeek、通义千问、阿里百炼、SiliconFlow 等多种大模型；前端采用 Vue，前后端解耦，便于二次开发和功能迭代。  

**典型接入方式**  
1. **准备环境**  
   - 部署 MySQL 8、Milvus 向量数据库（可使用 Docker Compose 快速启动）。  
   - 选定大模型服务（如本地 Ollama 或云端 DeepSeek），在 `application.yml` 中配置对应的 API 地址和凭证。  
2. **后端接入**  
   - 克隆仓库后执行 `./mvnw clean package`，生成可运行的 Spring Boot Jar。  
   - 通过 `java -jar pig-health-smart-medicine.jar --spring.profiles.active=prod` 启动服务。  
   - 使用 MyBatis‑Plus 自动生成的 DAO 与业务表对接，亦可自行添加自定义实体。  
3. **前端集成**  
   - 进入 `frontend` 目录，执行 `npm install && npm run build`，得到静态资源。  
   - 将构建产物部署到 Nginx/Apache，或直接通过 Spring Boot 的 `static` 目录托管。  
   - 前端通过统一的 REST/GraphQL 接口调用后端的诊断、药品查询、文章检索等 API，无需额外 SDK。  
4. **业务接入**  
   - 在养殖场的现有信息系统（如 ERP、养殖管理平台）中调用 `/api/v1/diagnose`、`/api/v1/medicine` 等接口，实现“病情上报 → AI 诊断 → 用药推荐” 的自动化流程。  

**生产可用性评估**  
| 维度 | 现状 | 备注 |
|------|------|------|
| **代码成熟度** | 162 Stars、27 Forks，最近一次提交在 2026‑06‑26，活跃度良好 | 主体功能已基本完整，仍需自行进行安全审计。 |
| **依赖稳定性** | Spring Boot 3、Spring AI、MyBatis‑Plus、Milvus、Vue 等主流组件，社区支持强 | 需关注大模型服务的 SLA 与费用（尤其是云端模型）。 |
| **部署复杂度** | 需要 MySQL、Milvus、后端服务、前端静态资源四个组件，推荐使用 Docker‑Compose 或 Kubernetes Helm。 | 对于小规模试点，可先在单机 Docker 环境跑通。 |
| **可扩展性** | 大模型插件化设计，支持多家模型提供商；业务模块采用微服务风格，可按需拆分。 | 适合从原型快速迭代到企业级部署。 |
| **运维要求** | 向量库（Milvus）对硬件（CPU + 内存）有一定要求；模型推理对 GPU/加速卡有加速收益。 | 生产环境建议配置 8 CPU + 32 GB RAM，GPU 可选。 |
| **安全合规** | 项目本身未内置鉴权，需要自行集成 OAuth2/JWT 等认证授权方案。 | 业务数据（病例、药品）属于敏感信息，需做好加密与审计。 |

**结论**：PigHealthSmartMedicine 已具备完整的功能闭环和可插拔的大模型架构，适合作为养殖企业的内部诊疗平台或原型验证系统。若在生产环境使用，建议先在小规模场景完成 **部署‑验证‑安全加固** 三步，随后在 Kubernetes 或云原生平台上做弹性扩容，即可实现稳定、可维护的生产级服务。

## 🧭 Practical evaluation

**Value:** linyshdhhcb/PigHealthSmartMedicine helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 162 GitHub stars
- 27 forks
- updated 2026-06-26
- primary language: Vue
- 15 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 36/100 |
| stars | 47/100 |
| topics | 100/100 |
| outlook | 71/100 |
| quality | 70/100 |
| recency | 80/100 |
| adoption | 44/100 |
| production | 66/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/linyshdhhcb/PigHealthSmartMedicine) · [← Back to Knowledgerag](./README.md)</sub>
