# 特征库专题

这个专题关注训练和推理阶段如何共享同一套特征定义，减少特征口径漂移和重复实现。

## 常见价值

- 训练 / 服务特征一致
- 在线和离线读取路径清晰
- 特征复用，不再每个模型各写一套 SQL
- 方便回放某个时间点的训练数据

## 关键主题

| 主题 | 说明 |
| --- | --- |
| 离线特征 | 训练和批量评分所需特征 |
| 在线特征 | 在线推理低延迟读取 |
| point-in-time join | 避免未来数据泄漏 |
| feature service | 把一组特征作为模型契约 |

## 关联阅读

- [Feast](../third_party/feast.md)
- [数据管道专题](./data-pipelines.md)
- [实验跟踪专题](./experiment-tracking.md)
- [模型注册专题](./model-registry.md)
- [特征工程专题](./feature-engineering.md)
- [特征服务专题](./feature-serving.md)
- [在线离线一致性专题](./online-offline-consistency.md)

返回 [索引](../README.md)
