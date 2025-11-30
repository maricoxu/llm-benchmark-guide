# HumanEval

> Python编程能力评测集，业界标准基准

## 📋 基本信息

| 项目 | 内容 |
|------|------|
| **分类** | Intelligence - 代码生成 |
| **测试条目数** | 164题 |
| **输入长度** | 函数签名和问题描述，通常2-3个句子 |
| **输出长度** | 完整函数实现，通常5-50行代码 |
| **评测时间** | 约1-2小时 |
| **覆盖场景** | Python代码生成能力评估 |

---

## 📖 评测集介绍

HumanEval是OpenAI开源的Python编程能力评测集，包含164个编程问题，每个问题包含函数签名、问题描述和测试用例。

### 特点

- **标准基准**: 业界广泛使用的代码生成基准
- **Python专注**: 专注于Python编程能力
- **测试驱动**: 每个问题都有测试用例验证

### 适用场景

- 代码生成能力基准测试
- Python编程能力评估
- 代码生成模型对比

---

## 🔗 资源链接

- **GitHub**: [HumanEval](https://github.com/openai/human-eval)
- **数据集**: [Hugging Face](https://huggingface.co/datasets/openai_humaneval)
- **论文**: [HumanEval论文](https://arxiv.org/abs/2107.03374)

---

## 📖 使用指南

### 1. 数据准备

```python
from datasets import load_dataset

dataset = load_dataset("openai_humaneval")
test_set = dataset["test"]  # 164题
```

### 2. 运行评测

#### 使用OpenCompass

```python
from opencompass import OpenCompass

config = {
    'dataset': 'humaneval_gen',
    'model': 'your_model',
    'temperature': 0
}

result = OpenCompass.run(config)
```

#### 使用lm-evaluation-harness

```bash
lm_eval --model hf \
    --model_args pretrained=your_model \
    --tasks humaneval \
    --batch_size 1
```

### 3. 结果分析

- **Pass@k**: 计算Pass@1、Pass@10、Pass@100
- **代码质量**: 分析生成的代码质量
- **错误分析**: 分析错误类型和原因

---

## ⚙️ 评测参数

- **Temperature**: 0（确定性输出）或 >0（多样性）
- **测试次数**: 通常测试1次（Temperature=0）或多次（Temperature>0）
- **Max Tokens**: 根据题目复杂度，通常200-1000

---

## 💡 最佳实践

1. **使用测试用例**: 使用提供的测试用例验证代码
2. **代码质量**: 不仅关注通过率，还关注代码质量
3. **错误分析**: 深入分析错误案例，找出模型弱点

---

## 📊 评测指标

### Pass@k

- **Pass@1**: 生成1次，通过测试用例的比例
- **Pass@10**: 生成10次，至少1次通过的比例
- **Pass@100**: 生成100次，至少1次通过的比例

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

### 示例1: 简单函数

**输入（Input）**:
```python
def has_close_elements(numbers: list, threshold: float) -> bool:
    """Check if in given list of numbers, are there any two numbers closer to each other than
    the given threshold.
    
    >>> has_close_elements([1.0, 2.0, 3.0], 0.5)
    False
    >>> has_close_elements([1.0, 2.8, 3.0, 4.0, 5.0, 2.0], 0.3)
    True
    """
```

**期望输出（Expected Output）**:
```python
def has_close_elements(numbers: list, threshold: float) -> bool:
    """Check if in given list of numbers, are there any two numbers closer to each other than
    the given threshold.
    
    >>> has_close_elements([1.0, 2.0, 3.0], 0.5)
    False
    >>> has_close_elements([1.0, 2.8, 3.0, 4.0, 5.0, 2.0], 0.3)
    True
    """
    for i in range(len(numbers)):
        for j in range(i + 1, len(numbers)):
            if abs(numbers[i] - numbers[j]) < threshold:
                return True
    return False
```

### 示例2: 字符串处理

**输入（Input）**:
```python
def separate_paren_groups(paren_string: str) -> list:
    """Input to this function is a string containing multiple groups of nested parentheses. Your goal is to
    separate those groups into separate strings and return the list of those.
    Separate groups are balanced (each open brace is properly closed). If a group is nested, it's all included.
    
    >>> separate_paren_groups('( ) (( )) (( )( ))')
    ['()', '(())', '(()())']
    """
```

**期望输出（Expected Output）**:
```python
def separate_paren_groups(paren_string: str) -> list:
    """Input to this function is a string containing multiple groups of nested parentheses. Your goal is to
    separate those groups into separate strings and return the list of those.
    Separate groups are balanced (each open brace is properly closed). If a group is nested, it's all included.
    
    >>> separate_paren_groups('( ) (( )) (( )( ))')
    ['()', '(())', '(()())']
    """
    result = []
    current = []
    depth = 0
    
    for char in paren_string:
        if char == '(':
            if depth == 0:
                current = []
            current.append(char)
            depth += 1
        elif char == ')':
            current.append(char)
            depth -= 1
            if depth == 0:
                result.append(''.join(current))
    
    return result
```

### 示例3: 算法实现

**输入（Input）**:
```python
def find_closest_elements(numbers: list) -> tuple:
    """From a supplied list of numbers (of length at least two) select and return two that are the closest to each
    other and return them in order (smaller number, larger number).
    
    >>> find_closest_elements([1.0, 2.0, 3.0, 4.0, 5.0, 2.2])
    (2.0, 2.2)
    >>> find_closest_elements([1.0, 2.0, 3.0, 4.0, 5.0, 2.0])
    (2.0, 2.0)
    """
```

**期望输出（Expected Output）**:
```python
def find_closest_elements(numbers: list) -> tuple:
    """From a supplied list of numbers (of length at least two) select and return two that are the closest to each
    other and return them in order (smaller number, larger number).
    
    >>> find_closest_elements([1.0, 2.0, 3.0, 4.0, 5.0, 2.2])
    (2.0, 2.2)
    >>> find_closest_elements([1.0, 2.0, 3.0, 4.0, 5.0, 2.0])
    (2.0, 2.0)
    """
    min_diff = float('inf')
    closest_pair = None
    
    for i in range(len(numbers)):
        for j in range(i + 1, len(numbers)):
            diff = abs(numbers[i] - numbers[j])
            if diff < min_diff:
                min_diff = diff
                closest_pair = (min(numbers[i], numbers[j]), max(numbers[i], numbers[j]))
    
    return closest_pair
```

---

## 📊 参考结果

| 模型 | Pass@1 | Pass@10 | Pass@100 | 备注 |
|------|--------|---------|----------|------|
| GPT-4 | ~67% | ~90% | ~97% | 参考值 |
| GPT-3.5 | ~48% | ~74% | ~88% | 参考值 |

*注：以上为参考值，实际结果可能因评测环境而异*

---

## 📚 相关资源

- [HumanEval GitHub](https://github.com/openai/human-eval)
- [Intelligence维度指南](../../../intelligence/README.md)

---

**最后更新**: 2025-11-30

