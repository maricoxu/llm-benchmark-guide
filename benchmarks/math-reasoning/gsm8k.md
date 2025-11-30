# GSM8K

> 小学数学问题评测集，评估基础数学推理能力

## 📋 基本信息

| 项目 | 内容 |
|------|------|
| **分类** | Intelligence - 数学推理 |
| **测试条目数** | 1,319题（测试集），8,500题（训练集） |
| **输入长度** | 1-2个句子 |
| **输出长度** | 数值答案或简短解题过程 |
| **评测时间** | 约2-4小时（1,319题） |
| **覆盖场景** | 基础数学推理能力 |

---

## 📖 评测集介绍

GSM8K（Grade School Math 8K）是一个包含8,500个小学数学问题的数据集，旨在评估模型的数学推理能力。测试集包含1,319题。

### 特点

- **基础数学**: 小学到初中水平的数学问题
- **推理过程**: 需要多步推理才能解决
- **标准评测**: 业界广泛使用的数学推理评测集

### 适用场景

- 基础数学推理能力评估
- 数学推理能力基准测试
- 模型数学能力快速评估

---

## 🔗 资源链接

- **GitHub**: [GSM8K](https://github.com/openai/grade-school-math)
- **数据集**: [Hugging Face](https://huggingface.co/datasets/gsm8k)
- **论文**: [GSM8K论文](https://arxiv.org/abs/2110.14168)

---

## 📖 使用指南

### 1. 数据准备

```python
from datasets import load_dataset

dataset = load_dataset("gsm8k", "main")
test_set = dataset["test"]  # 1,319题
```

### 2. 运行评测

#### 使用OpenCompass

```python
from opencompass import OpenCompass

config = {
    'dataset': 'gsm8k_gen',
    'model': 'your_model',
    'temperature': 0
}

result = OpenCompass.run(config)
```

### 3. 结果分析

- **准确率**: 计算正确答案的比例
- **推理过程分析**: 分析模型的推理过程是否正确
- **错误分析**: 分析错误类型和原因

---

## ⚙️ 评测参数

- **Temperature**: 0（确定性输出）
- **测试次数**: 通常测试1次
- **Max Tokens**: 根据题目复杂度，通常100-500

---

## 💡 最佳实践

1. **使用Chain-of-Thought**: 要求模型展示推理过程
2. **验证计算**: 验证模型的计算是否正确
3. **错误分析**: 深入分析错误案例，找出模型弱点

---

## 📊 参考结果

| 模型 | 准确率 | 备注 |
|------|--------|------|
| GPT-4 | ~97% | 参考值 |
| GPT-3.5 | ~57% | 参考值 |

*注：以上为参考值，实际结果可能因评测环境而异*

---

## 📚 相关资源

- [GSM8K GitHub](https://github.com/openai/grade-school-math)
- [Intelligence维度指南](../../../intelligence/README.md)

---

**最后更新**: 2025-11-30

