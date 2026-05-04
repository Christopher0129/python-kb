# PyIceberg

`PyIceberg` 适合在 Python 里操作 Iceberg Catalog 和表元数据，做表发现、命名空间管理和维护任务。

## 安装

```bash
pip install pyiceberg
```

## 基本示例

```python
from pyiceberg.catalog import load_catalog


catalog = load_catalog("production")
table = catalog.load_table("analytics.orders")
print(table)
```

## 常见能力

| 能力 | 说明 |
| --- | --- |
| `load_catalog(...)` | 加载 catalog 配置 |
| `catalog.load_table(...)` | 读取表元数据 |
| `catalog.list_tables(...)` | 列出命名空间下的表 |
| `catalog.create_namespace(...)` | 创建命名空间 |

## 使用建议

- 它更偏控制面和元数据面，不等于替代 Spark 的全部读写生态
- 设计 catalog 时要先明确权限、命名空间和多环境隔离
- 适合放在元数据治理、维护任务和平台工具链里

## 关联阅读

- [Lakehouse 表格式专题](../topics/table-formats-lakehouse.md)
- [Lakehouse Catalog 专题](../topics/lakehouse-catalogs.md)
- [Delta Lake 专题](../topics/delta-lake.md)
- [数据湖存储专题](../topics/data-lake-storage.md)

返回 [索引](../README.md)
