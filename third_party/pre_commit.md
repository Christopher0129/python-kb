# pre-commit

`pre-commit` 适合在提交前自动执行格式化、lint、类型检查等任务，减少低级问题进入仓库。

## 安装

```bash
pip install pre-commit
```

## 基本流程

1. 编写 `.pre-commit-config.yaml`
2. 运行 `pre-commit install`
3. 提交前自动执行检查

## 适合搭配的工具

- `ruff`
- `mypy`
- 格式化工具

## 关联阅读

- [ruff](./ruff.md)
- [mypy](./mypy.md)
- [代码质量专题](../topics/code-quality.md)

返回 [索引](../README.md)
