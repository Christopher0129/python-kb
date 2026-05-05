# 搜索 Query Rules 专题

这个专题关注在搜索排序之外，如何通过显式规则对特定查询、实体或业务场景做可控干预。

## 适用场景

- 某些品牌词、活动词需要固定置顶或屏蔽结果
- 产品团队需要对少量头部查询做人工纠偏
- 业务干预越来越多，已经不能靠散落代码硬编码

## 常见主题

- 置顶规则
- 屏蔽规则
- 查询重写
- 生效范围
- 规则冲突

## 设计要点

- Query Rules 要有明确优先级，避免多条规则互相覆盖而不可解释。
- 规则系统应区分临时运营干预和长期产品逻辑。
- 每条规则都需要生效范围、过期时间和变更审计。
- 规则数量增长后，必须有回放验证和离线效果评估能力。

## 关联阅读

- [搜索 Query Understanding 专题](./search-query-understanding.md)
- [搜索排序信号专题](./search-ranking-signals.md)
- [查询改写专题](./query-rewriting.md)
- [搜索实验专题](./search-experiments.md)
- [策略灰度发布专题](./policy-rollout-strategies.md)

返回 [索引](../README.md)
