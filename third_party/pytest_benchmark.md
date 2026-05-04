# pytest-benchmark

`pytest-benchmark` 适合在测试体系内做基准测试和性能回归比较。

## 安装

```bash
pip install pytest-benchmark
```

## 基本示例

```python
def work():
    return sum(range(1000))


def test_work(benchmark):
    result = benchmark(work)
    assert result > 0
```

## 适用场景

- 比较重构前后性能
- 监控热点函数退化
- 把性能检查纳入测试流程

## 关联阅读

- [pytest](./pytest.md)
- [cProfile](../stdlib/cprofile.md)
- [性能与调试专题](../topics/performance-debugging.md)
- [性能基准专题](../topics/benchmarking.md)

返回 [索引](../README.md)
