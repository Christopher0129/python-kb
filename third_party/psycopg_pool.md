# psycopg_pool

`psycopg_pool` 为 `psycopg` 提供同步和异步 PostgreSQL 连接池，适合服务端长连接管理。

## 安装

```bash
pip install psycopg[pool]
```

## 基本示例

```python
from psycopg_pool import ConnectionPool

pool = ConnectionPool("dbname=demo user=postgres", min_size=1, max_size=10)

with pool.connection() as conn:
    with conn.cursor() as cur:
        cur.execute("select now()")
        print(cur.fetchone())
```

## 常见能力

| 能力 | 说明 |
| --- | --- |
| `ConnectionPool(...)` | 创建同步连接池 |
| `AsyncConnectionPool(...)` | 创建异步连接池 |
| `pool.connection()` | 从池中借出连接 |
| `pool.wait()` | 等待连接池就绪 |

## 关联阅读

- [psycopg](./psycopg.md)
- [PostgreSQL 开发专题](../topics/postgresql-development.md)
- [连接池专题](../topics/connection-pooling.md)
- [异步数据库专题](../topics/async-database-access.md)

返回 [索引](../README.md)
