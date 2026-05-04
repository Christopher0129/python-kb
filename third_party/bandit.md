# Bandit

`Bandit` 适合做 Python 代码静态安全扫描，快速发现命令注入、不安全反序列化、弱随机等常见问题。

## 安装

```bash
pip install bandit
```

## 基本示例

```bash
bandit -r src
```

## 常见能力

| 能力 | 说明 |
| --- | --- |
| `bandit -r src` | 递归扫描目录 |
| `-f json -o bandit.json` | 导出机器可读结果 |
| `-x tests,docs` | 排除目录 |
| `-b baseline.json` | 使用 baseline 压住已知历史问题 |

## 使用建议

- 先把结果接入 CI，再逐步治理历史告警
- 对误报要有明确跳过规则，不要靠人工长期忽略
- 它更适合发现通用编码风险，不替代威胁建模和依赖漏洞扫描

## 关联阅读

- [安全基础专题](../topics/security-basics.md)
- [依赖扫描专题](../topics/dependency-scanning.md)
- [供应链安全专题](../topics/supply-chain-security.md)
- [subprocess](../stdlib/subprocess.md)

返回 [索引](../README.md)
