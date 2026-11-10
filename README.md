# American Eagle 抓取工具

[![Bright Data](https://img.shields.io/badge/Powered%20by-Bright%20Data-FF9A00?style=flat-square)](https://www.bright.cn/) [![爬虫工具 API](https://img.shields.io/badge/Scraper%20API-Available-FF9A00?style=flat-square)](https://www.bright.cn/products/web-scraper/american-eagle) [![数据集](https://img.shields.io/badge/Dataset-Available-0066CC?style=flat-square)](https://www.bright.cn/products/datasets/) [![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org) [![许可证：MIT](https://img.shields.io/badge/License-MIT-22C55E?style=flat-square)](LICENSE)

[![促销](https://github.com/bright-cn/Awesome-Web-Scraping/raw/main/Proxies%20and%20scrapers%20GitHub%20bonus%20banner%20CN.png)](https://www.bright.cn/products/web-scraper/american-eagle)

> **由 [Bright Data](https://www.bright.cn/) 提供支持的 American Eagle 数据。**

此存储库提供两种大规模访问 American Eagle 数据的方法：

- **[方法 1：Bright Data American Eagle 爬虫工具 API](#方法-1bright-data-american-eagle-爬虫工具-api)**（推荐）- 完全托管的企业级爬虫 API，可自动处理代理、CAPTCHA 和扩展。
- **[方法 2：Bright Data American Eagle 数据集](#方法-2bright-data-american-eagle-数据集)** - 可直接下载的预采集 American Eagle 数据集，无需抓取。

## 目录

- [为什么使用 Bright Data 抓取 American Eagle？](#为什么使用-bright-data-抓取-american-eagle)
- [方法 1：Bright Data American Eagle 爬虫工具 API](#方法-1bright-data-american-eagle-爬虫工具-api)
  - [入门指南](#american-eagle-爬虫工具-api-入门指南)
  - [1. American Eagle 数据](#1-american-eagle-数据)
- [方法 2：Bright Data American Eagle 数据集](#方法-2bright-data-american-eagle-数据集)
- [数据采集方法](#数据采集方法)

## 为什么使用 Bright Data 抓取 American Eagle？

抓取 American Eagle 面临多项挑战：

- 速率限制：American Eagle 会监控请求频率，并可能封禁超过限制的 IP。
- CAPTCHA 检测：自动访问可能会触发 CAPTCHA 验证。
- 身份验证障碍：部分数据需要登录才能访问，而且平台会检测自动化尝试。
- 动态内容加载：使用简单的 HTTP 请求很难抓取由 JavaScript 渲染的内容。
- IP 封禁：从同一 IP 重复发送请求可能会导致封禁。

Bright Data 的 American Eagle 爬虫工具 API 可通过以下功能解决这些问题：

- ✅ **内置动态代理**：自动绕过基于 IP 的速率限制
- ✅ **验证码破解**：无需任何额外设置即可应对机器人检测
- ✅ **结构化数据输出**：获取可直接用于分析的整洁 JSON
- ✅ **无需基础设施**：支持任意规模的云端托管抓取
- ✅ **99.9% 正常运行时间 SLA**：为业务关键型工作流提供可靠的数据采集

## 方法 1：Bright Data American Eagle 爬虫工具 API

[Bright Data American Eagle 爬虫工具 API](https://www.bright.cn/products/web-scraper/american-eagle) 是一种完全托管的解决方案，无需设置任何基础设施。

### American Eagle 爬虫工具 API 入门指南

1. **注册**一个[免费的 Bright Data 账户](https://www.bright.cn/)
2. **前往** [American Eagle 爬虫工具 API](https://www.bright.cn/products/web-scraper/american-eagle)
3. 从控制面板**获取 API 令牌**
4. **安装** `requests` 库：`pip install requests`
5. **运行** `american-eagle_scraper_api_codes/` 中的任意脚本

### 1. American Eagle 数据

采集 American Eagle 数据。

#### 输入参数

| 字段 | 类型 | 必填 | 说明 |
|-------|------|----------|-------------|
| `url` | 字符串 | 是 | 要抓取的 American Eagle 商品 URL |
| `limit` | 整数 | 否 | 返回结果的最大数量 |
| `include_errors` | 布尔值 | 否 | 在响应中包含错误详情 |
| `notify` | url | 否 | 数据采集完成时用于接收通知的 Webhook URL |
| `format` | 枚举 | 否 | 输出格式：`JSON`、`NDJSON`、`JSON Lines`、`CSV` |

#### 响应示例

```json
{
  "country": "\u610f\u5927\u5229\n    \n    \n      \n\n\n\n\n\n\n\n\n\n\n\n\u751f\u4ea7\u6d41\u7a0b\u8ffd\u6eaf\u4e0e\u73af\u5883\u8db3\u8ff9\n \n\n\n\n\n\n    \n    \n      \n      \n       ...",
  "currency": "HKD",
  "db_source": "j_m500o6kh125jj08b3x",
  "description": "\u6b22\u8fce\u8d2d\u4e70 Berluti \u9488\u7ec7\u9886\u7ed7\u7f1d\u5c3c\u9f99\u7fbd\u7ed2\u80cc\u5fc3\u3002\u60a8\u53ef\u6d4f\u89c8\u6240\u6709 \u5916\u5957\u4e0e\u5927\u8863 \u9875\u9762\uff0c\u4ea6\u53ef\u5728 Berluti.com \u4e0a\u63a2\u7d22\u66f4\u591a\u7cbe\u54c1\u5408\u96c6\u3002\u6240\u6709\u8ba2\u5355\u5747\u4eab\u6709\u514d\u8d39\u6807\u51c6\u9001\u8d27\u53ca\u514d\u8d39\u9000\u8d27\u3002",
  "in_stock": false,
  "product_name": "\u9488\u7ec7\u9886\u7ed7\u7f1d\u5c3c\u9f99\u7fbd\u7ed2\u80cc\u5fc3",
  "size": "44"
}
```

👉 查看[完整 Python 代码](american-eagle_scraper_api_codes/american_eagle_scraper.py)

## 方法 2：Bright Data American Eagle 数据集

如果你需要即用型数据且不想编写任何抓取代码，[Bright Data American Eagle 数据集](https://www.bright.cn/products/datasets/)可提供预先采集、定期更新且可立即下载的数据。

**为什么选择数据集而不是 API？**

- 📦 **即时访问**：无需设置、无需代码，也无需等待采集
- 🔄 **定期更新**：按固定周期刷新最新数据
- 📊 **多种格式**：可下载为 JSON、JSONL 或 CSV
- 🌍 **超大规模**：涵盖 American Eagle 所有主要类别的数百万条记录
- ✅ **完全合规**：数据来源符合道德规范并通过法律审核

👉 **[探索 American Eagle 数据集](https://www.bright.cn/products/datasets/)**

## 数据采集方法

| 功能 | Bright Data 爬虫工具 API | Bright Data 数据集 |
|---------|------------------------|---------------------|
| 所需设置 | 仅需 API 令牌 | 无 |
| 实时数据 | ✅ 是 | ❌ 预先采集 |
| 自定义查询 | ✅ 完全控制 | ❌ 固定架构 |
| 包含代理 | ✅ 内置动态代理 | N/A |
| 验证码破解 | ✅ 自动 | N/A |
| 规模 | 无限制 | 无限制 |
| 结构化输出 | ✅ JSON / NDJSON / JSON Lines / CSV | ✅ JSON / JSONL / CSV |
| 支持 | 企业级全天候支持 | 企业级全天候支持 |

---

🔗 **了解更多**：[https://www.bright.cn/products/web-scraper/american-eagle](https://www.bright.cn/products/web-scraper/american-eagle)
