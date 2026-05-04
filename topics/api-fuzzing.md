# API Fuzzing 专题

这个专题关注通过自动生成边界输入和异常输入，提前发现接口在参数校验、异常处理和兼容性上的薄弱点。

## 适用场景

- OpenAPI schema 已较完整
- 需要验证错误分支、异常输入和边界组合
- 接口变更频繁，人工样例覆盖不足

## 常见主题

- 基于 schema 的输入生成
- 正向与负向 case
- 边界值、缺字段、错类型
- 服务端 5xx 与容错暴露
- 兼容性回归

## 设计要点

- fuzzing 不是只追求“打挂服务”，而是验证契约边界是否清晰
- 要区分预期拒绝和非预期崩溃
- 结果应和错误码规范、告警和审计日志联动
- 自动化 fuzzing 适合放到 PR、夜间任务和发布前回归中

## 关联阅读

- [Schemathesis](../third_party/schemathesis.md)
- [OpenAPI 治理专题](./openapi-governance.md)
- [接口测试专题](./api-testing.md)
- [契约测试专题](./contract-testing.md)

返回 [索引](../README.md)
