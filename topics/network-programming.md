# 网络编程专题

这个专题把基础网络开发常见模块串起来：URL 处理、发请求、本地 HTTP 服务、Socket 通信、并发下载和异常处理。

## 先学哪些模块

| 模块 | 作用 | 推荐程度 |
| --- | --- | --- |
| `urllib` | 标准库 URL 处理和基础 HTTP | 必学 |
| `requests` | 更易用的 HTTP 客户端 | 高频 |
| `http.server` | 临时静态服务 | 高频 |
| `socket` | TCP/UDP 底层通信 | 高频 |
| `threading` / `queue` | 简单并发网络任务 | 常用 |
| `asyncio` | 高并发 I/O | 进阶 |
| `concurrent.futures` | 线程池 / 进程池并发 | 常用 |

## 典型工作流

### 1. 构造 URL 和查询参数

推荐组合：`urllib.parse`

```python
from urllib.parse import urlencode

query = urlencode({"q": "python", "page": 1})
url = f"https://example.com/search?{query}"
print(url)
```

### 2. 发送简单 HTTP 请求

推荐组合：`urllib.request` 或 `requests`

```python
from urllib.request import urlopen

with urlopen("https://example.com") as resp:
    print(resp.status)
```

```python
import requests

resp = requests.get("https://httpbin.org/get", timeout=10)
resp.raise_for_status()
print(resp.json())
```

### 3. 临时起本地文件服务

推荐组合：`http.server`

```bash
python -m http.server 8000
```

### 4. 写一个最小 TCP 通信程序

推荐组合：`socket`

```python
import socket

sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
sock.connect(("127.0.0.1", 9000))
sock.sendall(b"hello")
print(sock.recv(1024))
sock.close()
```

### 5. 做并发下载或并发请求

推荐组合：`ThreadPoolExecutor` + `requests`

```python
from concurrent.futures import ThreadPoolExecutor
import requests

def fetch(url):
    return requests.get(url, timeout=10).status_code

with ThreadPoolExecutor(max_workers=5) as pool:
    for status in pool.map(fetch, ["https://example.com"] * 3):
        print(status)
```

## 常见任务到模块映射

| 任务 | 模块组合 |
| --- | --- |
| 拼接带参数链接 | `urllib.parse` |
| 调接口和下载文件 | `requests` / `urllib.request` |
| 本地共享目录 | `http.server` |
| TCP 客户端 / 服务端 | `socket` |
| 批量并发请求 | `concurrent.futures` + `requests` |
| 高并发异步抓取 | `asyncio` |

## 常见异常要点

- 超时：`TimeoutError` 或第三方库的超时异常
- 连接失败：`ConnectionError`
- 连接被拒绝：`ConnectionRefusedError`
- 连接被重置：`ConnectionResetError`
- URL 编码问题：优先用 `quote()`、`urlencode()`

## 实战建议

- 简单接口优先 `requests`，基础 URL 编解码用 `urllib.parse`
- 网络代码始终带超时
- 批量请求时要控制并发，不要直接无限开线程
- 底层通信问题再回到 `socket` 排查

## 关联阅读

- [urllib](../stdlib/urllib.md)
- [http.server](../stdlib/http_server.md)
- [socket](../stdlib/socket.md)
- [threading](../stdlib/threading.md)
- [queue](../stdlib/queue.md)
- [concurrent.futures](../stdlib/concurrent_futures.md)
- [requests](../third_party/requests.md)
- [异常类型合集](../basics/exception-types.md)

返回 [索引](../README.md)
