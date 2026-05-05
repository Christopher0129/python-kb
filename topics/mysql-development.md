# MySQL 开发专题

这个专题关注 MySQL 在 Python 项目中的连接、事务、索引和读写实践。

## 适用场景

- 事务型业务系统的主要存储
- 报表与业务库混合的读写场景
- 既用 ORM 又保留手写 SQL 的服务端项目

## 常见主题

- 连接池与事务
- 参数化 SQL
- 批量写入
- 索引与执行计划
- ORM 与原生 SQL 取舍

## 设计要点

- 先弄清隔离级别、锁范围和热点写入模式
- 字符集、排序规则和时区必须统一约定
- 复杂分页、模糊查询和批量更新要从执行计划看成本
- 连接池大小应按数据库承载和请求模型一起调

## 关联阅读

- [PyMySQL](../third_party/pymysql.md)
- [mysqlclient](../third_party/mysqlclient.md)
- [数据库开发专题](./database-development.md)
- [SQL 优化专题](./sql-optimization.md)
- [MySQL 查询计划专题](./mysql-query-plans.md)
- [MySQL 锁冲突与争用专题](./mysql-locking-contention.md)
- [MySQL 在线改表专题](./mysql-online-schema-change.md)
- [数据仓库与 ETL 专题](./data-warehouse-etl.md)

返回 [索引](../README.md)
