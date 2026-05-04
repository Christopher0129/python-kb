# structlog

`structlog` 适合结构化日志输出，便于日志聚合、检索和链路排查。

## 安装

```bash
pip install structlog
```

## 基本示例

```python
import structlog

log = structlog.get_logger()
log.info("user_login", user_id=123, source="web")
```

## 适用场景

- 服务化项目
- 需要日志聚合检索
- 想让日志字段结构更稳定

## 关联阅读

- [logging](../stdlib/logging.md)
- [可观测性专题](../topics/observability.md)

返回 [索引](../README.md)
