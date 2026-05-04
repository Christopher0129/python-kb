# 代码质量专题

这个专题关注如何让 Python 项目保持可读、可维护、可重构。

## 关键工具

| 工具 | 作用 |
| --- | --- |
| `ruff` | lint 与格式化 |
| `mypy` | 类型检查 |
| `pre-commit` | 提交前自动检查 |
| `pytest` | 测试保障 |

## 质量改进思路

1. 统一风格
2. 让类型边界清晰
3. 用测试保护核心逻辑
4. 把检查接进提交和 CI

## 关联阅读

- [ruff](../third_party/ruff.md)
- [mypy](../third_party/mypy.md)
- [pre-commit](../third_party/pre_commit.md)
- [测试与质量专题](./testing-quality.md)

返回 [索引](../README.md)
