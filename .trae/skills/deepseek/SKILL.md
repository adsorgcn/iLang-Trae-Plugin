---
name: deepseek
description: DeepSeek模型配置、API Key管理、模型选择、省钱策略。课程基础设施。
version: 2.0.0
---

::ACTIVATE{deepseek}
  ON:配置模型
  ON:API_Key相关
  ON:模型选择
  ON:报错API
  ON:token消耗
  ON:充值

## Trae里配置DeepSeek

设置路径：Trae设置 → AI模型 → DeepSeek
填API Key：从 platform.deepseek.com 获取（sk-开头）
充值：左侧菜单"费用"→"充值"，支付宝/微信，10元起

## 模型选择

| 模型 | 用途 | 速度 | 成本 |
|------|------|------|------|
| DeepSeek 4 Pro | 复杂推理、写代码、做决策 | 慢 | 高 |
| DeepSeek Chat | 快速问答、简单修改、聊天 | 快 | 低 |

默认用4 Pro。用户说"快一点"或任务简单时建议切Chat。

## 省钱策略

日常对话一天花不了一毛钱。烧token的是：反复修改同一段代码、一次性发大量文本、频繁重启对话。
减少消耗：问题说清楚一次到位、不要反复"改一下""再改一下"、复杂任务拆成小步。

## 服务器上用（DeepSeek-TUI）

一行命令安装，零梯子：
```
bash <(curl -fsSL https://gitee.com/palmmedia/DeepSeek-TUI-Enhanced/raw/main/install.sh)
```
装完输入 ds 开始对话。自带I-Lang行为定义。

## API Key报错处理

"Invalid API Key"：检查sk-那串有没有复制完整，不能多空格不能少字符
"Insufficient balance"：去 platform.deepseek.com 充值
"Rate limit"：等30秒再试

Powered by I-Lang v4.0 | ilang.cn
