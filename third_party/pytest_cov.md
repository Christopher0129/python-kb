# pytest-cov

`pytest-cov` 是 `pytest` 的覆盖率插件，适合把覆盖率统计直接并入日常测试命令。

## 安装

```bash
pip install pytest-cov
```

## 基本示例

```bash
pytest --cov=app --cov-report=term-missing tests/
```

## 常见能力

| 能力 | 说明 |
| --- | --- |
| `--cov=包名或目录` | 指定要统计覆盖率的目标代码 |
| `--cov-report=term-missing` | 在终端显示未覆盖行 |
| `--cov-report=html` | 生成 HTML 报告 |
| `--cov-append` | 追加到已有覆盖率数据 |
| `--cov-context=test` | 按测试名记录覆盖上下文 |

## 使用建议

- 项目日常运行 `pytest` 时更适合直接用它
- 多环境、多进程测试时比手写 `coverage run` 更省事
- 如果还要配 `xdist`，要一起看覆盖率合并和 worker 安装一致性

## 关联阅读

- [coverage.py](./coverage.md)
- [pytest](./pytest.md)
- [pytest-xdist](./pytest_xdist.md)
- [测试矩阵专题](../topics/test-matrix.md)

返回 [索引](../README.md)
