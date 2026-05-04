# PostgreSQL 分区维护专题

这个专题关注 PostgreSQL 分区表的建模、冷热数据分层和日常维护操作。

## 适用场景

- 日志、事件、流水等持续增长的大表
- 需要按时间或租户隔离数据生命周期
- 需要降低单表索引和清理成本

## 常见主题

- 范围分区与列表分区
- 分区裁剪
- 新分区预创建
- 历史分区归档与删除
- 分区索引与唯一约束

## 设计要点

- 分区键要和主要查询条件一致，否则只会增加复杂度。
- 分区数量过多会推高规划成本，不能无限细切。
- 分区维护要自动化，包括建分区、归档、删除和校验。
- 跨分区唯一性、外键和批量写入路径要在设计早期确认。

## 关联阅读

- [PostgreSQL 开发专题](./postgresql-development.md)
- [分片与分区专题](./sharding-partitioning.md)
- [索引设计专题](./index-design.md)
- [Schema 迁移与回填专题](./schema-migrations-backfill.md)
- [备份与归档专题](./backup-archiving.md)

返回 [索引](../README.md)
