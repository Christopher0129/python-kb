# qdrant-client

`qdrant-client` 适合在 Python 中连接向量数据库，做相似度检索和语义搜索。

## 安装

```bash
pip install qdrant-client
```

## 基本示例

```python
from qdrant_client import QdrantClient
from qdrant_client.models import Distance, PointStruct, VectorParams

client = QdrantClient(":memory:")
client.create_collection(
    collection_name="docs",
    vectors_config=VectorParams(size=3, distance=Distance.COSINE),
)
client.upsert(
    collection_name="docs",
    points=[
        PointStruct(id=1, vector=[0.1, 0.2, 0.3], payload={"title": "postgres"}),
        PointStruct(id=2, vector=[0.4, 0.2, 0.1], payload={"title": "kubernetes"}),
    ],
)
result = client.query_points(
    collection_name="docs",
    query=[0.1, 0.2, 0.25],
    limit=3,
)
print(result)
```

## 适用场景

- 语义检索
- 文本向量搜索
- 检索增强生成系统

## 常见能力

| 能力 | 说明 |
| --- | --- |
| `QdrantClient(...)` | 创建 Qdrant 客户端 |
| `create_collection(...)` | 创建向量集合 |
| `upsert(...)` | 插入或覆盖点数据 |
| `query_points(...)` | 基于向量或过滤条件查询 |
| `scroll(...)` | 分页扫描集合 |

## 关联阅读

- [搜索系统专题](../topics/search-systems.md)
- [向量检索专题](../topics/vector-retrieval.md)
- [混合检索专题](../topics/hybrid-retrieval.md)
- [元数据过滤专题](../topics/metadata-filtering.md)
- [索引构建流水线专题](../topics/indexing-pipelines.md)
- [RAG 流水线专题](../topics/rag-pipelines.md)
- [数据仓库与 ETL 专题](../topics/data-warehouse-etl.md)

返回 [索引](../README.md)
