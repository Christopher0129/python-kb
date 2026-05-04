# aiofiles

`aiofiles` 适合在 `asyncio` 程序里执行本地文件 I/O，减少阻塞事件循环的风险。

## 安装

```bash
pip install aiofiles
```

## 基本示例

```python
import aiofiles


async def read_text(path):
    async with aiofiles.open(path, "r", encoding="utf-8") as f:
        return await f.read()
```

## 常见能力

| 能力 | 说明 |
| --- | --- |
| `aiofiles.open(...)` | 异步风格打开文件 |
| `await f.read()` / `await f.write()` | 异步读写文件 |
| `aiofiles.os` | 提供部分文件系统操作的异步包装 |
| `aiofiles.tempfile` | 提供异步临时文件接口 |

## 使用建议

- 适合本地磁盘文件，不等于网络文件系统天然高吞吐
- 大文件处理要配合分块读取，而不是一次性全读
- 如果只是少量文件 I/O，也可以评估是否直接放线程池更简单

## 关联阅读

- [asyncio](../stdlib/asyncio.md)
- [文件处理专题](../topics/file-processing.md)
- [异步编程专题](../topics/async-programming.md)
- [异步资源生命周期专题](../topics/async-resource-lifecycles.md)

返回 [索引](../README.md)
