# 数据库开发专题

这个专题把 Python 常见数据库开发链路串起来：本地 SQLite、ORM 建模、事务管理、迁移和查询组织。

## 先学哪些模块和库

| 模块 / 库 | 作用 | 推荐程度 |
| --- | --- | --- |
| `sqlite3` | 本地数据库、轻量入门 | 必学 |
| `SQLAlchemy` | ORM 和 SQL 工具 | 必学 |
| `Alembic` | 表结构迁移 | 进阶 |
| `datetime` | 时间字段处理 | 高频 |
| `decimal` | 金额等精确计算 | 高频 |

## 典型工作流

### 1. 用 SQLite 快速起步

```python
import sqlite3

conn = sqlite3.connect("demo.db")
cur = conn.cursor()
cur.execute("create table if not exists users (id integer primary key, name text)")
cur.execute("insert into users (name) values (?)", ("Tom",))
conn.commit()
conn.close()
```

### 2. 用 SQLAlchemy 组织模型

```python
from sqlalchemy import String
from sqlalchemy.orm import DeclarativeBase, Mapped, mapped_column


class Base(DeclarativeBase):
    pass


class User(Base):
    __tablename__ = "users"

    id: Mapped[int] = mapped_column(primary_key=True)
    name: Mapped[str] = mapped_column(String(50))
```

### 3. 用 Session 管事务

```python
from sqlalchemy.orm import Session

with Session(engine) as session:
    session.add(User(name="Amy"))
    session.commit()
```

### 4. 用 Alembic 管迁移

- 初始化迁移目录
- 生成迁移脚本
- 检查脚本
- 升级数据库

## 常见设计点

| 主题 | 建议 |
| --- | --- |
| 主键 | 保持稳定唯一 |
| 金额字段 | 优先精确数值方案 |
| 时间字段 | 统一时区和格式 |
| 事务 | 成组写入要明确提交或回滚 |
| 查询层 | 不要把 SQL 散落在各处 |

## 实战建议

- 小工具可先从 `sqlite3` 开始
- 项目变复杂后再引入 SQLAlchemy
- 表结构变化频繁时尽早接入迁移工具

## 关联阅读

- [sqlite3](../stdlib/sqlite3.md)
- [SQLAlchemy 2.x 基础](../database/sqlalchemy.md)
- [Alembic](../third_party/alembic.md)
- [decimal](../stdlib/decimal.md)
- [事务与隔离级别专题](./transaction-isolation.md)
- [索引设计专题](./index-design.md)
- [查询计划分析专题](./query-plan-analysis.md)
- [Schema 迁移与回填专题](./schema-migrations-backfill.md)
- [异步数据库专题](./async-database-access.md)
- [MySQL 开发专题](./mysql-development.md)
- [PostgreSQL 开发专题](./postgresql-development.md)
- [MongoDB 开发专题](./mongodb-development.md)
- [MySQL 查询计划专题](./mysql-query-plans.md)
- [MySQL 锁冲突与争用专题](./mysql-locking-contention.md)
- [MySQL 在线改表专题](./mysql-online-schema-change.md)
- [MongoDB 模式设计专题](./mongodb-schema-design.md)
- [MongoDB 索引与聚合专题](./mongodb-indexing-aggregation.md)
- [MongoDB Change Streams 专题](./mongodb-change-streams.md)
- [Redis 高级专题](./redis-advanced.md)

返回 [索引](../README.md)
