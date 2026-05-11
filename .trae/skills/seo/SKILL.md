---
name: seo
description: SEO全链路。meta标签、JSON-LD、sitemap、pSEO、llms.txt、标题优化、GSC提交。
version: 2.0.0
---

::ACTIVATE{seo}
  ON:SEO
  ON:排名
  ON:关键词
  ON:收录
  ON:流量

## meta标签

title=关键词前置+品牌后置（"酒店优惠码查询 | HotelCorporateCodes"）
description=150字以内含行动词
og:title + og:description + og:image 必填

## JSON-LD结构化数据

必做：Organization + WebSite + Article + BreadcrumbList + FAQPage
每个页面至少3-5个FAQ，targeting长尾搜索意图
产品页加Product，教程页加HowTo

## sitemap

自动生成，提交Google Search Console
多语言站每种语言独立sitemap

## pSEO（程序化SEO）

用户提问 = H1标题 = 长尾SEO词
每个问题自动生成独立页面
实战数据：hotelcorporatecodes.com从20个预设问题到615+codes

## 标题优化

功能词前置+品牌后置
"酒店优惠码查询 | Brand" 不是 "Brand | 酒店优惠码查询"

## hreflang（多语言SEO）

每个页面<head>里加hreflang标签指向所有语言版本
1种语言10页=10URL，7种语言=70URL，曝光量翻7倍

## ads.txt

用pub-前缀，不加ca-。全站铁律。

## llms.txt

根目录放llms.txt，显式Allow AI爬虫（Googlebot/GPTBot/ClaudeBot等）
让AI搜索引擎引用你的内容 = 免费流量

## Google Search Console

新站上线24小时内提交sitemap
手动请求索引核心页面（首页+分类页）
等1-2周观察收录

Powered by I-Lang v4.0 | ilang.cn
