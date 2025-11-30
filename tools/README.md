# 评测工具

> 评测框架和工具集合

## 📋 工具列表

### 评测框架

- [OpenCompass](frameworks/opencompass.md) - 开源的大模型评测工具
- [lm-evaluation-harness](frameworks/lm-evaluation-harness.md) - EleutherAI评测框架
- [EvalScope](frameworks/evalscope.md) - ModelScope评测框架（支持多种模型类型）
- [HELM](frameworks/helm.md) - 斯坦福全面评测框架

### 工具集

- [GPTScore](utilities/gptscore.md) - 文本生成质量评估
- [CodeBLEU](utilities/codebleu.md) - 代码生成评估

---

## 🛠️ 快速开始

### 使用OpenCompass

```bash
# 安装
pip install opencompass

# 运行评测
python run.py --models your_model --datasets mmlu
```

### 使用lm-evaluation-harness

```bash
# 安装
pip install lm-eval

# 运行评测
lm_eval --model hf --model_args pretrained=your_model --tasks mmlu
```

---

## 📚 相关资源

- [使用指南](../guides/README.md)
- [资源集合](../resources/README.md)

---

**最后更新**: 2025-11-30

