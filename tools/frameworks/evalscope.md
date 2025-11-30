# EvalScope

> ModelScope开源的模型评测与性能基准测试框架

## 📋 基本信息

- **GitHub**: https://github.com/modelscope/evalscope
- **文档**: https://evalscope.readthedocs.io/
- **开发者**: ModelScope（阿里云）
- **许可证**: Apache 2.0

## 📖 框架介绍

EvalScope是一个开源的模型评测与性能基准测试框架，专为多样化的模型评估需求设计。

### 核心特点

- **多模型类型支持**: LLM、多模态、Embedding、Reranker、CLIP等
- **多评测场景**: 端到端RAG评测、竞技场模式、模型推理性能压测等
- **可视化功能**: 支持结果分析和对比
- **灵活配置**: 支持数据集混合评测

## 🛠️ 安装和使用

### 安装

```bash
pip install evalscope
```

### 基本使用

```python
from evalscope import EvalScope

eval_scope = EvalScope()
result = eval_scope.evaluate(
    model='your_model',
    dataset='mmlu',
    task='multiple_choice'
)
```

## 💡 使用场景

### 开源数据集评测

对于开源数据集，一般使用QA release的镜像（安装evalscope）进行测试。

### 精度评测

精度评测通常使用evalscope和OpenCompass一起使用。

## 📚 相关资源

- [EvalScope GitHub](https://github.com/modelscope/evalscope)
- [EvalScope文档](https://evalscope.readthedocs.io/)

---

**最后更新**: 2025-11-30

