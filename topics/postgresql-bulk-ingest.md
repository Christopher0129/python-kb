# PostgreSQL 批量导入专题

这个专题关注 Python 服务或离线任务向 PostgreSQL 高效、安全地批量写入数据时的策略取舍。

## 适用场景

- 需要导入大批量日志、事件或业务记录
- 定时回填和数据迁移写入量大
- 单条插入过慢，事务和 WAL 压力明显

## 常见主题

- `COPY`
- 批量 insert
- 分批提交
- 去重与冲突处理
- 导入窗口控制

## 设计要点

- 批量导入追求吞吐，但不能忽略幂等、约束冲突和回滚成本。
- 导入作业要控制批次大小、提交频率和与在线业务的资源隔离。
- 导入链路最好暴露跳过条数、冲突条数、吞吐和失败原因分布。
- 回填或重放任务应先验证唯一键、索引和分区策略是否适配。

## 关联阅读

- [PostgreSQL 开发专题](./postgresql-development.md)
- [Schema 迁移与回填专题](./schema-migrations-backfill.md)
- [PostgreSQL WAL 与 Checkpoint 专题](./postgresql-wal-checkpoint.md)
- [连接池专题](./connection-pooling.md)
- [数据管道专题](./data-pipelines.md)

返回 [索引](../README.md)
