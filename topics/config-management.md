# 配置管理专题

这个专题把 Python 项目里的配置管理串起来：配置文件、环境变量、密钥边界和运行环境隔离。

## 常见配置来源

| 来源 | 适用场景 |
| --- | --- |
| 环境变量 | 密钥、部署环境差异 |
| `json` | 简单结构化配置 |
| `ini` | 旧项目或运维配置 |
| `toml` | 现代 Python 项目元数据和配置 |

## 推荐原则

- 密钥不要写死在代码里
- 配置读取集中到一处
- 区分默认值、开发环境、生产环境
- 普通配置和敏感配置分层管理

## 常见工具

- `os.environ`
- `configparser`
- `tomllib`
- `pydantic`
- `dynaconf`
- `Vault`

## 关联阅读

- [os](../stdlib/os.md)
- [configparser 与 tomllib](../stdlib/configparser_tomllib.md)
- [json](../stdlib/json.md)
- [pydantic](../third_party/pydantic.md)
- [pydantic-settings](../third_party/pydantic_settings.md)
- [dynaconf](../third_party/dynaconf.md)
- [密钥管理专题](./secrets-management.md)
- [项目结构专题](./project-structure.md)
- [运行时配置专题](./runtime-configuration.md)
- [配置结构校验专题](./config-schema-validation.md)
- [配置变更治理专题](./config-change-governance.md)
- [配置漂移检测专题](./config-drift-detection.md)
- [隐私治理专题](./privacy-governance.md)

返回 [索引](../README.md)
