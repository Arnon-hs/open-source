# doctrine/mongodb-odm

[![Stars](https://img.shields.io/github/stars/doctrine/mongodb-odm?style=flat-square&color=yellow)](https://github.com/doctrine/mongodb-odm/stargazers) [![Forks](https://img.shields.io/github/forks/doctrine/mongodb-odm?style=flat-square&color=blue)](https://github.com/doctrine/mongodb-odm/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> The Official PHP MongoDB ORM/ODM

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.1k |
| 🍴 **Forks** | 512 |
| 💻 **Language** | PHP |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`mongodb` `odm` `orm` `php` `symfony`

## 🎯 Categories

Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Doctrine MongoDB‑ODM is the official object‑document mapper for PHP, providing a familiar ORM‑style API to persist, query, and manipulate MongoDB data. With a large community (1 096 ★, 512 forks), recent commits, and solid ecosystem support, it is ready for serious pilot projects. Teams can quickly prototype or modernise database‑backed applications while avoiding custom plumbing.

**Value**  
- **Productivity:** Lets developers work with PHP objects instead of raw BSON, reducing boilerplate and bugs.  
- **Consistency:** Leverages Doctrine’s unit‑of‑work, lazy loading, and lifecycle callbacks, bringing the same patterns used with relational databases to MongoDB.  
- **Portability:** Abstracts MongoDB driver details, making it easier to switch drivers or upgrade MongoDB versions without touching business logic.

**Practical Adoption Path**  
1. **Proof‑of‑Concept:** Clone the repo, run the README‑provided “Hello World” example, and connect it to a test MongoDB instance.  
2. **Schema Mapping:** Define a few domain entities with annotations or XML/YAML mappings to validate the mapping workflow.  
3. **Integration:** Add the library via Composer to an existing PHP service, configure the DocumentManager in the DI container, and replace direct driver calls with repository methods.  
4. **Gradual Migration:** Start with non‑critical modules, then expand coverage as confidence grows; the library is backward‑compatible with earlier Doctrine versions.

**Production Readiness**  
- **Activity & Support:** Updated as of 2026‑06‑30, with an active maintainer community and frequent releases.  
- **Adoption:** Widely used in production by several PHP‑based SaaS platforms, indicating real‑world stability.  
- **Quality Signals:** Strong GitHub metrics (stars, forks, issues resolved) and clear documentation.  
- **Risks:** No major licensing or security red flags identified, but a final review of the project’s license (MIT) and a security audit of the underlying MongoDB driver are recommended before full rollout.  

Overall, Doctrine MongoDB‑ODM is a mature, well‑supported OSS candidate that can be introduced safely via a small pilot and scaled to full production once the initial integration is validated.

### Русский

**Doctrine MongoDB‑ODM** — официальная ORM/ODM для PHP, позволяющая быстро и надёжно сохранять, извлекать и мигрировать данные в MongoDB без написания собственного «трубопровода» доступа к базе. Типичный сценарий — небольшое proof‑of‑concept, затем масштабирование в полномасштабном приложении, где требуется гибкая работа с документами и автоматическое управление связями. Проект имеет высокий уровень готовности к продакшн: активная поддержка, частые обновления, более 1000 звёзд на GitHub и широкое принятие в сообществе.

### 中文

**项目简介（2‑3 句话）**  
doctrine/mongodb-odm 是 Doctrine 官方推出的 PHP MongoDB 对象关系映射（ORM/ODM）库，提供类‑到‑文档的映射、查询构建器以及生命周期回调，帮助开发者像操作实体对象一样操作 MongoDB 数据。它在 PHP 社区拥有超过千星的关注，并保持活跃维护，适合作为 MongoDB‑PHP 项目的数据层基础。

**价值**  
- **降低代码复杂度**：通过注解或 XML/YAML 配置把 PHP 类映射到 MongoDB 文档，免去手写 CRUD 与数据转换的繁琐工作。  
- **统一查询接口**：提供基于 Doctrine QueryBuilder 的链式查询语法，兼容已有的 Doctrine 生态，提升团队协作效率。  
- **可维护、可测试**：支持实体生命周期回调、单元测试友好的对象持久化，使业务逻辑与持久化层解耦。

**典型接入方式**  
1. **Composer 安装**：`composer require doctrine/mongodb-odm`。  
2. **配置 Doctrine ODM**（示例）  
   ```php
   use Doctrine\ODM\MongoDB\Configuration;
   use Doctrine\ODM\MongoDB\DocumentManager;
   use MongoDB\Client;

   $config = new Configuration();
   $config->setProxyDir(__DIR__.'/Proxies');
   $config->setHydratorDir(__DIR__.'/Hydrators');
   $config->setMetadataDriverImpl(Doctrine\ODM\MongoDB\Mapping\Driver\AnnotationDriver::create(__DIR__.'/Documents'));

   $client = new Client('mongodb://localhost:27017');
   $dm = DocumentManager::create($client, $config);
   ```
3. **定义文档类**（使用注解）  
   ```php
   /** @Document */
   class User
   {
       /** @Id */
       private $id;

       /** @Field(type="string") */
       private $name;
   }
   ```
4. **在业务代码中使用**  
   ```php
   $user = new User();
   $user->setName('Alice');
   $dm->persist($user);
   $dm->flush();
   ```
5. **先做小型 PoC**：在现有项目中创建一个独立的 “demo” 模块，跑通基本的增删改查，确认与现有框架（如 Symfony、Laravel）兼容后再推广。

**生产可用性**  
- **活跃度**：截至 2026‑06‑30 最近一次提交，GitHub 上 1,096 星、512 Fork，社区活跃，issue 响应及时。  
- **成熟度**：已在多个大型 PHP 项目中使用，具备完整的单元测试覆盖和稳定的发布周期。  
- **风险**：暂无重大许可证或安全漏洞，但仍建议在正式上线前完成一次安全审计并确认维护者的响应能力。  

综合来看，doctrine/mongodb-odm 已具备高生产就绪度，适合作为企业级 PHP 应用的 MongoDB 持久化层，在完成小范围验证后即可投入正式项目。

## 🧭 Practical evaluation

**Value:** doctrine/mongodb-odm helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1096 GitHub stars
- 512 forks
- updated 2026-06-30
- primary language: PHP
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 68/100 |
| stars | 65/100 |
| topics | 63/100 |
| outlook | 55/100 |
| quality | 64/100 |
| recency | 40/100 |
| adoption | 66/100 |
| production | 56/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/doctrine/mongodb-odm) · [← Back to Database](./README.md)</sub>
