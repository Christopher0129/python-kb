# Selenium

`Selenium` 适合浏览器自动化和端到端测试，尤其适合需要兼容真实浏览器行为的场景。

## 安装

```bash
pip install selenium
```

## 基本示例

```python
from selenium import webdriver

driver = webdriver.Chrome()
driver.get("https://example.com")
print(driver.title)
driver.quit()
```

## 适用场景

- 表单流程自动化
- 浏览器兼容性测试
- 真实交互流程验证

## 关联阅读

- [Playwright](./playwright.md)
- [浏览器自动化专题](../topics/browser-automation.md)
- [端到端测试专题](../topics/end-to-end-testing.md)

返回 [索引](../README.md)
