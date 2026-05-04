# 可观测性专题

这个专题关注系统如何被观察：日志、错误、健康状态和关键指标。

## 核心能力

| 主题 | 说明 |
| --- | --- |
| 日志 | 发生了什么 |
| 错误堆栈 | 为什么失败 |
| 健康检查 | 服务是否还活着 |
| 指标 | 是否变慢、变多、变少 |

## 应用层建议

- 给关键请求和任务打日志
- 重要错误记录完整上下文
- 暴露健康检查端点
- 给关键任务加耗时观测

## 关联阅读

- [logging](../stdlib/logging.md)
- [traceback](../stdlib/traceback.md)
- [性能与调试专题](./performance-debugging.md)
- [部署与运维专题](./deployment-operations.md)

返回 [索引](../README.md)
