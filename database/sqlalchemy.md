# SQLAlchemy 2.x 基础

`SQLAlchemy` 是 Python 最常用的 ORM 和 SQL 工具库之一，适合做数据库建模、查询和事务管理。

## 安装

```bash
pip install sqlalchemy
```

## 核心对象

| 对象 | 用途 |
| --- | --- |
| `create_engine()` | 创建数据库连接引擎 |
| `DeclarativeBase` | ORM 模型基类 |
| `mapped_column()` | 声明字段 |
| `Session()` | 会话和事务管理 |
| `select()` | 构造查询 |

## ORM 示例

```python
from sqlalchemy import String, create_engine, select
from sqlalchemy.orm import DeclarativeBase, Mapped, Session, mapped_column

engine = create_engine("sqlite:///demo.db", echo=False)

class Base(DeclarativeBase):
    pass

class User(Base):
    __tablename__ = "users"

    id: Mapped[int] = mapped_column(primary_key=True)
    name: Mapped[str] = mapped_column(String(50))

Base.metadata.create_all(engine)

with Session(engine) as session:
    session.add(User(name="Tom"))
    session.commit()

    users = session.scalars(select(User)).all()
    print(users)
```

## 常见流程

1. `create_engine()`
2. 定义 `Base` 和模型类
3. `Base.metadata.create_all(engine)`
4. 用 `Session` 增删改查

## 进一步会遇到什么

- 关系映射：一对多、多对多
- 查询优化：避免 N+1
- 事务边界：统一提交、回滚和异常处理
- 分页和筛选：列表接口的常见需求

## 实战建议

- 把模型定义、会话管理和业务查询分层
- 请求生命周期内使用明确的 `Session`
- 查询慢时先看 SQL 次数，再看单条 SQL

## 提醒

- 新项目建议按 SQLAlchemy 2.x 风格写法组织代码
- Web 项目里通常每次请求使用一次独立 `Session`

## 关联阅读

- [数据库开发专题](../topics/database-development.md)
- [SQLAlchemy 进阶专题](../topics/sqlalchemy-advanced.md)
- [SQL 优化专题](../topics/sql-optimization.md)

返回 [索引](../README.md)
