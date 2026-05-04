# 异步资源生命周期专题

这个专题关注异步服务里的资源如何初始化、复用、关闭，以及取消时怎么保证清理完整。

## 适用场景

- HTTP 客户端、数据库连接池、消息消费者
- 服务启动时需要预热资源
- 应用关闭时需要优雅退出

## 常见主题

- startup / shutdown 钩子
- 连接池和客户端单例
- 取消传播与清理
- 后台任务生命周期
- 资源泄漏与悬挂任务

## 设计要点

- 资源应该显式创建、显式关闭，而不是靠 GC
- 生命周期尽量挂到应用级作用域，而不是每次请求重复创建
- 任务取消时要保证 finally / context manager 真正执行
- 启动失败要能整体回滚，避免半初始化状态

## 关联阅读

- [asyncio](../stdlib/asyncio.md)
- [AnyIO](../third_party/anyio.md)
- [aiofiles](../third_party/aiofiles.md)
- [Starlette](../third_party/starlette.md)
- [FastAPI 生命周期与后台任务专题](./fastapi-lifespan-background.md)

返回 [索引](../README.md)
