# Python 知识库索引

这套知识库面向日常 Python 开发，按 `内置函数`、`标准库`、`第三方库`、`专题`、`实战案例` 组织，优先覆盖高频模块和常见工程场景。

## 快速入口

- [函数速查索引](./函数索引.md)
- [常用内置函数](./builtins/common-builtins.md)
- [标准库总览](#标准库)
- [专题学习](#专题)
- [实战案例](#实战案例)

## 标准库

### 文本、字符串、数据格式

- [string：字符串常量与模板](./stdlib/string.md)
- [re：正则表达式](./stdlib/re.md)
- [json：JSON 编解码](./stdlib/json.md)
- [csv：CSV 表格读写](./stdlib/csv.md)
- [pickle：对象序列化](./stdlib/pickle.md)
- [json 与 csv 组合速览](./stdlib/json_csv.md)
- [datetime：时间日期处理](./stdlib/datetime.md)
- [time：时间戳、休眠、性能计时](./stdlib/time.md)

### 数学与随机

- [math：数学函数与常量](./stdlib/math.md)
- [decimal：高精度十进制计算](./stdlib/decimal.md)
- [random：随机数与抽样](./stdlib/random.md)

### 文件、路径、系统交互

- [os：操作系统与目录遍历](./stdlib/os.md)
- [sys：解释器与运行时信息](./stdlib/sys.md)
- [pathlib：现代路径处理](./stdlib/pathlib.md)
- [glob：文件模式匹配](./stdlib/glob.md)
- [tempfile：临时文件与临时目录](./stdlib/tempfile.md)
- [shutil：复制、移动、归档](./stdlib/shutil.md)
- [subprocess：启动外部命令](./stdlib/subprocess.md)
- [argparse：命令行参数解析](./stdlib/argparse.md)

### 并发、网络、邮件

- [asyncio：异步编程](./stdlib/asyncio.md)
- [threading：多线程](./stdlib/threading.md)
- [queue：线程安全队列](./stdlib/queue.md)
- [concurrent.futures：线程池与进程池](./stdlib/concurrent_futures.md)
- [asyncio 与 threading：并发基础](./stdlib/asyncio_threading.md)
- [multiprocessing：多进程](./stdlib/multiprocessing.md)
- [urllib：URL 处理与基础 HTTP](./stdlib/urllib.md)
- [http.server：临时静态服务](./stdlib/http_server.md)
- [socket：TCP/UDP 网络通信](./stdlib/socket.md)
- [email：邮件内容构造](./stdlib/email.md)

### 数据存储、校验、标识

- [sqlite3：SQLite 数据库](./stdlib/sqlite3.md)
- [hashlib：哈希摘要](./stdlib/hashlib.md)
- [uuid：唯一标识](./stdlib/uuid.md)

### 容器、函数式、类型系统

- [collections：高频容器](./stdlib/collections.md)
- [itertools 与 functools：迭代器和函数工具](./stdlib/itertools_functools.md)
- [typing 与 dataclasses：类型标注和数据类](./stdlib/typing_dataclasses.md)

### 调试、测试、诊断

- [logging：日志](./stdlib/logging.md)
- [logging 与 subprocess 组合速览](./stdlib/logging_subprocess.md)
- [doctest：文档即测试](./stdlib/doctest.md)
- [unittest：标准单元测试框架](./stdlib/unittest.md)
- [pdb：交互式调试](./stdlib/pdb.md)

## 第三方常用库

- [requests：HTTP 请求](./third_party/requests.md)
- [numpy：数值计算](./third_party/numpy.md)
- [pandas：表格数据分析](./third_party/pandas.md)

## 专题

### 语言基础与代码组织

- [面向对象编程](./basics/oop.md)
- [异常处理](./basics/exceptions.md)
- [异常类型合集](./basics/exception-types.md)

### 场景专题

- [文件处理专题](./topics/file-processing.md)
- [网络编程专题](./topics/network-programming.md)

### Web 框架

- [Flask 入门](./frameworks/flask.md)
- [Django 入门](./frameworks/django.md)

### 数据库

- [SQLAlchemy 2.x 基础](./database/sqlalchemy.md)

## 实战案例

- [常见 Python 实战脚本](./examples/common_cases.md)

## 按场景导航

### 写脚本和命令行工具

- `argparse`：解析命令参数
- `sys`：拿启动参数、退出码、模块路径
- `subprocess`：调用外部程序
- `logging`：给脚本加日志

### 文本处理和日志清洗

- `string`：字符常量、模板拼接
- `re`：匹配、提取、替换
- `json`：结构化文本读写
- `csv`：表格文本输入输出
- `pickle`：对象序列化到本地文件

### 文件批处理

- `pathlib`：路径拼接、读写文件
- `os`：遍历目录、环境变量
- `glob`：按通配符批量找文件
- `tempfile`：生成安全的临时文件
- `shutil`：复制、移动、打包
- 进阶串联见 [文件处理专题](./topics/file-processing.md)

### 调试与测试

- `pdb`：断点调试
- `doctest`：给小函数补文档测试
- `unittest`：正式单元测试
- `异常类型合集`：按报错名快速定位原因

### 并发与通信

- `threading`：简单并发和阻塞库协作
- `queue`：线程之间传递任务
- `concurrent.futures`：快速上线程池或进程池
- `asyncio`：高并发 I/O
- `multiprocessing`：CPU 密集型并行
- `urllib`：基础 URL 处理与下载
- `http.server`：快速起一个本地文件服务
- `socket`：TCP/UDP 通信
- `email`：构造邮件正文和附件
- 进阶串联见 [网络编程专题](./topics/network-programming.md)

### 数据存储与安全

- `sqlite3`：本地嵌入式数据库
- `hashlib`：生成哈希摘要
- `uuid`：生成唯一 ID
- `pickle`：本地对象缓存
- `decimal`：金额等精确计算

## 学习顺序建议

1. 先看 [常用内置函数](./builtins/common-builtins.md)、[string](./stdlib/string.md)、[os](./stdlib/os.md)、[pathlib](./stdlib/pathlib.md)
2. 再看 [json](./stdlib/json.md)、[datetime](./stdlib/datetime.md)、[math](./stdlib/math.md)、[random](./stdlib/random.md)、[decimal](./stdlib/decimal.md)
3. 然后学习 [argparse](./stdlib/argparse.md)、[sys](./stdlib/sys.md)、[subprocess](./stdlib/subprocess.md)、[glob](./stdlib/glob.md)、[tempfile](./stdlib/tempfile.md)、[异常处理](./basics/exceptions.md)
4. 工程化阶段补 [logging](./stdlib/logging.md)、[unittest](./stdlib/unittest.md)、[pdb](./stdlib/pdb.md)、[异常类型合集](./basics/exception-types.md)、[queue](./stdlib/queue.md)
5. 数据处理时补 [csv](./stdlib/csv.md)、[pickle](./stdlib/pickle.md)、[sqlite3](./stdlib/sqlite3.md)、[hashlib](./stdlib/hashlib.md)
6. 按项目需要学习 [urllib](./stdlib/urllib.md)、[http.server](./stdlib/http_server.md)、[concurrent.futures](./stdlib/concurrent_futures.md)、[multiprocessing](./stdlib/multiprocessing.md)
7. Web 项目再进入 [Flask](./frameworks/flask.md)、[Django](./frameworks/django.md)
8. 场景串联时读 [文件处理专题](./topics/file-processing.md) 和 [网络编程专题](./topics/network-programming.md)

## 维护建议

- 新增模块时，同时更新本文件和 [函数速查索引](./函数索引.md)。
- 单模块文档优先保持四部分：用途、常用 API、示例、注意事项。
- 组合文档可以保留，但索引应优先指向单模块页面。
