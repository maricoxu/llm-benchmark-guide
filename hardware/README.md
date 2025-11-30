# Hardware（硬件）维度

> 评估硬件平台的性能表现

## 📋 概述

Hardware维度关注硬件平台的性能，包括：

- 🖥️ **GPU性能**: NVIDIA、AMD等GPU性能
- ⚡ **TPU性能**: Google TPU性能
- 🔋 **能效比**: 性能与功耗的比值
- 💰 **成本效益**: 硬件成本与性能的平衡

---

## 📊 评测指标

### 性能指标

- **吞吐量**: Tokens/秒、请求/秒
- **延迟**: 首Token延迟、端到端延迟
- **功耗**: 峰值功耗、平均功耗

### 能效指标

- **性能/功耗比**: 单位功耗的性能
- **性能/价格比**: 单位价格的性能

---

## 🛠️ 评测方法

### GPU性能评测

```python
import torch

def benchmark_gpu(model, inputs):
    # 预热
    model(inputs[0])
    
    # 评测
    start = torch.cuda.Event(enable_timing=True)
    end = torch.cuda.Event(enable_timing=True)
    
    start.record()
    outputs = model(inputs)
    end.record()
    
    torch.cuda.synchronize()
    latency = start.elapsed_time(end) / len(inputs)
    
    return latency
```

---

## 💡 硬件选型指南

### 推理场景

- **实时推理**: 低延迟GPU（如A100）
- **批量推理**: 高吞吐量GPU（如H100）
- **边缘推理**: 边缘计算芯片

### 训练场景

- **大规模训练**: 多GPU/TPU集群
- **微调**: 单GPU或少量GPU
- **分布式训练**: 多节点GPU集群

---

## 📚 相关资源

- [评测工具](../tools/README.md)
- [使用指南](../guides/README.md)

---

**最后更新**: 2025-11-30

