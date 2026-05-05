# MongoDB 模式设计专题

这个专题关注文档模型如何随着查询模式、更新频率和数据生命周期一起设计，而不是只按对象结构直译。

## 适用场景

- 一个业务对象含有大量嵌套字段和数组
- 不确定该嵌入还是引用
- 需要同时兼顾查询效率和模型演进

## 常见主题

- embed vs reference
- 文档大小与增长
- 高频更新字段拆分
- TTL 与归档
- shard key 与租户建模

## 设计要点

- MongoDB 模式设计应优先服务查询路径，而不是纯粹服务写入时的对象结构。
- 高频变化字段和低频核心字段混在一起，容易放大写放大与文档迁移成本。
- 数组、嵌套对象和多值字段很灵活，但索引与更新成本会同步增加。
- 文档库模式可以演进，但前提是先约束字段语义、缺省值和兼容规则。

## 关联阅读

- [MongoDB 开发专题](./mongodb-development.md)
- [MongoDB 索引与聚合专题](./mongodb-indexing-aggregation.md)
- [Schema 演进专题](./schema-evolution.md)
- [数据契约专题](./data-contracts.md)
- [MongoDB Change Streams 专题](./mongodb-change-streams.md)

返回 [索引](../README.md)
