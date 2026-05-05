# Kubernetes 多租户专题

这个专题关注多个团队、业务线或客户共用同一集群时的隔离边界、配额和治理约束。

## 适用场景

- 多团队共用平台，希望隔离资源和权限
- SaaS 平台需要按租户或业务域做命名空间分层
- 一次误操作可能波及整个集群

## 常见主题

- 命名空间隔离
- 资源配额
- 网络隔离
- 权限边界
- 成本归属

## 设计要点

- 多租户不是只建多个 namespace，还包括 RBAC、NetworkPolicy、Secret 边界和审计归属。
- 隔离越强，平台操作成本越高，要根据风险等级分层设计。
- 平台默认值要偏保守，例如资源限制、镜像策略和准入控制。
- 多租户治理最终要能回答“谁能动什么资源、花了多少成本、出了问题影响谁”。

## 关联阅读

- [Kubernetes ServiceAccount 与 RBAC 专题](./kubernetes-serviceaccount-rbac.md)
- [Kubernetes NetworkPolicy 专题](./kubernetes-network-policies.md)
- [Kubernetes 资源治理专题](./kubernetes-resource-management.md)
- [Kubernetes 准入控制专题](./kubernetes-admission-control.md)
- [成本治理专题](./cost-governance.md)

返回 [索引](../README.md)
