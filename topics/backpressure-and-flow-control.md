# 背压与流控专题

这个专题关注当上游生产速度大于下游处理速度时，系统如何限制堆积、传播压力并自我保护。

## 适用场景

- 消息消费和异步任务系统
- SSE / WebSocket 推送
- 批量导入、抓取和流式处理

## 常见主题

- 有界队列
- 并发上限
- rate limit 与窗口控制
- 消费速度与批大小
- 下游超时、重试与丢弃策略

## 设计要点

- 没有上限的队列通常只是把问题延后并放大
- 限流、连接池和 worker 数量应统一设计
- 观测上要关注队列长度、积压时间和拒绝率
- 背压策略要与业务容忍度匹配，例如阻塞、丢弃、降级或转离线

## 关联阅读

- [asyncio](../stdlib/asyncio.md)
- [AnyIO](../third_party/anyio.md)
- [缓存与队列专题](./cache-queues.md)
- [任务队列架构专题](./task-queue-architectures.md)
- [流处理专题](./stream-processing.md)

返回 [索引](../README.md)
