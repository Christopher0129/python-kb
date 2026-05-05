# 契约测试专题

这个专题关注接口实现和对外契约是否一致，而不是只做“返回 200 就算通过”。

## 常见方法

| 方法 | 说明 |
| --- | --- |
| schema 校验 | 响应字段、类型、状态码是否符合规范 |
| 基于 OpenAPI 的自动生成测试 | 用 schema 生成大量输入 |
| 向后兼容测试 | 新版本是否仍兼容旧客户端 |
| 消费者契约测试 | 验证关键消费者依赖的字段没有被破坏 |

## 常见工具

- `pytest`
- `httpx`
- `Schemathesis`
- `Pact`

## 实战建议

- 契约测试要纳入 CI，而不是只在联调时手动跑
- 对高风险接口保留旧版本或兼容性样例
- 失败报告里要能定位到具体字段、状态码或 schema 规则

## 关联阅读

- [Schemathesis](../third_party/schemathesis.md)
- [Pact](../third_party/pact.md)
- [接口测试专题](./api-testing.md)
- [API 版本治理专题](./api-versioning.md)
- [API 错误契约专题](./api-error-contracts.md)
- [OpenAPI SDK 生成专题](./openapi-sdk-generation.md)
- [FastAPI 进阶专题](./fastapi-advanced.md)
- [消费者驱动契约专题](./consumer-driven-contracts.md)

返回 [索引](../README.md)
