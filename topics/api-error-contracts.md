# API 错误契约专题

这个专题关注接口失败时应该返回什么、如何稳定返回，以及如何让调用方能正确处理错误。

## 适用场景

- 团队内部各服务错误格式不统一
- 外部调用方无法区分可重试和不可重试错误
- 线上排障时缺少 request id、错误码和上下文

## 常见主题

- 错误码体系
- 校验错误格式
- 可重试标记
- trace id / request id
- 用户可见信息与内部诊断信息分离

## 设计要点

- 错误契约是 API 契约的一部分，不能只在代码里临时抛异常。
- 错误体至少要包含稳定错误码、可读消息、诊断标识和时间上下文。
- 4xx、5xx 和业务失败要分清层级，避免所有错误都塞进 200 响应。
- 失败返回一旦进入 SDK 和客户端逻辑，就必须长期保持兼容。

## 关联阅读

- [API 开发专题](./api-development.md)
- [OpenAPI 治理专题](./openapi-governance.md)
- [契约测试专题](./contract-testing.md)
- [API 版本治理专题](./api-versioning.md)
- [日志关联与结构化日志专题](./log-correlation-structured-logging.md)

返回 [索引](../README.md)
