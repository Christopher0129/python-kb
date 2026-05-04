# 文件处理专题

这个专题把 Python 里最常见的文件处理链路串起来：找文件、读写内容、复制移动、临时文件、中间缓存、校验与导出。

## 先学哪些模块

| 模块 | 作用 | 推荐程度 |
| --- | --- | --- |
| `pathlib` | 路径拼接、遍历、读写文件 | 必学 |
| `glob` | 批量按模式查文件 | 高频 |
| `os` | 目录遍历、环境变量、底层操作 | 高频 |
| `shutil` | 复制、移动、归档 | 高频 |
| `tempfile` | 临时文件、临时目录 | 高频 |
| `json` / `csv` / `pickle` | 数据落盘格式 | 高频 |
| `hashlib` | 文件校验和去重 | 常用 |

## 典型工作流

### 1. 批量扫描文件

推荐组合：`pathlib` + `glob`

```python
from pathlib import Path

root = Path("data")
for file in root.rglob("*.csv"):
    print(file)
```

### 2. 读取、转换、输出

推荐组合：`Path.read_text()` + `json` / `csv`

```python
import json
from pathlib import Path

src = Path("config.json")
data = json.loads(src.read_text(encoding="utf-8"))
print(data)
```

### 3. 批量复制和归档

推荐组合：`shutil.copytree()` + `make_archive()`

```python
import shutil

shutil.copytree("project", "project_backup", dirs_exist_ok=True)
shutil.make_archive("project_backup", "zip", "project_backup")
```

### 4. 临时中转和安全写入

推荐组合：`tempfile` + `pathlib`

```python
import tempfile
from pathlib import Path

with tempfile.TemporaryDirectory() as temp_dir:
    temp_file = Path(temp_dir) / "result.txt"
    temp_file.write_text("ok", encoding="utf-8")
```

### 5. 文件校验和去重

推荐组合：`hashlib` + 分块读取

```python
import hashlib

hasher = hashlib.sha256()
with open("big.iso", "rb") as f:
    for chunk in iter(lambda: f.read(8192), b""):
        hasher.update(chunk)

print(hasher.hexdigest())
```

## 常见任务到模块映射

| 任务 | 模块组合 |
| --- | --- |
| 批量重命名图片 | `pathlib` + `glob` |
| 清洗 CSV 再导出 JSON | `csv` + `json` |
| 目录备份 | `shutil` + `pathlib` |
| 临时下载后再处理 | `tempfile` + `urllib` / `requests` |
| 缓存 Python 对象 | `pickle` |
| 文件完整性校验 | `hashlib` |

## 实战建议

- 新代码优先用 `pathlib`，只在需要底层系统能力时再补 `os`
- 公开交换数据优先 `json` / `csv`，只在本地缓存复杂对象时用 `pickle`
- 大文件处理不要一次性读入内存，优先分块
- 删除、移动、覆盖文件前先确认目标路径

## 关联阅读

- [pathlib](../stdlib/pathlib.md)
- [glob](../stdlib/glob.md)
- [tempfile](../stdlib/tempfile.md)
- [shutil](../stdlib/shutil.md)
- [pickle](../stdlib/pickle.md)
- [hashlib](../stdlib/hashlib.md)

返回 [索引](../README.md)
