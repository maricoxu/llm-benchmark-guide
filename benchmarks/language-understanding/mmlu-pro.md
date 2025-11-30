# MMLU-Pro

> 多领域语言理解评测集，支持16K长上下文

## 📋 基本信息

| 项目 | 内容 |
|------|------|
| **分类** | Intelligence - 语言理解 |
| **测试条目数** | 待定（MMLU原版约14,000题，Pro版本数量待确认） |
| **输入长度** | 平均1-2个句子，支持长上下文（16K tokens） |
| **输出长度** | 单个选项或简短答案 |
| **评测时间** | 单次评测：约1-2小时（取决于模型推理速度） |
| **Max Tokens** | 16K |
| **覆盖场景** | 多领域语言理解能力评估 |

---

## 📖 评测集介绍

MMLU-Pro是MMLU（Massive Multitask Language Understanding）的扩展版本，支持16K长上下文，用于评估模型在多领域语言理解任务上的能力。

### 特点

- **多领域覆盖**: 涵盖多个学科和领域
- **长上下文支持**: 支持16K tokens的长上下文
- **标准评测**: 业界广泛使用的评测集

### 适用场景

- 通用能力评估
- 多领域知识理解评估
- 长上下文理解能力评估

---

## 🔗 资源链接

- **GitHub**: [MMLU原版](https://github.com/hendrycks/test)
- **MMLU-Pro**: 待定（GitHub链接待确认）
- **论文**: [MMLU论文](https://arxiv.org/abs/2009.03300)

---

## 📖 使用指南

### 1. 数据准备

```bash
# 下载MMLU数据集
git clone https://github.com/hendrycks/test.git
cd test
```

### 2. 运行评测

#### 使用OpenCompass

```python
# 配置MMLU-Pro评测
from opencompass import OpenCompass

config = {
    'dataset': 'mmlu_pro',
    'model': 'your_model',
    'max_tokens': 16384,
    'temperature': 0
}

result = OpenCompass.run(config)
```

#### 使用lm-evaluation-harness

```bash
lm_eval --model hf \
    --model_args pretrained=your_model \
    --tasks mmlu \
    --batch_size 1
```

### 3. 结果分析

- **准确率**: 计算整体准确率
- **领域分析**: 分析不同领域的表现
- **错误分析**: 分析错误案例

---

## ⚙️ 评测参数

- **Temperature**: 0（确定性输出）
- **测试次数**: 通常测试1次
- **Max Tokens**: 16K
- **覆盖模型**: qwen3-235B-A22B-Thinking-2507/instruct, DeepSeek-R1-0528-bf16等

---

## 💡 最佳实践

1. **使用固定参数**: Temperature=0，确保结果可复现
2. **多次评测**: 如需要，可以多次评测取平均
3. **领域分析**: 分析模型在不同领域的表现
4. **对比分析**: 与基准模型对比，了解模型水平

---

## ❓ 常见问题

### Q: MMLU和MMLU-Pro有什么区别？

A: MMLU-Pro支持16K长上下文，而MMLU原版支持较短的上下文。MMLU-Pro更适合评估长上下文理解能力。

### Q: 如何选择合适的Max Tokens？

A: 根据评测集要求，MMLU-Pro建议使用16K tokens。如果模型不支持16K，可以适当降低。

### Q: 评测时间过长怎么办？

A: 可以采样部分题目进行快速评测，或者使用更快的硬件。

---

## 📊 参考结果

| 模型 | 准确率 | 备注 |
|------|--------|------|
| GPT-4 | ~86% | 参考值 |
| Claude-3 | ~85% | 参考值 |

*注：以上为参考值，实际结果可能因评测环境而异*

---

## 📚 相关资源

- [MMLU原版GitHub](https://github.com/hendrycks/test)
- [OpenCompass文档](https://opencompass.readthedocs.io/)
- [Intelligence维度指南](../../../intelligence/README.md)

---

**最后更新**: 2025-11-30

