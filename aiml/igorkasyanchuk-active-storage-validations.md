# igorkasyanchuk/active_storage_validations

[![Stars](https://img.shields.io/github/stars/igorkasyanchuk/active_storage_validations?style=flat-square&color=yellow)](https://github.com/igorkasyanchuk/active_storage_validations/stargazers) [![Forks](https://img.shields.io/github/forks/igorkasyanchuk/active_storage_validations?style=flat-square&color=blue)](https://github.com/igorkasyanchuk/active_storage_validations/network) [![Language](https://img.shields.io/badge/lang-Ruby-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Do it like => validates :photos, attached: true, content_type: ['image/png', 'image/jpg', 'image/jpeg'], size: { less_than: 500.kilobytes }, limit: { min: 1, max: 3 }, aspect_ratio: :landscape, dimension: { width: { in: 800..1600 }

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.2k |
| 🍴 **Forks** | 148 |
| 💻 **Language** | Ruby |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-05-09 |
| 🔍 **Source** | github |

## 🏷️ Topics

`active-storage` `activestorage` `rails` `validations`

## 🎯 Categories

AI/ML

## 📝 Summary

`active_storage_validations` is a Ruby gem that adds convenient, declarative validation helpers to Rails’ Active Storage attachments. It lets you enforce rules such as presence, allowed content types, file size limits, quantity constraints, aspect ratios, and dimension ranges directly in your models (e.g., `validates :photos, attached: true, content_type: ['image/png', 'image/jpg', 'image/jpeg'], size: { less_than: 500.kilobytes }, limit: { min: 1, max: 3 }, aspect_ratio: :landscape, dimension: { width: { in: 800..1600 } }`). This makes ensuring uploaded media meets your specifications simple and consistent across the application.

---

<sub>🔭 Discovered 2026-05-09 · [View on GitHub](https://github.com/igorkasyanchuk/active_storage_validations) · [← Back to AI/ML](./README.md)</sub>
