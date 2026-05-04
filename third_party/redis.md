# redis-py

`redis` 客户端适合缓存、计数器、队列、会话和轻量状态共享。

## 安装

```bash
pip install redis
```

## 基本示例

```python
import redis

r = redis.Redis(host="localhost", port=6379, decode_responses=True)
r.set("name", "Tom")
print(r.get("name"))
```

## 适用场景

- 缓存热点数据
- 登录会话存储
- 简单任务队列和计数器

## 关联阅读

- [缓存与队列专题](../topics/cache-queues.md)
- [celery](./celery.md)
- [配置管理专题](../topics/config-management.md)

返回 [索引](../README.md)
