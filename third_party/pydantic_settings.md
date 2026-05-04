# pydantic-settings

`pydantic-settings` 适合把环境变量和配置文件映射成结构化配置对象，常用于 FastAPI 和服务化项目。

## 安装

```bash
pip install pydantic-settings
```

## 基本示例

```python
from pydantic_settings import BaseSettings


class Settings(BaseSettings):
    app_name: str = "demo"
    debug: bool = False
    db_url: str


settings = Settings()
print(settings.app_name)
```

## 适用场景

- 服务配置统一收口
- 环境变量较多的项目
- 避免散落的 `os.environ.get(...)`

## 关联阅读

- [pydantic](./pydantic.md)
- [配置管理专题](../topics/config-management.md)

返回 [索引](../README.md)
