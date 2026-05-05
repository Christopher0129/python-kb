# Kubernetes Ingress 与流量入口专题

这个专题关注 Python Web 服务进入 Kubernetes 后，如何处理入口流量、路径路由、TLS 和北向流量治理。

## 适用场景

- 多个 HTTP / gRPC 服务需要统一入口
- 需要做域名、TLS、路径转发和限流
- 需要处理 WebSocket、长连接或大文件上传

## 常见主题

- Ingress Controller
- TLS 终止
- Path / Host 路由
- Header 透传
- WebSocket 与超时配置

## 设计要点

- 入口层超时、重试和应用层超时要统一，不然会出现诡异断流。
- WebSocket、SSE 和大上传场景要提前验证代理默认配置。
- 真实客户端 IP、trace header 和鉴权头要稳定透传。
- Ingress 适合统一入口治理，但复杂流量切分可能更适合网关或服务网格。

## 关联阅读

- [API 网关模式专题](./api-gateway-patterns.md)
- [Kubernetes 运维专题](./kubernetes-operations.md)
- [Kubernetes Ingress 灰度专题](./kubernetes-ingress-canary.md)
- [服务网格专题](./service-mesh.md)
- [健康检查与指标专题](./health-metrics.md)
- [HTTP/2 与流式响应专题](./http2-and-streaming.md)

返回 [索引](../README.md)
