# nestjs/typeorm

[![Stars](https://img.shields.io/github/stars/nestjs/typeorm?style=flat-square&color=yellow)](https://github.com/nestjs/typeorm/stargazers) [![Forks](https://img.shields.io/github/forks/nestjs/typeorm?style=flat-square&color=blue)](https://github.com/nestjs/typeorm/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> TypeORM module for Nest framework (node.js)  🍇

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.1k |
| 🍴 **Forks** | 223 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`javascript` `nest` `nestjs` `nodejs` `nosql` `sql` `typeorm` `typescript`

## 🎯 Categories

Backend

## 📝 Summary

### English

**Summary**  
NestJS/TypeORM is a well‑maintained TypeScript module that integrates the powerful TypeORM ORM into the NestJS framework, letting teams define entities, run migrations, and query databases with minimal boiler‑plate. With over 2 100 GitHub stars, recent commits, and strong community adoption, it’s ready for production use after a quick proof‑of‑concept.  

**Value**  
The library abstracts away low‑level database plumbing, enabling developers to persist, query, and migrate data using familiar Nest decorators and repository patterns, which speeds up development and reduces bugs in data‑access code.  

**Practical adoption path**  
1. Clone a minimal NestJS app and add the `@nestjs/typeorm` package.  
2. Follow the README to configure a test database (e.g., SQLite) and define a simple entity.  
3. Verify CRUD operations via a small controller/service – this serves as the proof‑of‑concept.  
4. Once validated, migrate the configuration to the target DB (PostgreSQL, MySQL, etc.) and integrate into existing Nest modules.  

**Production readiness**  
The project shows high production readiness: active maintenance (last commit 2026‑05‑12), a healthy star/fork count, TypeScript typings, and mature integration with Nest’s dependency‑injection system. After confirming licensing, security audit results, and that maintainers are responsive, it can be rolled out in a serious pilot or full‑scale production environment.

### Русский

**nest​js/typeorm** — модуль, который упрощает работу с базой данных в проектах на NestJS, предоставляя готовый слой TypeORM для сохранения, запросов и миграций без лишнего кода. Типичный сценарий внедрения — добавить модуль в небольшое proof‑of‑concept приложение, проверить конфигурацию в README и затем расширить его на все сервисы, где требуется быстрый доступ к данным. По оценкам, проект готов к production: активные коммиты, более 2100 звёзд, широкое принятие в сообществе и стабильный набор функций, требующие лишь окончательной проверки лицензии и безопасности.

### 中文

**简短介绍**  
`nestjs/typeorm` 是为 NestJS 框架提供的官方 TypeORM 集成模块，使得在 Node.js 项目中使用 TypeScript 编写的实体类即可直接进行数据库的增删改查、事务管理和迁移等操作。它让开发者能够以声明式、面向对象的方式管理持久化层，省去大量手写 SQL 与连接管理的工作。

**价值**  
- **统一的开发体验**：在 Nest 的依赖注入体系中直接使用 Repository/EntityManager，代码结构清晰、可测试。  
- **加速原型和迭代**：通过装饰器定义实体，自动同步 schema，快速搭建数据库驱动的原型应用。  
- **降低维护成本**：统一的迁移工具（`typeorm migration:*`）与查询构建器，让业务逻辑与数据访问解耦，减少自研数据层代码。

**典型接入方式**  
1. **安装**：`npm i @nestjs/typeorm typeorm`（以及对应的数据库驱动，如 `pg`、`mysql2` 等）。  
2. **配置模块**：在根模块 `AppModule` 中引入 `TypeOrmModule.forRoot({...})`，提供数据库连接选项（host、port、username、password、database、entities、synchronize 等）。  
3. **注入 Repository**：在业务模块中使用 `TypeOrmModule.forFeature([User])` 注册实体，然后在服务类构造函数中通过 `@InjectRepository(User) private readonly userRepo: Repository<User>` 获取仓库进行 CRUD。  
4. **迁移管理**：使用 TypeORM CLI 或 Nest 脚本执行 `typeorm migration:generate`、`migration:run` 等命令，完成 schema 版本控制。

**生产可用性**  
- **成熟度**：项目活跃，最近一次提交在 2026‑05‑12，拥有 2 128+ ⭐、223+ 🍴，并被 Nest 官方文档推荐。  
- **生态兼容**：完整支持 Nest 的模块化、依赖注入和拦截器，兼容常见的关系型数据库（PostgreSQL、MySQL、MariaDB、SQLite、MSSQL）以及部分 NoSQL（MongoDB）。  
- **可靠性**：社区提供丰富的最佳实践、错误处理和事务示例，且已有多家企业在生产环境中使用。只需在正式部署前完成安全审计（许可证、依赖漏洞）并进行一次小规模的 POC，即可视为具备高生产就绪度的 OSS 组件。

## 🧭 Practical evaluation

**Value:** nestjs/typeorm helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2128 GitHub stars
- 223 forks
- updated 2026-05-12
- primary language: TypeScript
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 59/100 |
| stars | 71/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 80/100 |
| recency | 80/100 |
| adoption | 67/100 |
| production | 72/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/nestjs/typeorm) · [← Back to Backend](./README.md)</sub>
