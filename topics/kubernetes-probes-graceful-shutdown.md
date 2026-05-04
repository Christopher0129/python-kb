# Kubernetes 探针与优雅停机专题

这个专题关注 Python 服务在 Kubernetes 中的启动探针、存活探针、就绪探针和停机收敛过程。

## 适用场景

- 滚动发布期间出现瞬时 5xx
- worker 被杀掉后任务丢失或重复执行
- 服务启动慢、预热长或连接初始化复杂

## 常见主题

- startupProbe
- livenessProbe
- readinessProbe
- preStop hook
- terminationGracePeriodSeconds

## 设计要点

- 就绪探针表达的是“可接流量”，不是“进程已启动”。
- 存活探针过严会把短暂抖动放大成反复重启。
- 优雅停机要同时覆盖 HTTP 请求、后台任务、消息消费和连接池释放。
- 探针阈值要基于真实启动和关闭时序，而不是拍脑袋设置。

## 关联阅读

- [Kubernetes 运维专题](./kubernetes-operations.md)
- [健康检查与指标专题](./health-metrics.md)
- [Worker 运行治理专题](./worker-runtime-operations.md)
- [部署与运维专题](./deployment-operations.md)
- [渐进式交付专题](./progressive-delivery.md)

返回 [索引](../README.md)
