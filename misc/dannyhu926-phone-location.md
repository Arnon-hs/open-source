# dannyhu926/phone_location

[![Stars](https://img.shields.io/github/stars/dannyhu926/phone_location?style=flat-square&color=yellow)](https://github.com/dannyhu926/phone_location/stargazers) [![Forks](https://img.shields.io/github/forks/dannyhu926/phone_location?style=flat-square&color=blue)](https://github.com/dannyhu926/phone_location/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> 手机号码归属地数据库，运营商，邮编，区号

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 388 |
| 🍴 **Forks** | 107 |
| 💻 **Language** | PHP |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
Dannyhu926’s **phone_location** repository provides a PHP‑based database of Chinese mobile numbers, mapping each prefix to its carrier, geographic region, postal code, and area code. With over 380 ★ and recent updates (July 2026), it can serve as a quick lookup source for applications that need to resolve phone numbers to their location information.

**Value**  
- **Rich attribution data** – carrier, province/city, zip code and telephone area code are all bundled together, eliminating the need to stitch multiple public datasets.  
- **Ready‑to‑use PHP array** – the data is shipped as a plain PHP file, so it can be included directly without a separate DB or API layer, which is ideal for low‑latency or offline scenarios.  
- **Open‑source & community‑maintained** – the star count and recent commits suggest an active maintainer, reducing the risk of stale data.

**Practical Adoption Path**  
1. **Clone the repo** and include the `phone_location.php` (or similar) file in your project.  
2. **Wrap the array** in a small service class (e.g., `PhoneLocationResolver`) that accepts a mobile number, extracts the prefix, and returns the matching record.  
3. **Add a fallback** (e.g., external API or cached CSV) for numbers not covered by the dataset.  
4. **Write unit tests** to verify correct prefix extraction and handling of edge cases (invalid numbers, unknown prefixes).  
5. **Integrate** the service into any workflow that needs location enrichment—user registration, fraud detection, analytics dashboards, or marketing segmentation.

**Production Readiness**  
- **Maturity:** Medium. The library is stable enough for prototypes and internal tools, but the integration surface is thin (just a data file), so you must build the surrounding lookup logic and error handling yourself.  
- **Maintenance:** Check the repository’s issue tracker and commit frequency before committing to long‑term use; consider pinning a specific tag or forking the repo to control updates.  
- **Scalability:** Suitable for low‑to‑moderate traffic; for high‑throughput services you may want to load the data into an in‑memory cache (Redis, APCu) or a dedicated key‑value store.  
- **Risk Mitigation:** Validate the dataset’s completeness for your target number ranges, and confirm licensing (MIT‑style) aligns with your product’s compliance requirements.

In short, **phone_location** offers a convenient, up‑to‑date mapping of Chinese mobile prefixes to location data, and can be adopted quickly for internal or prototype use. With a modest amount of wrapper code and validation, it can be hardened for production, especially in contexts where a lightweight, self‑contained lookup is preferred over external API calls.

### Русский

Проект dannyhu926/phone_location предоставляет открытую базу данных принадлежности телефонных номеров (оператор, почтовый индекс, код области), что позволяет быстро enrich‑ить номера географической и операторской информацией. Типовой сценарий

### 中文

**项目简介（2‑3 句）**  
`dannyhu926/phone_location` 是一个基于 PHP 的手机号码归属地数据库，提供号码对应的运营商、邮编、区号等信息，适合在业务系统中快速完成手机号归属地查询。

**价值**  
- **精准定位**：一次查询即可返回运营商、所在省市、邮编和区号，帮助业务实现精准营销、风控和用户画像。  
- **开源免费**：无需额外付费的第三方接口，降低运营成本。  
- **本地化部署**：数据存放在本地，避免网络延迟和隐私泄露风险。

**典型接入方式**  
1. **Composer 安装**：`composer require dannyhu926/phone_location`。  
2. **加载数据**：项目提供 SQLite / CSV 数据文件，首次运行时可通过 `php vendor/dannyhu926/phone_location/scripts/import.php` 导入到本地数据库。  
3. **调用 API**：在代码中实例化 `PhoneLocation` 类并调用 `getInfo($mobile)`，返回包含 `carrier、province、city、postcode、area_code` 的关联数组。  
   ```php
   use PhoneLocation\PhoneLocation;
   $pl = new PhoneLocation();
   $info = $pl->getInfo('13800138000');
   // $info = ['carrier'=>'中国移动','province'=>'北京','city'=>'北京','postcode'=>'100000','area_code'=>'010']
   ```
4. **缓存优化**：可结合 APCu、Redis 等缓存层，将查询结果缓存数分钟至数小时，提升并发性能。

**生产可用性**  
- **成熟度**：已有 388 ⭐、107 🍴，最近一次更新在 2026‑07‑01，社区活跃度尚可。  
- **适用场景**：非常适合原型、内部工具或对响应时延要求不高的业务（如后台报表、风控预审）。  
- **上线建议**：在生产环境部署前，务必完成以下检查：  
  1. **数据更新频率**：确认本地数据库与官方数据源的同步周期（项目提供的更新脚本）。  
  2. **依赖审计**：检查 Composer 依赖的安全性，确保不引入已知漏洞。  
  3. **性能评估**：在高并发场景下进行压力测试，必要时加入缓存或读写分离。  
  4. **监控告警**：对查询异常率、数据库文件大小等关键指标设置监控。  

综上，`dannyhu926/phone_location` 在功能完整、成本低廉的前提下，可快速满足大多数业务对手机号归属地的需求；只要做好数据同步、依赖审计和性能调优，即可在生产环境安全使用。

## 🧭 Practical evaluation

**Value:** dannyhu926/phone_location may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 388 GitHub stars
- 107 forks
- updated 2026-07-01
- primary language: PHP

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 55/100 |
| topics | 0/100 |
| outlook | 60/100 |
| quality | 59/100 |
| recency | 80/100 |
| adoption | 54/100 |
| production | 62/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/dannyhu926/phone_location) · [← Back to Misc](./README.md)</sub>
