# C-Eval

> 中文综合能力评估评测集，涵盖52个学科

## 📋 基本信息

| 项目 | 内容 |
|------|------|
| **分类** | Intelligence - 语言理解（中文） |
| **测试条目数** | 13,948题 |
| **输入长度** | 1-2个句子 |
| **输出长度** | 单个选项或简短答案 |
| **评测时间** | 数小时（取决于模型推理速度） |
| **覆盖场景** | 中文模型能力评估 |

---

## 📖 评测集介绍

C-Eval是一个专为评估中文语言模型性能而设计的基准数据集，涵盖52个不同学科，难度涵盖初中、高中、大学和专业级别。

### 特点

- **中文评测**: 专门针对中文模型
- **多学科覆盖**: 52个学科
- **多难度级别**: 初中、高中、大学、专业级别
- **全面评估**: 评估模型在中文环境下的高级知识和推理能力

### 适用场景

- 中文模型能力评估
- 多学科知识评估
- 中文理解能力评估

---

## 🔗 资源链接

- **GitHub**: [C-Eval](https://github.com/SJTU-LIT/ceval)
- **论文**: [C-Eval论文](https://arxiv.org/abs/2305.08322)
- **数据集**: [Hugging Face](https://huggingface.co/datasets/ceval/ceval-exam)

---

## 📖 使用指南

### 1. 数据准备

```bash
# 使用Hugging Face下载
from datasets import load_dataset

dataset = load_dataset("ceval/ceval-exam")
```

### 2. 运行评测

#### 使用OpenCompass

```python
from opencompass import OpenCompass

config = {
    'dataset': 'ceval_gen',
    'model': 'your_model',
    'temperature': 0
}

result = OpenCompass.run(config)
```

### 3. 结果分析

- **整体准确率**: 计算所有学科的平均准确率
- **学科分析**: 分析不同学科的表现
- **难度分析**: 分析不同难度级别的表现

---

## ⚙️ 评测参数

- **Temperature**: 0（确定性输出）
- **测试次数**: 通常测试1次
- **覆盖学科**: 52个学科

---

## 💡 最佳实践

1. **完整评测**: 建议评测所有52个学科
2. **学科分析**: 分析模型在不同学科的表现
3. **难度分析**: 分析模型在不同难度级别的表现
4. **对比分析**: 与其他中文模型对比

---

## 📊 参考结果

| 模型 | 准确率 | 备注 |
|------|--------|------|
| GPT-4 | ~85% | 参考值 |
| Qwen-72B | ~82% | 参考值 |

*注：以上为参考值，实际结果可能因评测环境而异*

---

## 📚 相关资源

- [C-Eval GitHub](https://github.com/SJTU-LIT/ceval)
- [C-Eval论文](https://arxiv.org/abs/2305.08322)
- [Intelligence维度指南](../../../intelligence/README.md)

---

**最后更新**: 2025-11-30

