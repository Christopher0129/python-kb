# PostgreSQL 锁与并发专题

这个专题关注 PostgreSQL 在高并发下的锁等待、死锁和并发更新问题。

## 适用场景

- 多 worker 同时更新同一批记录
- 事务偶发超时或死锁
- 上线后出现锁等待堆积

## 常见主题

- 行锁与表锁
- `FOR UPDATE`
- 死锁
- 长事务
- 等待链分析

## 设计要点

- 锁冲突问题通常是查询顺序、事务范围和访问模式共同导致
- 同一业务对象的更新顺序应尽量固定
- 死锁重试要和幂等设计一起考虑
- 线上排查要结合慢 SQL、事务时长和会话等待状态

## 关联阅读

- [PostgreSQL 开发专题](./postgresql-development.md)
- [PostgreSQL 死锁排障专题](./postgresql-deadlock-troubleshooting.md)
- [PostgreSQL 长事务专题](./postgresql-long-transactions.md)
- [事务与隔离级别专题](./transaction-isolation.md)
- [查询计划分析专题](./query-plan-analysis.md)
- [连接池专题](./connection-pooling.md)

返回 [索引](../README.md)
