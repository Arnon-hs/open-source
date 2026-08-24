# OPCFoundation/UA-.NETStandard

[![Stars](https://img.shields.io/github/stars/OPCFoundation/UA-.NETStandard?style=flat-square&color=yellow)](https://github.com/OPCFoundation/UA-.NETStandard/stargazers) [![Forks](https://img.shields.io/github/forks/OPCFoundation/UA-.NETStandard?style=flat-square&color=blue)](https://github.com/OPCFoundation/UA-.NETStandard/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-48%2F100-brightgreen?style=flat-square)](#)

> OPC Unified Architecture .NET Standard

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.3k |
| 🍴 **Forks** | 1.1k |
| 💻 **Language** | C# |
| 📈 **Score** | 48/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

Here's a brief summary of the project:

OPCFoundation/UA-.NETStandard is an open-source implementation of the OPC Unified Architecture standard in .NET Standard, allowing for integration with various industrial automation systems. While it has a significant number of GitHub stars and forks, its practical adoption path requires manual inspection and validation of the integration process, making it more suitable for prototypes or internal workflows. Before committing to production, users should carefully assess the dependency and maintenance costs associated with this project.

In terms of value, the project offers a standardized interface for integrating with OPC Unified Architecture systems, which can be beneficial for companies operating in the industrial automation space. However, its production readiness is limited due to the need for manual inspection and potential integration complexities.

The practical adoption path for this project involves the following steps:

1. Review the project's README and activity to ensure it aligns with the desired workflow.
2. Inspect the integration process and validate the setup cost before committing to production.
3. Perform dependency and maintenance checks to ensure the project is suitable for production use.

Overall, OPCFoundation/UA-.NETStandard is a useful project for prototyping or internal workflows, but its production readiness requires careful evaluation and validation.

### Русский

Резюме:

Проект OPCFoundation/UA-.NETStandard представляет собой реализацию стандарта OPC Unified Architecture для платформы .NET Standard. Он может быть полезен в сценариях интеграции, когда README и активность проекта соответствуют конкретному бизнес-процессу. Проект готов к использованию в прототипах или внутренних рабочих процессах, но требует тщательного проверки зависимости и обслуживания перед внедрением в производственную среду.

### 中文

**简短介绍**  
OPCFoundation/UA-.NETStandard 是 OPC Unified Architecture（OPC UA）的官方 .NET Standard 实现，提供跨平台的 OPC UA 客户端和服务端库，帮助开发者在 Windows、Linux、macOS 等环境中以 C# 快速构建工业物联网应用。

**价值**  
- **跨平台**：基于 .NET Standard 1.6+，一次编写代码即可在多种操作系统上运行。  
- **标准兼容**：完整实现 OPC UA 1.04/1.05 规范，支持安全模型、订阅、历史访问等核心功能。  
- **活跃社区**：超过 2 k 星、1 k Fork，官方维护并定期更新，文档和示例丰富，降低学习成本。  

**典型接入方式**  
1. **通过 NuGet 引入**：在项目中执行 `dotnet add package OPCFoundation.NetStandard.Opc.Ua`（或对应的子包），即可获得客户端/服务端 API。  
2. **客户端示例**：  
   ```csharp
   var config = new ApplicationConfiguration()
   {
       ApplicationName = "MyUaClient",
       ApplicationUri = Utils.Format(@"urn:{0}:MyUaClient", Utils.GetHostName()),
       // 证书、加密等配置...
   };
   await config.Validate(ApplicationType.Client);
   var endpoint = CoreClientUtils.SelectEndpoint("opc.tcp://server:4840", useSecurity: true);
   var session = await Session.Create(config, new ConfiguredEndpoint(null, endpoint, EndpointConfiguration.Create(config)), false, "", 60000, null, null);
   var value = session.ReadValue("ns=2;s=MyVariable");
   Console.WriteLine($"Value: {value.Value}");
   ```
3. **服务端示例**：创建 `StandardServer` 派生类，实现自定义节点模型后调用 `Server.Start()`，即可对外提供 OPC UA 服务。  
4. **配置与证书**：使用 `ApplicationInstance` 自动生成或加载 X.509 证书，配合 `SecurityPolicy` 完成安全通信。  

**生产可用性**  
- **成熟度**：项目已稳定多年，官方持续维护，代码质量和测试覆盖率较高，适合作为生产环境的底层通信库。  
- **准备度**：在正式上线前，需要完成以下检查：  
  1. **安全配置**：确认证书管理、加密算法和访问控制符合企业安全策略。  
  2. **性能评估**：根据并发订阅数、消息频率进行压测，必要时调优 `SessionPool`、`Subscription` 参数。  
  3. **依赖管理**：确保目标平台的 .NET Runtime 与库兼容（.NET 5/6/7 推荐），并锁定 NuGet 版本防止意外升级。  
- **适用场景**：原型开发、内部系统集成、以及经充分测试后的生产线监控、数据采集和控制系统均可使用。  

综上，OPCFoundation/UA-.NETStandard 提供了一个可靠、跨平台的 OPC UA 实现，使用 NuGet 即可快速集成，经过安全与性能验证后完全可以在生产环境中部署。

## 🧭 Practical evaluation

**Value:** OPCFoundation/UA-.NETStandard may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 2322 GitHub stars
- 1056 forks
- updated 2026-07-03
- primary language: C#

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 76/100 |
| stars | 72/100 |
| topics | 0/100 |
| outlook | 51/100 |
| quality | 58/100 |
| recency | 40/100 |
| adoption | 73/100 |
| production | 52/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/OPCFoundation/UA-.NETStandard) · [← Back to Misc](./README.md)</sub>
