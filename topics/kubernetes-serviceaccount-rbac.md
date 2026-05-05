# Kubernetes ServiceAccount 与 RBAC 专题

这个专题关注 Python 服务在 Kubernetes 中如何声明服务身份、绑定权限并避免过度授权。

## 适用场景

- Pod 需要访问集群 API 或外部云资源
- 多个服务共享默认账号，权限边界不清晰
- 平台需要审计哪个服务拥有了哪些集群权限

## 常见主题

- ServiceAccount
- Role / ClusterRole
- RoleBinding
- 最小权限
- 权限审计

## 设计要点

- 不要让业务 Pod 长期依赖 `default` ServiceAccount。
- RBAC 授权要按命名空间、资源类型和操作粒度收敛。
- 权限申请、变更和回收应纳入发布与审计流程。
- ServiceAccount 身份和工作负载身份、Secret 分发策略要协同治理。

## 关联阅读

- [Kubernetes 工作负载身份专题](./kubernetes-workload-identity.md)
- [Kubernetes Secret 分发专题](./kubernetes-secret-distribution.md)
- [RBAC 与 ABAC 专题](./rbac-abac.md)
- [服务间认证专题](./service-to-service-auth.md)
- [Kubernetes 运维专题](./kubernetes-operations.md)

返回 [索引](../README.md)
