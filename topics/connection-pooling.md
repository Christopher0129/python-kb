# 连接池专题

这个专题关注数据库、HTTP、消息中间件连接如何复用，以及池大小、超时和阻塞行为如何调优。

## 适用场景

- API 服务需要频繁访问数据库或下游 HTTP
- 任务系统有大量并发 worker
- 压测下出现排队、超时或连接耗尽

## 常见主题

- pool size 与 max overflow
- acquire timeout
- keepalive 与 idle timeout
- 请求并发与连接复用
- 连接泄漏排查

## 设计要点

- 连接池大小应按进程数、worker 数和下游容量一起估算
- 请求并发大于池容量时，要明确是等待、失败还是降级
- 连接池不是越大越好，过大可能压垮下游
- 压测和线上观测都要记录排队时间、超时和重建频率

## 关联阅读

- [httpx](../third_party/httpx.md)
- [asyncpg](../third_party/asyncpg.md)
- [databases](../third_party/databases.md)
- [异步数据库专题](./async-database-access.md)
- [压测专题](./load-testing.md)

返回 [索引](../README.md)
