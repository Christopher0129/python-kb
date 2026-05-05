# 日志关联与结构化日志专题

这个专题关注日志如何在服务、任务、消息和异步链路之间保持可关联，而不是只把字符串打印得更整齐。

## 适用场景

- 日志很多，但无法串起同一个请求的全过程
- 多服务联调时看不到上下游对应关系
- 敏感字段混杂在日志里，难以治理

## 常见主题

- request id / trace id
- structured logging
- 统一字段命名
- 日志脱敏
- 日志等级与采样

## 设计要点

- 结构化日志的价值在于字段稳定可筛选，而不是仅仅输出 JSON。
- request id、tenant id、user id、task id 等字段要先定义哪些能进日志、哪些必须脱敏。
- 错误日志要能关联到 span、指标和告警，不要各自成为孤岛。
- 高流量路径要考虑采样和字段瘦身，否则日志系统会先成为瓶颈。

## 关联阅读

- [可观测性专题](./observability.md)
- [遥测与链路追踪专题](./telemetry-tracing.md)
- [观测埋点专题](./observability-instrumentation.md)
- [审计日志专题](./audit-logging.md)
- [安全基础专题](./security-basics.md)

返回 [索引](../README.md)
