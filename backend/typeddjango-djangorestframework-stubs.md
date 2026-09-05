# typeddjango/djangorestframework-stubs

[![Stars](https://img.shields.io/github/stars/typeddjango/djangorestframework-stubs?style=flat-square&color=yellow)](https://github.com/typeddjango/djangorestframework-stubs/stargazers) [![Forks](https://img.shields.io/github/forks/typeddjango/djangorestframework-stubs?style=flat-square&color=blue)](https://github.com/typeddjango/djangorestframework-stubs/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> PEP-484 stubs for django-rest-framework

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 538 |
| 🍴 **Forks** | 138 |
| 💻 **Language** | Python |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`django` `django-rest-framework` `mypy` `pep484` `python`

## 🎯 Categories

Backend

## 📝 Summary

### English

**Summary**  
`typeddjango/djangorestframework-stubs` provides PEP‑484 type‑hint stubs for the Django‑REST‑Framework (DRF), enabling static type‑checkers such as MyPy to understand DRF’s dynamic APIs. With 538 ★, recent commits (as of 2026‑06‑23), and growing community adoption, it is a mature open‑source component ready for pilot projects.

**Value**  
The stub package fills a critical gap in the Python data‑stack: DRF’s runtime‑generated serializers, viewsets, and request/response objects are otherwise invisible to type checkers, leading to noisy “Any” types and missed errors. By adding precise type information, developers gain earlier detection of mismatched fields, improved IDE autocomplete, and more maintainable codebases—especially valuable for large Django services that already enforce type checking.

**Practical adoption path**  

1. **Proof‑of‑concept** – Add the package to a sandboxed service (`pip install djangorestframework-stubs`) and enable `--strict` MyPy checking. Verify that existing DRF code type‑checks without a flood of false positives.  
2. **Readme validation** – Follow the repository’s README instructions (e.g., adding `django-stubs` and `djangorestframework-stubs` to `mypy.ini`’s `plugins` section) and confirm that the configuration works with your CI pipeline.  
3. **Incremental rollout** – Enable the stubs for a single Django app or a set of serializers, gradually expanding coverage while fixing any uncovered type errors.  
4. **Full integration** – Once confidence is built, add the stubs to the production `requirements.txt`/`poetry.lock`, lock the version, and make the MyPy strictness a mandatory gate in CI.

**Production readiness**  
The project scores high on production readiness: it is actively maintained (last update 2026‑06‑23), has a solid user base (538 ★, 138 forks), and is written in Python—the same language stack as the target application. No major licensing or security red flags appear, though a final review of the MIT license and maintainer activity is advisable. Overall, the stubs are mature enough for a serious pilot and, after the small proof‑of‑concept phase, can be promoted to a production‑grade dependency.

### Русский

**typeddjango/djangorestframework-stubs** — это набор PEP‑484 типовых подсказок (stubs) для Django REST Framework, позволяющий включить статическую типизацию в проекты на Python и получать более точные подсказки и проверки в IDE и mypy. Типичный сценарий внедрения — добавить зависимость в `requirements-dev.txt`, включить `mypy`‑конфигурацию с `plugins = ["django-stubs", "djangorestframework-stubs"]` и выполнить небольшую пробную проверку существующего кода; при положительном результате можно расширить покрытие на весь сервис. По оценке готовности проект считается «production‑ready»: активные коммиты, более 500 звёзд, широкое принятие в сообществе и отсутствие критических рисков, однако перед масштабным rollout следует окончательно проверить лицензию и безопасность зависимостей.

### 中文

**项目简介**  
`typeddjango/djangorestframework-stubs` 为 Django REST Framework（DRF）提供 PEP‑484 类型存根（`.pyi`），让 IDE 与类型检查工具（mypy、pyright 等）能够对 DRF 的视图、序列化器、路由等进行静态类型推断。

**价值**  
- **提升开发体验**：在编辑器中获得自动补全、跳转和即时类型错误提示，显著降低调试成本。  
- **代码质量保障**：配合 mypy/pyright 等工具，能够在 CI 中捕获 API 参数、返回值以及序列化字段的不匹配，防止运行时异常。  
- **无侵入式**：仅通过安装类型存根，不需要修改现有的 DRF 代码或配置，即可在项目中启用。

**典型接入方式**  
1. **安装**  
   ```bash
   pip install djangorestframework-stubs
   ```
2. **在项目的 `mypy.ini`（或 `pyproject.toml`）中启用**  
   ```ini
   [mypy]
   plugins = pydantic.mypy
   disallow_untyped_calls = True
   disallow_untyped_defs = True
   ignore_missing_imports = True
   ```
3. **在代码中使用类型注解**  
   ```python
   from rest_framework.views import APIView
   from rest_framework.request import Request
   from rest_framework.response import Response

   class HelloView(APIView):
       def get(self, request: Request) -> Response:
           return Response({"msg": "hello"})
   ```
4. **在 CI 中运行类型检查**  
   ```bash
   mypy myproject/
   ```

**生产可用性**  
- **活跃度**：截至 2026‑06‑23 最近一次提交，拥有 538 ★、138 Fork，社区活跃且持续维护。  
- **兼容性**：支持最新的 Django 4.x 与 DRF 3.14+，并已在多个开源项目中验证。  
- **风险**：许可证为 MIT，符合企业合规；暂无已知安全漏洞。唯一需要关注的是后续 DRF 主版本升级时的存根同步情况。  

综合来看，`djangorestframework-stubs` 已具备 **高生产就绪度**，适合作为类型安全的第一步在现有 DRF 项目中试点，随后可在全链路 CI/CD 中推广。

## 🧭 Practical evaluation

**Value:** typeddjango/djangorestframework-stubs may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 538 GitHub stars
- 138 forks
- updated 2026-06-23
- primary language: Python
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 54/100 |
| stars | 58/100 |
| topics | 63/100 |
| outlook | 70/100 |
| quality | 70/100 |
| recency | 80/100 |
| adoption | 57/100 |
| production | 70/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/typeddjango/djangorestframework-stubs) · [← Back to Backend](./README.md)</sub>
