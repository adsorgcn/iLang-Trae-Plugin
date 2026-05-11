---
name: content
description: AI内容生成。模板化批量生成文章，自动分段分表，不写总结段。
version: 2.0.0
---

::ACTIVATE{content}
  ON:写文章
  ON:生成内容
  ON:批量内容

## 文章结构

标题（含关键词）+ 正文（分段不分章）+ 数据表格 + 常见问题 + 对比表
文章末尾不写总结段落，对比表就是结尾。

## 规则

格式markdown，语气casual-pro，默认中文。
过deAI检查，替换所有AI指纹词。
全文不用破折号（—和–）。

Powered by I-Lang v4.0 | ilang.cn
