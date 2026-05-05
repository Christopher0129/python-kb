# 认证与授权专题

这个专题关注服务如何识别“你是谁”以及“你能做什么”。

## 常见主题

| 主题 | 说明 |
| --- | --- |
| 认证 | 用户或服务身份校验 |
| 授权 | 权限和角色控制 |
| Token | 无状态访问凭证 |
| 权限边界 | 区分公开接口和受限接口 |

## 应用层建议

- 把认证逻辑收敛在中间件或依赖层
- 不要在每个业务函数里重复做鉴权
- 权限错误和业务错误分开处理
- 对高风险接口结合限流、审计日志和告警策略

## 关联阅读

- [FastAPI 进阶专题](./fastapi-advanced.md)
- [API 开发专题](./api-development.md)
- [安全基础专题](./security-basics.md)
- [Token 认证专题](./token-authentication.md)
- [OAuth2 与 OpenID Connect 专题](./oauth2-oidc.md)
- [RBAC 与 ABAC 专题](./rbac-abac.md)
- [风险认证专题](./risk-based-authentication.md)
- [API Key 治理专题](./api-key-management.md)
- [服务间认证专题](./service-to-service-auth.md)
- [策略引擎专题](./policy-engines.md)
- [限流专题](./rate-limiting.md)

返回 [索引](../README.md)
