# Python 知识库首页

这套知识库面向日常 Python 开发，适合用来：快速查函数、按场景找模块、按路线系统学习。

## 快速入口

- [函数速查索引](./函数索引.md)
- [常用内置函数](./builtins/common-builtins.md)
- [语法与数据类型](./basics/syntax-data-types.md)
- [控制流](./basics/control-flow.md)
- [异常类型合集](./basics/exception-types.md)
- [常见 Python 实战脚本](./examples/common_cases.md)
- [Python 小项目模板](./examples/mini_projects.md)
- [算法与数据结构专题](./topics/algorithms-data-structures.md)
- [数据可视化专题](./topics/data-visualization.md)
- [数据清洗专题](./topics/data-cleaning.md)
- [文件处理专题](./topics/file-processing.md)
- [命令行自动化专题](./topics/automation-cli.md)
- [接口测试专题](./topics/api-testing.md)
- [网络编程专题](./topics/network-programming.md)
- [Web 抓取专题](./topics/web-scraping.md)
- [性能与调试专题](./topics/performance-debugging.md)
- [数据库开发专题](./topics/database-development.md)
- [项目结构专题](./topics/project-structure.md)
- [异步编程专题](./topics/async-programming.md)
- [API 开发专题](./topics/api-development.md)
- [配置管理专题](./topics/config-management.md)
- [打包与发布专题](./topics/packaging-release.md)
- [部署与运维专题](./topics/deployment-operations.md)
- [代码质量专题](./topics/code-quality.md)
- [CI/CD 专题](./topics/ci-cd.md)
- [Docker 专题](./topics/docker-basics.md)
- [缓存与队列专题](./topics/cache-queues.md)
- [实时通信专题](./topics/realtime-communication.md)
- [Linux 与 Python 运维专题](./topics/linux-python-ops.md)
- [SQL 优化专题](./topics/sql-optimization.md)
- [安全基础专题](./topics/security-basics.md)
- [Excel 自动化专题](./topics/excel-automation.md)
- [数据管道专题](./topics/data-pipelines.md)
- [备份与归档专题](./topics/backup-archiving.md)
- [图像处理专题](./topics/image-processing.md)

## 学习路线

| 目标 | 推荐入口 |
| --- | --- |
| 从零开始补 Python 常用能力 | [常用内置函数](./builtins/common-builtins.md) → [string](./stdlib/string.md) → [os](./stdlib/os.md) → [pathlib](./stdlib/pathlib.md) |
| 打牢语法和基础心智模型 | [语法与数据类型](./basics/syntax-data-types.md) → [控制流](./basics/control-flow.md) → [函数与作用域](./basics/functions-scope.md) → [推导式与生成器](./basics/comprehensions-generators.md) |
| 写脚本、命令行工具、自动化任务 | [argparse](./stdlib/argparse.md) → [sys](./stdlib/sys.md) → [subprocess](./stdlib/subprocess.md) → [logging](./stdlib/logging.md) |
| 做文件处理和数据清洗 | [csv](./stdlib/csv.md) → [json](./stdlib/json.md) → [pathlib](./stdlib/pathlib.md) → [文件处理专题](./topics/file-processing.md) → [数据清洗专题](./topics/data-cleaning.md) |
| 做网络请求和接口调用 | [urllib](./stdlib/urllib.md) → [requests](./third_party/requests.md) → [httpx](./third_party/httpx.md) → [网络编程专题](./topics/network-programming.md) |
| 补测试、调试和排错能力 | [unittest](./stdlib/unittest.md) → [pdb](./stdlib/pdb.md) → [traceback](./stdlib/traceback.md) → [性能与调试专题](./topics/performance-debugging.md) |
| 补算法、数据结构和刷题基础 | [算法与数据结构专题](./topics/algorithms-data-structures.md) → [collections](./stdlib/collections.md) → [itertools 与 functools](./stdlib/itertools_functools.md) |
| 做 Excel、图表和数据汇报 | [pandas](./third_party/pandas.md) → [openpyxl](./third_party/openpyxl.md) → [matplotlib](./third_party/matplotlib.md) → [数据可视化专题](./topics/data-visualization.md) |
| 进入现代 Python 测试流 | [pytest](./third_party/pytest.md) → [unittest.mock](./stdlib/unittest_mock.md) → [测试与质量专题](./topics/testing-quality.md) → [接口测试专题](./topics/api-testing.md) |
| 进入 Web 后端开发 | [Flask 入门](./frameworks/flask.md) 或 [FastAPI 入门](./frameworks/fastapi.md) → [SQLAlchemy 2.x 基础](./database/sqlalchemy.md) → [项目结构专题](./topics/project-structure.md) |
| 做异步网络或高并发抓取 | [asyncio](./stdlib/asyncio.md) → [httpx](./third_party/httpx.md) → [aiohttp](./third_party/aiohttp.md) → [Web 抓取专题](./topics/web-scraping.md) |
| 学数据库建模和迁移 | [sqlite3](./stdlib/sqlite3.md) → [SQLAlchemy 2.x 基础](./database/sqlalchemy.md) → [Alembic](./third_party/alembic.md) → [数据库开发专题](./topics/database-development.md) |
| 学配置、发布和部署 | [导入、包与虚拟环境](./basics/imports-venv.md) → [配置管理专题](./topics/config-management.md) → [打包与发布专题](./topics/packaging-release.md) → [部署与运维专题](./topics/deployment-operations.md) |
| 建立团队工程质量约束 | [typing 与 dataclasses](./stdlib/typing_dataclasses.md) → [mypy](./third_party/mypy.md) → [ruff](./third_party/ruff.md) → [代码质量专题](./topics/code-quality.md) → [CI/CD 专题](./topics/ci-cd.md) |
| 做缓存、后台任务和实时系统 | [queue](./stdlib/queue.md) → [redis-py](./third_party/redis.md) → [celery](./third_party/celery.md) → [websockets](./third_party/websockets.md) → [缓存与队列专题](./topics/cache-queues.md) |

