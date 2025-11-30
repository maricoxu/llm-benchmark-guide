# Terminal Bench Hard

> 终端环境问题解决评测集

## 📋 基本信息

| 项目 | 内容 |
|------|------|
| **分类** | Intelligence - 综合能力（系统级） |
| **测试条目数** | 待定 |
| **输入长度** | 终端任务描述，通常包含系统环境信息 |
| **输出长度** | 终端命令序列或解决方案 |
| **评测时间** | 待定 |
| **覆盖场景** | 终端环境问题解决能力评估 |

---

## 📖 评测集介绍

Terminal Bench Hard是Terminal Bench的hard子集，评估模型在终端环境中解决现实世界问题的能力，比如编译代码、配置服务器、玩游戏、训模型、调试系统等任务。

### 特点

- **系统级任务**: 评估系统级问题解决能力
- **实际场景**: 贴近实际应用场景
- **多样化任务**: 涵盖多种终端任务

### 适用场景

- 系统级问题解决能力评估
- 终端环境应用能力评估
- 实际应用能力评估

---

## 🔗 资源链接

- **GitHub**: 待定
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
    'dataset': 'terminal_bench_hard',
    'model': 'your_model',
    'temperature': 0
}

result = OpenCompass.run(config)
```

### 3. 结果分析

- **任务完成率**: 计算任务完成的比例
- **命令正确性**: 分析生成的命令是否正确
- **错误分析**: 分析错误类型和原因

---

## ⚙️ 评测参数

- **Temperature**: 待定
- **测试次数**: 待定
- **覆盖模型**: qwen3-235B-A22B-Thinking-2507, DeepSeek-R1-0528-bf16等

---

## 📝 输入输出示例

### 示例1: 编译代码

**输入（Input）**:
```
任务: 在Linux终端中，如何编译一个C++文件 main.cpp？

请给出完整的命令序列。
```

**期望输出（Expected Output）**:
```
使用g++编译器编译：
g++ -o main main.cpp

如果需要指定C++标准：
g++ -std=c++17 -o main main.cpp

如果需要调试信息：
g++ -g -o main main.cpp
```

### 示例2: 配置服务器

**输入（Input）**:
```
任务: 如何在Linux服务器上安装和配置Nginx？

请给出步骤和命令。
```

**期望输出（Expected Output）**:
```
1. 安装Nginx：
   sudo apt-get update
   sudo apt-get install nginx

2. 启动Nginx：
   sudo systemctl start nginx

3. 设置开机自启：
   sudo systemctl enable nginx

4. 检查状态：
   sudo systemctl status nginx
```

---

## 💡 最佳实践

1. **系统知识**: 确保模型具备足够的系统知识
2. **命令验证**: 验证生成的命令是否正确
3. **安全性**: 注意命令的安全性

---

## 📊 参考结果

| 模型 | 完成率 | 备注 |
|------|--------|------|
| 待定 | 待定 | 参考值 |

*注：以上为参考值，实际结果可能因评测环境而异*

---

## 📚 相关资源

- [Intelligence维度指南](../../../intelligence/README.md)

---

**最后更新**: 2025-11-30

