# Optuna

`Optuna` 适合做超参数搜索、剪枝和实验管理，是 Python 里很常用的超参优化框架。

## 安装

```bash
pip install optuna
```

## 基本示例

```python
import optuna


def objective(trial):
    x = trial.suggest_float("x", 0, 10)
    return x ** 2


study = optuna.create_study()
study.optimize(objective, n_trials=20)
```

## 常见能力

| 能力 | 说明 |
| --- | --- |
| `optuna.create_study()` | 创建搜索实验 |
| `trial.suggest_float(...)` | 采样连续参数 |
| `trial.suggest_int(...)` | 采样整数参数 |
| `trial.suggest_categorical(...)` | 采样离散候选 |
| `study.optimize(...)` | 执行多轮搜索 |

## 使用建议

- 先定义清楚目标指标、搜索空间和停止条件
- 训练成本高时应启用剪枝、并行和持久化 storage
- 结果要和实验跟踪系统关联，而不是只看 best trial

## 关联阅读

- [scikit-learn](./scikit_learn.md)
- [模型评估专题](../topics/ml-evaluation.md)
- [实验跟踪专题](../topics/experiment-tracking.md)
- [传统机器学习专题](../topics/classical-ml.md)

返回 [索引](../README.md)
