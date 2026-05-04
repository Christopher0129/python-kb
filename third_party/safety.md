# Safety

`Safety` 适合做 Python 依赖安全扫描和许可证扫描，更偏向供应链治理流程。

## 安装

```bash
pip install safety
```

## 基本示例

```bash
safety scan
safety license
```

## 常见能力

| 能力 | 说明 |
| --- | --- |
| `safety scan` | 扫描当前项目里的依赖风险 |
| `safety system-scan` | 扫描本机 Python 环境 |
| `safety license` | 审计依赖许可证 |
| `safety auth login` | 登录后使用完整扫描能力 |

## 使用建议

- 如果团队不希望引入登录流程，可优先用 `pip-audit` 做基础漏洞扫描
- 更适合和组织级安全治理、许可证治理、审计报表一起使用
- 不要只看“有无漏洞”，还要看暴露面、修复窗口和补丁可行性

## 关联阅读

- [pip-audit](./pip_audit.md)
- [依赖扫描专题](../topics/dependency-scanning.md)
- [隐私治理专题](../topics/privacy-governance.md)
- [供应链安全专题](../topics/supply-chain-security.md)

返回 [索引](../README.md)
