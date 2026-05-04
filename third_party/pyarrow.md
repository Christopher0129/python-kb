# PyArrow

`PyArrow` 适合处理 Arrow 内存格式、Parquet 文件和跨系统列式数据交换。

## 安装

```bash
pip install pyarrow
```

## Arrow Table 示例

```python
import pyarrow as pa

table = pa.table({"name": ["Tom", "Amy"], "age": [18, 20]})
print(table)
```

## Parquet 写入示例

```python
import pyarrow as pa
import pyarrow.parquet as pq

table = pa.table({"value": [1, 2, 3]})
pq.write_table(table, "demo.parquet")
```

## 适用场景

- Parquet 读写
- Arrow 内存列式交换
- 与 DuckDB、Polars、Pandas 互操作

## 关联阅读

- [DuckDB](./duckdb.md)
- [Polars](./polars.md)
- [Parquet 与 Arrow 专题](../topics/parquet-arrow.md)

返回 [索引](../README.md)
