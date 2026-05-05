# 缓存与队列专题

这个专题关注 Python 系统里的缓存、异步任务和消息缓冲。

## 常见工具

| 工具 | 作用 |
| --- | --- |
| `redis` | 缓存、计数器、轻量队列 |
| `celery` | 后台任务与定时任务 |
| `queue` | 单进程内线程安全队列 |

## 适用场景

- 热点数据缓存
- 异步发送邮件
- 大任务拆到后台执行

## 关联阅读

- [redis-py](../third_party/redis.md)
- [celery](../third_party/celery.md)
- [Dramatiq](../third_party/dramatiq.md)
- [arq](../third_party/arq.md)
- [queue](../stdlib/queue.md)
- [异步编程专题](./async-programming.md)
- [Redis 高级专题](./redis-advanced.md)
- [Redis Streams 消费专题](./redis-streams-consumers.md)
- [Redis 分布式锁专题](./redis-distributed-locks.md)
- [Redis 缓存失效策略专题](./redis-cache-invalidation.md)
- [任务队列架构专题](./task-queue-architectures.md)
- [缓存稳定性专题](./cache-stability-patterns.md)

返回 [索引](../README.md)
