# 依赖扫描专题

这个专题关注第三方依赖和镜像中的已知漏洞、许可证风险和修复流程。

## 适用场景

- 团队已经使用大量三方库
- 需要把安全扫描接入 CI
- 需要对高危漏洞设定修复时限

## 常见主题

- SBOM 与依赖清单
- 已知漏洞扫描
- 许可证扫描
- 锁文件治理
- 自动修复与人工评审

## 设计要点

- 先固定依赖版本，再谈可重复审计
- 高危漏洞要有升级策略和例外审批机制
- 扫描结果应能区分开发依赖、运行时依赖和传递依赖
- 工具只是发现入口，真正关键的是修复流程和所有权

## 关联阅读

- [pip-audit](../third_party/pip_audit.md)
- [Safety](../third_party/safety.md)
- [Bandit](../third_party/bandit.md)
- [依赖治理专题](./dependency-governance.md)
- [供应链安全专题](./supply-chain-security.md)

返回 [索引](../README.md)
