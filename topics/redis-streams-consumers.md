# Redis Streams 消费专题

这个专题关注 Redis Streams 在轻量消息流、消费组和积压治理中的使用边界。

## 适用场景

- 需要比 list / pubsub 更可控的轻量消息流
- 希望按消费组分摊任务
- 需要查看 pending、重试和堆积情况

## 常见主题

- `XADD`
- `XGROUP`
- `XREADGROUP`
- pending list
- 重试、认领与死信

## 设计要点

- Streams 适合中轻量任务流，但不应在高保留、高吞吐场景里替代成熟日志系统。
- 消费成功确认只是开始，真正难点是积压、超时、重复处理和回补机制。
- 事件体设计要尽量自描述，并保留幂等键和诊断字段。
- 生产侧、消费侧和运维侧都要能看到 lag、pending 和失败分布。

## 关联阅读

- [Redis 高级专题](./redis-advanced.md)
- [消息系统专题](./message-systems.md)
- [缓存与队列专题](./cache-queues.md)
- [任务队列架构专题](./task-queue-architectures.md)
- [消费者组运维专题](./consumer-group-operations.md)

返回 [索引](../README.md)
