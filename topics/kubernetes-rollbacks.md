# Kubernetes 回滚专题

这个专题关注镜像、配置、特性开关和依赖切换出问题后，如何快速、安全地撤回到稳定状态。

## 适用场景

- 发布后错误率迅速上升
- 配置、索引或数据库变更与代码发布耦合紧密
- 平台团队需要统一回滚路径和审计流程

## 常见主题

- Deployment 回滚
- Helm 回滚
- 配置回滚
- 特性开关回退
- 数据变更补偿

## 设计要点

- 真正的回滚不只涉及镜像版本，还包括配置、索引和数据库状态。
- 回滚路径应预先演练，而不是等事故发生时临时拼命令。
- 自动回滚阈值要和监控、告警、变更窗口联动。
- 回滚后仍要保留现场信息，避免“恢复了但根因丢了”。

## 关联阅读

- [Kubernetes 滚动交付专题](./kubernetes-rolling-delivery.md)
- [Helm 与 Chart 专题](./helm-charts.md)
- [配置灰度与回滚专题](./config-rollout-strategies.md)
- [发布策略专题](./deployment-strategies.md)
- [事故响应专题](./incident-response.md)

返回 [索引](../README.md)
