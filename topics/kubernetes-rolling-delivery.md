# Kubernetes 滚动交付专题

这个专题关注 Python 服务在 Kubernetes 中的滚动发布、金丝雀、回滚和发布窗口控制。

## 适用场景

- 发布期需要降低中断与回滚成本
- 新旧版本需要短时并存
- API 服务与异步消费服务的发布约束不同

## 常见主题

- RollingUpdate
- maxUnavailable 与 maxSurge
- 金丝雀与灰度
- 回滚策略
- 发布前后验证

## 设计要点

- 滚动交付策略取决于服务启动时间、连接建立时间和探针稳定时间。
- 消费型服务发布时要考虑 rebalance、积压和幂等，不等同于无状态 API。
- 发布成功标准应显式定义，包括错误率、延迟、消费滞后和业务指标。
- 回滚路径要覆盖镜像、配置、数据库开关和索引版本，不只是 Deployment。

## 关联阅读

- [Kubernetes 运维专题](./kubernetes-operations.md)
- [Kubernetes 探针与优雅停机专题](./kubernetes-probes-graceful-shutdown.md)
- [发布策略专题](./deployment-strategies.md)
- [渐进式交付专题](./progressive-delivery.md)
- [GitOps 交付专题](./gitops-delivery.md)

返回 [索引](../README.md)
