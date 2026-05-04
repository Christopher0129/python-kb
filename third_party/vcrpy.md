# VCR.py

`VCR.py` 适合把真实 HTTP 响应录制成 cassette，在测试里做可回放的接口交互。

## 安装

```bash
pip install vcrpy
```

## 基本示例

```python
import requests
import vcr

with vcr.use_cassette("fixtures/httpbin.yaml"):
    response = requests.get("https://httpbin.org/get", timeout=5)
    assert response.status_code == 200
```

## 常见能力

| 能力 | 说明 |
| --- | --- |
| `vcr.use_cassette(...)` | 录制或回放 HTTP 交互 |
| `record_mode="once"` | 已有 cassette 时拒绝新请求漂移 |
| `filter_headers=[...]` | 过滤敏感请求头 |
| `filter_query_parameters=[...]` | 过滤敏感查询参数 |

## 使用建议

- 适合对外部 API 做稳定回归，不适合替代集成环境验证
- cassette 文件应纳入代码审查，避免误提交敏感信息
- 接口变化快时要搭配契约测试，不要只信历史录制结果

## 关联阅读

- [requests](./requests.md)
- [httpx](./httpx.md)
- [HTTP Mock 与录制专题](../topics/http-mocking-recording.md)
- [接口测试专题](../topics/api-testing.md)

返回 [索引](../README.md)
