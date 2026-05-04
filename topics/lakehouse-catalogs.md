# Lakehouse Catalog 专题

这个专题关注 Lakehouse 里的 catalog、namespace、表发现和元数据治理。

## 适用场景

- 多团队共享数据湖表
- 需要统一表命名、权限和元数据入口
- Spark、Flink、Trino、Python 工具要共享同一套表目录

## 常见主题

- catalog 与 namespace
- 元数据服务
- 表发现与血缘
- 环境隔离
- 权限与命名规范

## 设计要点

- catalog 是控制面，不只是“表能不能读”
- 命名空间要反映团队、域和环境边界
- 多引擎共享时要先统一 schema 演进和提交规范
- 维护任务、审计和清理策略也应围绕 catalog 组织

## 关联阅读

- [PyIceberg](../third_party/pyiceberg.md)
- [Lakehouse 表格式专题](./table-formats-lakehouse.md)
- [数据湖存储专题](./data-lake-storage.md)
- [Schema 演进专题](./schema-evolution.md)

返回 [索引](../README.md)
