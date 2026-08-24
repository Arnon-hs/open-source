# getsentry/responses

[![Stars](https://img.shields.io/github/stars/getsentry/responses?style=flat-square&color=yellow)](https://github.com/getsentry/responses/stargazers) [![Forks](https://img.shields.io/github/forks/getsentry/responses?style=flat-square&color=blue)](https://github.com/getsentry/responses/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> A utility for mocking out the Python Requests library.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4.3k |
| 🍴 **Forks** | 369 |
| 💻 **Language** | Python |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`tag-production`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary**  
*getsentry/responses* is a lightweight Python library that lets you mock out the `requests` HTTP client, enabling deterministic unit‑ and integration‑tests without making real network calls. With over 4 k GitHub stars and recent activity (last commit 2026‑06‑25), it has become the de‑facto tool for developers who need to stub HTTP endpoints in a clean, declarative way.

**Value proposition**  
- **Fast, reliable testing** – By intercepting `requests` calls, you can define expected responses inline, eliminating flaky external‑service dependencies and dramatically speeding up test suites.  
- **Zero‑code intrusion** – No changes to production code are required; you simply decorate or context‑manage the test block, keeping the production path untouched.  
- **Broad ecosystem support** – Works with any library that uses `requests` (e.g., `urllib3`, `httpx` wrappers), making it a universal mock layer for Python HTTP clients.

**Practical adoption path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Evaluate the README & examples** – Run the provided quick‑start snippet in a sandbox to confirm it satisfies your mocking needs. | Validates API compatibility and confirms the library’s ergonomics. |
| 2️⃣  | **Add the dependency** – `pip install responses` (or lock it in `requirements.txt`/`poetry`). | Straightforward installation; no compiled extensions. |
| 3️⃣  | **Write a pilot test** – Replace an existing integration test that hits a real API with a `responses.activate` block, defining the expected URL, method, status, and payload. | Demonstrates the library’s effect on test reliability and speed. |
| 4️⃣  | **Run CI** – Ensure the test passes on your CI pipeline and that the library does not interfere with other mocking tools (e.g., `unittest.mock`). | Detects potential conflicts early. |
| 5️⃣  | **Lock version & monitor** – Pin to a known good release (e.g., `responses==0.25.0`) and add a periodic check (e.g., Dependabot) for security updates. | Mitigates supply‑chain risk and ensures future compatibility. |
| 6️⃣  | **Scale** – Gradually replace remaining external‑service calls across the codebase, using fixtures or custom helpers to keep test code DRY. | Leverages the library’s full value in larger projects. |

**Production readiness**  
- **Maturity:** High community adoption (4.3 k stars, 369 forks) and recent maintenance indicate a stable codebase.  
- **Risk level:** Medium – suitable for prototypes, internal tools, and test suites, but production use requires a final review of the license (MIT), security posture (no known CVEs), and confirmation that the maintainers are still responsive.  
- **Operational impact:** The library only affects test environments; it does not ship to production code, so runtime overhead is nil.  

**Conclusion**  
*getsentry/responses* is a well‑established, easy‑to‑integrate mocking utility that can immediately improve test reliability. After a quick pilot and a standard dependency‑review process, it is safe to adopt for internal and pre‑production workflows, with only modest additional diligence needed before using it in critical production pipelines.

### Русский

**getsentry/responses** — небольшая библиотека для подмены запросов, отправляемых через `requests`, что позволяет писать быстрые и надёжные тесты без реального обращения к внешним API. Она удобно интегрируется в пайплайны CI/CD и прототипы сервисов, где требуется имитация HTTP‑взаимодействий, однако перед выводом в продакшн стоит проверить лицензию, актуальность зависимостей и наличие активных мейнтейнеров. В текущем состоянии проект имеет средний уровень готовности: подходит для внутренних и экспериментальных решений, но требует дополнительного аудита перед критически важными развертываниями.

### 中文

**项目简介**  
`getsentry/responses` 是一个用于 **mock Python Requests 库** 的轻量工具，帮助在单元测试或原型开发阶段拦截、模拟 HTTP 请求，避免真实网络调用。

**价值**  
- **快速搭建测试环境**：只需几行代码即可定义期望的请求/响应，提升测试的可靠性与执行速度。  
- **降低外部依赖**：不必依赖真实的 API 服务或网络环境，避免因网络波动导致的 flaky tests。  
- **兼容性好**：直接 patch `requests`，对现有代码几乎零侵入，适用于任何使用 `requests` 的 Python 项目。

**典型接入方式**  
```python
import responses
import requests

@responses.activate
def test_my_api():
    # 注册要拦截的请求及返回的假数据
    responses.add(
        responses.GET,
        "https://api.example.com/data",
        json={"id": 1, "name": "demo"},
        status=200,
    )

    # 业务代码仍然使用 requests 发起请求
    resp = requests.get("https://api.example.com/data")
    assert resp.json() == {"id": 1, "name": "demo"}
```
- 在测试文件或 fixture 中使用 `@responses.activate`（或 `with responses.RequestsMock():`）即可激活拦截。  
- 通过 `responses.add`、`responses.replace`、`responses.assert_call_count` 等 API 完成请求匹配、返回定制以及调用断言。

**生产可用性**  
- **成熟度**：GitHub ★4.3k、Fork 369，活跃维护至 2026‑06‑25，代码质量和社区认可度较高。  
- **适用场景**：非常适合 **原型、内部工具、CI 测试套件**，在这些环境下可直接使用而无需额外审计。  
- **生产环境**：不建议在正式业务代码中直接使用 `responses` 进行请求拦截（因为它会全局 patch `requests`），但可在 **预发布/回归测试** 中安全使用。若要在生产系统中使用，需要：  
  1. 确认许可证兼容（MIT）。  
  2. 通过安全审计检查是否存在已知漏洞。  
  3. 将其作为 **dev‑dependency**，并在 CI 中锁定版本，防止意外升级导致行为变化。  

综上，`getsentry/responses` 是一个 **成熟且易上手的请求 Mock 框架**，非常适合在测试与原型阶段使用；在正式生产环境中应保持为开发依赖并做好版本与安全管理。

## 🧭 Practical evaluation

**Value:** getsentry/responses may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 4350 GitHub stars
- 369 forks
- updated 2026-06-25
- primary language: Python
- 1 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 64/100 |
| stars | 77/100 |
| topics | 13/100 |
| outlook | 52/100 |
| quality | 60/100 |
| recency | 40/100 |
| adoption | 74/100 |
| production | 55/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/getsentry/responses) · [← Back to Misc](./README.md)</sub>
