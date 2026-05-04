# coverage.py

`coverage.py` 适合统计测试覆盖率，帮助团队看到哪些代码路径被执行过、哪些分支还没有覆盖到。

## 安装

```bash
pip install coverage
```

## 基本示例

```bash
coverage run -m pytest
coverage report
coverage html
```

## 常见能力

| 能力 | 说明 |
| --- | --- |
| `coverage run -m pytest` | 执行测试并采集覆盖率数据 |
| `coverage report` | 在终端输出覆盖率摘要 |
| `coverage html` | 生成可浏览的 HTML 报告 |
| `coverage xml` | 生成 CI 常用的 XML 报告 |
| `--branch` | 统计分支覆盖率，而不只是语句覆盖率 |

## 使用建议

- 用 `--branch` 看条件分支是否真的被验证
- 把忽略规则和 `fail-under` 放到配置文件里，避免命令行散落
- 覆盖率适合发现盲区，不适合替代测试质量判断

## 关联阅读

- [pytest-cov](./pytest_cov.md)
- [测试与质量专题](../topics/testing-quality.md)
- [测试进阶专题](../topics/testing-advanced.md)
- [CI/CD 专题](../topics/ci-cd.md)

返回 [索引](../README.md)
