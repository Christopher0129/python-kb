# APScheduler

`APScheduler` 适合在 Python 进程内做定时任务调度。

## 安装

```bash
pip install apscheduler
```

## 基本示例

```python
from apscheduler.schedulers.blocking import BlockingScheduler


def job():
    print("run")


scheduler = BlockingScheduler()
scheduler.add_job(job, "interval", minutes=5)
scheduler.start()
```

## 适用场景

- 定时清理任务
- 周期同步任务
- 简单报表任务

## 关联阅读

- [celery](./celery.md)
- [任务调度专题](../topics/task-scheduling.md)
- [部署与运维专题](../topics/deployment-operations.md)

返回 [索引](../README.md)
