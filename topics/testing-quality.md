# 测试与质量专题

这个专题关注 Python 项目如何从“能运行”走到“可验证、可回归、可维护”。

## 先学哪些模块和库

| 模块 / 库 | 作用 | 推荐程度 |
| --- | --- | --- |
| `pytest` | 主测试框架 | 必学 |
| `unittest` | 标准库测试基础 | 高频 |
| `unittest.mock` | 替换外部依赖 | 高频 |
| `doctest` | 文档示例校验 | 常用 |
| `logging` | 记录测试排查信息 | 常用 |

## 一个基本测试分层

| 层级 | 目标 |
| --- | --- |
| 单元测试 | 校验单个函数或类 |
| 集成测试 | 校验模块之间协作 |
| 接口测试 | 校验外部 HTTP 行为 |
| 回归测试 | 复现并防止历史 bug 再次出现 |

## 常见测试策略

### 1. 纯函数优先直接测

```python
def add(a, b):
    return a + b


def test_add():
    assert add(1, 2) == 3
```

### 2. 外部依赖用 mock 隔离

```python
from unittest.mock import Mock, patch


def test_fetch():
    fake_resp = Mock()
    fake_resp.json.return_value = {"ok": True}

    with patch("requests.get", return_value=fake_resp):
        assert fake_resp.json()["ok"] is True
```

### 3. 参数化覆盖边界

```python
import pytest


@pytest.mark.parametrize("value,expected", [
    (0, False),
    (1, True),
])
def test_flag(value, expected):
    assert bool(value) is expected
```

## 质量改进建议

- 出现 bug 后，先补复现测试再修
- 优先覆盖核心业务路径和边界条件
- 把网络、文件、数据库等外部依赖隔离到边界层

## 关联阅读

- [pytest](../third_party/pytest.md)
- [coverage.py](../third_party/coverage.md)
- [pytest-cov](../third_party/pytest_cov.md)
- [unittest](../stdlib/unittest.md)
- [unittest.mock](../stdlib/unittest_mock.md)
- [接口测试专题](./api-testing.md)
- [测试金字塔与切片专题](./test-pyramids-and-slicing.md)
- [API Fuzzing 专题](./api-fuzzing.md)
- [性能与调试专题](./performance-debugging.md)

返回 [索引](../README.md)
