# celery

`celery` 适合执行异步后台任务，如发邮件、生成报表、批量同步和定时任务。

## 安装

```bash
pip install celery
```

## 最小示例

```python
from celery import Celery

app = Celery("tasks", broker="redis://localhost:6379/0")


@app.task
def add(a, b):
    return a + b
```

## 适用场景

- 耗时任务异步化
- 定时批处理
- Web 请求与后台任务解耦

## 关联阅读

- [redis-py](./redis.md)
- [缓存与队列专题](../topics/cache-queues.md)
- [部署与运维专题](../topics/deployment-operations.md)

返回 [索引](../README.md)
