# 数据可视化专题

这个专题把数据分析和图表输出常见链路串起来：读取数据、清洗字段、汇总统计、画图展示、导出图片或 Excel 报表。

## 先学哪些模块

| 模块 | 作用 | 推荐程度 |
| --- | --- | --- |
| `pandas` | 表格数据读取、清洗、聚合 | 必学 |
| `matplotlib` | 折线图、柱状图、散点图等基础可视化 | 必学 |
| `numpy` | 数值计算、数组处理 | 常用 |
| `openpyxl` | Excel 读写、工作表和样式处理 | 高频 |

## 典型工作流

### 1. 读取 CSV 或 Excel

推荐组合：`pandas` / `openpyxl`

```python
import pandas as pd

df = pd.read_csv("sales.csv")
print(df.head())
```

```python
from openpyxl import load_workbook

wb = load_workbook("report.xlsx")
ws = wb.active
print(ws["A1"].value)
```

### 2. 清洗和筛选数据

推荐组合：`pandas`

```python
import pandas as pd

df = pd.read_csv("sales.csv")
df = df.dropna(subset=["city", "amount"])
df["amount"] = df["amount"].astype(float)
result = df.loc[df["amount"] > 100]
print(result.head())
```

### 3. 分组统计

推荐组合：`groupby()`

```python
summary = df.groupby("city")["amount"].sum().sort_values(ascending=False)
print(summary)
```

### 4. 画图展示

推荐组合：`pandas` + `matplotlib`

```python
import matplotlib.pyplot as plt

summary.plot(kind="bar", title="City Sales")
plt.xlabel("city")
plt.ylabel("amount")
plt.tight_layout()
plt.show()
```

### 5. 导出结果

推荐组合：`to_csv()` / `to_excel()` / `savefig()`

```python
summary.to_csv("summary.csv")
plt.savefig("summary.png")
```

## 常见任务到模块映射

| 任务 | 模块组合 |
| --- | --- |
| 读取 Excel 名单表 | `openpyxl` / `pandas.read_excel()` |
| 清洗 CSV 后做统计 | `pandas` |
| 生成趋势图和柱状图 | `matplotlib` |
| 导出分析结果到 Excel | `pandas` + `openpyxl` |
| 大量数值运算 | `numpy` |

## 常见图表选择

| 图表 | 适用场景 |
| --- | --- |
| 折线图 | 时间趋势 |
| 柱状图 | 分类对比 |
| 散点图 | 相关性分析 |
| 直方图 | 分布情况 |

## 实战建议

- 先用 `pandas` 把数据整理干净，再考虑画图
- 图表导出通常优先 `savefig()`，适合做周报、月报
- Excel 重格式化、单元格样式细调时再用 `openpyxl`
- 数据量很大时，先关注字段类型和内存占用

## 关联阅读

- [pandas](../third_party/pandas.md)
- [matplotlib](../third_party/matplotlib.md)
- [openpyxl](../third_party/openpyxl.md)
- [numpy](../third_party/numpy.md)

返回 [索引](../README.md)
