# Playwright

`Playwright` 适合浏览器自动化、页面抓取和端到端测试，尤其适合依赖 JavaScript 渲染的页面。

## 安装

```bash
pip install playwright
playwright install
```

## 基本示例

```python
from playwright.sync_api import sync_playwright


with sync_playwright() as p:
    browser = p.chromium.launch()
    page = browser.new_page()
    page.goto("https://example.com")
    print(page.title())
    browser.close()
```

## 适用场景

- 端到端测试
- JS 渲染页面抓取
- 浏览器行为自动化

## 关联阅读

- [Web 抓取专题](../topics/web-scraping.md)
- [浏览器自动化专题](../topics/browser-automation.md)
- [测试与质量专题](../topics/testing-quality.md)

返回 [索引](../README.md)
