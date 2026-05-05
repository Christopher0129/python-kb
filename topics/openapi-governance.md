# OpenAPI 治理专题

这个专题关注 OpenAPI 不只是“自动生成文档”，而是接口契约、客户端生成和演进控制的治理基础。

## 适用场景

- 团队协作 API 开发
- 自动生成 SDK 或测试
- 多版本接口长期演进

## 常见主题

- schema 规范约束
- 错误响应模型统一
- 示例与文档质量
- 客户端生成与同步
- breaking change 检查

## 设计要点

- OpenAPI 要和真实行为保持一致，不能只当展示页面
- 错误码、分页、鉴权头等横切协议应统一建模
- 接口演进要配合契约测试和版本治理
- 自动生成客户端前要先控制 schema 质量

## 关联阅读

- [API 版本治理专题](./api-versioning.md)
- [API 错误契约专题](./api-error-contracts.md)
- [API 分页与过滤专题](./api-pagination-filtering.md)
- [OpenAPI SDK 生成专题](./openapi-sdk-generation.md)
- [契约测试专题](./contract-testing.md)
- [Schemathesis](../third_party/schemathesis.md)

返回 [索引](../README.md)
