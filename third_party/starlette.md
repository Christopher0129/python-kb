# Starlette

`Starlette` 是轻量 ASGI 框架，适合直接构建中间件、路由和基础服务骨架，也常作为 FastAPI 的底层能力来源。

## 安装

```bash
pip install starlette
```

## 基本示例

```python
from starlette.applications import Starlette
from starlette.responses import PlainTextResponse
from starlette.routing import Route


async def homepage(request):
    return PlainTextResponse("ok")


app = Starlette(routes=[Route("/", homepage)])
```

## 常见能力

| 能力 | 说明 |
| --- | --- |
| `Starlette(...)` | 创建 ASGI 应用 |
| `Route(...)` | 定义 HTTP 路由 |
| `Middleware(...)` | 挂载中间件 |
| `lifespan` | 管理启动与关闭生命周期 |

## 使用建议

- 当你需要比 FastAPI 更薄的抽象层时，它很合适
- 很多服务级能力都应该落在中间件和生命周期，而不是散到每个路由
- 如果项目后续会扩到 WebSocket、SSE 或纯 ASGI 中间件，它是很好的基础层

## 关联阅读

- [FastAPI 入门](../frameworks/fastapi.md)
- [FastAPI 进阶专题](../topics/fastapi-advanced.md)
- [API 网关模式专题](../topics/api-gateway-patterns.md)
- [异步资源生命周期专题](../topics/async-resource-lifecycles.md)

返回 [索引](../README.md)
