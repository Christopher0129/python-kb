# pip-audit

`pip-audit` 适合扫描当前环境、项目路径或 `requirements` 文件里的已知依赖漏洞。

## 安装

```bash
pip install pip-audit
```

## 基本示例

```bash
pip-audit -r requirements.txt
pip-audit .
```

## 常见能力

| 能力 | 说明 |
| --- | --- |
| `pip-audit -r requirements.txt` | 审计指定依赖文件 |
| `pip-audit .` | 审计当前项目 |
| `pip-audit --locked .` | 审计项目里的锁文件 |
| `pip-audit --format json` | 导出 JSON 结果 |
| `pip-audit --fix` | 自动升级有漏洞的依赖 |

## 使用建议

- 适合放进 CI 和本地提交流程
- 自动修复前要先确认升级窗口与兼容风险
- 对生产项目更重要的是固定版本、锁文件和修复 SLA

## 关联阅读

- [依赖扫描专题](../topics/dependency-scanning.md)
- [依赖治理专题](../topics/dependency-governance.md)
- [供应链安全专题](../topics/supply-chain-security.md)
- [pre-commit](./pre_commit.md)

返回 [索引](../README.md)
