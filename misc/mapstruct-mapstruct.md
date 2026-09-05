# mapstruct/mapstruct

[![Stars](https://img.shields.io/github/stars/mapstruct/mapstruct?style=flat-square&color=yellow)](https://github.com/mapstruct/mapstruct/stargazers) [![Forks](https://img.shields.io/github/forks/mapstruct/mapstruct?style=flat-square&color=blue)](https://github.com/mapstruct/mapstruct/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> An annotation processor for generating type-safe bean mappers

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 7.7k |
| 🍴 **Forks** | 1k |
| 💻 **Language** | Java |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`annotation-processor` `bean-mapping` `java` `javabeans` `mapping` `mapstruct` `no-reflection` `records`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
MapStruct is an annotation‑processor library that generates type‑safe, compile‑time mappers for converting between Java bean types. With over 7 600 GitHub stars, frequent releases, and a large Java ecosystem presence, it is a mature, production‑ready tool for reducing boilerplate mapping code. It is especially valuable when you need high‑performance, compile‑time‑checked conversions in micro‑services or layered architectures.

**Value**  
- **Zero‑runtime overhead**: Mappers are generated as plain Java code, so there is no reflection or proxy cost.  
- **Type safety**: Errors are caught at compile time, preventing runtime mapping bugs.  
- **Declarative mapping**: Simple `@Mapper` interfaces let you express complex field‑to‑field transformations with a few annotations or custom methods.  
- **Extensible**: Supports custom type converters, expression mapping, and integration with Spring, CDI, or plain Java.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Add the `mapstruct-processor` and `mapstruct` dependencies to a small module, write a sample `@Mapper` interface, and verify the generated implementation compiles and works.  
2. **Readme validation** – Follow the official README to configure the annotation processor for your build tool (Maven, Gradle, or IDE). This step ensures the integration steps are clear for your CI pipeline.  
3. **Incremental rollout** – Replace existing manual bean‑copy code or third‑party mappers in a low‑risk service, measuring compile‑time impact and runtime performance.  
4. **Full‑scale migration** – Once the pilot proves stable, adopt MapStruct across the codebase, leveraging its Spring/DI integration to inject mappers where needed.

**Production Readiness**  
- **High**: The project shows recent activity (last commit 2026‑06‑27), a large contributor base, and strong adoption signals (7 600+ stars, 1 000+ forks).  
- **Ecosystem fit**: Official support for Spring, Spring Boot, Jakarta EE, and Quarkus makes it compatible with most Java stacks.  
- **Risk mitigation**: The primary unknown is the initial setup cost; a small PoC and README walkthrough will confirm the required build‑tool configuration before committing to a larger migration.  

Overall, MapStruct is a robust, well‑maintained OSS candidate that can be safely piloted and, after a brief validation phase, promoted to production for any Java project that needs efficient, type‑safe bean mapping.

### Русский

MapStruct — это аннотационный процессор для Java, генерирующий типобезопасные мапперы между bean‑классами, что позволяет избавиться от ручного написания кода преобразования и уменьшить количество ошибок. Типичный сценарий внедрения — добавить зависимость MapStruct в проект, создать интерфейсы‑мэпперы с нужными аннотациями и проверить работу на небольшом proof‑of‑concept, опираясь на подробный README. Проект имеет высокую готовность к продакшну: активная поддержка, более 7 000 звёзд, регулярные обновления и широкое принятие в экосистеме Java.

### 中文

MapStruct 是一个基于

## 🧭 Practical evaluation

**Value:** mapstruct/mapstruct may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 7666 GitHub stars
- 1031 forks
- updated 2026-06-27
- primary language: Java
- 8 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 75/100 |
| stars | 83/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 86/100 |
| recency | 80/100 |
| adoption | 81/100 |
| production | 72/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/mapstruct/mapstruct) · [← Back to Misc](./README.md)</sub>
