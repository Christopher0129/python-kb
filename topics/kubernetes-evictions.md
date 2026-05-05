# Kubernetes 驱逐与抢占专题

这个专题关注节点资源压力、优先级和调度策略导致的 Pod 驱逐、抢占和服务抖动。

## 适用场景

- 节点内存紧张时 Pod 被频繁驱逐
- 同一服务在高峰时稳定性波动明显
- 平台层需要区分可牺牲负载和核心负载

## 常见主题

- Eviction
- PriorityClass
- requests / limits
- 节点压力信号
- QoS 类别

## 设计要点

- 驱逐问题通常不是单个 Pod 配置问题，而是集群资源治理问题。
- Python 服务要明确哪些实例可被牺牲，哪些必须优先保活。
- 排障时应同时看节点事件、Pod QoS、资源申请与真实用量偏差。
- 驱逐治理要与自动扩缩容、容量规划和成本优化一起评估。

## 关联阅读

- [Kubernetes 资源治理专题](./kubernetes-resource-management.md)
- [Kubernetes 自动扩缩容专题](./kubernetes-autoscaling.md)
- [Kubernetes Pod 排障专题](./kubernetes-pod-debugging.md)
- [容量规划专题](./capacity-planning.md)
- [Kubernetes 成本优化专题](./kubernetes-cost-optimization.md)

返回 [索引](../README.md)
