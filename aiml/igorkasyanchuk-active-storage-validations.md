# igorkasyanchuk/active_storage_validations

[![Stars](https://img.shields.io/github/stars/igorkasyanchuk/active_storage_validations?style=flat-square&color=yellow)](https://github.com/igorkasyanchuk/active_storage_validations/stargazers) [![Forks](https://img.shields.io/github/forks/igorkasyanchuk/active_storage_validations?style=flat-square&color=blue)](https://github.com/igorkasyanchuk/active_storage_validations/network) [![Language](https://img.shields.io/badge/lang-Ruby-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Do it like => validates :photos, attached: true, content_type: ['image/png', 'image/jpg', 'image/jpeg'], size: { less_than: 500.kilobytes }, limit: { min: 1, max: 3 }, aspect_ratio: :landscape, dimension: { width: { in: 800..1600 }

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.2k |
| 🍴 **Forks** | 148 |
| 💻 **Language** | Ruby |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-05-09 |
| 🔍 **Source** | github |

## 🏷️ Topics

`active-storage` `activestorage` `rails` `validations`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

`active_storage_validations` is a Ruby gem that adds convenient, declarative validation helpers to Rails’ Active Storage attachments. It lets you enforce rules such as presence, allowed content types, file size limits, quantity constraints, aspect ratios, and dimension ranges directly in your models (e.g., `validates :photos, attached: true, content_type: ['image/png', 'image/jpg', 'image/jpeg'], size: { less_than: 500.kilobytes }, limit: { min: 1, max: 3 }, aspect_ratio: :landscape, dimension: { width: { in: 800..1600 } }`). This makes ensuring uploaded media meets your specifications simple and consistent across the application.

### Русский

**Active Storage Validations** – это open‑source библиотека для Ruby on Rails, расширяющая возможности `ActiveStorage` удобными валидаторами. Она позволяет в один строковый вызов проверять наличие вложений, тип контента, размер, количество файлов, соотношение сторон и размеры изображений (например, `validates :photos, attached: true, content_type: ['image/png', 'image/jpg', 'image/jpeg'], size: { less_than: 500.kilobytes }, limit: { min: 1, max: 3 }, aspect_ratio: :landscape, dimension: { width: { in: 800..1600 } }`). Проект находится в категории AI/ML и подходит для быстрого внедрения строгих правил загрузки медиа‑файлов в любые Rails‑приложения.

### 中文

igorkasyanchuk/active_storage_validations：igorkasyanchuk/active_storage_validations helps add AI capability without starting from a blank model stack.。适合用于prototype AI features、build RAG or agent workflows。Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

## 🧭 Practical evaluation

**Value:** igorkasyanchuk/active_storage_validations helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1175 GitHub stars
- 148 forks
- updated 2026-05-09
- primary language: Ruby
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| usefulness | 58/100 |
| quality | 76/100 |
| integration | 46/100 |
| production | 75/100 |
| outlook | 77/100 |
| adoption | 62/100 |
| stars | 65/100 |
| forks | 54/100 |
| recency | 100/100 |
| topics | 50/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-09 · [View on GitHub](https://github.com/igorkasyanchuk/active_storage_validations) · [← Back to AI/ML](./README.md)</sub>
