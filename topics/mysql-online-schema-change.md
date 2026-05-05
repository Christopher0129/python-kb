# MySQL 在线改表专题

这个专题关注 MySQL 大表结构变更如何控制元数据锁、切换风险和回滚复杂度。

## 适用场景

- 大表新增列、索引或调整字段类型
- 迁移窗口短，不能接受长时间不可写
- DDL 执行后经常把业务线程全部堵住

## 常见主题

- MySQL Online DDL
- metadata lock
- 影子表复制与切换
- 回填、双写与兼容期
- `gh-ost` / `pt-online-schema-change`

## 设计要点

- 在线改表的关键不是工具名字，而是把 schema 变更拆成可观测的多个阶段。
- 元数据锁时间很短也可能造成明显雪崩，必须提前识别长事务和大查询。
- 改表前要明确回退点，特别是数据回填和应用代码兼容窗口。
- 对高风险字段变更，优先选择先加后切、逐步迁移而不是一步替换。

## 关联阅读

- [MySQL 开发专题](./mysql-development.md)
- [Schema 迁移与回填专题](./schema-migrations-backfill.md)
- [MySQL 锁冲突与争用专题](./mysql-locking-contention.md)
- [数据库开发专题](./database-development.md)
- [部署与运维专题](./deployment-operations.md)

返回 [索引](../README.md)