## 按任务查找

### 写脚本和自动化

- `argparse`：解析命令参数
- `sys`：拿启动参数、退出码、模块路径
- `subprocess`：调用外部程序
- `logging`：记录运行日志
- `tempfile`：安全创建临时文件
- 进阶串联见 [命令行自动化专题](./topics/automation-cli.md)

### 文件和目录处理

- `pathlib`：路径拼接、读写文件
- `os`：遍历目录、环境变量
- `glob`：批量匹配文件
- `shutil`：复制、移动、打包
- `zipfile` / `tarfile`：压缩包归档和解压
- `hashlib`：文件校验
- 进阶串联见 [文件处理专题](./topics/file-processing.md)

### 文本和数据格式

- `string`：字符常量、模板字符串
- `re`：匹配、提取、替换
- `json`：结构化数据读写
- `csv`：表格文本输入输出
- `xml.etree.ElementTree`：XML 解析与生成
- `pickle`：本地对象缓存
- `datetime` / `time`：时间处理和计时
- 进阶串联见 [数据清洗专题](./topics/data-cleaning.md)

### 并发和网络

- `threading`：简单多线程
- `queue`：线程安全队列
- `concurrent.futures`：线程池和进程池
- `asyncio`：高并发 I/O
- `multiprocessing`：CPU 密集型并行
- `urllib` / `requests` / `httpx`：HTTP 请求
- `http.server`：临时本地文件服务
- `socket`：TCP/UDP 通信
- `websockets` / `grpcio`：实时通信和服务间调用
- 进阶串联见 [网络编程专题](./topics/network-programming.md)

### 数据存储和精确计算

- `sqlite3`：本地数据库
- `SQLAlchemy`：ORM 和数据库访问
- `Alembic`：数据库迁移
- `uuid`：唯一 ID
- `hashlib`：哈希摘要
- `decimal`：金额等精确计算
- 进阶串联见 [数据库开发专题](./topics/database-development.md)

### 数据分析、图表和 Excel

- `numpy`：数组和数值计算
- `pandas`：表格数据清洗和聚合
- `matplotlib`：基础可视化和折线柱状图
- `seaborn` / `plotly`：统计图和交互图
- `openpyxl`：读写 Excel 文件、样式、工作表
- `streamlit`：快速包装数据工具页面
- 系统整理见 [数据可视化专题](./topics/data-visualization.md)

### 算法、数据结构和刷题

- `list` / `dict` / `set`：最常用基础结构
- `collections.deque`：队列、双端队列、滑动窗口
- `collections.Counter`：计数和频率统计
- `itertools`：组合、排列、笛卡尔积
- `bisect` / `heapq`：二分边界与优先队列
- 系统整理见 [算法与数据结构专题](./topics/algorithms-data-structures.md)

### 配置、发布和运维

