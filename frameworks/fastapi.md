# FastAPI 入门

`FastAPI` 适合构建现代 JSON API，类型标注、自动文档和异步支持都比较强。

## 安装

```bash
pip install fastapi uvicorn
```

## 最小示例

```python
from fastapi import FastAPI
from pydantic import BaseModel

app = FastAPI()


class UserIn(BaseModel):
    name: str
    age: int


@app.get("/")
def home():
    return {"message": "hello fastapi"}


@app.post("/users")
def create_user(user: UserIn):
    return {"ok": True, "user": user.model_dump()}
```

运行：

```bash
uvicorn app:app --reload
```

## 高频对象

| 对象 / API | 用途 |
| --- | --- |
| `FastAPI()` | 创建应用 |
| `@app.get()` / `@app.post()` | 注册路由 |
| `BaseModel` | 定义请求和响应数据结构 |
| `Query()` / `Path()` | 声明查询参数和路径参数 |
| `Depends()` | 依赖注入 |
| `BackgroundTasks` | 后台任务 |
| `middleware` | 请求中间件 |

## 适用场景

- REST API
- 异步接口服务
- 内部平台服务
- 需要自动生成 OpenAPI 文档的项目

## 使用建议

- 已经大量使用类型标注的项目更容易发挥它的优势
- 简单小工具可以继续用 Flask；接口规模和约束变复杂时再考虑 FastAPI
- 数据校验、响应模型、依赖注入最好尽早规范起来
- 进阶项目要尽早规划中间件、认证、生命周期和健康检查

## 关联阅读

- [Flask 入门](./flask.md)
- [typing 与 dataclasses](../stdlib/typing_dataclasses.md)
- [asyncio](../stdlib/asyncio.md)
- [项目结构专题](../topics/project-structure.md)
- [FastAPI 进阶专题](../topics/fastapi-advanced.md)
- [认证与授权专题](../topics/auth-authorization.md)
- [服务中间件专题](../topics/service-middleware.md)

返回 [索引](../README.md)
