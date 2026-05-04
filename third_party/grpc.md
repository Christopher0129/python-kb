# grpcio

`grpcio` 适合服务之间的高性能 RPC 通信，尤其适合内部微服务接口。

## 安装

```bash
pip install grpcio grpcio-tools
```

## 核心概念

| 概念 | 说明 |
| --- | --- |
| `.proto` | 接口与消息定义 |
| stub | 客户端调用代理 |
| servicer | 服务端实现 |

## 适用场景

- 服务间调用
- 严格约束接口结构
- 多语言系统集成

## 关联阅读

- [实时通信专题](../topics/realtime-communication.md)
- [API 开发专题](../topics/api-development.md)

返回 [索引](../README.md)
