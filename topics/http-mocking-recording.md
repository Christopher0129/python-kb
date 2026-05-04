# HTTP Mock 与录制专题

这个专题关注测试外部 HTTP 依赖时，如何用 mock、录制或回放控制不稳定因素。

## 适用场景

- 第三方 API 调用测试
- Webhook 回调验证
- 需要隔离真实网络波动的服务测试

## 常见主题

- 请求拦截与响应伪造
- 请求参数和头部断言
- 录制回放与快照
- 错误码、超时、重试场景模拟
- 与契约测试的边界

## 设计要点

- mock 应聚焦外部边界，不要把内部业务逻辑一起伪造
- 录制回放数据要注意脱敏和时效
- 超时、429、500 等失败路径要主动覆盖
- 对关键第三方依赖仍应保留少量真实集成验证

## 关联阅读

- [respx](../third_party/respx.md)
- [VCR.py](../third_party/vcrpy.md)
- [httpx](../third_party/httpx.md)
- [接口测试专题](./api-testing.md)
- [Webhooks 专题](./webhooks.md)

返回 [索引](../README.md)
