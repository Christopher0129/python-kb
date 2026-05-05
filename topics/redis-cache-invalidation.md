# Redis 缓存失效策略专题

这个专题关注缓存如何失效、如何回收，以及如何控制脏读和回源风暴。

## 适用场景

- 业务大量依赖 Redis 缓存加速读取
- 数据更新后经常出现缓存脏读
- 热点 key 过期时容易把下游数据库打穿

## 常见主题

- cache-aside
- write-through / write-behind
- 版本号与逻辑过期
- 批量失效
- 事件驱动失效

## 设计要点

- 缓存问题常常不是“有没有缓存”，而是失效边界、回源保护和一致性窗口设计不清。
- 热点 key 需要预热、抖动过期和单飞保护，避免雪崩与击穿。
- 缓存值应尽量带版本、时间戳或来源信息，方便诊断脏数据。
- 缓存一致性和系统吞吐是权衡关系，必须先明确可接受的旧数据窗口。

## 关联阅读

- [Redis 高级专题](./redis-advanced.md)
- [缓存与队列专题](./cache-queues.md)
- [缓存稳定性专题](./cache-stability-patterns.md)
- [在线离线一致性专题](./online-offline-consistency.md)
- [配置灰度与回滚专题](./config-rollout-strategies.md)

返回 [索引](../README.md)
