# Kubernetes 资源治理专题

这个专题关注 Python 服务在 Kubernetes 中的 CPU、内存、临时存储和 Pod 密度治理。

## 适用场景

- OOMKilled、CPU 限流或节点挤压频繁出现
- API 服务、异步 worker 和批处理任务混部
- 需要把资源配额和自动扩缩容联动起来

## 常见主题

- requests 与 limits
- QoS 类别
- OOM 排查
- 临时存储治理
- Namespace 配额与 LimitRange

## 设计要点

- Python 进程内存峰值通常来自缓存、批量对象和序列化，不能只看平均值。
- CPU limit 过低会影响 GC、压缩、加解密和 JSON 编解码延迟。
- worker 型服务要同时考虑单 Pod 并发度和每任务资源消耗。
- 资源治理要和 HPA、队列长度和节点容量一起评估，避免局部最优。

## 关联阅读

- [Kubernetes 运维专题](./kubernetes-operations.md)
- [Kubernetes 自动扩缩容专题](./kubernetes-autoscaling.md)
- [Kubernetes 驱逐与抢占专题](./kubernetes-evictions.md)
- [容量规划专题](./capacity-planning.md)
- [性能基准专题](./benchmarking.md)
- [Worker 运行治理专题](./worker-runtime-operations.md)

返回 [索引](../README.md)
