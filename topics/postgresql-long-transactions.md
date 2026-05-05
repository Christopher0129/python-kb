# PostgreSQL 长事务专题

这个专题关注长事务对锁、VACUUM、复制延迟和连接池稳定性的连锁影响。

## 适用场景

- 连接长期处于 `idle in transaction`
- VACUUM 追不上，表膨胀持续增长
- 副本延迟、锁等待和连接耗尽同时出现

## 常见主题

- `idle in transaction`
- 事务范围过大
- 应用层批量处理
- 游标与分页读取
- 自动提交策略

## 设计要点

- 长事务常常来自应用层流程过长，而不是数据库本身性能不足。
- 事务内不要混入外部网络调用、复杂计算和长时间循环处理。
- 线上治理要同时设置超时、暴露指标并保留会话级诊断信息。
- 长事务问题如果不收敛，会同时污染锁、膨胀、复制和备份链路。

## 关联阅读

- [事务与隔离级别专题](./transaction-isolation.md)
- [PostgreSQL VACUUM 与膨胀专题](./postgresql-vacuum-bloat.md)
- [PostgreSQL 复制延迟专题](./postgresql-replication-lag.md)
- [PostgreSQL 死锁排障专题](./postgresql-deadlock-troubleshooting.md)
- [PostgreSQL 连接耗尽专题](./postgresql-connection-exhaustion.md)

返回 [索引](../README.md)
