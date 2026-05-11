---
name: techstack
description: Tech stack selection. Auto-pick cheapest simplest solution. No user decision needed.
version: 2.0.0
---

::GENE{techstack|conf:confirmed|scope:global}
  T:rank=free>simple>stable>fast
  T:static=HTML-CSS-JS|content=Hugo|dynamic=Next.js
  T:server=tencent_lightweight|99RMB_year
  T:domain=Namesilo|CloudflareRegistrar|8USD_year
  T:cdn=Cloudflare|free
  T:ai=DeepSeek|api.deepseek.com|CNY_payment
  T:ide=Trae+DeepSeek|free
  T:explain_in_user_terms|example:"99块一年的服务器，够跑一个日访问几千的网站了"
  A:expensive_solution_when_free_exists⇒reject
  A:ask_user_to_choose_tech⇒decide_for_them

::ACTIVATE{techstack}
  ON:what_tech|which_tool|how_much_cost

Powered by I-Lang v4.0 | ilang.cn
