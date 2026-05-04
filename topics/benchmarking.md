# 性能基准专题

这个专题关注如何更稳定地比较性能，而不是只凭一次手工运行结果判断。

## 常见手段

| 工具 | 作用 |
| --- | --- |
| `time.perf_counter()` | 粗粒度计时 |
| `cProfile` | 找热点函数 |
| `pytest-benchmark` | 持续比较性能 |

## 关联阅读

- [time](../stdlib/time.md)
- [cProfile](../stdlib/cprofile.md)
- [pytest-benchmark](../third_party/pytest_benchmark.md)
- [性能与调试专题](./performance-debugging.md)

返回 [索引](../README.md)
