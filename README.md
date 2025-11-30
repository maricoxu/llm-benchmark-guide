# 🚀 LLM Benchmark Guide

> **The Comprehensive Guide to Evaluating and Analyzing AI Model Capabilities**

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

<div align="center">

**全面的LLM评测集指南，按Intelligence、Speed、Price、Hardware四维分类组织**

[English](#) | [中文](#)

</div>

---

## 📖 为什么需要这个指南？

在AI快速发展的今天，如何**科学地评估和分析AI模型的能力**成为了关键问题。

### 🤔 你是否有这些困惑？

- ❓ **评测集太多，不知道如何选择？**
- ❓ **评测结果看不懂，不知道如何分析？**
- ❓ **训练后评估和推理引擎评估有什么区别？**
- ❓ **如何从Intelligence、Speed、Price、Hardware四个维度全面评估模型？**

### ✨ 这个指南能帮你什么？

✅ **信息全面**: 覆盖所有主流评测集，持续更新  
✅ **逻辑清晰**: 按Intelligence/Speed/Price/Hardware四维分类  
✅ **使用方便**: 提供选择指南、使用示例、工具集成  
✅ **深度解析**: 不仅告诉你是什么，还告诉你为什么和怎么做  

---

## 🎯 核心价值

### 1. 系统化的评测集分类

我们按照 **Artificial Analysis** 的分类方法，将评测集分为四个维度：

- 🧠 **Intelligence（智能程度）**: 评估模型的准确性、推理能力和适应性
- ⚡ **Speed（速度）**: 衡量模型的推理速度、延迟和吞吐量
- 💰 **Price（价格）**: 考虑模型训练和推理的成本
- 🖥️ **Hardware（硬件）**: 评估硬件平台的性能表现

### 2. 全面的评测集覆盖

- 📚 **50+ 主流评测集**: MMLU、HumanEval、GSM8K、LiveCodeBench等
- 🔍 **详细文档**: 每个评测集都有详细的介绍和使用指南
- 🔗 **资源链接**: GitHub、论文、数据集链接一应俱全

### 3. 实用的使用指南

- 📖 **选择指南**: 告诉你如何根据需求选择评测集
- 🛠️ **工具集成**: OpenCompass、lm-evaluation-harness等工具使用
- 💡 **最佳实践**: 评测方法、结果分析、报告撰写

---

## 🗺️ 快速导航

### 📊 评测集分类

| 维度 | 说明 | 文档 |
|------|------|------|
| 🧠 **Intelligence** | 智能程度评估 | [查看详情](intelligence/README.md) |
| ⚡ **Speed** | 速度评估 | [查看详情](speed/README.md) |
| 💰 **Price** | 成本分析 | [查看详情](price/README.md) |
| 🖥️ **Hardware** | 硬件评测 | [查看详情](hardware/README.md) |

### 📚 评测集详细列表

**主要评测集目录**: [benchmarks/](benchmarks/)

- [语言理解](benchmarks/language-understanding/) - MMLU、C-Eval、Xiezhi等
- [数学推理](benchmarks/math-reasoning/) - AIME、GSM8K、MATH等
- [代码生成](benchmarks/code-generation/) - HumanEval、LiveCodeBench等
- [推理能力](benchmarks/reasoning/) - BBH、AA-LCR等
- [多模态](benchmarks/multimodal/) - MMMU、MMStar等
- [综合能力](benchmarks/comprehensive/) - Terminal Bench、τ²-Bench等

### 🛠️ 工具和指南

- [评测工具](tools/) - OpenCompass、lm-evaluation-harness等
- [使用指南](guides/) - 快速开始、选择指南、问题排查
- [资源集合](resources/) - 论文、数据集、Awesome Lists

---

## 🚀 快速开始

### 1. 选择合适的评测集

根据你的需求选择评测集：

- **评估模型能力** → [Intelligence维度](intelligence/README.md)
- **评估推理速度** → [Speed维度](speed/README.md)
- **分析成本效益** → [Price维度](price/README.md)
- **评估硬件性能** → [Hardware维度](hardware/README.md)

### 2. 查看评测集详情

进入 [benchmarks/](benchmarks/) 目录，查看具体评测集的详细文档。

### 3. 使用评测工具

参考 [tools/](tools/) 目录，使用OpenCompass等工具进行评测。

### 4. 阅读使用指南

查看 [guides/](guides/) 目录，了解评测方法和最佳实践。

---

## 📊 评测集统计

<div align="center">

| 维度 | 评测集数量 | 覆盖领域 |
|------|-----------|---------|
| 🧠 Intelligence | 30+ | 语言理解、数学推理、代码生成、多模态等 |
| ⚡ Speed | 10+ | 延迟、吞吐量、优化等 |
| 💰 Price | 5+ | 成本分析、ROI等 |
| 🖥️ Hardware | 10+ | GPU、TPU、能效比等 |

**总计**: 50+ 评测集，持续更新中...

</div>

---

## 🎓 如何分析AI模型能力？

### 第一步：明确评估目标

- **模型能力评估**: 评估模型在任务上的表现
- **推理引擎评估**: 验证推理引擎的精度和性能
- **成本效益分析**: 分析模型的使用成本

### 第二步：选择评测集

根据评估目标选择合适的评测集：

- **通用能力**: MMLU、C-Eval
- **数学能力**: AIME、GSM8K、MATH
- **代码能力**: HumanEval、LiveCodeBench
- **多模态能力**: MMMU、MMStar

### 第三步：运行评测

使用评测工具（如OpenCompass）运行评测，获取结果。

### 第四步：分析结果

- **任务指标**: 准确率、F1等
- **对比分析**: 与基准模型对比
- **错误分析**: 分析错误案例

### 第五步：综合评估

从Intelligence、Speed、Price、Hardware四个维度综合评估。

---

## 📈 项目路线图

### Phase 1: 基础建设（已完成）
- [x] 仓库结构设计
- [x] 核心评测集文档（30+）
- [x] 四维分类体系
- [x] 使用指南

### Phase 2: 工具集成（进行中）
- [ ] OpenCompass集成示例 - 为每个评测集提供OpenCompass配置文件
- [ ] lm-evaluation-harness集成示例 - 为每个评测集提供lm-eval配置
- [ ] 自定义评测模板 - 提供自定义评测的模板和框架
- [ ] 自动化评测脚本 - 批量评测和报告生成工具

> 💡 **为什么需要工具集成？** 降低使用门槛，提供开箱即用的配置和示例，让用户快速上手。

### Phase 3: 社区建设（计划中）
- [ ] 评测结果对比
- [ ] 社区贡献指南
- [ ] 定期更新评测集
- [ ] 建立评测标准

---

## 🤝 贡献

欢迎贡献！请查看 [CONTRIBUTING.md](CONTRIBUTING.md) 了解如何贡献。

### 贡献方式

- 🐛 **报告问题**: 在Issues中报告问题或提出建议
- 📝 **改进文档**: 改进文档、添加评测集
- 💻 **提交代码**: 提交评测工具、示例代码
- 🌟 **Star支持**: Star一下，让更多人看到

---

## 📚 相关资源

### Awesome系列

- [awesome-LLM-benchmarks](https://github.com/wgwang/awesome-LLM-benchmarks) - 评测集资源集合
- [awesome-LLMs-In-China](https://github.com/wgwang/awesome-LLMs-In-China) - 中国大模型列表

### 评测平台

- [Artificial Analysis](https://artificialanalysis.ai/) - AI模型评测平台
- [Papers with Code](https://paperswithcode.com/) - 论文和代码集合

### 评测工具

- [OpenCompass](https://github.com/open-compass/opencompass) - 开源评测框架
- [lm-evaluation-harness](https://github.com/EleutherAI/lm-evaluation-harness) - EleutherAI评测框架
- [EvalScope](https://github.com/modelscope/evalscope) - ModelScope评测框架（支持多种模型类型和评测场景）

---

## 📱 关注我们

<div align="center">

### 微信公众号：老许漫谈AIInfra

<img src="imgs/wechat-qrcode.png" alt="微信公众号" width="200"/>

**扫码关注，获取更多AI系统知识**

- 📖 技术文章和深度解析
- 🔍 评测集使用指南
- 💡 最佳实践和案例分享
- 🎯 行业动态和技术趋势

**在微信中搜索"老许漫谈AIInfra"也可以找到我们**

</div>

---

## 📄 许可证

本项目采用 [MIT License](LICENSE) 许可证。

---

<div align="center">

**如果这个项目对你有帮助，请给一个 ⭐ Star！**

Made with ❤️ by [老许漫谈AIInfra](https://github.com/maricoxu)

</div>

