# pytest-dev/pytest-rerunfailures

[![Stars](https://img.shields.io/github/stars/pytest-dev/pytest-rerunfailures?style=flat-square&color=yellow)](https://github.com/pytest-dev/pytest-rerunfailures/stargazers) [![Forks](https://img.shields.io/github/forks/pytest-dev/pytest-rerunfailures?style=flat-square&color=blue)](https://github.com/pytest-dev/pytest-rerunfailures/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> a pytest plugin that re-runs failed tests up to -n times to eliminate flakey failures

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 471 |
| 🍴 **Forks** | 102 |
| 💻 **Language** | Python |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

Here's a brief summary and explanation of the project:

**Summary:** pytest-dev/pytest-rerunfailures is an open-source plugin that helps eliminate flaky failures in tests by re-running failed tests up to a specified number of times. This plugin is useful for prototyping AI features, building RAG or agent workflows, and evaluating model tooling. It's a Python-based plugin that integrates with the pytest testing framework.

**Value:** The project adds AI capability to the pytest testing framework, enabling developers to prototype AI features and evaluate model tooling more effectively. This plugin helps to reduce flaky failures, which is a common issue in AI and machine learning development.

**Practical Adoption Path:** To adopt this plugin, developers can start by evaluating its feasibility through a small proof of concept and checking the README documentation. Once they're satisfied with the plugin's functionality, they can integrate it into their testing workflow. However, before production, they should perform dependency and maintenance checks to ensure the plugin is stable and secure.

**Production Readiness:** The plugin is considered medium in terms of production readiness, meaning it's useful for prototypes or internal workflows but may not be suitable for production environments without further review and testing. The plugin has a moderate level of maintenance and has not been updated recently, so

### Русский

Резюме проекта pytest-dev/pytest-rerunfailures:

Проект pytest-dev/pytest-rerunfailures - это плагин pytest, который позволяет повторно запускать провалившиеся тесты до -n раз, чтобы исключить случайные ошибки. Это полезно для добавления AI-способностей без создания новой модели. Typical сценарий использования: прототипирование AI-функций, создание RAG или агентов, оценка инструментов для моделей.

Проект имеет средний уровень готовности к production (Medium), что означает, что он может быть полезен для прототипирования или внутренних потоков работы, но требует проверки зависимостей и поддержки перед включением в производство.

### 中文

**项目简介**

pytest-rerunfailures 是一个 pytest 插件，用于重跑失败的测试，最大限度地减少测试的不稳定性。

**价值**

该项目的价值在于，它能够帮助开发者在测试过程中减少不稳定性，通过重跑失败的测试，提高测试的可靠性和准确性。对于需要构建可靠的测试环境的项目，pytest-rerunfailures 是一个很好的选择。

**典型接入方式**

为了接入 pytest-rerunfailures，需要在 pytest 的配置文件中添加以下设置：
```makefile
[pytest]
rerunfailures = 3  # 重跑失败的测试次数
```
还需要在测试文件中使用 `pytest.mark.reruns` 装饰器来指定重跑的次数和间隔。
```python
import pytest

@pytest.mark.reruns(3, delay=1)  # 重跑 3 次，间隔 1 秒
def test_example():
    # 测试代码
    pass
```
**生产可用性**

pytest-rerunfailures 的生产可用性为中等。虽然它是一个稳定的

## 🧭 Practical evaluation

**Value:** pytest-dev/pytest-rerunfailures helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 471 GitHub stars
- 102 forks
- updated 2026-08-17
- primary language: Python

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 50/100 |
| stars | 57/100 |
| topics | 0/100 |
| outlook | 60/100 |
| quality | 60/100 |
| recency | 80/100 |
| adoption | 55/100 |
| production | 67/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-08-17 · [View on GitHub](https://github.com/pytest-dev/pytest-rerunfailures) · [← Back to Misc](./README.md)</sub>
