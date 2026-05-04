# LangChain

`LangChain` 适合组织提示词、模型调用、检索和工具编排，是常见的 LLM 应用框架之一。

## 安装

```bash
pip install langchain
```

## 基本示例

```python
from langchain_core.prompts import ChatPromptTemplate

template = ChatPromptTemplate([
    ("system", "You are a helpful assistant."),
    ("human", "{question}"),
])

prompt = template.invoke({"question": "What is Python?"})
print(prompt)
```

## 适用场景

- Prompt 模板管理
- 检索增强问答
- 多步骤 LLM 应用编排

## 关联阅读

- [LlamaIndex](./llamaindex.md)
- [RAG 流水线专题](../topics/rag-pipelines.md)
- [向量检索专题](../topics/vector-retrieval.md)

返回 [索引](../README.md)
