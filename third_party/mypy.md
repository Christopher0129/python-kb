# mypy

`mypy` 是 Python 常用静态类型检查工具，适合在运行前发现类型不匹配、空值风险和接口误用。

## 安装

```bash
pip install mypy
```

## 基本用法

```bash
mypy app
```

## 示例

```python
def add(a: int, b: int) -> int:
    return a + b


result = add("1", 2)
```

`mypy` 会指出参数类型不匹配。

## 适用场景

- 中大型项目
- FastAPI / 数据模型较多的项目
- 想提前发现重构风险的代码库

## 关联阅读

- [typing 与 dataclasses](../stdlib/typing_dataclasses.md)
- [pydantic](./pydantic.md)
- [代码质量专题](../topics/code-quality.md)

返回 [索引](../README.md)
