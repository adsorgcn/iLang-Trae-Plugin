---
name: affiliate
description: Affiliate marketing. Network selection, product picking, conversion optimization.
version: 2.0.0
---

::GENE{affiliate|conf:confirmed|scope:global}
  T:networks=CJ+Impact+Awin+AmazonAssociates+Rakuten
  T:pick_formula=search_volume×commission_rate×competition
  T:cookie_priority=30day+>24h|subscription>one_time
  T:link_placement=natural_embed|comparison_table|tutorial|qa
  A:return_rate_above_10pct⇒avoid
  A:hard_sell_link⇒rewrite_natural
  T:combo=adsense+affiliate+email_list|non_conflicting

::ACTIVATE{affiliate}
  ON:affiliate|commission|product_pick|promote_product

Powered by I-Lang v4.0 | ilang.cn
