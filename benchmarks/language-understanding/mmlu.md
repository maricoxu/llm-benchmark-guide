# MMLU

> 多任务语言理解评测集，业界标准基准

## 📋 基本信息

| 项目 | 内容 |
|------|------|
| **分类** | Intelligence - 语言理解 |
| **测试条目数** | ~14,000题 |
| **输入长度** | 平均1-2个句子 |
| **输出长度** | 单个选项或简短答案 |
| **评测时间** | 单次评测：约2-4小时（取决于模型推理速度） |
| **覆盖场景** | 多领域语言理解能力评估 |

---

## 📖 评测集介绍

MMLU（Massive Multitask Language Understanding）是一个大规模多任务语言理解评测集，包含约14,000道题目，涵盖57个不同的任务和领域，是业界广泛使用的标准基准。

### 特点

- **大规模**: 包含约14,000道题目
- **多领域**: 涵盖57个不同的任务和领域
- **标准基准**: 业界广泛使用的评测集
- **输入输出**: 输入通常为1-2个句子的选择题，输出为单个选项（A/B/C/D）

### 与MMLU-Pro的区别

- **MMLU**: 原版MMLU，支持标准上下文长度
- **MMLU-Pro**: 扩展版本，支持16K长上下文，题目可能有所不同

### 适用场景

- 通用能力评估
- 多领域知识理解评估
- 模型能力基准测试

### 适用模型

- **大模型（>10B）**: 推荐使用，能充分发挥模型能力
- **中等模型（1B-10B）**: 可以使用，但可能表现有限
- **小模型（<1B）**: 不推荐，难度过高

---

## 🔗 资源链接

- **GitHub**: [MMLU](https://github.com/hendrycks/test)
- **论文**: [MMLU论文](https://arxiv.org/abs/2009.03300)
- **数据集**: [Hugging Face](https://huggingface.co/datasets/cais/mmlu)

---

## 📖 使用指南

### 1. 数据准备

```python
from datasets import load_dataset

# 使用Hugging Face下载
dataset = load_dataset("cais/mmlu", "all")
test_set = dataset["test"]  # 约14,000题
```

### 2. 运行评测

#### 使用OpenCompass

```python
from opencompass import OpenCompass

config = {
    'dataset': 'mmlu',
    'model': 'your_model',
    'temperature': 0
}

result = OpenCompass.run(config)
```

#### 使用lm-evaluation-harness

```bash
lm_eval --model hf \
    --model_args pretrained=your_model \
    --tasks mmlu \
    --batch_size 1
```

### 3. 结果分析

- **整体准确率**: 计算所有题目的平均准确率
- **领域分析**: 分析不同领域的表现
- **任务分析**: 分析不同任务的表现
- **错误分析**: 分析错误案例

---

## ⚙️ 评测参数

- **Temperature**: 0（确定性输出）
- **测试次数**: 通常测试1次
- **覆盖领域**: 57个不同的任务和领域

---

## 💡 最佳实践

1. **使用固定参数**: Temperature=0，确保结果可复现
2. **完整评测**: 建议评测所有57个任务
3. **领域分析**: 分析模型在不同领域的表现
4. **对比分析**: 与基准模型对比，了解模型水平

---

## 📝 输入输出示例

> **注意**: 以下示例基于MMLU数据集的典型格式，用于说明评测集的结构。真实题目请从[MMLU GitHub仓库](https://github.com/hendrycks/test)或[Hugging Face](https://huggingface.co/datasets/cais/mmlu)获取。

### 示例1: 历史类题目

**输入（Input）**:
```
问题: 以下哪个事件标志着第一次世界大战的结束？

A. 凡尔赛条约的签署
B. 德国投降
C. 奥匈帝国解体
D. 俄国革命

请选择正确答案。
```

**期望输出（Expected Output）**:
```
B. 德国投降

第一次世界大战于1918年11月11日以德国投降而结束。凡尔赛条约是战后和平条约，签署于1919年。
```

### 示例2: 科学类题目

**输入（Input）**:
```
问题: 在生物学中，DNA的双螺旋结构是由谁发现的？

A. 达尔文和孟德尔
B. 沃森和克里克
C. 巴斯德和科赫
D. 门捷列夫和居里

请选择正确答案。
```

**期望输出（Expected Output）**:
```
B. 沃森和克里克

DNA的双螺旋结构是由詹姆斯·沃森和弗朗西斯·克里克在1953年发现的。
```

### 示例3: 数学类题目

**输入（Input）**:
```
问题: 如果一个数的平方等于16，那么这个数可能是多少？

A. 只有4
B. 只有-4
C. 4或-4
D. 8或-8

请选择正确答案。
```

**期望输出（Expected Output）**:
```
C. 4或-4

因为 4² = 16 且 (-4)² = 16，所以这个数可能是4或-4。
```

---

## 📊 参考结果

| 模型 | 准确率 | 备注 |
|------|--------|------|
| GPT-4 | ~86% | 参考值 |
| Claude-3 | ~85% | 参考值 |
| GPT-3.5 | ~70% | 参考值 |

*注：以上为参考值，实际结果可能因评测环境而异*

---

## 📚 相关资源

- [MMLU GitHub](https://github.com/hendrycks/test)
- [MMLU-Pro](mmlu-pro.md) - 支持16K长上下文的扩展版本
- [OpenCompass文档](https://opencompass.readthedocs.io/)
- [Intelligence维度指南](../../../intelligence/README.md)

---

**最后更新**: 2025-01-XX

