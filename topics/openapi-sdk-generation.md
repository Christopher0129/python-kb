# OpenAPI SDK 生成专题

这个专题关注如何基于 OpenAPI 规范生成客户端 SDK，并保证规范、实现和发布节奏长期一致。

## 适用场景

- 同一个 API 被多个语言或多个团队复用
- 希望减少手写客户端和字段漂移
- 需要把契约升级同步到 SDK 发布流程

## 常见主题

- schema 稳定性
- 命名与分组约定
- 错误模型生成
- mock / 示例同步
- SDK 版本发布

## 设计要点

- SDK 生成之前先治理规范质量，否则只是把不稳定 schema 批量扩散。
- 生成代码是否可用，取决于命名一致性、示例质量和错误模型完整度。
- 接口弃用、分页协议、鉴权头和错误响应要优先标准化。
- SDK 发布要和 API 变更记录、兼容检查和客户端迁移指引一起走。

## 关联阅读

- [OpenAPI 治理专题](./openapi-governance.md)
- [API 版本治理专题](./api-versioning.md)
- [API 错误契约专题](./api-error-contracts.md)
- [契约测试专题](./contract-testing.md)
- [消费者驱动契约专题](./consumer-driven-contracts.md)

返回 [索引](../README.md)
