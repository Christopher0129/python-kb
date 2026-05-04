# SQLAlchemy 进阶专题

这个专题关注 SQLAlchemy 在真实项目里的进阶用法，而不是只停留在最小增删改查。

## 常见主题

| 主题 | 说明 |
| --- | --- |
| 关系加载 | 一对多、多对多关系管理 |
| 查询优化 | 避免 N+1 和过度查询 |
| 事务边界 | 统一提交和回滚策略 |
| 分页 | 列表接口分页查询 |

## 实战建议

- 先观察查询次数，再观察单次慢查询
- 服务层不要把数据库会话传得到处都是
- Web 请求和后台任务都要明确事务边界

## 关联阅读

- [SQLAlchemy 2.x 基础](../database/sqlalchemy.md)
- [SQL 优化专题](./sql-optimization.md)
- [数据库开发专题](./database-development.md)

返回 [索引](../README.md)
