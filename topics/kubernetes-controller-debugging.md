# Kubernetes 控制器排障专题

这个专题关注 Deployment、StatefulSet、Job、HPA 等控制器没有按预期收敛时的排查路径。

## 适用场景

- 资源 YAML 看起来没问题，但状态迟迟不收敛
- 控制器不断回滚、重建或重复 reconcile
- 平台上有多个 operator 和控制器，责任边界不清楚

## 常见主题

- reconcile 失败
- status 不一致
- 事件排查
- 控制器日志
- 资源依赖链

## 设计要点

- 控制器排障要先明确“谁是 owner”，不要把所有异常都归因给 Pod 本身。
- 状态问题通常要同时看 spec、status、event 和 controller log。
- 多控制器共享同一资源时，最容易出现字段互相覆盖和持续抖动。
- 排障完成后要沉淀 runbook，否则同类问题会一再重演。

## 关联阅读

- [Kubernetes 运维专题](./kubernetes-operations.md)
- [Kubernetes Pod 排障专题](./kubernetes-pod-debugging.md)
- [Kubernetes 回滚专题](./kubernetes-rollbacks.md)
- [Runbook 与运维手册专题](./runbooks-and-ops.md)
- [事故响应专题](./incident-response.md)

返回 [索引](../README.md)