- `os.environ`：环境变量配置
- `configparser` / `tomllib`：配置文件读取
- `logging`：运行日志
- `shutil` / `zipfile`：备份归档
- `gunicorn` / `uvicorn` / Docker：服务部署入口
- 系统整理见 [配置管理专题](./topics/config-management.md)、[打包与发布专题](./topics/packaging-release.md)、[部署与运维专题](./topics/deployment-operations.md)、[Docker 专题](./topics/docker-basics.md)

### 工程质量与协作

- `pytest`：自动化测试
- `mypy`：类型检查
- `ruff`：lint 和格式化
- `pre-commit`：提交前自动检查
- 系统整理见 [代码质量专题](./topics/code-quality.md) 和 [CI/CD 专题](./topics/ci-cd.md)

### 测试、调试和排错

- `doctest`：文档即测试
- `unittest`：正式单元测试
- `unittest.mock`：替换外部依赖
- `pytest`：更常用的测试框架和夹具系统
- `pdb`：断点调试
- `traceback` / `cProfile`：堆栈诊断和性能分析
- [异常处理](./basics/exceptions.md)：异常写法和捕获方式
- [异常类型合集](./basics/exception-types.md)：按报错名定位原因
- 接口测试串联见 [接口测试专题](./topics/api-testing.md)
- 综合整理见 [测试与质量专题](./topics/testing-quality.md) 和 [性能与调试专题](./topics/performance-debugging.md)

## 标准库总览

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
- [statistics：基础统计计算](./stdlib/statistics.md)
- [enum 与 fractions：枚举和精确分数](./stdlib/enum_fractions.md)

### 文件、路径、系统交互

- [os：操作系统与目录遍历](./stdlib/os.md)
- [sys：解释器与运行时信息](./stdlib/sys.md)
- [pathlib：现代路径处理](./stdlib/pathlib.md)
- [glob：文件模式匹配](./stdlib/glob.md)
- [tempfile：临时文件与临时目录](./stdlib/tempfile.md)
- [shutil：复制、移动、归档](./stdlib/shutil.md)
- [subprocess：启动外部命令](./stdlib/subprocess.md)
- [argparse：命令行参数解析](./stdlib/argparse.md)
- [contextlib：上下文管理工具](./stdlib/contextlib.md)
- [io 与 textwrap：内存流与文本排版](./stdlib/io_textwrap.md)
- [copy 与 pprint：复制与格式化打印](./stdlib/copy_pprint.md)
- [zipfile 与 tarfile：压缩归档](./stdlib/zipfile_tarfile.md)
- [configparser 与 tomllib：配置文件读取](./stdlib/configparser_tomllib.md)

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
- [secrets 与 base64：安全随机与编码](./stdlib/secrets_base64.md)

### 数据存储、校验、标识

- [sqlite3：SQLite 数据库](./stdlib/sqlite3.md)
- [hashlib：哈希摘要](./stdlib/hashlib.md)
- [uuid：唯一标识](./stdlib/uuid.md)

### 容器、函数式、类型系统

- [collections：高频容器](./stdlib/collections.md)
- [itertools 与 functools：迭代器和函数工具](./stdlib/itertools_functools.md)
- [typing 与 dataclasses：类型标注和数据类](./stdlib/typing_dataclasses.md)
- [bisect 与 heapq：二分与堆](./stdlib/bisect_heapq.md)

### 调试、测试、诊断

- [logging：日志](./stdlib/logging.md)
- [logging 与 subprocess 组合速览](./stdlib/logging_subprocess.md)
- [traceback：异常堆栈处理](./stdlib/traceback.md)
- [cProfile：性能剖析](./stdlib/cprofile.md)
- [doctest：文档即测试](./stdlib/doctest.md)
- [unittest：标准单元测试框架](./stdlib/unittest.md)
- [unittest.mock：模拟与替换](./stdlib/unittest_mock.md)
- [pdb：交互式调试](./stdlib/pdb.md)
- [xml.etree.ElementTree：XML 处理](./stdlib/xml_parsing.md)

## 第三方常用库

