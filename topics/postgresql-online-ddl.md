# PostgreSQL 在线 DDL 专题

这个专题关注大表结构变更如何尽量减少锁表、阻塞和回滚风险，让迁移可以在生产环境安全执行。

## 适用场景

- 大表新增索引、列或约束
- 迁移窗口很短，不能长时间锁业务写入
- 线上经常因为 DDL 把接口卡死

## 常见主题

- `CREATE INDEX CONCURRENTLY`
- 分阶段迁移
- 约束延迟校验
- 回填与切换
- 迁移回滚

## 设计要点

- 在线 DDL 的核心不是“零风险”，而是把风险拆成可观测、可回退的小步骤。
- 大表变更通常要拆成 schema 变更、数据回填、代码兼容、最终切换四段。
- 迁移脚本要能中断后继续，而不是失败后只能整段重跑。
- 任何在线 DDL 都要先明确锁级别、持续时间和失败回滚策略。

## 关联阅读

- [PostgreSQL 开发专题](./postgresql-development.md)
- [Schema 迁移与回填专题](./schema-migrations-backfill.md)
- [PostgreSQL 锁与并发专题](./postgresql-locking.md)
- [PostgreSQL 长事务专题](./postgresql-long-transactions.md)
- [PostgreSQL 批量导入专题](./postgresql-bulk-ingest.md)

返回 [索引](../README.md)
