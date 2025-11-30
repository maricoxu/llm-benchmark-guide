# MMMU

> 跨学科多模态理解评测集

## 📋 基本信息

| 项目 | 内容 |
|------|------|
| **分类** | Intelligence - 多模态 |
| **测试条目数** | 待定 |
| **输入长度** | 多模态输入（图像、文本等） |
| **输出长度** | 综合答案 |
| **评测时间** | 待定 |
| **覆盖场景** | 跨学科多模态理解能力评估 |

---

## 📖 评测集介绍

MMMU（Massive Multitask Multimodal Understanding）是跨学科多模态理解评测集，用于评估模型在多模态任务上的能力。

### 特点

- **跨学科**: 涵盖多个学科
- **多模态**: 图像、文本等多模态输入
- **综合理解**: 评估综合多模态理解能力

### 适用场景

- 多模态能力评估
- 跨学科多模态理解评估
- 综合多模态能力评估

---

## 🔗 资源链接

- **GitHub**: [MMMU](https://github.com/MMMU-Benchmark/MMMU)
- **论文**: 待定
- **数据集**: 待定

---

## 📖 使用指南

### 1. 数据准备

```python
# 待定具体的数据加载方法
```

### 2. 运行评测

#### 使用OpenCompass

```python
from opencompass import OpenCompass

config = {
    'dataset': 'mmmu',
    'model': 'your_model',
    'temperature': 0
}

result = OpenCompass.run(config)
```

### 3. 结果分析

- **准确率**: 计算正确答案的比例
- **学科分析**: 分析不同学科的表现
- **模态分析**: 分析不同模态的表现

---

## ⚙️ 评测参数

- **Temperature**: 待定
- **测试次数**: 待定
- **覆盖模型**: Qwen3-VL-235B-A22B-Instruct, Qwen3-VL-235B-A22B-Thinking等

---

## 📝 输入输出示例

### 示例1: 图像理解

**输入（Input）**:
```
图像: [一张包含数学公式的图像]
问题: 这个公式表示什么？

请给出答案。
```

**期望输出（Expected Output）**:
```
这是欧拉公式：e^(iπ) + 1 = 0
它连接了数学中最重要的几个常数。
```

### 示例2: 图表理解

**输入（Input）**:
```
图像: [一张柱状图，显示不同国家的GDP]
问题: 哪个国家的GDP最高？

请给出答案。
```

**期望输出（Expected Output）**:
```
根据图表，美国的GDP最高。
```

---

## 📊 参考结果

| 模型 | 准确率 | 备注 |
|------|--------|------|
| Qwen3-VL-235B-Instruct | 70.44 | 参考值 |
| Qwen3-VL-235B-Thinking | 66.33 | 参考值 |
| InTernVL3-38B | 70.67 | 参考值 |
| Qwen2.5-VL-72B | 68.33 | 参考值 |

*注：以上为参考值，实际结果可能因评测环境而异*

---

## 📚 相关资源

- [MMMU GitHub](https://github.com/MMMU-Benchmark/MMMU)
- [Intelligence维度指南](../../../intelligence/README.md)

---

**最后更新**: 2025-11-30

