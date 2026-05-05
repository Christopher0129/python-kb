# API 分页与过滤专题

这个专题关注列表接口如何在性能、稳定性和可用性之间设计分页、排序和过滤协议。

## 适用场景

- 列表接口需要支持复杂筛选和排序
- 数据量持续增长，偏移量分页越来越慢
- 前后端、开放平台和内部服务都在复用同一套查询接口

## 常见主题

- offset / limit
- keyset pagination
- cursor pagination
- 过滤表达式
- 排序字段白名单

## 设计要点

- 分页协议一旦对外暴露，很难随意修改，必须先约束排序稳定性和兼容策略。
- offset 分页适合浅分页和管理后台，不适合高并发深翻页接口。
- 过滤条件要白名单化，避免把数据库查询能力直接暴露成不受控 DSL。
- 返回体应显式说明 next cursor、总数语义和排序依据，避免客户端猜测。

## 关联阅读

- [API 开发专题](./api-development.md)
- [API 版本治理专题](./api-versioning.md)
- [OpenAPI 治理专题](./openapi-governance.md)
- [SQL 优化专题](./sql-optimization.md)
- [搜索过滤设计专题](./search-filter-design.md)

返回 [索引](../README.md)
