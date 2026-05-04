# kafka-python

`kafka-python` 适合在 Python 中连接 Kafka，处理消息生产和消费。

## 安装

```bash
pip install kafka-python
```

## 基本示例

```python
from kafka import KafkaProducer

producer = KafkaProducer(bootstrap_servers="localhost:9092")
producer.send("demo-topic", b"hello")
producer.flush()
```

## 适用场景

- 日志流和事件流
- 异步消息解耦
- 多服务之间松耦合通信

## 关联阅读

- [缓存与队列专题](../topics/cache-queues.md)
- [消息系统专题](../topics/message-systems.md)

返回 [索引](../README.md)
