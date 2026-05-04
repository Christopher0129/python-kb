# 接口测试专题

这个专题把 Python 里常见的接口测试链路串起来：发请求、断言响应、构造测试数据、临时文件、异常校验和批量化测试。

## 先学哪些模块和库

| 模块 / 库 | 作用 | 推荐程度 |
| --- | --- | --- |
| `requests` | 发 HTTP 请求 | 必学 |
| `pytest` | 组织测试、断言、夹具、参数化 | 必学 |
| `json` | 构造和校验 JSON 数据 | 高频 |
| `tempfile` | 临时测试文件和目录 | 常用 |
| `unittest.mock` / mock 思路 | 替换外部依赖 | 进阶 |
| `logging` | 输出接口测试日志 | 常用 |

## 典型工作流

### 1. 发送请求并断言状态码

推荐组合：`requests` + `pytest`

```python
import requests

def test_health():
    resp = requests.get("https://httpbin.org/status/200", timeout=10)
    assert resp.status_code == 200
```

### 2. 断言 JSON 响应结构

推荐组合：`resp.json()`

```python
import requests

def test_get_user():
    resp = requests.get("https://httpbin.org/json", timeout=10)
    resp.raise_for_status()
    data = resp.json()
    assert isinstance(data, dict)
```

### 3. 参数化多个测试场景

推荐组合：`pytest.mark.parametrize`

```python
import pytest

@pytest.mark.parametrize("status", [200, 201, 204])
def test_status(status):
    assert status in {200, 201, 204}
```

### 4. 用夹具复用会话或测试数据

推荐组合：`@pytest.fixture`

```python
import pytest
import requests

@pytest.fixture
def session():
    s = requests.Session()
    yield s
    s.close()
```

### 5. 临时文件和上传测试

推荐组合：`tempfile`

```python
import tempfile
from pathlib import Path

def test_temp_file():
    with tempfile.TemporaryDirectory() as d:
        p = Path(d) / "demo.json"
        p.write_text('{"ok": true}', encoding="utf-8")
        assert p.exists()
```

## 常见断言点

| 类型 | 断言内容 |
| --- | --- |
| 状态码 | `200`、`201`、`400`、`401`、`404`、`500` |
| 响应头 | `Content-Type`、鉴权头、缓存头 |
| JSON 字段 | 是否存在、字段类型、字段值 |
| 响应时间 | 是否超出预期 |
| 错误响应 | 错误码、错误信息、异常结构 |

## 常见任务到模块映射

| 任务 | 模块组合 |
| --- | --- |
| 调接口并校验响应 | `requests` + `pytest` |
| 复用登录态 | `requests.Session()` + `fixture` |
| 批量跑参数场景 | `pytest.mark.parametrize` |
| 临时上传文件测试 | `tempfile` + `pathlib` |
| 打日志辅助排查 | `logging` |

## 实战建议

- 所有 HTTP 请求都带 `timeout`
- 断言不要只看状态码，最好同时校验 JSON 字段
- 需要复用请求头、Token、Session 时，优先用 `fixture`
- 外部服务不稳定时，要区分“接口逻辑失败”和“网络环境失败”

## 关联阅读

- [requests](../third_party/requests.md)
- [pytest](../third_party/pytest.md)
- [tempfile](../stdlib/tempfile.md)
- [json](../stdlib/json.md)
- [logging](../stdlib/logging.md)
- [异常类型合集](../basics/exception-types.md)

返回 [索引](../README.md)
