# MongoDB Change Streams 专题

这个专题关注如何把 MongoDB 的变更事件安全地接入下游，而不是把 Change Streams 当作绝对可靠的事件总线。

## 适用场景

- 需要把 MongoDB 变更同步到搜索、缓存或分析链路
- 需要构建轻量 CDC 或订阅机制
- 希望在文档写入后触发异步任务

## 常见主题

- resume token
- 断点续读
- 事件幂等
- 顺序与重复消费
- 下游补偿与回放

## 设计要点

- Change Streams 更像增量订阅接口，不等于完整可靠的业务事件系统。
- 任何基于变更流的链路都要准备断连恢复、重复事件和补偿重放方案。
- 下游如果要求强契约和长期保留，通常还要补 outbox、审计或离线回补能力。
- 变更流和聚合、分片、权限模型之间有耦合，不能只从代码层面理解。

## 关联阅读

- [MongoDB 开发专题](./mongodb-development.md)
- [MongoDB 模式设计专题](./mongodb-schema-design.md)
- [消息系统专题](./message-systems.md)
- [变更数据捕获专题](./change-data-capture.md)
- [Outbox / Inbox 模式专题](./outbox-inbox-patterns.md)

返回 [索引](../README.md)
