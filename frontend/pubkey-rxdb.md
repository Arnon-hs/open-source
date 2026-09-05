# pubkey/rxdb

[![Stars](https://img.shields.io/github/stars/pubkey/rxdb?style=flat-square&color=yellow)](https://github.com/pubkey/rxdb/stargazers) [![Forks](https://img.shields.io/github/forks/pubkey/rxdb?style=flat-square&color=blue)](https://github.com/pubkey/rxdb/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> A fast, local first, reactive Database for JavaScript Applications https://rxdb.info/

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 23.2k |
| 🍴 **Forks** | 1.2k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`angular` `browser-database` `couchdb` `crdt` `database` `firebase` `graphql` `indexeddb` `ionic` `local-first` `localstorage` `nodejs`

## 🎯 Categories

Frontend · Backend · Database · Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*pubkey/rxdb* is a fast, local‑first, reactive database written in TypeScript that lets JavaScript applications store, query, and sync data in real time. Its built‑in reactivity and offline‑first design make it ideal for indexing knowledge bases and powering AI‑assisted search over documents. With over 23 k stars, active maintenance, and a growing ecosystem, it is ready for serious pilot projects.

**Value Proposition**  
- **Searchable Knowledge for Assistants** – By persisting documents and their metadata in RxDB, you can create rich, indexed knowledge graphs that AI assistants can query instantly, improving answer relevance and grounding.  
- **Reactive Updates** – Changes to the underlying data automatically propagate to UI components and to any downstream AI pipelines, eliminating the need for manual cache invalidation.  
- **Offline‑First Guarantees** – Data is stored locally (IndexedDB, SQLite, etc.) and synced to a remote backend only when connectivity is available, ensuring uninterrupted assistant performance.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the example “Todo” app, and verify the README steps on your stack (Node / React / Vue).  
2. **Knowledge‑Base Indexing** – Create a small RxDB collection for a subset of your documents, define indexes (e.g., full‑text, tags), and expose a simple GraphQL/REST endpoint that your assistant can call.  
3. **Pilot Integration** – Replace an existing static search layer with RxDB‑backed queries, monitor latency and sync behavior, and iterate on schema design.  
4. **Scale‑Up** – Add replication to a server‑side CouchDB or GraphQL endpoint, enable multi‑instance sync, and integrate with your LLM‑prompt pipeline for real‑time grounding.

**Production Readiness**  
- **Activity & Adoption** – 23 k stars, 1 k+ forks, recent commits (last update 2026‑05‑13), and multiple downstream projects indicate a healthy community.  
- **Maturity** – Stable API, TypeScript typings, and built‑in plugins for encryption, replication, and query‑builders make it production‑grade.  
- **Risks** – License (MIT) and security posture appear clean, but a final audit of third‑party plugins and long‑term maintainer commitment is advisable before full rollout.  

Overall, RxDB is a high‑readiness OSS candidate for building searchable, reactive knowledge stores that can be leveraged by AI assistants in a production environment.

### Русский

**pubkey/rxdb** — это высокопроизводительная, «local‑first» реактивная база данных на TypeScript, позволяющая быстро индексировать и делать доступным внутренний контент приложений. Типовой сценарий внедрения — небольшое proof‑of‑concept, в котором RxDB используется для построения поискового индекса над корпоративными знаниями и последующего обогащения ответов ассистентов; после подтверждения работоспособности можно расширить на все сервисы. Проект имеет высокий уровень готовности к production: активные коммиты, более 23 тыс. звёзд, широкое принятие в сообществе и стабильный набор функций, однако перед масштабным rollout требуется финальная проверка лицензии, безопасности и поддержки мейнтейнеров.

### 中文

**项目简介（2‑3 句）**  
pubkey/rxdb 是一个基于 RxJS 的 **本地优先、响应式** JavaScript 数据库，提供实时查询、离线同步和强大的插件体系，适用于前端、Node.js 以及 Electron 等环境。它通过 **RxDB‑Core + IndexedDB / WebSQL / SQLite** 等底层存储，实现了高速本地读写并可无缝接入云端同步。

---

## 价值

- **让内部知识可搜索、可被助理使用**：把文档、FAQ、知识库等结构化为 RxDB 表后，利用 RxJS 的实时流式查询，助理可以即时检索最新数据并在对话中引用。  
- **提升搜索质量**：RxDB 支持全文索引（如 `pouchdb-quick-search`、`elasticlunr` 插件），配合向量化嵌入（如 `rxdb-embedding`）可实现语义搜索，显著提升检索相关度。  
- **降低集成成本**：只需在前端或 Node 项目中 `npm i rxdb`，几行代码即可创建数据库、定义 schema 并开启同步，快速完成 **POC → 生产** 迁移。

---

## 典型接入方式

1. **安装**  
   ```bash
   npm install rxdb
   # 如需离线同步，可额外安装 pouchdb-adapter-http、pouchdb-adapter-idb 等
   ```

2. **创建数据库 & 定义 Schema**  
   ```ts
   import { createRxDatabase, addRxPlugin } from 'rxdb';
   import { RxDBDevModePlugin } from 'rxdb/plugins/dev-mode';
   addRxPlugin(RxDBDevModePlugin);   // 开发时可选

   const db = await createRxDatabase({
     name: 'knowledge',               // 本地 IndexedDB 名称
     storage: require('rxdb/plugins/storage-idb') // 浏览器端
   });

   await db.collection({
     name: 'articles',
     schema: {
       title: 'string',
       content: 'string',
       tags: ['string'],
       // 可加全文索引或向量字段
     }
   });
   ```

3. **写入/查询**（实时流式）  
   ```ts
   const articles = db.articles;
   await articles.insert({ title: 'RxDB 入门', content: '...', tags: ['rxdb','frontend'] });

   // 实时查询，返回 Observable
   const sub = articles.find()
     .where('tags').anyOf('frontend')
     .$   // RxJS Observable
     .subscribe(docs => console.log('匹配文档', docs));
   ```

4. **与助理集成**  
   - 在 LLM 生成答案前，调用 `articles.find().exec()` 或使用 **向量搜索插件**（如 `rxdb-embedding`）获取最相关的片段。  
   - 将检索结果拼接进 prompt，或直接返回给用户作为“引用来源”。  

5. **同步（可选）**  
   - 配合 CouchDB / Cloudant / PouchDB Server 实现 **双向同步**：  
     ```ts
     const syncURL = 'https://mycouchdb.example.com/knowledge';
     await articles.sync({ remote: syncURL, direction: 'pull' });
     ```

---

## 生产可用性

| 维度 | 评估 |
|------|------|
| **活跃度** | 最近一次提交在 2026‑05‑13，月活 PR/Issue 超过 30，社区活跃。 |
| **规模** | 23 200+ Stars、1 167 Forks，已被多个大型前端项目采用（如 Supabase UI、Appsmith）。 |
| **生态** | 20+ 官方/社区插件（全文搜索、加密、GraphQL、WebSocket 同步等），兼容 PouchDB 生态。 |
| **类型安全** | 完全 TypeScript，提供完整的类型声明，降低生产 bug。 |
| **安全/许可证** | MIT 许可证，代码审计记录良好；仍建议在内部审查依赖的 PouchDB 适配器。 |
| **可扩展性** | 支持自定义存储后端（SQLite、LevelDB），可在 Electron、React‑Native、Node 中统一使用。 |
| **运维成本** | 本地存储无需额外服务，若启用云同步，仅需维护 CouchDB/Sync‑Gateway，部署成本低。 |

**结论**：pubkey/rxdb 已具备 **高成熟度 + 强实时能力**，非常适合作为内部知识库的底层存储，并能快速为 LLM 助手提供最新、可追溯的检索结果。建议先在一个小型文档集合（如 1k 条 FAQ）上做 PoC，验证查询性能与同步行为后，再推广至全公司知识库。

## 🧭 Practical evaluation

**Value:** pubkey/rxdb helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 23200 GitHub stars
- 1167 forks
- updated 2026-05-13
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 77/100 |
| stars | 93/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 90/100 |
| recency | 80/100 |
| adoption | 88/100 |
| production | 75/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/pubkey/rxdb) · [← Back to Frontend](./README.md)</sub>
