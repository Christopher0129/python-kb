# rank-bm25

`rank-bm25` 适合在 Python 中快速构建 BM25 关键词检索原型、召回基线和混合检索实验。

## 安装

```bash
pip install rank-bm25
```

## 基本示例

```python
from rank_bm25 import BM25Okapi

documents = [
    "python async database pooling",
    "postgresql vacuum and bloat",
    "kubernetes rolling deployment",
]
tokenized = [doc.split() for doc in documents]
bm25 = BM25Okapi(tokenized)

scores = bm25.get_scores("postgresql vacuum".split())
print(scores)
```

## 常见能力

| 能力 | 说明 |
| --- | --- |
| `BM25Okapi(...)` | 创建 BM25 检索器 |
| `get_scores(...)` | 获取查询对语料的打分 |
| `get_top_n(...)` | 返回最相关文档 |

## 关联阅读

- [搜索系统专题](../topics/search-systems.md)
- [混合检索专题](../topics/hybrid-retrieval.md)
- [查询改写专题](../topics/query-rewriting.md)
- [相关性调优专题](../topics/relevance-tuning.md)

返回 [索引](../README.md)
