# FAISS

`FAISS` 适合本地高维向量相似度搜索，常见于召回、去重和语义检索原型。

## 安装

```bash
pip install faiss-cpu
```

## 基本示例

```python
import faiss
import numpy as np

dim = 4
index = faiss.IndexFlatL2(dim)

xb = np.array([[1.0, 0.0, 0.0, 0.0], [0.9, 0.1, 0.0, 0.0]], dtype="float32")
index.add(xb)

xq = np.array([[1.0, 0.0, 0.0, 0.0]], dtype="float32")
distances, indices = index.search(xq, 1)
print(indices)
```

## 适用场景

- 本地向量检索原型
- 小规模语义搜索
- 向量召回基础实验

## 关联阅读

- [向量检索专题](../topics/vector-retrieval.md)
- [RAG 流水线专题](../topics/rag-pipelines.md)

返回 [索引](../README.md)
