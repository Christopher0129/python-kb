# Locust

`Locust` 适合用 Python 定义压测用户行为，做接口、会话和业务路径级别的负载测试。

## 安装

```bash
pip install locust
```

## 基本示例

```python
from locust import HttpUser, between, task


class ApiUser(HttpUser):
    wait_time = between(1, 3)

    @task
    def health(self):
        self.client.get("/health")
```

运行：

```bash
locust -f locustfile.py --host http://127.0.0.1:8000
```

## 常见能力

| 能力 | 说明 |
| --- | --- |
| `HttpUser` | 定义一个会发 HTTP 请求的虚拟用户 |
| `@task` | 声明用户行为 |
| `between(a, b)` | 控制用户两次行为之间的等待时间 |
| `--headless -u 50 -r 5 -t 1m` | 无 UI 执行固定时长压测 |

## 使用建议

- 压测脚本应尽量接近真实业务路径，而不只是单接口轰炸
- 把登录、列表、详情、写入等操作比例设计清楚
- 压测要结合限流、连接池、缓存命中和下游容量一起看

## 关联阅读

- [load testing](../topics/load-testing.md)
- [性能基准专题](../topics/benchmarking.md)
- [连接池专题](../topics/connection-pooling.md)
- [可观测性专题](../topics/observability.md)

返回 [索引](../README.md)
