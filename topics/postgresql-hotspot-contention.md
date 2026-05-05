# PostgreSQL 热点争用专题

这个专题关注高并发下少数热点行、热点键或热点索引页被频繁竞争时的定位与缓解方法。

## 适用场景

- 某些接口在高峰期 RT 抖动明显
- 单个计数器、库存行或租户记录成为热点
- 锁等待、更新冲突或 WAL 压力集中在少数对象上

## 常见主题

- 热点行
- 乐观并发
- 分桶拆分
- 批量聚合
- 争用指标

## 设计要点

- 热点问题往往不是数据库“不够快”，而是数据模型把所有写流量压到少数键上。
- 先区分行锁竞争、索引页竞争和连接池拥塞，再决定优化方向。
- 降低争用常见手法是拆热点、缩短事务、异步聚合和减少同步写次数。
- 优化后要验证是否只是把热点从数据库挪到了缓存或队列。

## 关联阅读

- [PostgreSQL 锁与并发专题](./postgresql-locking.md)
- [PostgreSQL 幂等写入专题](./postgresql-idempotent-writes.md)
- [连接池专题](./connection-pooling.md)
- [PostgreSQL 统计与观测专题](./postgresql-stats-observability.md)
- [容量规划专题](./capacity-planning.md)

返回 [索引](../README.md)
