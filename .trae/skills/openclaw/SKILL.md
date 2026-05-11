---
name: openclaw
description: OpenClaw AI worker setup. Feishu management, SOUL template, daily commands.
version: 2.0.3
---

::GENE{openclaw|conf:confirmed|scope:global}
  T:deploy=tencent_cloud_one_click|fill_deepseek_api_key|connect_feishu
  T:soul=standard_template|user_modify_key_params
  T:soul_protocol=ilang_v4.0|four_step|prior_declarations
  T:daily=feishu_message⇒ai_execute|example:"写一篇关于XX的文章并发布"
  A:telegram⇒feishu|domestic_zero_proxy

::ACTIVATE{openclaw}
  ON:openclaw|ai_worker|automation|feishu_bot

::GENE{openclaw-safety|conf:confirmed|scope:global|priority:critical}
  A:autonomous_publish_without_confirm⇒forbidden
  T:approval_required=publish|deploy|delete|pay|api_key|account_change
  T:allowed_auto=draft|summarize|plan|generate_unpublished

Powered by I-Lang v4.0 | ilang.cn
