# SciCode

> 科学计算代码生成评测集

## 📋 基本信息

| 项目 | 内容 |
|------|------|
| **分类** | Intelligence - 代码生成（科学计算） |
| **测试条目数** | 待定 |
| **输入长度** | 科学计算问题描述 |
| **输出长度** | 科学计算代码实现 |
| **评测时间** | 待定 |
| **覆盖场景** | 科学计算代码生成能力评估 |

---

## 📖 评测集介绍

SciCode是用于评估模型在科学计算代码生成任务上能力的评测集。

### 特点

- **科学计算**: 专注于科学计算代码
- **专业性**: 需要科学计算知识
- **实用性强**: 贴近实际科学计算任务

### 适用场景

- 科学计算代码生成能力评估
- 科学计算模型评估

---

## 🔗 资源链接

- **GitHub**: 待定
- **论文**: 待定
- **数据集**: 待定

---

## ⚙️ 评测参数

- **Temperature**: 待定
- **测试次数**: 待定
- **覆盖模型**: qwen3-235B-A22B-Thinking-2507等

---

## 📝 输入输出示例

### 示例1: 数值计算

**输入（Input）**:
```python
# 问题: 计算矩阵的特征值和特征向量
# 使用numpy实现

请完成函数。
```

**期望输出（Expected Output）**:
```python
import numpy as np

def compute_eigen(matrix):
    eigenvalues, eigenvectors = np.linalg.eig(matrix)
    return eigenvalues, eigenvectors
```

---

## 📚 相关资源

- [Intelligence维度指南](../../../intelligence/README.md)

---

**最后更新**: 2025-11-30

