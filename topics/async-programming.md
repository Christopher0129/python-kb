# 异步编程专题

这个专题把 Python 异步开发常见链路串起来：协程、任务调度、异步 HTTP、超时控制和并发边界。

## 先学哪些模块和库

| 模块 / 库 | 作用 | 推荐程度 |
| --- | --- | --- |
| `asyncio` | 异步运行时核心 | 必学 |
| `httpx` | 异步 HTTP 客户端 | 高频 |
| `aiohttp` | 高并发 HTTP 客户端 | 高频 |
| `asyncio.Queue` | 异步任务队列 | 常用 |
| `asyncio.wait_for()` | 超时控制 | 高频 |

## 核心概念

| 概念 | 说明 |
| --- | --- |
| 协程 | `async def` 定义的可挂起函数 |
| 任务 | 交给事件循环调度的协程 |
| 事件循环 | 负责驱动协程执行 |

## 基础示例

```python
import asyncio


async def work(name):
    await asyncio.sleep(1)
    return f"done: {name}"


async def main():
    tasks = [asyncio.create_task(work("a")), asyncio.create_task(work("b"))]
    print(await asyncio.gather(*tasks))


asyncio.run(main())
```

## 常见工作流

1. 定义异步函数
2. 创建任务
3. 用 `gather()` 或 `wait()` 并发等待
4. 用 `wait_for()` 加超时

## 实战建议

- 异步函数里不要直接调用阻塞式 I/O
- 控制并发量，不要无限制创建任务
- 网络请求要带超时和异常处理

## 关联阅读

- [asyncio](../stdlib/asyncio.md)
- [httpx](../third_party/httpx.md)
- [aiohttp](../third_party/aiohttp.md)
- [AnyIO](../third_party/anyio.md)
- [aiofiles](../third_party/aiofiles.md)
- [网络编程专题](./network-programming.md)
- [Web 抓取专题](./web-scraping.md)
- [异步资源生命周期专题](./async-resource-lifecycles.md)
- [背压与流控专题](./backpressure-and-flow-control.md)
- [连接池专题](./connection-pooling.md)

返回 [索引](../README.md)
