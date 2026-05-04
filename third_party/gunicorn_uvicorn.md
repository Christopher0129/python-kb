# gunicorn 与 uvicorn

`gunicorn` 和 `uvicorn` 常用于部署 Python Web 服务。

## 常见分工

| 工具 | 适用场景 |
| --- | --- |
| `uvicorn` | ASGI 应用，如 FastAPI |
| `gunicorn` | WSGI/ASGI 服务管理，常配 worker |

## 示例

```bash
uvicorn app:app --host 0.0.0.0 --port 8000
gunicorn app:app -w 4
```

## 关联阅读

- [FastAPI 入门](../frameworks/fastapi.md)
- [Flask 入门](../frameworks/flask.md)
- [部署与运维专题](../topics/deployment-operations.md)
- [Docker 专题](../topics/docker-basics.md)

返回 [索引](../README.md)
