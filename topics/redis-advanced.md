# Redis 高级专题

这个专题关注超出“简单缓存”的 Redis 用法，包括流、位图、HyperLogLog、Lua 和文档模型。

## 适用场景

- 轻量事件流和消费组处理
- 高并发计数、去重、限流和排行榜
- 需要 Redis JSON / Search 文档模型的应用

## 常见主题

- Redis Streams
- 发布订阅
- Bitmap / HyperLogLog
- 分布式锁
- Redis Search / JSON 生态

## 设计要点

- 先区分缓存、队列、流和主存储，不要混成一个职责
- TTL、淘汰策略和持久化方式会直接影响数据可靠性
- 分布式锁不是银弹，重点是业务幂等和超时恢复
- Redis Search / JSON 适合中轻量文档模型，但不应替代所有数据库

## 关联阅读

- [redis-py](../third_party/redis.md)
- [Redis OM](../third_party/redis_om.md)
- [缓存与队列专题](./cache-queues.md)
- [消息系统专题](./message-systems.md)
- [任务队列架构专题](./task-queue-architectures.md)
- [Redis Streams 消费专题](./redis-streams-consumers.md)
- [Redis 分布式锁专题](./redis-distributed-locks.md)
- [Redis 缓存失效策略专题](./redis-cache-invalidation.md)

返回 [索引](../README.md)
