# Token 生命周期专题

这个专题关注访问令牌从签发、续期、吊销到失效的完整生命周期治理。

## 适用场景

- 系统使用 JWT、session token 或短期 service token
- 需要同时处理登录态体验和安全风险
- 多终端、多设备和多服务场景令牌规则复杂

## 常见主题

- access / refresh token
- 续期策略
- 吊销与黑名单
- 时钟漂移
- token 轮换

## 设计要点

- Token 生命周期设计要平衡用户体验、权限收敛速度和后端复杂度。
- 自包含 JWT 便于扩展，但吊销和即时失效能力较弱。
- 续期逻辑、设备管理和风险检测应纳入统一身份治理。
- 服务身份 token 和用户身份 token 不应混用同一策略。

## 关联阅读

- [Token 认证专题](./token-authentication.md)
- [OAuth2 与 OpenID Connect 专题](./oauth2-oidc.md)
- [服务间认证专题](./service-to-service-auth.md)
- [API Key 治理专题](./api-key-management.md)
- [密钥轮换专题](./secrets-rotation.md)

返回 [索引](../README.md)
