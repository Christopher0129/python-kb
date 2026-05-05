# Kubernetes 优先级与抢占专题

这个专题关注如何通过优先级和抢占保护关键业务，同时避免平台陷入“谁都想最高优先级”的失控状态。

## 适用场景

- 在线服务和批处理争抢同一批节点
- 高峰期资源不足，关键服务需要优先存活
- 发生驱逐、调度失败或抢占后很难解释原因

## 常见主题

- PriorityClass
- 抢占策略
- 关键服务保护
- 批处理降级
- 资源挤兑

## 设计要点

- 优先级是平台治理工具，不是业务团队自助拉满的按钮。
- 关键链路服务要配合 PDB、资源保障和节点池一起设计。
- 抢占策略上线前要明确哪些工作负载可以被牺牲。
- 事故排障时要同时看调度日志、事件和资源配额，而不是只看 Pod 状态。

## 关联阅读

- [Kubernetes 驱逐专题](./kubernetes-evictions.md)
- [Kubernetes 资源治理专题](./kubernetes-resource-management.md)
- [Kubernetes 调度与亲和性专题](./kubernetes-scheduling-affinity.md)
- [Kubernetes 节点池专题](./kubernetes-node-pools.md)
- [Kubernetes PDB 与可用性专题](./kubernetes-pdb-availability.md)

返回 [索引](../README.md)
