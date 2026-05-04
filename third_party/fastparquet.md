# fastparquet

`fastparquet` 适合以 Pandas 为中心读写 Parquet，做轻量分析、批处理和列式文件交换。

## 安装

```bash
pip install fastparquet
```

## 基本示例

```python
import pandas as pd
from fastparquet import ParquetFile, write


df = pd.DataFrame({"id": [1, 2], "score": [0.8, 0.9]})
write("sample.parquet", df)

pf = ParquetFile("sample.parquet")
loaded = pf.to_pandas()
```

## 常见能力

| 能力 | 说明 |
| --- | --- |
| `write(...)` | 写入 Parquet 文件 |
| `ParquetFile(...)` | 打开 Parquet 文件或数据集 |
| `to_pandas()` | 读成 Pandas DataFrame |
| `iter_row_groups()` | 按 row group 迭代读取 |

## 使用建议

- 更适合以 Pandas 为中心的读写链路
- 处理大表时要注意 row group、压缩和分区策略
- 如果项目大量依赖 Arrow 生态，也要评估 `pyarrow` 一侧的兼容性

## 关联阅读

- [PyArrow](./pyarrow.md)
- [Parquet 与 Arrow 专题](../topics/parquet-arrow.md)
- [列式数据处理专题](../topics/columnar-data-processing.md)
- [Lakehouse Catalog 专题](../topics/lakehouse-catalogs.md)

返回 [索引](../README.md)
