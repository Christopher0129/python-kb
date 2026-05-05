# 指标基数治理专题

这个专题关注指标标签如何设计、哪些标签不能打，以及如何避免监控系统被高基数拖垮。

## 适用场景

- Prometheus 指标数量快速膨胀
- 新增指标后抓取、查询或存储成本明显上升
- 团队喜欢把用户 ID、请求 ID 直接打成 label

## 常见主题

- label 设计边界
- histogram bucket 规划
- 高基数字段识别
- recording rule
- 监控成本治理

## 设计要点

- 指标适合承载聚合趋势，不适合承载每个请求或每个用户的唯一标识。
- 高基数问题常常不是某个指标单独过大，而是多个 label 组合相乘。
- 指标命名、标签字典和 bucket 方案要在团队层面统一，而不是由每个服务自由发挥。
- 当观测成本变成真实问题时，要先减标签和归并维度，再考虑扩容。

## 关联阅读

- [可观测性专题](./observability.md)
- [遥测与链路追踪专题](./telemetry-tracing.md)
- [观测埋点专题](./observability-instrumentation.md)
- [成本治理专题](./cost-governance.md)
- [容量规划专题](./capacity-planning.md)

返回 [索引](../README.md)
