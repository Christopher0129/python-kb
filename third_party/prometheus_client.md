# prometheus-client

`prometheus-client` 适合给 Python 服务暴露指标，如请求数、耗时和任务状态。

## 安装

```bash
pip install prometheus-client
```

## 基本示例

```python
from prometheus_client import Counter

REQUESTS = Counter("demo_requests_total", "Total requests")
REQUESTS.inc()
```

## 常见指标类型

| 类型 | 用途 |
| --- | --- |
| `Counter` | 单调递增计数 |
| `Gauge` | 当前值 |
| `Histogram` | 延迟分布 |

## 关联阅读

- [可观测性专题](../topics/observability.md)
- [健康检查与指标专题](../topics/health-metrics.md)

返回 [索引](../README.md)
