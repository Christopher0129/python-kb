# API 开发专题

这个专题关注如何用 Python 构建 API 服务，包括路由、请求校验、响应结构、异常处理和数据库访问。

## 先学哪些框架和库

| 框架 / 库 | 作用 | 推荐程度 |
| --- | --- | --- |
| `Flask` | 轻量 API 和原型 | 高频 |
| `FastAPI` | 现代类型化 API | 必学 |
| `pydantic` | 数据校验与模型 | 高频 |
| `SQLAlchemy` | 数据库访问 | 高频 |
| `pytest` | 接口测试 | 高频 |

## 一个最小 API 结构

```text
app/
  main.py
  schemas.py
  service.py
  models.py
  db.py
```

## 关键设计点

| 主题 | 建议 |
| --- | --- |
| 路由层 | 只负责接入和出参，不承载重业务 |
| 校验层 | 用模型声明字段约束 |
| 服务层 | 放业务逻辑 |
| 存储层 | 统一数据库和外部依赖访问 |
| 契约层 | 明确 schema、版本和兼容策略 |

## 适用路线

- 快速原型：Flask
- 强类型 JSON API：FastAPI

## 关联阅读

- [Flask 入门](../frameworks/flask.md)
- [FastAPI 入门](../frameworks/fastapi.md)
- [pydantic](../third_party/pydantic.md)
- [SQLAlchemy 2.x 基础](../database/sqlalchemy.md)
- [接口测试专题](./api-testing.md)
- [API 版本治理专题](./api-versioning.md)
- [API 分页与过滤专题](./api-pagination-filtering.md)
- [API 错误契约专题](./api-error-contracts.md)
- [幂等与重试专题](./idempotency-retries.md)
- [契约测试专题](./contract-testing.md)
- [gRPC 进阶专题](./grpc-advanced.md)
- [GraphQL API 专题](./graphql-apis.md)

返回 [索引](../README.md)
