# 评测集详细分类

> 全面的评测集文档，按任务类型分类组织

## 📋 分类总览

| 分类 | 说明 | 评测集数量 | 文档 |
|------|------|-----------|------|
| [语言理解](language-understanding/) | 评估语言理解能力 | 10+ | [查看](language-understanding/README.md) |
| [数学推理](math-reasoning/) | 评估数学推理能力 | 8+ | [查看](math-reasoning/README.md) |
| [代码生成](code-generation/) | 评估代码生成能力 | 6+ | [查看](code-generation/README.md) |
| [推理能力](reasoning/) | 评估推理能力 | 5+ | [查看](reasoning/README.md) |
| [多模态](multimodal/) | 评估多模态能力 | 8+ | [查看](multimodal/README.md) |
| [综合能力](comprehensive/) | 评估综合能力 | 5+ | [查看](comprehensive/README.md) |

---

## 🔍 快速查找

### 按评测集名称

#### 语言理解类
- [MMLU](language-understanding/mmlu.md) - 多任务语言理解（标准版）
- [MMLU-Pro](language-understanding/mmlu-pro.md) - 多领域语言理解（16K长上下文）
- [C-Eval](language-understanding/c-eval.md) - 中文综合能力评估
- [Xiezhi](language-understanding/xiezhi.md) - 领域知识评估
- [GPQA Diamond](language-understanding/gpqa-diamond.md) - 科学专业知识
- [SimpleQA](language-understanding/simpleqa.md) - 简单问答评测集
- [IFBench](language-understanding/ifbench.md) - 人机交互

#### 数学推理类
- [AIME](math-reasoning/aime.md) - 美国数学邀请赛
- [GSM8K](math-reasoning/gsm8k.md) - 小学数学问题
- [MATH500](math-reasoning/math500.md) - 数学竞赛题目

#### 代码生成类
- [HumanEval](code-generation/humaneval.md) - Python编程能力
- [LiveCodeBench](code-generation/livecodebench.md) - 真实代码任务
- [MBPP](code-generation/mbpp.md) - 入门级Python编程
- [Code Generation Lite](code-generation/code-generation-lite.md) - 代码生成轻量版
- [SciCode](code-generation/scicode.md) - 科学计算代码

### 按使用场景

- **通用能力评估**: [MMLU](language-understanding/mmlu.md)、[MMLU-Pro](language-understanding/mmlu-pro.md)、[C-Eval](language-understanding/c-eval.md)
- **数学能力评估**: [AIME](math-reasoning/aime.md)、[GSM8K](math-reasoning/gsm8k.md)、[MATH500](math-reasoning/math500.md)
- **代码能力评估**: [HumanEval](code-generation/humaneval.md)、[LiveCodeBench](code-generation/livecodebench.md)
- **多模态能力评估**: [MMMU](multimodal/mmmu.md)、[MMStar](multimodal/mmstar.md)、[HallusionBench](multimodal/hallusionbench.md)、[Al2D_TEST](multimodal/al2d-test.md)、[OCRBench](multimodal/ocrbench.md)
- **综合能力评估**: [AGIEval](comprehensive/agieval.md)、[GeoBench](comprehensive/geobench.md)、[Terminal Bench Hard](comprehensive/terminal-bench.md)、[τ²-Bench Telecom](comprehensive/tau2-bench-telecom.md)
- **推理能力评估**: [BBH](reasoning/bbh.md)、[AA-LCR](reasoning/aa-lcr.md)、[Humanity's Last Exam](reasoning/humanitys-last-exam.md)

---

## 📚 评测集详细文档

每个评测集都有独立的文档，包含：

- 📋 **基本信息**: 测试条目数、输入/输出长度、评测时间
- 🔗 **资源链接**: GitHub、论文、数据集链接
- 📖 **使用指南**: 如何使用评测集
- 💡 **最佳实践**: 评测方法和注意事项
- 📊 **结果分析**: 如何分析评测结果

---

## 🎯 评测集选择指南

### 根据评估目标选择

| 评估目标 | 推荐评测集 |
|---------|-----------|
| **通用能力** | MMLU-Pro、C-Eval、Xiezhi |
| **数学能力** | AIME、GSM8K、MATH500 |
| **代码能力** | HumanEval、LiveCodeBench、MBPP |
| **推理能力** | BBH、AA-LCR |
| **多模态能力** | MMMU、MMStar、HallusionBench |

### 根据模型规模选择

| 模型规模 | 推荐评测集 |
|---------|-----------|
| **小模型（<1B）** | GSM8K、HumanEval |
| **中等模型（1B-10B）** | MMLU、C-Eval、MATH500 |
| **大模型（>10B）** | MMLU-Pro、AIME、LiveCodeBench |

### 根据应用场景选择

| 应用场景 | 推荐评测集 |
|---------|-----------|
| **中文应用** | C-Eval、Xiezhi、CLUE |
| **代码应用** | HumanEval、LiveCodeBench、MBPP |
| **数学应用** | AIME、GSM8K、MATH500 |
| **多模态应用** | MMMU、MMStar |

---

## 📊 评测集统计

<div align="center">

| 分类 | 评测集数量 | 主要评测集 |
|------|-----------|-----------|
| 语言理解 | 10+ | MMLU、MMLU-Pro、C-Eval、Xiezhi、GPQA Diamond、SimpleQA、IFBench |
| 数学推理 | 8+ | AIME2024/2025、GSM8K、MATH500 |
| 代码生成 | 6+ | HumanEval、LiveCodeBench v5/v6、MBPP、Code Generation Lite、SciCode |
| 推理能力 | 5+ | BBH、AA-LCR、Humanity's Last Exam |
| 多模态 | 8+ | MMMU、MMStar、HallusionBench、Al2D_TEST、OCRBench |
| 综合能力 | 5+ | AGIEval、GeoBench、Terminal Bench Hard、τ²-Bench Telecom |

**总计**: 40+ 评测集，持续更新中...

</div>

---

## 🤝 贡献

欢迎添加新的评测集或改进现有文档！

### 如何贡献

1. Fork 本仓库
2. 创建新的评测集文档或改进现有文档
3. 提交 Pull Request

### 文档格式

请参考现有评测集文档的格式，包含：
- 基本信息表格
- 评测集介绍
- 资源链接
- 使用指南
- 最佳实践

---

## 📚 相关资源

- [Intelligence维度指南](../intelligence/README.md)
- [评测工具](../tools/README.md)
- [使用指南](../guides/README.md)

---

**最后更新**: 2025-11-30

