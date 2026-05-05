# PostgreSQL 死锁排障专题

这个专题关注 PostgreSQL 在并发更新、批处理和跨表事务中出现死锁时的定位与缓解策略。

## 适用场景

- 线上偶发 `deadlock detected`
- 同一批接口在高并发下成功率波动明显
- 事务逻辑复杂，涉及多表更新和补偿操作

## 常见主题

- 锁获取顺序
- 死锁图分析
- 重试策略
- 幂等保障
- 热点行竞争

## 设计要点

- 死锁不是单个 SQL 的问题，通常是多事务交错顺序不一致导致。
- 业务层重试必须和幂等设计一起考虑，否则可能把错误放大成重复写入。
- 高并发热点写入要优先减少事务内工作量和锁持有时间。
- 排障时要同时保留 SQL、事务边界、调用链和重试记录。

## 关联阅读

- [PostgreSQL 锁与并发专题](./postgresql-locking.md)
- [事务与隔离级别专题](./transaction-isolation.md)
- [PostgreSQL 统计与观测专题](./postgresql-stats-observability.md)
- [幂等与重试专题](./idempotency-retries.md)
- [PostgreSQL 长事务专题](./postgresql-long-transactions.md)

返回 [索引](../README.md)
