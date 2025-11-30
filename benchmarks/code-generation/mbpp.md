# MBPP

> 入门级Python编程题，大规模代码生成评测

## 📋 基本信息

| 项目 | 内容 |
|------|------|
| **分类** | Intelligence - 代码生成 |
| **测试条目数** | 974题 |
| **输入长度** | 编程问题描述，通常1-2个段落 |
| **输出长度** | 完整函数实现，通常5-30行代码 |
| **评测时间** | 约3-6小时（974题） |
| **覆盖场景** | 入门级Python编程能力评估 |

---

## 📖 评测集介绍

MBPP（Mostly Basic Python Problems）是入门级Python编程题数据集，包含974题，用于评估模型在基础Python编程任务上的能力。

### 特点

- **入门级**: 基础Python编程问题
- **大规模**: 974题，适合大规模评测
- **实用性强**: 贴近实际编程任务
- **输入输出**: 输入为1-2个段落的编程问题描述，输出为完整函数实现（通常5-30行代码，100-500 tokens）

### 适用场景

- 代码生成能力大规模评估
- 基础Python编程能力评估
- 代码生成模型对比

### 适用模型

- **所有规模模型**: 适合所有规模的模型，是代码生成的基础评测集
- **代码专用模型**: 特别推荐，如CodeLlama、StarCoder等
- **通用大模型**: 推荐使用，能全面评估代码生成能力

---

## 🔗 资源链接

- **GitHub**: [MBPP](https://github.com/google-research/google-research/tree/master/mbpp)
- **数据集**: [Hugging Face](https://huggingface.co/datasets/mbpp)
- **论文**: 待定

---

## 📖 使用指南

### 1. 数据准备

```python
from datasets import load_dataset

dataset = load_dataset("mbpp")
test_set = dataset["test"]  # 974题
```

### 2. 运行评测

#### 使用OpenCompass

```python
from opencompass import OpenCompass

config = {
    'dataset': 'mbpp',
    'model': 'your_model',
    'temperature': 0
}

result = OpenCompass.run(config)
```

### 3. 结果分析

- **Pass@k**: 计算Pass@1、Pass@10、Pass@100
- **代码质量**: 分析生成的代码质量
- **错误分析**: 分析错误类型和原因

---

## ⚙️ 评测参数

- **Temperature**: 0（确定性输出）
- **测试次数**: 通常测试1次
- **Max Tokens**: 根据题目复杂度，通常200-500

---

## 📝 输入输出示例

### 示例1: 列表操作

**输入（Input）**:
```python
def remove_duplicates(lst):
    """Remove duplicates from a list while preserving order.
    
    >>> remove_duplicates([1, 2, 2, 3, 4, 4, 5])
    [1, 2, 3, 4, 5]
    >>> remove_duplicates(['a', 'b', 'b', 'c'])
    ['a', 'b', 'c']
    """
```

**期望输出（Expected Output）**:
```python
def remove_duplicates(lst):
    """Remove duplicates from a list while preserving order.
    
    >>> remove_duplicates([1, 2, 2, 3, 4, 4, 5])
    [1, 2, 3, 4, 5]
    >>> remove_duplicates(['a', 'b', 'b', 'c'])
    ['a', 'b', 'c']
    """
    seen = set()
    result = []
    for item in lst:
        if item not in seen:
            seen.add(item)
            result.append(item)
    return result
```

### 示例2: 字符串处理

**输入（Input）**:
```python
def count_words(text):
    """Count the number of words in a text string.
    
    >>> count_words("Hello world")
    2
    >>> count_words("This is a test")
    4
    """
```

**期望输出（Expected Output）**:
```python
def count_words(text):
    """Count the number of words in a text string.
    
    >>> count_words("Hello world")
    2
    >>> count_words("This is a test")
    4
    """
    return len(text.split())
```

### 示例3: 数学计算

**输入（Input）**:
```python
def factorial(n):
    """Calculate the factorial of a number.
    
    >>> factorial(5)
    120
    >>> factorial(0)
    1
    """
```

**期望输出（Expected Output）**:
```python
def factorial(n):
    """Calculate the factorial of a number.
    
    >>> factorial(5)
    120
    >>> factorial(0)
    1
    """
    if n == 0 or n == 1:
        return 1
    result = 1
    for i in range(2, n + 1):
        result *= i
    return result
```

---

## 💡 最佳实践

1. **使用测试用例**: 使用提供的测试用例验证代码
2. **代码质量**: 不仅关注通过率，还关注代码质量
3. **错误分析**: 深入分析错误案例，找出模型弱点

---

## 📊 参考结果

| 模型 | Pass@1 | 备注 |
|------|--------|------|
| DeepSeek R1 | 待定 | 参考值 |

*注：以上为参考值，实际结果可能因评测环境而异*

---

## 📚 相关资源

- [MBPP GitHub](https://github.com/google-research/google-research/tree/master/mbpp)
- [Intelligence维度指南](../../../intelligence/README.md)

---

**最后更新**: 2025-11-30

