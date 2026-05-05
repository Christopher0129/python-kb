# Kubernetes Ingress 灰度专题

这个专题关注通过 Ingress、Gateway 或流量层配置实现按比例、按头部或按用户的渐进式发布。

## 适用场景

- 新版本需要先小流量验证
- 同时存在多租户或特定用户灰度需求
- 应用层不方便自行做复杂流量分发

## 常见主题

- 流量百分比
- Header 路由
- Cookie 路由
- 观测与自动回滚
- 多入口一致性

## 设计要点

- 灰度流量策略要和监控、回滚阈值、配置版本一起设计。
- 多入口、多地域和 CDN 前置场景要明确灰度边界，否则容易出现“灰度不闭环”。
- 用户级灰度比简单百分比灰度更利于复现，但要注意状态一致性。
- 流量灰度不能替代数据库和索引变更的兼容性设计。

## 关联阅读

- [Kubernetes Ingress 与流量入口专题](./kubernetes-ingress-traffic.md)
- [渐进式交付专题](./topics/progressive-delivery.md)
- [Kubernetes 回滚专题](./kubernetes-rollbacks.md)
- [发布策略专题](./deployment-strategies.md)
- [事故响应专题](./incident-response.md)

返回 [索引](../README.md)
