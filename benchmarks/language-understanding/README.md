# 语言理解评测集

> 评估模型的语言理解能力，包括通用语言理解和中文语言理解

## 📋 评测集列表

| 评测集 | 测试条目 | 输入长度 | 输出长度 | 文档 |
|--------|---------|---------|---------|------|
| [MMLU-Pro](mmlu-pro.md) | ~14,000 | 1-2句 | 选项 | [查看](mmlu-pro.md) |
| [C-Eval](c-eval.md) | 13,948 | 1-2句 | 选项 | [查看](c-eval.md) |
| [Xiezhi](xiezhi.md) | 249,587 | 题目描述 | 选项 | [查看](xiezhi.md) |
| [GPQA Diamond](gpqa-diamond.md) | 待定 | 1-2段 | 短答案 | [查看](gpqa-diamond.md) |
| [IFBench](ifbench.md) | 待定 | 交互任务 | 交互响应 | [查看](ifbench.md) |
| [CLUE](clue.md) | 因任务而异 | 几十-几百字符 | 标签/答案 | [查看](clue.md) |

---

## 🎯 评测集特点

### 通用语言理解
- **MMLU-Pro**: 多领域语言理解，16K上下文
- **GPQA Diamond**: 科学专业知识问答
- **AA-LCR**: 高级推理能力

### 中文语言理解
- **C-Eval**: 中文综合能力评估，52个学科
- **Xiezhi**: 领域知识评估，516个领域
- **CLUE**: 中文语言理解基准，多任务

---

## 📊 使用建议

### 通用能力评估
推荐使用 **MMLU-Pro** 或 **C-Eval**，覆盖多个领域和学科。

### 中文能力评估
推荐使用 **C-Eval** 或 **Xiezhi**，专门针对中文模型。

### 专业知识评估
推荐使用 **GPQA Diamond**，评估科学专业知识。

---

## 🔗 相关资源

- [Intelligence维度指南](../../intelligence/README.md)
- [评测工具](../../tools/README.md)

---

**最后更新**: 2025-11-30

