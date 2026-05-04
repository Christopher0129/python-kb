# CI/CD 专题

这个专题关注 Python 项目如何把测试、lint、类型检查和发布流程自动化。

## 常见流水线步骤

1. 安装依赖
2. 运行 `ruff`
3. 运行 `mypy`
4. 运行 `pytest`
5. 构建或发布

## 典型价值

- 降低回归风险
- 保证多人协作的一致性
- 让发布流程可重复

## 关联阅读

- [代码质量专题](./code-quality.md)
- [ruff](../third_party/ruff.md)
- [mypy](../third_party/mypy.md)
- [pytest](../third_party/pytest.md)
- [打包与发布专题](./packaging-release.md)

返回 [索引](../README.md)
