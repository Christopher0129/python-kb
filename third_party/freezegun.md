# Freezegun

`Freezegun` 适合在测试里冻结“当前时间”，验证时间窗口、过期逻辑和定时行为。

## 安装

```bash
pip install freezegun
```

## 基本示例

```python
import datetime as dt
from freezegun import freeze_time


@freeze_time("2026-01-01 08:00:00")
def test_expire_window():
    assert dt.datetime.now() == dt.datetime(2026, 1, 1, 8, 0, 0)
```

## 常见能力

| 能力 | 说明 |
| --- | --- |
| `@freeze_time(...)` | 作为装饰器冻结时间 |
| `with freeze_time(...):` | 作为上下文管理器局部冻结 |
| 冻结 `datetime` / `date` / `time` | 统一控制常见时间来源 |

## 使用建议

- 先统一项目的取时入口，再决定哪里用冻结时间
- 遇到 `monotonic`、调度器或跨时区逻辑时，要分清墙上时间和单调时钟
- 时间测试要补边界：月底、跨天、DST、过期前后 1 秒

## 关联阅读

- [datetime](../stdlib/datetime.md)
- [time](../stdlib/time.md)
- [时间与时钟测试专题](../topics/time-and-clock-testing.md)
- [任务调度专题](../topics/task-scheduling.md)

返回 [索引](../README.md)
