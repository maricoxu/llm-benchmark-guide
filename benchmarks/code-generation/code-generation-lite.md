# Code Generation Lite

> 代码生成轻量版评测集，快速评估代码生成能力

## 📋 基本信息

| 项目 | 内容 |
|------|------|
| **分类** | Intelligence - 代码生成 |
| **测试条目数** | 待定（轻量版，题目数量较少） |
| **输入长度** | 函数签名和问题描述，通常1-3个句子 |
| **输出长度** | 完整函数实现，通常5-30行代码 |
| **评测时间** | 约30-60分钟 |
| **覆盖场景** | 代码生成能力快速评估 |

---

## 📖 评测集介绍

Code Generation Lite是代码生成评测集的轻量版本，包含较少的题目，用于快速评估模型的代码生成能力。适合需要快速测试或资源有限的情况。

### 特点

- **轻量快速**: 题目数量较少，评测时间短
- **标准格式**: 遵循标准代码生成评测格式
- **快速评估**: 适合快速评估代码生成能力
- **输入输出**: 输入为函数签名和问题描述（通常1-3个句子），输出为完整函数实现（通常5-30行代码）

### 适用场景

- 代码生成能力快速评估
- 资源有限的评测场景
- 初步能力测试

### 适用模型

- **所有规模模型**: 适合所有规模的模型
- **小模型（<1B）**: 推荐使用，快速评估基础代码能力
- **大模型（>10B）**: 可以使用，但可能过于简单

---

## 🔗 资源链接

- **GitHub**: 待补充
- **数据集**: 待补充
- **论文**: 待补充

---

## 📖 使用指南

### 1. 数据准备

```python
# 待补充具体的数据加载方法
from datasets import load_dataset

# dataset = load_dataset("code_generation_lite")
```

### 2. 运行评测

#### 使用OpenCompass

```python
from opencompass import OpenCompass

config = {
    'dataset': 'code_generation_lite',
    'model': 'your_model',
    'temperature': 0
}

result = OpenCompass.run(config)
```

#### 使用lm-evaluation-harness

```bash
lm_eval --model hf \
    --model_args pretrained=your_model \
    --tasks code_generation_lite \
    --batch_size 1
```

### 3. 结果分析

- **Pass@k**: 计算Pass@1、Pass@10等指标
- **代码质量**: 分析生成的代码质量
- **错误分析**: 分析错误类型和原因

---

## ⚙️ 评测参数

- **Temperature**: 0（确定性输出）或 >0（多样性）
- **测试次数**: 通常测试1次（Temperature=0）或多次（Temperature>0）
- **Max Tokens**: 根据题目复杂度，通常200-500

---

## 💡 最佳实践

1. **快速评估**: 适合快速评估代码生成能力
2. **代码质量**: 不仅关注通过率，还关注代码质量
3. **完整评测**: 如需全面评估，建议使用完整版评测集（如HumanEval）

---

## 📊 评测指标

### Pass@k

- **Pass@1**: 生成1次，通过测试用例的比例
- **Pass@10**: 生成10次，至少1次通过的比例

### 计算方式

```python
from math import comb

def pass_at_k(n, c, k):
    """
    n: 总样本数
    c: 正确样本数
    k: 生成次数
    """
    if n - c < k:
        return 1.0
    return 1.0 - comb(n - c, k) / comb(n, k)
```

---

## 📝 输入输出示例

> **注意**: 以下示例基于Code Generation Lite数据集的典型格式，用于说明评测集的结构。真实题目请从Code Generation Lite数据集获取。

### 示例1: 简单函数

**输入（Input）**:
```python
def add_numbers(a: int, b: int) -> int:
    """Add two numbers and return the result.
    
    >>> add_numbers(2, 3)
    5
    >>> add_numbers(-1, 1)
    0
    """
```

**期望输出（Expected Output）**:
```python
def add_numbers(a: int, b: int) -> int:
    """Add two numbers and return the result.
    
    >>> add_numbers(2, 3)
    5
    >>> add_numbers(-1, 1)
    0
    """
    return a + b
```

### 示例2: 字符串处理

**输入（Input）**:
```python
def reverse_string(s: str) -> str:
    """Reverse a string.
    
    >>> reverse_string("hello")
    'olleh'
    >>> reverse_string("")
    ''
    """
```

**期望输出（Expected Output）**:
```python
def reverse_string(s: str) -> str:
    """Reverse a string.
    
    >>> reverse_string("hello")
    'olleh'
    >>> reverse_string("")
    ''
    """
    return s[::-1]
```

### 示例3: 列表操作

**输入（Input）**:
```python
def find_max(numbers: list) -> int:
    """Find the maximum number in a list.
    
    >>> find_max([1, 5, 3, 9, 2])
    9
    >>> find_max([-1, -5, -3])
    -1
    """
```

**期望输出（Expected Output）**:
```python
def find_max(numbers: list) -> int:
    """Find the maximum number in a list.
    
    >>> find_max([1, 5, 3, 9, 2])
    9
    >>> find_max([-1, -5, -3])
    -1
    """
    if not numbers:
        raise ValueError("List cannot be empty")
    return max(numbers)
```

---

## 📊 参考结果

| 模型 | Pass@1 | Pass@10 | 备注 |
|------|--------|---------|------|
| GPT-4 | 待定 | 待定 | 参考值 |
| GPT-3.5 | 待定 | 待定 | 参考值 |

*注：以上为参考值，实际结果可能因评测环境而异*

---

## 📚 相关资源

- [HumanEval](humaneval.md) - 完整版代码生成评测集
- [Intelligence维度指南](../../../intelligence/README.md)
- [代码生成评测集](README.md)

---

**最后更新**: 2025-01-XX