- [requests：HTTP 请求](./third_party/requests.md)
- [httpx：同步 / 异步 HTTP 客户端](./third_party/httpx.md)
- [aiohttp：异步 HTTP 客户端](./third_party/aiohttp.md)
- [Beautiful Soup 4：HTML 解析](./third_party/beautifulsoup4.md)
- [rich：终端富文本输出](./third_party/rich.md)
- [typer：现代 CLI](./third_party/typer.md)
- [jinja2：模板引擎](./third_party/jinja2.md)
- [pillow：图像处理](./third_party/pillow.md)
- [numpy：数值计算](./third_party/numpy.md)
- [pandas：表格数据分析](./third_party/pandas.md)
- [matplotlib：基础数据可视化](./third_party/matplotlib.md)
- [seaborn：统计图表](./third_party/seaborn.md)
- [plotly：交互式图表](./third_party/plotly.md)
- [streamlit：快速数据应用](./third_party/streamlit.md)
- [openpyxl：Excel 读写](./third_party/openpyxl.md)
- [pytest：测试框架](./third_party/pytest.md)
- [mypy：静态类型检查](./third_party/mypy.md)
- [ruff：lint 与格式化](./third_party/ruff.md)
- [pre-commit：提交前检查](./third_party/pre_commit.md)
- [pydantic：数据校验与建模](./third_party/pydantic.md)
- [redis-py：缓存与队列基础](./third_party/redis.md)
- [celery：后台任务](./third_party/celery.md)
- [websockets：WebSocket 实时通信](./third_party/websockets.md)
- [grpcio：RPC 通信](./third_party/grpc.md)
- [gunicorn 与 uvicorn：服务部署入口](./third_party/gunicorn_uvicorn.md)
- [Alembic：数据库迁移](./third_party/alembic.md)

## 专题与扩展

### 语言基础

- [语法与数据类型](./basics/syntax-data-types.md)
- [控制流](./basics/control-flow.md)
- [函数与作用域](./basics/functions-scope.md)
- [可迭代对象与迭代器](./basics/iterables-iterators.md)
- [导入、包与虚拟环境](./basics/imports-venv.md)
- [面向对象编程](./basics/oop.md)
- [函数与模块组织](./basics/functions-modules.md)
- [推导式与生成器](./basics/comprehensions-generators.md)
- [装饰器与上下文管理](./basics/decorators-context-managers.md)
- [异常处理](./basics/exceptions.md)
- [异常类型合集](./basics/exception-types.md)

### 场景专题

- [算法与数据结构专题](./topics/algorithms-data-structures.md)
- [数据可视化专题](./topics/data-visualization.md)
- [数据清洗专题](./topics/data-cleaning.md)
- [文件处理专题](./topics/file-processing.md)
- [命令行自动化专题](./topics/automation-cli.md)
- [接口测试专题](./topics/api-testing.md)
- [网络编程专题](./topics/network-programming.md)
- [Web 抓取专题](./topics/web-scraping.md)
- [异步编程专题](./topics/async-programming.md)
- [API 开发专题](./topics/api-development.md)
- [性能与调试专题](./topics/performance-debugging.md)
- [测试与质量专题](./topics/testing-quality.md)
- [数据库开发专题](./topics/database-development.md)
- [项目结构专题](./topics/project-structure.md)
- [配置管理专题](./topics/config-management.md)
- [打包与发布专题](./topics/packaging-release.md)
- [部署与运维专题](./topics/deployment-operations.md)
- [代码质量专题](./topics/code-quality.md)
- [CI/CD 专题](./topics/ci-cd.md)
- [Docker 专题](./topics/docker-basics.md)
- [缓存与队列专题](./topics/cache-queues.md)
- [实时通信专题](./topics/realtime-communication.md)
- [Linux 与 Python 运维专题](./topics/linux-python-ops.md)
- [SQL 优化专题](./topics/sql-optimization.md)
- [安全基础专题](./topics/security-basics.md)
- [Excel 自动化专题](./topics/excel-automation.md)
- [数据管道专题](./topics/data-pipelines.md)
- [备份与归档专题](./topics/backup-archiving.md)
- [图像处理专题](./topics/image-processing.md)

### Web 和数据库

- [Flask 入门](./frameworks/flask.md)
- [FastAPI 入门](./frameworks/fastapi.md)
- [Django 入门](./frameworks/django.md)
- [SQLAlchemy 2.x 基础](./database/sqlalchemy.md)

### 实战案例

- [常见 Python 实战脚本](./examples/common_cases.md)
- [Python 小项目模板](./examples/mini_projects.md)

## 维护建议

- 新增模块时，同时更新本文件和 [函数速查索引](./函数索引.md)
- 单模块文档优先保持：用途、常用 API、示例、注意事项
- 组合文档可以保留，但首页应优先指向单模块页面或专题页
