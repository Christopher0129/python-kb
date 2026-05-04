# Evidently

`Evidently` 适合做数据漂移、数据质量和模型效果评估，常用于 ML/AI 系统上线前后监控。

## 安装

```bash
pip install evidently
```

## 基本示例

```python
from evidently import Report
from evidently.presets import DataDriftPreset


report = Report([DataDriftPreset()])
result = report.run(current_data, reference_data)
```

## 常见能力

| 能力 | 说明 |
| --- | --- |
| `Report([...])` | 构建一次评估报告 |
| `DataDriftPreset()` | 运行数据漂移评估 |
| `ClassificationPreset()` | 运行分类质量评估 |
| `RegressionPreset()` | 运行回归质量评估 |

## 使用建议

- 参考集和当前集的口径必须稳定，否则结果会误导判断
- 线上告警不要只盯单一漂移指标，要和业务指标、模型指标一起看
- 很适合与实验跟踪、发布策略和 incident 流程联动

## 关联阅读

- [模型评估专题](../topics/ml-evaluation.md)
- [实验跟踪专题](../topics/experiment-tracking.md)
- [模型服务专题](../topics/model-serving.md)
- [在线离线一致性专题](../topics/online-offline-consistency.md)

返回 [索引](../README.md)
