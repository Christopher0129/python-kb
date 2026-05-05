# Redis 分布式锁专题

这个专题关注 Redis 锁什么时候能用、什么时候不该用，以及如何避免把锁当成一致性银弹。

## 适用场景

- 定时任务抢占执行
- 并发提交的轻量互斥
- 需要限制同一资源同一时刻只有一个执行者

## 常见主题

- `SET NX EX`
- 锁续期与过期
- fencing token
- 锁丢失与误删
- 幂等与补偿

## 设计要点

- Redis 锁只能降低并发冲突概率，不能替代业务幂等、版本检查和状态机约束。
- 锁值必须带唯一标识，释放时要校验“是不是自己加的锁”。
- 长任务比短任务更容易遇到锁续期、脑裂和误判完成问题。
- 如果资源冲突可在数据库或业务状态层解决，优先不要把复杂一致性押在缓存锁上。

## 关联阅读

- [Redis 高级专题](./redis-advanced.md)
- [幂等与重试专题](./idempotency-retries.md)
- [PostgreSQL Advisory Lock 专题](./postgresql-advisory-locks.md)
- [任务调度专题](./task-scheduling.md)
- [Worker 运行治理专题](./worker-runtime-operations.md)

返回 [索引](../README.md)
