# LlamaIndex

`LlamaIndex` 适合把文档加载、切分、索引和检索组织成更清晰的 RAG 管线。

## 安装

```bash
pip install llama-index
```

## 基本示例

```python
from llama_index.core import SimpleDirectoryReader, VectorStoreIndex

documents = SimpleDirectoryReader("data").load_data()
index = VectorStoreIndex.from_documents(documents)
```

## 适用场景

- 文档问答
- 向量检索流程封装
- 数据加载到检索层的统一编排

## 关联阅读

- [LangChain](./langchain.md)
- [RAG 流水线专题](../topics/rag-pipelines.md)
- [向量检索专题](../topics/vector-retrieval.md)

返回 [索引](../README.md)
