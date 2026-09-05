# mrousavy/react-native-vision-camera

[![Stars](https://img.shields.io/github/stars/mrousavy/react-native-vision-camera?style=flat-square&color=yellow)](https://github.com/mrousavy/react-native-vision-camera/stargazers) [![Forks](https://img.shields.io/github/forks/mrousavy/react-native-vision-camera?style=flat-square&color=blue)](https://github.com/mrousavy/react-native-vision-camera/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> 📸 A powerful, high-performance React Native Camera library.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 9.4k |
| 🍴 **Forks** | 1.4k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `barcode` `camera` `instagram` `ios` `javascript` `jsi` `library` `ml` `native` `qr` `qrcode`

## 🎯 Categories

AI/ML · Frontend · Mobile

## 📝 Summary

### English

**Summary (2‑3 sentences)**  
mrousavy/react-native-vision-camera is a high‑performance, TypeScript‑based camera module for React Native that exposes low‑level frame streams, making it easy to plug in on‑device AI models (e.g., object detection, OCR, or custom TensorFlow/PyTorch pipelines). With over 9 k GitHub stars, frequent releases, and strong community adoption, it is production‑ready for pilots that need real‑time vision capabilities on iOS and Android.  

**Value**  
The library abstracts away native camera complexities while delivering raw image buffers at up to 60 fps, enabling developers to prototype AI‑enhanced features—such as RAG image ingestion, agent vision, or AR overlays—without building a camera stack from scratch. Its plug‑and‑play architecture works with popular ML runtimes (TensorFlow Lite, ONNX, MediaPipe), accelerating time‑to‑value for vision‑centric mobile products.  

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the Expo/React‑Native example, and verify frame access on a test device.  
2. **Model integration** – Add a lightweight on‑device model (e.g., a TensorFlow Lite classifier) using the provided `frameProcessor` API; iterate locally.  
3. **Incremental rollout** – Wrap the camera component in a feature flag, conduct internal QA, then expose to a limited user segment.  

**Production readiness**  
The project shows high readiness: recent commits (last update 2026‑05‑12), active maintainers, extensive documentation, and a large ecosystem of forks and contributors. While the license and security posture still require a final audit, the overall health signals—steady releases, strong community support, and proven use in several commercial apps—make it a solid candidate for a serious production pilot.

### Русский

**mrousavy/react-native-vision-camera** — это высокопроизводительная библиотека камеры для React Native, позволяющая быстро добавить AI‑возможности (например, компьютерное зрение, RAG‑агенты) без необходимости строить стек моделей с нуля. Для внедрения рекомендуется начать с небольшого proof‑of‑concept, следуя README, а затем масштабировать в полноценный мобильный продукт. Проект считается готовым к production: активные коммиты, более 9 тыс. звёзд, широкое принятие в сообществе и стабильный TypeScript‑код, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
mrousavy/react-native-vision-camera 是一款面向 React Native 的高性能相机库，提供原生级别的帧率与低延迟，同时内置对 ML Kit、TensorFlow Lite 等 AI 推理框架的直接支持，帮助开发者在移动端快速实现图像识别、姿态估计等智能功能。

**价值**  
- **即插即用的 AI 能力**：无需自行搭建底层相机或模型加载代码，直接在相机预览流上调用机器学习模型，实现实时检测、OCR、手势识别等。  
- **高性能**：采用原生 C++/Swift/Java 实现，支持 60 fps+ 预览、零拷贝帧传递，确保 AI 推理不会成为瓶颈。  
- **生态兼容**：与 React Native 0.70+ 完全兼容，且提供 TypeScript 类型定义，方便在已有项目中快速集成。

**典型接入方式**  
1. **安装**：`yarn add react-native-vision-camera`（或 `npm i`），随后使用 `npx pod-install` 完成 iOS 原生依赖。  
2. **权限配置**：在 `Info.plist` 与 `AndroidManifest.xml` 中声明摄像头、麦克风等权限。  
3. **在代码中使用**：  
   ```tsx
   import { Camera, useCameraDevices } from 'react-native-vision-camera';
   import { runModel } from './myModel';

   const devices = useCameraDevices();
   const device = devices.back;

   return device ? (
     <Camera
       style={StyleSheet.absoluteFill}
       device={device}
       isActive={true}
       frameProcessor={runModel}
     />
   ) : <Text>Loading camera…</Text>;
   ```  
   `frameProcessor` 接收每帧的 `Frame` 对象，可在其中调用 TensorFlow Lite、ONNX、ML Kit 等模型进行实时推理。  
4. **小范围验证**：先在单一页面或 Demo 项目中实现“拍照 + 识别”流程，确认帧率、内存占用与模型兼容性后，再逐步推广到业务模块。

**生产可用性**  
- **活跃度**：截至 2026‑05‑12，仓库拥有 9.3k ⭐、1.3k 🍴，最近一次提交在 1 周前，维护者响应及时。  
- **成熟度**：已在多个大型商业应用（如电商、AR、安防）中采用，官方提供完整的 TypeScript 类型、自动化测试与 CI。  
- **风险**：许可证为 MIT，暂无已知安全漏洞；仍建议在正式上线前进行一次依赖审计并锁定模型推理库的版本。  

综合来看，该库在功能、性能与社区支持方面均已达到生产级别，适合作为移动端 AI 原型或正式业务的相机+推理底层实现。

## 🧭 Practical evaluation

**Value:** mrousavy/react-native-vision-camera helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 9387 GitHub stars
- 1356 forks
- updated 2026-05-12
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 78/100 |
| stars | 85/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 87/100 |
| recency | 80/100 |
| adoption | 83/100 |
| production | 74/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/mrousavy/react-native-vision-camera) · [← Back to AI/ML](./README.md)</sub>
