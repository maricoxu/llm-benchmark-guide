# 代码生成评测集

> 评估模型的代码生成能力

## 📋 评测集列表

| 评测集 | 测试条目 | 输入长度 | 输出长度 | 文档 |
|--------|---------|---------|---------|------|
| [HumanEval](humaneval.md) | 164 | 2-3句 | 5-50行 | [查看](humaneval.md) |
| [LiveCodeBench](livecodebench.md) | v5-167, v6-175 | 代码+描述 | 10-100行 | [查看](livecodebench.md) |
| [MBPP](mbpp.md) | 974 | 1-2段 | 5-30行 | [查看](mbpp.md) |
| [Code Generation Lite](code-generation-lite.md) | 待定 | 1-3句 | 5-30行 | [查看](code-generation-lite.md) |
| [SciCode](scicode.md) | 待定 | 科学计算问题 | 科学计算代码 | [查看](scicode.md) |

---

## 🎯 评测集特点

### 实际代码任务
- **LiveCodeBench**: 真实代码任务，支持32K/64K长上下文
- **SciCode**: 科学计算代码生成

### 标准代码评测
- **HumanEval**: Python编程能力基准
- **MBPP**: 入门级Python编程，大规模评测

---

## 📊 使用建议

### 代码能力基准测试
推荐使用 **HumanEval**，业界标准基准。

### 实际代码能力评估
推荐使用 **LiveCodeBench**，更贴近实际应用。

### 大规模代码能力评估
推荐使用 **MBPP**，包含974题。

---

## 🔗 相关资源

- [Intelligence维度指南](../../intelligence/README.md)
- [评测工具](../../tools/README.md)

---

**最后更新**: 2025-11-30

