# PostgreSQL 复制与故障切换专题

这个专题关注 PostgreSQL 主从复制、只读副本、故障切换和应用侧连接策略。

## 适用场景

- 业务库需要读写分离
- 需要为主库故障准备切换预案
- 需要控制复制延迟对查询结果的一致性影响

## 常见主题

- 物理复制与流复制
- 同步复制与异步复制
- 复制槽与 WAL 保留
- 只读副本查询路由
- 故障检测与主备切换

## 设计要点

- 复制方案先决定恢复目标，再决定同步级别，不能只看吞吐。
- 读写分离必须承认复制延迟存在，并为读己写场景准备兜底路径。
- 应用连接串、连接池和服务发现要支持主从角色切换。
- 备库不是天然的报表库，还要评估长查询、VACUUM 和回放延迟的冲突。

## 关联阅读

- [PostgreSQL 开发专题](./postgresql-development.md)
- [PostgreSQL 锁与并发专题](./postgresql-locking.md)
- [PostgreSQL VACUUM 与膨胀专题](./postgresql-vacuum-bloat.md)
- [连接池专题](./connection-pooling.md)
- [运行时配置专题](./runtime-configuration.md)

返回 [索引](../README.md)
