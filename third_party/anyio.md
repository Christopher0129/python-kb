# AnyIO

`AnyIO` 适合写结构化并发代码，并在 `asyncio` / `Trio` 风格运行时之间保持更一致的抽象。

## 安装

```bash
pip install anyio
```

## 基本示例

```python
from anyio import create_task_group, fail_after, run, sleep


async def worker(name):
    with fail_after(2):
        await sleep(1)
        print(name)


async def main():
    async with create_task_group() as tg:
        tg.start_soon(worker, "a")
        tg.start_soon(worker, "b")


run(main)
```

## 常见能力

| 能力 | 说明 |
| --- | --- |
| `create_task_group()` | 结构化并发任务组 |
| `fail_after(...)` | 超时后抛异常 |
| `move_on_after(...)` | 超时后提前退出作用域 |
| `run(...)` | 运行异步入口 |

## 使用建议

- 它更强调“任务作用域”和“整体收束”，适合服务启动、并发子任务和清理逻辑
- 超时与取消语义要和业务重试策略一起设计
- 用它时要把资源释放放进显式作用域里，而不是依赖隐式回收

## 关联阅读

- [asyncio](../stdlib/asyncio.md)
- [异步编程专题](../topics/async-programming.md)
- [异步资源生命周期专题](../topics/async-resource-lifecycles.md)
- [背压与流控专题](../topics/backpressure-and-flow-control.md)

返回 [索引](../README.md)
