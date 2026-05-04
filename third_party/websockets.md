# websockets

`websockets` 适合实现 WebSocket 实时通信，如聊天室、实时通知和流式数据推送。

## 安装

```bash
pip install websockets
```

## 基本示例

```python
import asyncio
import websockets


async def echo(ws):
    async for message in ws:
        await ws.send(message)


async def main():
    async with websockets.serve(echo, "127.0.0.1", 8765):
        await asyncio.Future()


asyncio.run(main())
```

## 关联阅读

- [asyncio](../stdlib/asyncio.md)
- [实时通信专题](../topics/realtime-communication.md)
- [网络编程专题](../topics/network-programming.md)

返回 [索引](../README.md)
