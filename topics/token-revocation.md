# Token 吊销专题

这个专题关注用户登出、权限变更、凭证泄露后，令牌如何尽快失效并在全链路收敛。

## 适用场景

- JWT 已发出，但需要立刻让它失效
- 账号封禁、角色变更或设备下线后权限不能继续生效
- 多服务间存在本地缓存或网关缓存

## 常见主题

- 黑名单
- token 版本号
- 短期 token
- 缓存失效
- 风险强制下线

## 设计要点

- 吊销能力取决于 token 设计，不存在“所有 JWT 都能实时吊销”的免费方案。
- 黑名单策略要考虑查询成本、缓存一致性和过期清理。
- 权限高风险场景更适合缩短 token 寿命并增加二次校验。
- 吊销链路应覆盖网关、应用和下游缓存，而不是只改认证中心。

## 关联阅读

- [Token 生命周期专题](./token-lifecycle.md)
- [Token 认证专题](./token-authentication.md)
- [OAuth2 与 OpenID Connect 专题](./oauth2-oidc.md)
- [认证与授权专题](./auth-authorization.md)
- [审计日志专题](./audit-logging.md)

返回 [索引](../README.md)
